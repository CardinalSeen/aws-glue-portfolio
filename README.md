# AWS Glue Portfolio

A comprehensive collection of AWS Glue labs and projects demonstrating data catalog management, ETL transformations, job orchestration, and data quality implementations.

## 🚀 The Core Pipeline & Data Quality

As an applicant for the **AWS Community Builders 2027 cohort** under the Data category, I am excited to share one of my hands-on technical practices using AWS Glue.

For this post, I am walking through a workshop from the AWS Builders Data Engineer track focusing on AWS Glue.

**AWS Glue** is AWS's serverless data integration service that handles everything from data ingestion to aggregated pipelines. As a data engineer, ensuring that data is clean, structured, and reliable is critical for downstream users such as data analysts, data scientists, and other analytics professionals.

### 💰 About Costs & Learning Investment

To keep each article focused and digestible, I selected specific highlights from each lab. Everything covered here can be explored within the AWS Free Tier boundary (with just a tiny note on minor resource costs like EC2 instances, but well worth it for the hands-on practice!).

**Important Note:** The other features such as AWS ETL integration, job runs, and crawlers are not included in the free tier. I included this in my personal bill in order to learn AWS Glue in my way, so that when I apply as a Cloud Data Engineer, I know how to use AWS Glue effectively.

## 📁 Project Structure

### Lab 01: Glue Data Catalog
- **lab-01-01-aws-console**: Creating and managing Glue Data Catalog using AWS Console
- **lab-01-02-aws-cli**: Creating and managing Glue Data Catalog using AWS CLI

### Lab 02: Basic Transformations
Demonstrations of fundamental ETL operations including:
- Data source configuration
- Field filtering and dropping
- Schema changes
- Join operations
- Aggregations
- S3 output targets

### Lab 04: Glue Job Orchestration
Workflow automation demonstrations including:
- Trigger creation
- Workflow design
- Job and crawler orchestration
- Multi-step ETL pipelines

### Lab 06: Glue Data Quality in ETL Jobs
Data quality implementations featuring:
- Data quality evaluation rules
- Quality outcome monitoring
- S3 target configuration

## 🛠️ Technologies Used

- AWS Glue
- AWS S3
- AWS CLI
- Python (PySpark)

## 📸 Documentation

Each lab includes detailed screenshots documenting the complete process from setup to execution.

## 🎯 Key Learning Outcomes

- AWS Glue Data Catalog management
- ETL job development and optimization
- Workflow orchestration and automation
- Data quality rule implementation
- Both Console and CLI approaches to AWS Glue

## ✅ Key Takeaways

Throughout this AWS Glue workshop, I gained deep insights into building production-grade data pipelines:

### Technical Mastery
- **Metadata Management**: Understanding how AWS Glue Data Catalog functions as a cloud-native Hive Metastore, automatically discovering and cataloging data schemas across multiple formats (CSV, JSON, Parquet)
- **Visual ETL Development**: Leveraging AWS Glue Studio's drag-and-drop interface while maintaining awareness of the underlying PySpark transformations
- **Workflow Orchestration**: Building complex, event-driven pipelines with proper trigger logic and dependency management
- **Data Quality First**: Implementing strict validation rules that fail fast and prevent corrupted data from reaching downstream consumers

### Professional Engineering Practices
- **Fail-Fast Philosophy**: I would rather deal with a failed pipeline that alerts me immediately than let a flawed job run continuously, producing bad data and racking up cloud costs
- **Pragmatic Data Engineering**: I am a pragmatic data engineer who evaluates the possible outputs based on my decisions and learns from other people's experiences
- **Cost Optimization**: Proactively reducing worker counts (from 10 to 5), disabling unnecessary features, and monitoring DPU usage to stay within budget
- **SLA Buffer Strategy**: Setting internal execution targets stricter than business requirements (e.g., 12-minute buffer for 15-minute SLA)
- **Documentation Discipline**: Every transformation, every quality rule, and every design decision must be documented and justified

### Data Integrity Principles
- **Data Quality = Data Integrity**: Once data integrity is compromised, stakeholders lose confidence in reporting
- **No Silent Failures**: Unvalidated transformations create three major risks: unexpected cloud costs, corrupted downstream data, and flawed executive decisions
- **Stop, Fix, Re-run**: When a job fails, stop the pipeline, fix the root cause, and re-run only the affected task—never blindly proceed to downstream steps

