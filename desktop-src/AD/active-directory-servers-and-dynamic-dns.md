---
title: Active Directory-Server und dynamisches DNS
description: Die Active Directory-Server veröffentlichen ihre Adressen, damit Clients sie finden können, die nur den Domänennamen kennen.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Dynamisches DNS Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9508bd571cf60d3801cc5708276ff9399494e354ee3559efd0a3ffa0b96836a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025200"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Active Directory-Server und dynamisches DNS

Die Active Directory-Server veröffentlichen ihre Adressen, damit Clients sie finden können, die nur den Domänennamen kennen. Active Directory-Server werden mithilfe der Dienstressourceneinträge (Service Resource Records, SRV RRs) in DNS veröffentlicht. Die SRV-RR ist ein DNS-Eintrag, der verwendet wird, um den Namen eines Diensts der Adresse eines Servers zu zuordnen, der den Dienst anbietet. Der Name einer SRV-RR ist in der folgenden Form:


```C++
<service>.<protocol>.<domain>
```



Active Directory-Server bieten den LDAP-Dienst über das TCP-Protokoll an, sodass veröffentlichte Namen "ldap.tcp. <domain> " sind. Daher ist die SRV-RR für fabrikam.com "ldap.tcp.fabrikam.com". Zusätzliche Daten zur SRV-RR geben die Priorität und Gewichtung für den Server an, sodass Clients den besten Server für ihre Anforderungen auswählen können.

Wenn ein Active Directory-Server installiert ist, verwendet er dynamisches DNS, um sich selbst zu veröffentlichen. Da sich TCP/IP-Adressen ändern können, überprüfen Server ihre Registrierungen in regelmäßigen Abständen, um sicherzustellen, dass sie korrekt sind, und aktualisieren sie bei Bedarf.

Dynamisches DNS ist eine kürzliche Ergänzung des DNS-Standards. Dynamisches DNS definiert ein Protokoll zum dynamischen Aktualisieren eines DNS-Servers mit neuen Daten. Vor dem dynamischen DNS mussten Administratoren die von DNS-Servern gespeicherten Einträge manuell konfigurieren.

 

 




