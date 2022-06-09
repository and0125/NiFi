# Nifi

## Basic Terms

Data flow: the movement of data from source to a destination. This data can be in any format.

Data pipeline: this refers to movement and transformation of data/content from source to destination. The difference between data flow and data pipelines is the transformation steps that can take place in the pipeline but doesn't happen in data flows. This could happen in a batch process but can also happen in a data stream.

ETL: extract transform load processes. This is a batch process, this reads the data from every source, then transforms it, then loads it to the destination.

These three terms are used interchangeably, but they have exact definitions.

## Frameworks for Data Flow

At a high level, transferring data from source to destination should be easy, and can be done in any coding language of choice.

Before coding, you want to make sure you are able to handle the use case of the transference of the data.

Four v's can help you evaluate the approach to the data movement:

- volume: refers to the amount of data generated every second.
- Velocity: refers to the speed at which new data is generated and the speed at which data moves through the pipeline.
- Variety: the different types of data in use.
- Veracity: refers to the messiness or consistency of the data format. Also to the trustworthiness/integrity of the data.

The solution you should implement may need to handle multiple formats, various sources and destinations, may need to be reliably scalable for large volume and high velocity data; also you should consider the data cleansing and data validation logistics.

You should aim for as high a throughput as possible with the lowest latency.

## Nifi in this Context

defintion: apache nifi supports powerful and scalable directed graphs of data routing, transformation, and system mediation logic.

This is complicated, but simply Nifi was built to automate the flow of data between systems. It can propogate any data content from any source to any destination. This is a bold definition, but it is true enough.

## Installing Apache Nifi

its pretty similar to install Nifi on any type of computer; just use the OS specific startup file. You'll need java installed on the machine.

Nifi has a default port of 8080. You can look at localhost:8080/nifi to see the nifi landing page once you execute the `run-nifi.bat` file.

## Nifi User Interface

This is one of Nifi's best features. You can drag and drop components and create a simple or complex data flow.

You can finish a simple workflow in a minute. For example, you can add processors from their processors list and pull start a workflow from there. The demo was of him making a GetFile processor and setting the directory from where the processor pulled, and sending that data into a PutFile processor that adds the data to an output directory.

Each processor has settings, scheduling, properties and a comment section to alter details of the processor.

Use the play button to start the processors. In the example, the GetFile processor was continously monitoring the input folder, and this pulled the data instantaneously into the output folder.
