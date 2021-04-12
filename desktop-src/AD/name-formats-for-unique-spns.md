---
title: Namens Formate für eindeutige SPNs
description: Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Namens Formate für eindeutige SPNs AD
- Dienst Prinzipal Name AD, namens Formate für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206256"
---
# <a name="name-formats-for-unique-spns"></a>Namens Formate für eindeutige SPNs

Ein SPN muss in der Gesamtstruktur, in der er registriert ist, eindeutig sein. Wenn Sie nicht eindeutig ist, tritt bei der Authentifizierung ein Fehler auf. Die SPN-Syntax hat vier Elemente: zwei erforderliche Elemente und zwei weitere Elemente, die Sie ggf. verwenden können, um einen eindeutigen Namen zu erhalten, wie in der folgenden Tabelle aufgeführt.


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;&lt;Dienstklasse&gt;&quot;</td>
<td>Eine Zeichenfolge, die die allgemeine Dienstklasse identifiziert. Beispiel: &quot; SQLServer &quot; . Es gibt bekannte Dienst Klassennamen, wie z. b &quot; &quot; . www für einen Webdienst oder &quot; LDAP &quot; für einen Verzeichnisdienst. Im Allgemeinen kann dies eine beliebige Zeichenfolge sein, die für die Dienstklasse eindeutig ist. Beachten Sie, dass die SPN-Syntax einen Schrägstrich (/) zum Trennen von Elementen verwendet, sodass dieses Zeichen nicht in einem Dienst Klassennamen vorkommen kann.</td>
</tr>
<tr class="even">
<td>&quot;&lt;Host&gt;&quot;</td>
<td>Der Name des Computers, auf dem der-Dienst ausgeführt wird. Dies kann ein voll qualifizierter DNS-Name oder ein NetBIOS-Name sein. Beachten Sie, dass NetBIOS-Namen innerhalb einer Gesamtstruktur nicht unbedingt eindeutig sind. Folglich ist ein SPN, der einen NetBIOS-Namen enthält, möglicherweise auch nicht eindeutig.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;Port&gt;&quot;</td>
<td>Eine optionale Portnummer zur Unterscheidung zwischen mehreren Instanzen derselben Dienstklasse auf einem einzelnen Host Computer. Lassen Sie diese Komponente Weg, wenn der Dienst den Standardport für die Dienstklasse verwendet.</td>
</tr>
<tr class="even">
<td>&quot;&lt;Dienst Name&gt;&quot;</td>
<td>Ein optionaler Name, der in den SPNs eines replizierungsdiensts verwendet wird, um die Daten oder Dienste zu identifizieren, die vom Dienst oder der vom Dienst bereitgestellten Domäne bereitgestellt werden. Diese Komponente kann eines der folgenden Formate aufweisen:
<ul>
<li>Der Distinguished Name oder die objectGUID eines Objekts in Active Directory Domain Services, z. b. ein Dienst Verbindungspunkt (Service Connection Point, SCP).</li>
<li>Der DNS-Name der Domäne für einen Dienst, der einen angegebenen Dienst für eine Domäne als Ganzes bereitstellt.</li>
<li>Der DNS-Name eines SRV-oder MX-Einsatzes.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Welche Komponenten in den SPNs eines dienstanders vorhanden sind, hängt davon ab, wie der Dienst identifiziert und repliziert wird. Es gibt zwei grundlegende Szenarien: Host basierte Dienste und replizierungsdienste.

## <a name="host-based-services"></a>Host basierte Dienste

Bei einem Host basierten Dienst wird die Komponente " &lt; Dienst Name &gt; " ausgelassen, da der Dienst durch die Dienstklasse und den Namen des Host Computers, auf dem der Dienst installiert ist, eindeutig identifiziert wird.


```C++
<service class>/<host>
```



Die Dienstklasse allein ist ausreichend, um für Clients die Funktionen zu identifizieren, die der Dienst bereitstellt. Sie können Instanzen der Dienstklasse auf vielen Computern installieren, und jede Instanz bietet Dienste, die mit Ihrem Host Computer identifiziert werden. FTP und Telnet sind Beispiele für Host basierte Dienste. Die SPNs einer Host basierten Dienst Instanz können die Portnummer enthalten, wenn der Dienst einen nicht standardmäßigen Port verwendet oder mehrere Instanzen des Diensts auf dem Host vorhanden sind.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Replizierungsdienste

Bei einem replizierbaren Dienst kann eine oder mehrere Instanzen des Dienstanbieter (Replikate) vorhanden sein, und Clients unterscheiden sich nicht, mit welchem Replikat Sie eine Verbindung herstellen, da jeweils derselbe Dienst bereitstellt. Die SPNs für jedes Replikat verfügen über die gleichen " &lt; Service Class &gt; "-und " &lt; Service Name &gt; "-Komponenten, wobei " &lt; Dienst Name &gt; " genauer identifiziert, welche Funktionen vom Dienst bereitgestellt werden. Nur die &lt; Komponenten "Host &gt; " und " &lt; Port &gt; " unterscheiden sich von SPN zum SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Ein Beispiel für einen replizierbaren Dienst ist eine Instanz eines Daten Bank Dienstanbieter, der den Zugriff auf eine angegebene Datenbank ermöglicht. In diesem Fall identifiziert " &lt; Dienstklasse &gt; " die Datenbankanwendung, und " &lt; Dienst Name &gt; " identifiziert die jeweilige Datenbank. " &lt; Service Name &gt; " kann der Distinguished Name eines Dienst Verbindungs Punkts (Service Connection Point, SCP) sein, der die Verbindungsdaten für die Datenbank enthält.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Wenn der NetBIOS-Name von Clients zum Verfassen eines Dienst Prinzipal namens verwendet wird, muss jedes Replikat auch einen SPN registrieren, der den NetBIOS-Namen enthält.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Ein weiteres Beispiel für einen replizierbaren Dienst ist ein Dienst, der Dienste für eine gesamte Domäne bereitstellt. In diesem Fall &lt; handelt es sich bei der Komponente "Dienst Name &gt; " um den DNS-Namen der Domäne, die bereitgestellt wird. Ein Kerberos-KDC ist ein Beispiel für diese Art von Replizierungsdienst.

Beachten Sie, dass das System bei einer Änderung des DNS-Namens eines Computers das " &lt; Host &gt; "-Element für alle registrierten SPNs für diesen Host in der Gesamtstruktur aktualisiert.

 

 




