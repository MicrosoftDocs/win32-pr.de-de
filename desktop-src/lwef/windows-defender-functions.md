---
title: Windows Defender-Funktionen
description: Funktionen, die von apps aufgerufen werden, um Scans, Signatur Updates oder Informationen von Windows Defender anzufordern.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389792"
---
# <a name="windows-defender-functions"></a>Windows Defender-Funktionen

Funktionen, die von apps aufgerufen werden, um Scans, Signatur Updates oder Informationen von Windows Defender anzufordern.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>Mperrormessageformat</strong></a></td>
<td>Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>Mpfrememory</strong></a></td>
<td>Gibt Arbeitsspeicher für den Malware Schutz-Manager frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>Mplenker schließen</strong></a></td>
<td>Schließt das von <a href="mpmanageropen.md"><strong>mpmanageropen</strong></a>, <a href="mpscanstart.md"><strong>mpscanstart</strong></a>, <a href="mpthreatopen.md"><strong>mporial Open</strong></a>oder <a href="mpupdatestart.md"><strong>mpupdatestart</strong></a>zurückgegebene Handle.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>Mpmanageropen</strong></a></td>
<td>Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>Mpmanagerstatus Query</strong></a></td>
<td><strong>Nicht unterstützt.</strong> Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>Mpmanagerstatus-QUERYEX</strong></a></td>
<td>Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>Mpmanagerversionquery</strong></a></td>
<td>Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>Mpscancontrol</strong></a></td>
<td>Ermöglicht das Steuern einer Überprüfung, die asynchron über <a href="mpscanstart.md"><strong>mpscanstart</strong></a>initiiert wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>Mpscanstart</strong></a></td>
<td>Startet einen Scanvorgang.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>Mpzerenumerate</strong></a></td>
<td>Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>Mpbedrohlich öffnen</strong></a></td>
<td>Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück. Diese Funktion kann verwendet werden, um von einer bestimmten Überprüfung erkannte Bedrohungen, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder alle Bedrohungen in der Signaturdatenbank zu öffnen.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>Mpbedrohlich Query</strong></a></td>
<td>Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>Mpupdatecontrol</strong></a></td>
<td>Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über <a href="mpupdatestart.md"><strong>mpupdatestart</strong></a>initiiert wurde.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>Mpupdatestart</strong></a></td>
<td>Startet einen Signatur Aktualisierungs Vorgang.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>Wdenable</strong></a></td>
<td>Ändert den Windows Defender-Status in ein oder aus.<br/>
<blockquote>
[!Note]<br />
Ab Windows 10, Version 1607 und Windows Server 2016, gibt die <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>wdenable</strong></a> -Funktion immer <strong>E_NOTIMPL</strong>zurück.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>Wdstatus</strong></a></td>
<td>Gibt den aktuellen Status von Windows Defender zurück.<br/></td>
</tr>
</tbody>
</table>



 

 

 





