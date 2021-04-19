---
description: Mit den Funktionen in diesem Abschnitt werden Druckertreiber auf einem Computer installiert und konfiguriert.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Referenz zur Druckertreiber Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362311"
---
# <a name="printer-driver-installation-reference"></a>Referenz zur Druckertreiber Installation

Mit den Funktionen in diesem Abschnitt werden Druckertreiber auf einem Computer installiert und konfiguriert.

## <a name="in-this-section"></a>In diesem Abschnitt



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
<td><a href="addmonitor.md"><strong>Addmonitor</strong></a><br/></td>
<td>Mit der <a href="/windows/desktop/printdocs/addmonitor"><strong>addmonitor</strong></a> -Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td>Die Funktion <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die Funktion <strong>AddPort</strong> wird vom Port Monitor exportiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>Addprinterdriver</strong></a><br/></td>
<td>Mit der <a href="/windows/desktop/printdocs/addprinterdriver"><strong>addprinterdriver</strong></a> -Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.<br/> Wenn Sie Druckertreiber installieren oder aktualisieren, können Sie die <a href="addprinterdriverex.md"><strong>addprinterdriverex</strong></a> -Funktion verwenden, da Sie strikte Upgrades, strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von den Dateizeitstempeln) zulässt.<br/>
<blockquote>
[!Note]<br />
Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen. Verwenden Sie stattdessen " <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a> ".
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>Addprinterdriverex</strong></a><br/></td>
<td>Die Funktion <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>addprinterdriverex</strong></a> installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien. Neben den Funktionen von <a href="addprinterdriver.md"><strong>addprinterdriver</strong></a>bietet es auch Optionen, die das strikte Upgrade, das strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von Dateizeitstempeln) ermöglichen.<br/>
<blockquote>
[!Note]<br />
Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen. Verwenden Sie stattdessen " <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a> ".
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>Addprintprocessor</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/addprintprocessor"><strong>addprintprocessor</strong></a> -Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>Addprintprovidor</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/addprintprovidor"><strong>addprintprovidor</strong></a> -Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>Coreprinterdriverinstalliert</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>coreprinterdriverinstallierte</strong></a> -Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>Deletemonitor</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/deletemonitor"><strong>deletemonitor</strong></a> -Funktion entfernt einen von der <a href="addmonitor.md"><strong>addmonitor</strong></a> -Funktion hinzugefügten Port Monitor.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>DeletePort</strong></a><br/></td>
<td>Die Funktion <a href="/windows/desktop/printdocs/deleteport"><strong>deletePort</strong></a> zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>Deleteprinterdriver</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>deleteprinterdriver</strong></a> -Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.<br/> Um die dem Treiber zugeordneten Dateien zu löschen und den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber für einen Server zu entfernen, verwenden Sie die Funktion <a href="deleteprinterdriverex.md"><strong>deleteprinterdriverex</strong></a> .<br/> <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>Deleteprinterdriver</strong></a> löscht einen Treiber nur dann, wenn keine Version des Treibers für die angegebene Umgebung verwendet wird. <a href="deleteprinterdriverex.md"><strong>Deleteprinterdriverex</strong></a> kann bestimmte Versionen des Treibers löschen.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>Deleteprinterdriverex</strong></a><br/></td>
<td>Mit der <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>deleteprinterdriverex</strong></a> -Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht. Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>Deleteprinterdriverpackage</strong></a><br/></td>
<td>Löscht ein Druckertreiber Paket aus dem Treiber Speicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>Deleteprintprocessor</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>deleteprintprocessor</strong></a> -Funktion entfernt einen von der <a href="addprintprocessor.md"><strong>addprintprocessor</strong></a> -Funktion hinzugefügten Druck Prozessor.<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>Deleteprintprovidor</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>deleteprintprovidor</strong></a> -Funktion entfernt einen von der <a href="addprintprovidor.md"><strong>addprintprovidor</strong></a> -Funktion hinzugefügten Druckanbieter.<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>Enumüberwachungen</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/enummonitors"><strong>enummonitors</strong></a> -Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/enumports"><strong>enumports</strong></a> -Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>Enumprinterdrivers</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>enumprinterdrivers</strong></a> -Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>Enumprintprocessordatatypes</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>enumprintprocessordatatypes</strong></a> -Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>Enumprintprozessoren</strong></a><br/></td>
<td>Die Funktion <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>enumprintprozessoren</strong></a> listet die auf dem angegebenen Server installierten Druck Prozessoren auf.<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>Getcoreprinterdrivers</strong></a><br/></td>
<td>Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>Getprinterdriver</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/getprinterdriver"><strong>getprinterdriver</strong></a> -Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von <strong>getprinterdriver</strong> installiert.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td>Die <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> -Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert <strong>GetPrinterDriver2</strong> ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>Getprinterdriverdirectory</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>getprinterdriverdirectory</strong></a> -Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br/></td>
<td>Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>Getprintprocessordirectory</strong></a><br/></td>
<td>Die <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>getprintprocessordirectory</strong></a> -Funktion Ruft den Pfad zum Druck Prozessor Verzeichnis auf dem angegebenen Server ab.<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>Installprinterdriverfrompackage</strong></a><br/></td>
<td>Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Druck Servers befindet.<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>Uploadprinterdriverpackage</strong></a><br/></td>
<td>Lädt einen Druckertreiber in den Treiber Speicher des Druck Servers hoch, sodass er durch Aufrufen von <a href="installprinterdriverfrompackage.md"><strong>installprinterdriverfrompackage</strong></a>installiert werden kann.<br/></td>
</tr>
</tbody>
</table>



 

 

