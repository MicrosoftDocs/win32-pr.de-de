---
title: ADO LDAP-Bereich-Dialekt
description: Wenn Sie ActiveX Directory Objects (ADO) mit dem LDAP-Dialekt verwenden, sind für das Attribut und den Bereichsspezifizierer keine Anführungszeichen erforderlich.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADO LDAP, umfangreiches Dialekt, ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855368"
---
# <a name="ado-ldap-ranging-dialect"></a>ADO LDAP-Bereich-Dialekt

Wenn Sie ActiveX Directory Objects (ADO) mit dem LDAP-Dialekt verwenden, sind für das Attribut und den Bereichsspezifizierer keine Anführungszeichen erforderlich.

Im folgenden finden Sie ein Beispiel für den ADO LDAP-Dialekt.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




