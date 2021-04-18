---
title: ADO-SQL-Bereich-Dialekt
description: Bei Verwendung von ADO (ActiveX Directory Objects) mit dem SQL-Dialekt müssen einfache Anführungszeichen (') um das Attribut und den Bereichsspezifizierer verwendet werden.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADO-SQL-Bereich mit Umfang reichender Dialekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338971"
---
# <a name="ado-sql-ranging-dialect"></a><span data-ttu-id="5fc83-104">ADO-SQL-Bereich-Dialekt</span><span class="sxs-lookup"><span data-stu-id="5fc83-104">ADO SQL Ranging Dialect</span></span>

<span data-ttu-id="5fc83-105">Bei Verwendung von ADO (ActiveX Directory Objects) mit dem SQL-Dialekt müssen einfache Anführungszeichen (') um das Attribut und den Bereichsspezifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc83-105">When using the ActiveX Directory Objects (ADO), using the SQL dialect, single quotation marks (') must be used around the attribute and range specifier.</span></span> <span data-ttu-id="5fc83-106">Im folgenden finden Sie ein Beispiel für den ADO SQL-Dialekt.</span><span class="sxs-lookup"><span data-stu-id="5fc83-106">The following is an example of the ADO SQL dialect.</span></span>


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