## ⚖️ Pros and Cons of Using AWS Glue

### ✅ Advantages

#### Serverless Architecture
- **No Infrastructure Management**: Zero server maintenance, patching, or scaling concerns
- **Auto-Scaling**: Automatically adjusts resources based on workload demands
- **Pay-per-Use**: Only pay for resources consumed during job execution (DPU-hours)

#### Integration with AWS Ecosystem
- **Seamless S3 Integration**: Native support for data lakes on S3
- **Athena Compatibility**: Query cataloged data directly using SQL
- **EMR & Redshift Connectivity**: Easy integration with other AWS analytics services
- **CloudWatch Monitoring**: Built-in logging and metrics for observability

#### Visual Development Experience
- **Glue Studio**: Low-code interface for rapid prototyping
- **Code Generation**: Automatically generates PySpark scripts from visual pipelines
- **Data Preview**: Inspect transformations at each step before running jobs

#### Built-in Data Quality
- **Automated Rule Recommendations**: Glue suggests quality rules based on data profiling
- **CloudWatch Integration**: Real-time quality metrics and alerting
- **Fail-Fast Validation**: Stop pipelines immediately when quality thresholds aren't met

### ❌ Disadvantages

#### Cost Considerations
- **Not Always Cheaper**: For heavy, continuous workloads, long-running EMR clusters or self-managed Spark may be more cost-effective
- **DPU Pricing**: Can become expensive with large-scale transformations or frequent job runs
- **Limited Free Tier**: Crawlers, ETL jobs, and streaming are outside Free Tier boundaries

#### Limited Customization
- **Spark Version Lag**: AWS Glue may not support the latest Apache Spark features immediately
- **Restricted Libraries**: Some Python packages require custom builds or aren't supported
- **Transformation Constraints**: Complex logic may require dropping into custom PySpark code

#### Debugging Challenges
- **Black Box Execution**: Less visibility into Spark driver/executor logs compared to self-managed clusters
- **Slower Iteration**: Each test run incurs startup time and costs
- **Limited Local Development**: Testing locally requires Docker emulation, not identical to production

#### Vendor Lock-in
- **AWS-Specific**: Migration to other cloud providers or on-premises requires significant refactoring
- **Glue-Specific APIs**: Code written for Glue may not translate directly to standard PySpark

## 🎯 As an Aspiring Cloud Data Engineer

My journey through these AWS Glue labs reflects my commitment to becoming a **Cloud Data Engineer** who understands not just how to build pipelines, but how to build them **right**:

### Technical Versatility
- **Multi-Platform Expertise**: Combining AWS Glue knowledge with Databricks experience (currently preparing for Databricks Certified Data Engineer Professional exam)
- **Console + CLI Proficiency**: Comfortable with both visual interfaces for rapid prototyping and command-line tools for automation
- **Infrastructure as Code**: Understanding CloudFormation, IAM roles, and programmatic resource deployment

### Production-Ready Mindset
- **Cost-Conscious Engineering**: Every architectural decision considers compute costs, storage costs, and operational overhead
- **Quality Over Speed**: Prioritizing data integrity and validation over rushing pipelines to production
- **Monitoring & Observability**: Setting up CloudWatch dashboards, error alerts, and quality metrics from day one

### Business Alignment
- **SLA Awareness**: Building pipelines that meet business requirements with internal buffers for safety
- **Stakeholder Communication**: Documenting pipelines so non-technical stakeholders understand data lineage
- **Pragmatic Decision-Making**: Knowing when to skip optional features (like error injection tests) based on real-world failure patterns

## 🏆 As an AWS Community Builder Applicant (Data Category)

Applying for the **AWS Community Builders 2027 cohort** represents my commitment to not just learning AWS technologies, but **sharing that knowledge** with the broader data engineering community:

### Community Contribution Vision
- **Technical Writing**: Creating comprehensive, beginner-friendly documentation (like this portfolio) that goes beyond official docs
- **Real-World Insights**: Sharing honest pros/cons, cost breakdowns, and lessons learned from production pipelines
- **Fail-Fast Stories**: Teaching others through my mistakes—like why I skip error injection tests based on Databricks workflow experience

