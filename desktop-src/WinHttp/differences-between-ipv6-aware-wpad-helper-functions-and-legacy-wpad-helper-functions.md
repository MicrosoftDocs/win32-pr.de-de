---
title: IPv6-Aware und ältere WPAD-Hilfsfunktionen
description: Unterschiede zwischen IPv6-Aware WPAD-Hilfsfunktionen und älteren WPAD-Hilfsfunktionen
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366083"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware und ältere WPAD-Hilfsfunktionen

In den folgenden Tabellen werden die Unterschiede zwischen den neuen WPAD-Hilfsobjekten und den alten WPAD-Hilfsfunktionen erläutert. Die neuen Funktionen sind mit einem Sternchen gekennzeichnet.



<table>
<thead>
<tr class="header">
<th>Functions</th>
<th>Eingabe</th>
<th>Output</th>
<th>Grund für Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>IPv4-Adresse</td>
<td rowspan="2">Die Funktion "ex" gibt eine Liste von IPv6/IPv4 zurück. Erforderlich, da IPv6-oder IPv4-Adressen mehrere Unicastadressen für eine einzelne Schnittstelle aufweisen können. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>dnsresolveex *</td>
<td>Host</td>
<td>Liste der IPv6/IPv4-Adressen</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Functions</th>
<th>Eingabe</th>
<th>Output</th>
<th>Grund für Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isresolveable</td>
<td>IPv4-Host</td>
<td>TRUE/FALSE</td>
<td rowspan="2">Die Funktion Ex gibt true zurück, wenn ein Host in eine IPv6-oder IPv4-Adresse aufgelöst werden kann. Die Legacy Funktion gibt nur dann true zurück, wenn der Host zu einer IPv4-Adresse aufgelöst wird. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>isresolveableex *</td>
<td>IPv6/IPv4-Host</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Functions</th>
<th>Eingabe</th>
<th>Output</th>
<th>Grund für Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIpAddress</td>
<td>none</td>
<td>IPv4-Adresse</td>
<td rowspan="2">Die Funktion "ex" gibt eine Liste von IPv6/IPv4 zurück. Erforderlich, da IPv6-oder IPv4-Adressen mehrere Unicastadressen für eine einzelne Schnittstelle $ {Remove} $ aufweisen können.<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>none</td>
<td>Liste der IPv6/IPv4-Adressen</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Functions</th>
<th>Eingabe</th>
<th>Output</th>
<th>Grund für Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Host, durch Punkte getrenntes IP-Adress Muster, IP-Adress Maske</td>
<td>TRUE/FALSE</td>
<td rowspan="2">Stellen Sie eine auf IP-Version unabhängige Weise bereit, um zu ermitteln, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet. Außerdem ist die Mask-Notation in IPv4 veraltet. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>isinnettex *</td>
<td>IP-Adress Präfix</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



| Functions           | Eingabe                       | Output                             | Grund für Änderungen                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| "menpaddresslist"\* | Liste der IPv6/IPv4-Adressen | Sortierte Liste der IPv6/IPv4-Adressen | Es gibt keine Entsprechung für die Legacy Funktion, da Legacy Funktionen nur eine einzelne IPv4-Adresse zurückgegeben haben, daher war keine Sortierung erforderlich. |



 



| Functions          | Eingabe | Output                     | Grund für Änderungen                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GetClientVersion\* | none  | WPAD-Engine-Versionsnummer | Diese Funktion gibt derzeit Version 1,0 zurück. Wir haben diese Funktion hinzugefügt, damit IT-Administratoren ihr WPAD aktualisieren können, sodass Sie mit unterschiedlichen Versionen der WPAD-Engine funktionieren, ohne dass die vorhandene Bereitstellung unterbrochen wird. |



 

> [!Note]  
> Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.

 

 

 



