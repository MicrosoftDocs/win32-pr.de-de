---
title: ADO SQL Ranging Dialect
description: Bei Verwendung des ActiveX Directory Objects (ADO) mit dem SQL-Dialekt müssen um das Attribut und den Bereichsspezifizierer einfache Anführungszeichen (') verwendet werden.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADO SQL Ranging Dialect ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad714a514bb926239ebb521391d40d097e7f4ee6ccf50208aaed4bba54d8af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181144"
---
# <a name="ado-sql-ranging-dialect"></a>ADO SQL Ranging Dialect

Bei Verwendung des ActiveX Directory Objects (ADO) mit dem SQL-Dialekt müssen um das Attribut und den Bereichsspezifizierer einfache Anführungszeichen (') verwendet werden. Im Folgenden finden Sie ein Beispiel für den ADO-SQL Dialekt.


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




