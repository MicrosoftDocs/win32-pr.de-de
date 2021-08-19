---
title: ADO LDAP Ranging Dialect
description: Wenn ActiveX Directory Objects (ADO) mit dem LDAP-Dialekt verwendet wird, sind für das Attribut und den Bereichsspezifizierer keine Anführungszeichen erforderlich.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADO LDAP Ranging Dialect ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15dba9b7a701b792321ef327d7b5f9893ef3daa0a5eaad80ea151c2b2c90cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023988"
---
# <a name="ado-ldap-ranging-dialect"></a>ADO LDAP Ranging Dialect

Wenn ActiveX Directory Objects (ADO) mit dem LDAP-Dialekt verwendet wird, sind für das Attribut und den Bereichsspezifizierer keine Anführungszeichen erforderlich.

Im Folgenden ist ein Beispiel für den ADO LDAP-Dialekt aufgeführt.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




