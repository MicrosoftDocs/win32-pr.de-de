---
title: Active Directory Server und dynamisches DNS
description: Die Active Directory Server veröffentlichen ihre Adressen so, dass Clients Sie nur mit dem Domänen Namen ermitteln können.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- dynamische DNS-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707223"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Active Directory Server und dynamisches DNS

Die Active Directory Server veröffentlichen ihre Adressen so, dass Clients Sie nur mit dem Domänen Namen ermitteln können. Active Directory Server werden mithilfe der Dienst Ressourcen Einträge (SRV RRs) in DNS veröffentlicht. SRV RR ist ein DNS-Datensatz, der verwendet wird, um den Namen eines diensdienstanbieter der Adresse eines Servers zuzuordnen, der den Dienst anbietet. Der Name eines SRV RR hat folgendes Format:


```C++
<service>.<protocol>.<domain>
```



Active Directory Server bieten den LDAP-Dienst über das TCP-Protokoll, sodass veröffentlichte Namen "LDAP. TCP <domain> " lauten. Daher ist SRV RR für fabrikam.com "LDAP.TCP.fabrikam.com". Zusätzliche Daten über SRV RR geben die Priorität und Gewichtung für den Server an, sodass Clients den besten Server für Ihre Anforderungen auswählen können.

Wenn ein Active Directory Server installiert ist, verwendet er Dynamic DNS, um sich selbst zu veröffentlichen. Da TCP/IP-Adressen geändert werden können, überprüfen Server in regelmäßigen Abständen ihre Registrierungen, um sicherzustellen, dass Sie korrekt sind, und aktualisieren Sie ggf..

Dynamic DNS ist eine neuere Ergänzung zum DNS-Standard. Dynamic DNS definiert ein Protokoll zum dynamischen Aktualisieren eines DNS-Servers mit neuen Daten. Vor dem dynamischen DNS mussten Administratoren die von DNS-Servern gespeicherten Datensätze manuell konfigurieren.

 

 




