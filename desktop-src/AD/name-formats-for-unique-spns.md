---
title: Namensformate für eindeutige SPNs
description: Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Namensformate für eindeutige SPNs AD
- Dienstprinzipalname AD , Namensformate für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b041f88bc025c604ec5f0ad9a6bf5ba7f4cdabc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472335"
---
# <a name="name-formats-for-unique-spns"></a>Namensformate für eindeutige SPNs

Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein. Wenn sie nicht eindeutig ist, tritt bei der Authentifizierung ein Fehler auf. Die SPN-Syntax verfügt über vier Elemente: zwei erforderliche Elemente und zwei zusätzliche Elemente, die Sie bei Bedarf verwenden können, um einen eindeutigen Namen zu erstellen, wie in der folgenden Tabelle aufgeführt.


```C++
<service class>/<host>:<port>/<service name>
```






| Element | Beschreibung | 
|---------|-------------|
| "<service class>" | Eine Zeichenfolge, die die allgemeine Dienstklasse identifiziert. Beispiel: "SqlServer". Es gibt bekannte Dienstklassennamen, z. B. "www" für einen Webdienst oder "ldap" für einen Verzeichnisdienst. Im Allgemeinen kann dies eine beliebige Zeichenfolge sein, die für die Dienstklasse eindeutig ist. Beachten Sie, dass die SPN-Syntax einen Schrägstrich (/) verwendet, um Elemente zu trennen, sodass dieses Zeichen nicht in einem Dienstklassennamen angezeigt werden kann. | 
| "<host>" | Der Name des Computers, auf dem der Dienst ausgeführt wird. Dabei kann es sich um einen vollqualifizierten DNS-Namen oder einen NetBIOS-Namen handelt. Beachten Sie, dass NetBIOS-Namen innerhalb einer Gesamtstruktur nicht unbedingt eindeutig sind. Folglich ist ein SPN, der einen NetBIOS-Namen enthält, möglicherweise auch nicht eindeutig. | 
| "<port>" | Eine optionale Portnummer, um zwischen mehreren Instanzen derselben Dienstklasse auf einem einzelnen Hostcomputer zu unterscheiden. Lässt diese Komponente aus, wenn der Dienst den Standardport für seine Dienstklasse verwendet. | 
| "<service name>" | Ein optionaler Name, der in den SPNs eines replizierbaren Diensts verwendet wird, um die Daten oder Dienste zu identifizieren, die vom Dienst oder der vom Dienst bereitgestellten Domäne bereitgestellt werden. Diese Komponente kann eines der folgenden Formate aufweisen:<ul><li>Der Distinguished Name oder objectGUID eines Objekts in Active Directory Domain Services, z. B. ein Dienstverbindungspunkt (Service Connection Point, SCP).</li><li>Der DNS-Name der Domäne für einen Dienst, der einen angegebenen Dienst für eine Domäne als Ganzes bereitstellt.</li><li>Der DNS-Name eines SRV- oder MX-Eintrags.</li></ul> | 




 

Welche Komponenten in den SPNs eines Diensts vorhanden sind, hängt davon ab, wie der Dienst identifiziert und repliziert wird. Es gibt zwei grundlegende Szenarien: hostbasierte Dienste und replizierbare Dienste.

## <a name="host-based-services"></a>Hostbasierte Dienste

Bei einem hostbasierten Dienst wird die &lt; Komponente "Dienstname" &gt; ausgelassen, da der Dienst durch die Dienstklasse und den Namen des Hostcomputers, auf dem der Dienst installiert ist, eindeutig identifiziert wird.


```C++
<service class>/<host>
```



Die Dienstklasse allein reicht aus, um für Clients die Features zu identifizieren, die der Dienst bereitstellt. Sie können Instanzen der Dienstklasse auf vielen Computern installieren, und jede Instanz stellt Dienste bereit, die mit ihrem Hostcomputer identifiziert werden. FTP und Telnet sind Beispiele für hostbasierte Dienste. Die SPNs einer hostbasierten Dienstinstanz können die Portnummer enthalten, wenn der Dienst einen nicht standardmäßigen Port verwendet oder mehrere Instanzen des Diensts auf dem Host vorhanden sind.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Replizierbare Dienste

Für einen replizierbaren Dienst können eine oder mehrere Instanzen des Diensts (Replikate) vorhanden sein, und Clients unterscheiden nicht, mit welchem Replikat sie eine Verbindung herstellen, da jede instanz denselben Dienst bereitstellt. Die SPNs für jedes Replikat verfügen über die gleichen Komponenten " &lt; Dienstklasse &gt; " und " &lt; Dienstname &gt; ", wobei " &lt; Dienstname " die vom Dienst &gt; bereitgestellten Funktionen genauer identifiziert. Nur die &lt; Komponenten " host " und optional " port " unterscheiden sich von &gt; &lt; &gt; SPN zu SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Ein Beispiel für einen replizierbaren Dienst wäre eine Instanz eines Datenbankdiensts, der Zugriff auf eine angegebene Datenbank bereitstellt. In diesem Fall identifiziert die &lt; Dienstklasse &gt; die Datenbankanwendung und der &lt; Dienstname &gt; die spezifische Datenbank. &lt;"Dienstname" &gt; kann der Distinguished Name eines Dienstverbindungspunkts (Service Connection Point, SCP) sein, der Verbindungsdaten für die Datenbank enthält.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Wenn Clients den NetBIOS-Namen verwenden, um den SPN eines Diensts zu erstellen, muss jedes Replikat auch einen SPN registrieren, der den NetBIOS-Namen enthält.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Ein weiteres Beispiel für einen replizierbaren Dienst ist ein Dienst, der Dienste für eine gesamte Domäne bereitstellt. In diesem Fall ist die &lt; Komponente "Dienstname" &gt; der DNS-Name der Domäne, die bedient wird. Ein Kerberos-KDC ist ein Beispiel für diese Art von replizierbaren Dienst.

Beachten Sie, dass das System das &lt; Hostelement für alle registrierten SPNs für diesen Host in der Gesamtstruktur aktualisiert, wenn sich der DNS-Name eines &gt; Computers ändert.

 

 




