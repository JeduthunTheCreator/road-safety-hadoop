## Road Safety Big Data Analysis (Hadoop MapReduce)
[![Java](https://img.shields.io/badge/Java-17+-ED8B00?style=flat&logo=java&logoColor=white)](https://react.dev/)

### Overview 
A distributed data engineering project analysing 100,000+ road accident records using Hadoop MapReduce to uncover patterns in casualty severity. 

## Tech Stack
- Java (MapReduce implementation)
- Hadoop (HDFS + YARN)
- Apache Spark
- Ubuntu (VM-based cluster)
- Eclipse IDE

## System Architecture
- Multi-node Hadoop cluster (5 nodes)
  - 1 NameNode
  - 1 Secondary NameNode
  - 3 DataNodes
- Distributed storage using HDFS
- MapReduce job for data processing
- Optional Spark integration for advanced analytics
  
<p align="center">
  <img src="assets/Hadoop Cluster diagram.drawio.png" width="400">
</p>

## Problem Identification
Road traffic accidents generate massive datasets, but extracting actionable insights at scale is challenging.

This project uses Hadoop MapReduce to analyse UK road safety data and identify how accident frequency varies across severity levels.

## Key Results
- Severity Band 1: 1,671 accidents
- Severity Band 2: 23,500 accidents
- Severity Band 3: 102,705 accidents

Less severe accidents are significantly more frequent, highlighting where preventive measures could have the highest impact.

## Data Processing Pipeline
- Load CSV dataset into HDFS
- Mapper extracts accident severity data
- Reducer aggregates unique accident counts
- Output stored in HDFS

## Running the Project
```bash
# Upload dataset to HDFS
hadoop fs -put dataset.csv /input

# Run MapReduce job
hadoop jar AccidentIndexPerCasualtySeverity.jar /input /output
```

## Future Improvements
- Add location & time-based analysis
- Build a real-time pipeline
- Apply machine learning for accident prediction

## Demo
### Configuration 



## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---
<div align="center"> Made with ❤️ by Jeduthun Idemudia </div>