### Why the Data Category?
- **Data Quality Advocacy**: Championing the principle that "data quality directly equals data integrity"
- **Cloud Cost Education**: Helping teams understand the true cost of serverless data pipelines
- **Cross-Platform Knowledge**: Bridging AWS Glue with Databricks, Great Expectations, dbt, and other data tools

### What I Bring to the Community
- **Mentorship Experience**: As a Support Instructor at For The Women Foundation, I've taught data engineering concepts to women entering tech
- **Practical Focus**: Emphasis on production-ready patterns over toy examples
- **Honest Communication**: Transparent about costs, limitations, and when AWS Glue is (or isn't) the right choice

## 👩‍🏫 My Experience as a Support Instructor at For The Women (FTW) Foundation

During my time mentoring at the **For The Women (FTW) Foundation**, I served as a **Data Engineer Support Instructor**, guiding women in tech through their journey into data engineering:

### Teaching Philosophy
- **Data Quality is Non-Negotiable**: I constantly reminded our scholars that no matter how repetitive data quality checks feel, a failed job should never trigger downstream tasks
- **Fail Fast, Fail Visibly**: I would much rather see a pipeline fail early, where we can isolate the bottleneck, check the logs, and re-run only the failed task
- **Pragmatic Engineering**: Teaching scholars to make informed decisions about which instructions to follow and which to adapt based on real-world cause-and-effect outcomes

### What I Taught
- **Fundamentals of Data Engineering and Data Architecture**: Building strong foundational knowledge in data modeling, pipeline design patterns, and scalable architecture principles
- **Databricks Workflows**: Helping scholars build and monitor ETL pipelines integrated via VS Code
- **Data Quality Standards**: Requiring concrete data quality measurements to prove pipelines were production-ready before capstone presentations
- **Professional Communication**: Training scholars to explain technical decisions to non-technical stakeholders

### Impact on My AWS Glue Practice
The lessons I teach at FTW directly inform how I approach AWS Glue:
- **Documentation First**: Every lab README explains not just "how" but "why"
- **Cost Transparency**: Warning about features outside Free Tier, just like I'd warn scholars about Databricks DBU costs
- **Inclusive Language**: Writing documentation that welcomes beginners while respecting experienced engineers

### Why This Matters
As a Support Instructor, I learned that **the best engineers aren't those who know the most tools—they're the ones who can teach others to use those tools effectively and ethically**. This portfolio isn't just about showcasing my AWS Glue skills; it's about demonstrating my ability to **guide others** through the same learning journey.

## 🔗 Connect with Me

I'm always eager to discuss data engineering, AWS Glue, Databricks, and building inclusive tech communities:

- **LinkedIn**: [Connect with me](https://www.linkedin.com/in/marc-sandrino-78927b112/)
- **GitHub**: [View my repositories](https://github.com/CardinalSeen)
- **Email**: sandrinomarc@gmail.com

**Let's build better data pipelines together!** 🚀

## 📚 Workshop Reference

This portfolio is based on the official AWS Glue Workshop:

**AWS Glue Immersion Day Workshop**  
🔗 [https://catalog.us-east-1.prod.workshops.aws/workshops/ee59d21b-4cb8-4b3d-a629-24537cf37bb5/en-US](https://catalog.us-east-1.prod.workshops.aws/workshops/ee59d21b-4cb8-4b3d-a629-24537cf37bb5/en-US)

I have completed and documented the core modules from this workshop, adding my own insights, teaching perspectives, and production engineering best practices throughout the implementation.

## 📝 Portfolio Notes

This portfolio demonstrates hands-on experience with AWS Glue across various use cases and complexity levels, combining technical expertise with a commitment to data quality, cost awareness, and community education.

> **💡 Note on Cloud Cost Management (FinOps):** 
> Because AWS Glue ETL jobs, crawlers, and interactive sessions are billed per DPU-hour outside the AWS Free Tier, all AWS resources in these labs were terminated and cleaned up immediately after validation to prevent ongoing sandbox charges. As a result, this repository archives complete, step-by-step execution screenshots, CLI commands, and generated PySpark scripts as permanent proof of work.
