---
title: Updated - Analysis Services for SQL Server docs | Microsoft Docs
description: Display snippets of updated content for recently changed in documentation, for Analysis Services for Microsoft SQL Server.
services: na
documentationcenter: ''
author: MightyPen
manager: jhubbard
editor: ''
ms.service: na
ms.topic: updart-autogen
ms.technology: database-engine
ms.custom: UpdArt.exe
ms.workload: analysis-services
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: updart-autogen
ms.date: 09/27/2017
ms.author: genemi
---
# New and Recently Updated: Analysis Services for SQL Server



Nearly every day Microsoft updates some of its existing articles on its [Docs.Microsoft.com](http://docs.microsoft.com/) documentation website. This article displays excerpts from recently updated articles. Links to new articles might also be listed.

This article is generated by a program that is rerun periodically. Occasionally an excerpt can appear with imperfect formatting, or as markdown from the source article. Images are never displayed here.

Recent updates are reported for the following date range and subject:



- *Date range of updates:* &nbsp; **2017-09-11** &nbsp; -to- &nbsp; **2017-09-27**
- *Subject area:* &nbsp; **Analysis Services for SQL Server**.




&nbsp;

## New Articles Created Recently

The following links jump to new articles that have been added recently.


***There are no new articles to list, this time.***



&nbsp;

## Updated Articles with Excerpts

This section displays the excerpts of updates gathered from articles that have recently experienced a large update.

The excerpts displayed here appear separated from their proper semantic context. Also, sometimes an excerpt is separated from important markdown syntax that surrounds it in the actual article. Therefore these excerpts are for general guidance only. The excerpts only enable you to know whether your interests warrant taking the time to click and visit the actual article.

For these and other reasons, do not copy code from these excerpts, and do not take as exact truth any text excerpt. Instead, visit the actual article.





&nbsp;

<a name="compactupdatedlist"/>

### Compact List of Articles Updated Recently

This compact list provides links to all the updated articles that are listed in the Excerpts section.

1. [What&#39;s new in SQL Server 2017 Analysis Services](#TitleNum_1)




&nbsp;

&nbsp;

<a name="TitleNum_1"/>

### 1. &nbsp; [What&#39;s new in SQL Server 2017 Analysis Services](what-s-new-in-sql-server-analysis-services-2017.md)

*Updated: 2017-09-22* &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 

<!-- Source markdown line 143.  ms.author= "owend".  -->

&nbsp;


<!-- git diff --ignore-all-space --unified=0 c8d75883f07e6e32859728d09139920eb9bf65c5 d206e83413d15a6e6116120e4a98dda9c8ce81d8  (PR=3278  ,  Filename=what-s-new-in-sql-server-analysis-services-2017.md  ,  Dirpath=docs\analysis-services\  ,  MergeCommitSha40=656e62f36446db4ef5b232129130a0253d2aebdf) -->



**Object-level security**

This release introduces [object-level security--../analysis-services/tabular-models/object-level-security.md) for tables and columns. In addition to restricting access to table and column data, sensitive table and column names can be secured. This helps prevent a malicious user from discovering such a table exists.

Object-level security must be set using the JSON-based metadata, Tabular Model Scripting Language (TMSL), or Tabular Object Model (TOM).

For example, the following code helps secure the Product table in the sample Adventure Works tabular model by setting the **MetadataPermission** property of the **TablePermission** class to **None**.

```
//Find the Users role in Adventure Works and secure the Product table
ModelRole role = db.Model.Roles.Find("Users");
Table productTable = db.Model.Tables.Find("Product");
if (role != null && productTable != null)
{
    TablePermission tablePermission;
    if (role.TablePermissions.Contains(productTable.Name))
    {
        tablePermission = role.TablePermissions[productTable.Name];
    }
    else
    {
        tablePermission = new TablePermission();
        role.TablePermissions.Add(tablePermission);
        tablePermission.Table = productTable;
    }
    tablePermission.MetadataPermission = MetadataPermission.None;
}
db.Update(UpdateOptions.ExpandFull);
```

**Dynamic Management Views (DMVs)**

[DMVs--../analysis-services/instances/use-dynamic-management-views-dmvs-to-monitor-analysis-services.md) are queries in SQL Server Profiler that return information about local server operations and server health.
This release includes improvements to [Dynamic Management Views](https://docs.microsoft.com/sql/analysis-services/instances/use-dynamic-management-views-dmvs-to-monitor-analysis-services) (DMV) for tabular models at the 1200 and 1400 compatibility levels.







## Similar Articles

<!--  HOW TO:
    Refresh this file's line items with the latest 'Count-in-Similars*' content.
    Then run Run-533-*.BAT
-->

This section lists very similar articles for recently updated articles in other subject areas, within our public GitHub.com repository: [MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs/).

#### Subject areas which do have new or recently updated articles

- [New + Updated (0+1): **Advanced Analytics for SQL** docs](../advanced-analytics/new-updated-advanced-analytics.md)
- [New + Updated (0+1): **Analysis Services for SQL** docs](../analysis-services/new-updated-analysis-services.md)
- [New + Updated (4+1): **Database Engine for SQL** docs](../database-engine/new-updated-database-engine.md)
- [New + Updated (17+0): **Integration Services for SQL** docs](../integration-services/new-updated-integration-services.md)
- [New + Updated (3+0): **Linux for SQL** docs](../linux/new-updated-linux.md)
- [New + Updated (1+1): **Relational Databases for SQL** docs](../relational-databases/new-updated-relational-databases.md)
- [New + Updated (2+0): **Reporting Services for SQL** docs](../reporting-services/new-updated-reporting-services.md)
- [New + Updated (0+1): **SQL Server Management Studio (SSMS)** docs](../ssms/new-updated-ssms.md)
- [New + Updated (0+1): **Transact-SQL** docs](../t-sql/new-updated-t-sql.md)

#### Subject areas which have no new or recently updated articles

- [New + Updated (0+0): **ActiveX Data Objects (ADO) for SQL** docs](../ado/new-updated-ado.md)
- [New + Updated (0+0): **Connect to SQL** docs](../connect/new-updated-connect.md)
- [New + Updated (0+0): **Data Quality Services for SQL** docs](../data-quality-services/new-updated-data-quality-services.md)
- [New + Updated (0+0): **Data Mining Extensions (DMX) for SQL** docs](../dmx/new-updated-dmx.md)
- [New + Updated (0+0): **Master Data Services (MDS) for SQL** docs](../master-data-services/new-updated-master-data-services.md)
- [New + Updated (0+0): **Multidimensional Expressions (MDX) for SQL** docs](../mdx/new-updated-mdx.md)
- [New + Updated (0+0): **ODBC (Open Database Connectivity) for SQL** docs](../odbc/new-updated-odbc.md)
- [New + Updated (0+0): **PowerShell for SQL** docs](../powershell/new-updated-powershell.md)
- [New + Updated (0+0): **Samples for SQL** docs](../sample/new-updated-sample.md)
- [New + Updated (0+0): **Microsoft SQL Server** docs](../sql-server/new-updated-sql-server.md)
- [New + Updated (0+0): **SQL Server Data Tools (SSDT)** docs](../ssdt/new-updated-ssdt.md)
- [New + Updated (0+0): **SQL Server Migration Assistant (SSMA)** docs](../ssma/new-updated-ssma.md)
- [New + Updated (0+0): **Tools for SQL** docs](../tools/new-updated-tools.md)
- [New + Updated (0+0): **XQuery for SQL** docs](../xquery/new-updated-xquery.md)


