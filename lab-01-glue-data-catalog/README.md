# Lab 1: Working with the Glue Data Catalog

## 📚 Overview

Welcome to Lab 1: Working with the AWS Glue Data Catalog!

The **AWS Glue Data Catalog** serves as AWS's cloud-native, fully managed version of the Apache Hive Metastore. In contrast, a local Apache Hive Metastore is an open-source tool running on your own environment or Docker setup, functioning as a "librarian" or catalog system that stores crucial metadata - such as table schemas, column data types, and physical file locations.

## 🔄 Localhost vs Cloud: A Comparison

In this session, we distinguish the key operational differences between managing metadata locally versus in the cloud, weighing the pros and cons of both approaches:

### Localhost (Apache Hive Metastore)
- ✅ Offers complete control and zero cloud operational costs ($0)
- ✅ Ideal for local development, testing, and isolated sandboxes
- ❌ Requires manual server maintenance
- ❌ Complex Docker configurations
- ❌ Custom scaling as your data footprint grows

### Cloud (AWS Glue Data Catalog)
- ✅ Operates as a serverless, zero-maintenance service
- ✅ Seamlessly scales and integrates directly with analytical engines like Amazon Athena, EMR, Redshift, and PySpark
- ✅ Frees data engineers from infrastructural overhead
- ❌ Introduces pay-per-request pricing

## 🎯 Learning Objectives

Join me as we discover how data catalogs function under the hood! As a data engineer, understanding how metadata libraries manage and organize underlying data assets is essential for building scalable, production-ready data pipelines.

## 📂 Lab Structure

This lab is divided into two approaches:

### [Lab 1.1: AWS Console](./lab-01-01-aws-console/)
Learn how to create and manage the Glue Data Catalog using the AWS Management Console's visual interface. Perfect for:
- Quick prototyping
- Visual learners
- Understanding the concepts before automation

### [Lab 1.2: AWS CLI](./lab-01-02-aws-cli/)
Learn how to create and manage the Glue Data Catalog using command-line tools. Essential for:
- Automation and scripting
- CI/CD pipelines
- Infrastructure as Code practices

## ✅ Key Takeaways

For this lab, we set up the Glue crawler using both the AWS Management Console and the AWS CLI. While the console offers an intuitive, visual way to get started quickly, we also practiced creating the database and crawlers through the AWS CLI to strengthen our programming skills and execute infrastructure scripts provided by the Data Architect.

Advanced optional topics, such as **S3 Event Notifications**, **Python Boto3**, **Athena**, **CloudFormation**, and **Spark**, were skipped for now so we could focus on mastering the fundamentals. This keeps the walkthrough simple to replicate, share, and apply across self-paced learning environments.

**Whether you rely on the console or write CLI commands depends on your project requirements, the tools your team has chosen, and your own engineering instinct. What matters most is that your pipeline runs cleanly without errors or failing its quality checks.**

## 🛠️ What You'll Learn

By completing this lab, you will understand:

- How AWS Glue Data Catalog organizes metadata
- The difference between databases, tables, and crawlers
- How crawlers automatically discover and catalog data
- Schema inference for multiple data formats (CSV, JSON)
- Both GUI and programmatic approaches to Glue management
- Best practices for metadata management in the cloud

## 🚀 Getting Started

1. Start with [Lab 1.1: AWS Console](./lab-01-01-aws-console/) to understand the concepts visually
2. Then proceed to [Lab 1.2: AWS CLI](./lab-01-02-aws-cli/) to learn automation techniques
3. Compare both approaches to decide what works best for your use case

## 📋 Prerequisites

- AWS Account with appropriate IAM permissions
- Basic understanding of S3 and data formats (CSV, JSON)
- AWS CLI installed and configured (for Lab 1.2)
- CloudFormation stack deployed with workshop resources

## 🔗 Next Steps

After completing this lab, proceed to [Lab 02: Basic Transformations](../lab-02-basic-transformations/) to learn how to transform and process your cataloged data.
