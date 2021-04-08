---
description: 'In diesem Abschnitt werden die Eigenschaften aufgelistet, die Windows Installer definiert sind:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Eigenschafts Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae30800d3c718549ecc887e3438d743881f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756486"
---
# <a name="property-reference"></a>Eigenschafts Verweis

In diesem Abschnitt werden die Eigenschaften aufgelistet, die Windows Installer definiert sind:

-   [Eigenschaften von Komponenten Speicherort](#component-location-properties)
-   [Konfigurations Eigenschaften](#configuration-properties)
-   [Datums-und Uhrzeit Eigenschaften](#date-time-properties)
-   [Eigenschaften von featureinstallationsoptionen](#feature-installation-options-properties)
-   [Hardware Eigenschaften](#hardware-properties)
-   [Eigenschaften des Installations Status](#installation-status-properties)
-   [Betriebs System Eigenschaften](#operating-system-properties)
-   [Eigenschaften von Produktinformationen](#product-information-properties)
-   [Aktualisierungs Eigenschaften für Zusammenfassungs Informationen](#summary-information-update-properties)
-   [Eigenschaften von System Ordnern](#system-folder-properties)
-   [Eigenschaften von Benutzerinformationen](#user-information-properties)

Weitere Eigenschaften können durch erstellte Daten oder benutzerdefinierte Aktionen angegeben werden. Eigenschaften, deren Namen keine Kleinbuchstaben enthalten, sind öffentliche Eigenschaften und können in der Befehlszeile angegeben werden.

Informationen zu den Werten des Registrierungsschlüssels für die **Deinstallation** , die von den Eigenschaften des Installationsprogramms bereitgestellt werden, finden Sie unter [deinstallieren](uninstall-registry-key.md)

## <a name="component-location-properties"></a>Eigenschaften von Komponenten Speicherort

In der folgenden Liste finden Sie Links zu weiteren Informationen zu den Eigenschaften des Komponenten Speicher Orts.



| Eigenschaft                                                            | BESCHREIBUNG                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Originaldatabase**](originaldatabase.md)<br/>             | Das Installationsprogramm legt diese Eigenschaft auf die Datenbank "gestartet-aus", die Datenbank für die Quelle oder die zwischengespeicherte Datenbank fest.<br/>                                                                                     |
| [**"Parser-originaldatabase"**](parentoriginaldatabase.md)<br/> | Das Installationsprogramm legt diese Eigenschaft für Installationen fest, die von einer [gleichzeitigen Installation](concurrent-installations.md) ausgeführt werden.<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Stammverzeichnis, das die Quelldateien enthält.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Gibt das Stammverzeichnis für die Installation an. Bei einer [administrativen Installation](administrative-installation.md) ist diese Eigenschaft der Speicherort, an dem das Installationspaket kopiert wird.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

In der folgenden Liste finden Sie Links zu weiteren Informationen zu anderen konfigurierbaren Eigenschaften.



| Eigenschaft                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinspiel**](action.md)<br/>                                                     | Anfängliche Aktion, die aufgerufen wird, nachdem das Installationsprogramm initialisiert wurde.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Bestimmt, wo Konfigurationsinformationen gespeichert werden.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Arpauthorizedcdfprefix**](arpauthorizedcdfprefix.md)<br/>                     | Die URL des Aktualisierungs Kanals für eine Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**Arpcomments**](arpcomments.md)<br/>                                           | Enthält Kommentare **für die Software** in der **Systemsteuerung**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Arpcontact**](arpcontact.md)<br/>                                             | Stellt **den Kontakt** für die Option "Software" in der **Systemsteuerung** bereit.<br/>                                                                                                                                                                                                                                                                                                          |
| [**Arpinstalllocation**](arpinstalllocation.md)<br/>                             | Voll qualifizierter Pfad zum primären Ordner einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**Arpnomodify**](arpnomodify.md)<br/>                                           | Deaktiviert die Funktionalität, die ein Produkt ändert.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Deaktiviert die Funktionen, die ein Produkt entfernen.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Arpnorepair**](arpnorepair.md)<br/>                                           | Deaktiviert die Schaltfläche **Reparieren** im Assistenten für Programme.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**Arpproducticon**](arpproducticon.md)<br/>                                     | Gibt das primäre Symbol für das Installationspaket an.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**Arpreadme**](arpreadme.md)<br/>                                               | Enthält eine **Info** Datei **für die Option** "Software" in der **Systemsteuerung**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**Arpsize**](arpsize.md)<br/>                                                   | Geschätzte Größe einer Anwendung in Kilobyte.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Verhindert, dass eine Anwendung in der **Liste "** Software" angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Arpurlinfoabout**](arpurlinfoabout.md)<br/>                                   | URL für die Startseite einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**Arpurlupdateinfo**](arpurlupdateinfo.md)<br/>                                 | URL für Anwendungs Update Informationen.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Availablefreereg**](availablefreereg.md)<br/>                                 | Registrierungsbereich (in Kilobyte), der für eine Anwendung erforderlich ist. Wird von der [Aktion "Zuweisung-gistryspace](allocateregistryspace-action.md)" verwendet.<br/>                                                                                                                                                                                                                                              |
| [**CCP- \_ Laufwerk**](ccp-drive.md)<br/>                                              | Der Stammpfad für die qualifizierenden Produkte für CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Defaultuifont**](defaultuifont.md)<br/>                                       | Der Standard Schriftart Stil, der für Steuerelemente verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Disableadvtverknüpfungen**](disableadvtshortcuts.md)<br/>                         | Legen Sie fest, um die Generierung der spezifischen Verknüpfungen zu deaktivieren, die [Installation bei Bedarf](installation-on-demand.md)unterstützen.<br/>                                                                                                                                                                                                                                                            |
| [**Disablemedia**](-disablemedia.md)<br/>                                        | Verhindert, dass das Installationsprogramm Medienquellen, z. b. CD-ROMs, als gültige Quellen für das Produkt registriert.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Deaktiviert Rollbacks für die aktuelle Konfiguration.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Von ExecuteAction initiierte Aktion der obersten Ebene.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Executemode**](executemode.md)<br/>                                           | Ausführungs Modus, der vom Installationsprogramm ausgeführt wird.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Verbessert die Installations Leistung in bestimmten OEM-Szenarios.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Anfängliche Ebene, auf der die-Funktionen installiert werden.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**Limitui**](limitui.md)<br/>                                                   | Auf der Benutzeroberfläche als "Basic" begrenzt.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Logaction**](logaction.md)<br/>                                               | Liste der zu protokollierenden Aktions Namen.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**Mediapackagepath**](mediapackagepath.md)<br/>                                 | Diese Eigenschaft muss auf den relativen Pfad festgelegt werden, wenn sich das Installationspaket nicht im Stammverzeichnis der CD-ROM befindet.<br/>                                                                                                                                                                                                                                                               |
| [**Msiarpsettingsidentifier**](msiarpsettingsidentifier.md)<br/>                 | Diese optionale Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungs Speicherorte, an denen die Anwendung die Einstellungen und Einstellungen des Benutzers speichert. Verfügbar mit Windows Installer 4,0.<br/>                                                                                                                                                                                        |
| [**Msidisableeeui**](msidisableeeui.md)<br/>                                     | Deaktivieren Sie die eingebettete Benutzeroberfläche für die Installation.<br/> **[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.<br/>                                                                                                                                                                                                           |
| [**Msifastinstall**](msifastinstall.md)<br/>                                     | Verkürzen Sie den Zeitaufwand für die Installation eines großen Windows Installer Pakets.<br/> **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                                                                                                                                                                                              |
| [**Msiinstallperuser**](msiinstallperuser.md)<br/>                               | Fordert an, dass der Windows Installer das Paket nur für den aktuellen Benutzer installiert.<br/> **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                                                                                                                                                                                  |
| [**Msinodisablemedia**](msinodisablemedia.md)<br/>                               | Legen Sie diese Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die [**disablemedia**](-disablemedia.md) -Eigenschaft festlegt.<br/>                                                                                                                                                                                                                                                                        |
| [**Msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md)<br/>   | Legen Sie diese Eigenschaft in der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md) auf 1 (eins) fest, um die upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md) eines bestimmten Produkts anzuwenden. Verfügbar ab Windows Installer 3,0.<br/>                                                                                     |
| [**Msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md)<br/> | Wenn diese Eigenschaft auf 1 festgelegt wurde, kann das Installationsprogramm die Registrierung aufheben und redundante Komponenten deinstallieren, um zu verhindern, dass verwaiste Komponenten auf dem Computer übrig bleiben.<br/> **[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Ermöglicht dem Autor das Festlegen eines primären Ordners für eine-Installation. Wird verwendet, um die Werte für die Eigenschaften [**primaryvolumepath**](primaryvolumepath.md), [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md), [**primaryvolumespacerequired**](primaryvolumespacerequired.md)und [**primaryvolumespaceremainung**](primaryvolumespaceremaining.md) zu ermitteln.<br/> |
| [**Privilegierten**](privileged.md)<br/>                                             | Führt eine Installation mit erhöhten Rechten aus.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Promptrollbackcost**](promptrollbackcost.md)<br/>                             | Aktion, wenn nicht genügend Speicherplatz für die Installation vorhanden ist.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**Star**](reboot.md)<br/>                                                     | Erzwingt oder unterdrückt einen Neustart.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Unterdrückt die Anzeige von Eingabe Aufforderungen für Neustarts für den Benutzer. Alle benötigten Neustarts erfolgen automatisch.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Standard Laufwerk für eine-Installation.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Eine Tabelle, die das Sequenz Tabellen Schema aufweist.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**Shortfile-Namen**](shortfilenames.md)<br/>                                     | Bewirkt, dass kurze Dateinamen verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**Kranz**](transforms.md)<br/>                                             | Liste der Transformationen, die auf eine Datenbank angewendet werden sollen.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**Transformsatsource**](transformsatsource.md)<br/>                             | Informiert das Installationsprogramm darüber, dass sich die Transformationen für ein Produkt an der Quelle befinden.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Transformssecure**](transformssecure.md)<br/>                                 | Wenn Sie die [**transformsecure**](transformssecure.md) -Eigenschaft auf 1 (eins) festlegen, wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Benutzer Computer an einem Speicherort zwischengespeichert werden, an dem der Benutzer keinen Schreibzugriff hat.<br/>                                                                                                                                                           |
| [**Msilogfileloation**](msilogfilelocation.md)<br/>                             | Der Installer legt den Wert dieser Eigenschaft auf den vollständigen Pfad der Protokolldatei fest, wenn die Protokollierung aktiviert wurde. Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Legt den Standard Protokollierungs Modus für das Windows Installer Paket fest. Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.<br/>                                                                                                                                                                                                                                                   |
| [**Msiuserealadminerkennungs**](msiuserealadmindetection.md)<br/>                 | Legen Sie diese Eigenschaft auf 1 fest, um anzufordern, dass das Installationsprogramm beim Festlegen der [**AdminUser**](adminuser.md) -Eigenschaft tatsächliche Benutzerinformationen verwendet. Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Datums-und Uhrzeit Eigenschaften

Die [**Datums**](date.md) -und [**Uhrzeit**](time.md) Eigenschaften sind Live Eigenschaften, die vom Installationsprogramm beim Extrahieren von Daten festgelegt werden.



| Eigenschaft                        | BESCHREIBUNG                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Das aktuelle Datum.<br/> |
| [**Time**](time.md)<br/> | Die aktuelle Zeit.<br/> |



 

## <a name="feature-installation-options-properties"></a>Eigenschaften von featureinstallationsoptionen

In der folgenden Liste finden Sie Links zu weiteren Informationen zu den Eigenschaften der Optionen für die Funktions Installation.



| Eigenschaft                                                                | BESCHREIBUNG                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adddefault**](adddefault.md)<br/>                             | Liste der Funktionen, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Liste der lokal zu installierenden Features.<br/>                                                                                                                              |
| [**Addsource**](addsource.md)<br/>                               | Die Liste der Funktionen, die von der Quelle ausgeführt werden sollen.<br/>                                                                                                                                |
| [**Benen**](advertise.md)<br/>                               | Liste der angekündigten Features.<br/>                                                                                                                                     |
| [**Compadddefault**](compadddefault.md)<br/>                     | Liste der Komponenten, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                                       |
| [**Compaddlocal**](compaddlocal.md)<br/>                         | Liste der lokal zu installierenden Komponenten-IDs.<br/>                                                                                                                         |
| [**Compaddsource**](compaddsource.md)<br/>                       | Liste der Komponenten-IDs, die von den Quell Medien ausgeführt werden sollen.<br/>                                                                                                                        |
| [**Fileadddefault**](fileadddefault.md)<br/>                     | Liste der Datei Schlüssel für Dateien, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                              |
| [**Fileaddlocal**](fileaddlocal.md)<br/>                         | Liste der Datei Schlüssel für Dateien, die lokal ausgeführt werden sollen.<br/>                                                                                                                         |
| [**Fileaddsource**](fileaddsource.md)<br/>                       | Liste der Datei Schlüssel, die vom Quell Medium ausgeführt werden sollen.<br/>                                                                                                                     |
| [**Msidisableluapatching**](msidisableluapatching.md)<br/>       | Durch Festlegen dieser Eigenschaft wird das Patchen einer Anwendung mit geringsten Berechtigungen verhindert.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Liste der Patches, die während der Installation entfernt werden sollen.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Gibt an, ob das Paket den [Neustart-Manager](../rstmgr/restart-manager-portal.md) oder die [FilesInUse](filesinuse-dialog.md) -Funktionalität verwendet.<br/>                                          |
| [**Msidisablermrestart**](msidisablermrestart.md)<br/>           | Gibt an, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren und neu gestartet werden sollen, um die Installation des Updates zu ermöglichen.<br/> |
| [**Msirmshutdown**](msirmshutdown.md)<br/>                       | Gibt an, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren werden sollen, um die Installation des Updates zu ermöglichen.<br/>               |
| [**Msipatchremove**](msipatchremove.md)<br/>                     | Durch Festlegen dieser Eigenschaft werden Patches entfernt.<br/>                                                                                                                                 |
| [**Patch**](patch.md)<br/>                                       | Wenn Sie diese Eigenschaft festlegen, wird ein Patch angewendet.<br/>                                                                                                                                 |
| [**Installieren Sie**](reinstall.md)<br/>                               | Die Liste der Funktionen, die neu installiert werden sollen.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Eine Zeichenfolge, die Buchstaben enthält, die den Typ der auszuführenden Neuinstallation angeben.<br/>                                                                                          |
| [**Aufgeh**](remove.md)<br/>                                     | Liste der zu entfernenden Features.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Hardware Eigenschaften

In der folgenden Liste sind die Hardware Eigenschaften aufgeführt, die beim Start von der Windows Installer festgelegt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="alpha.md"><strong>Alpha</strong></a><br/></td>
<td>Die numerische Prozessor Ebene bei Ausführung auf einem Alpha Prozessor.<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft ist veraltet, die Alpha Plattform wird von Windows Installer nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="borderside.md"><strong>Borderside</strong></a><br/></td>
<td>Die Breite des Fensterrahmens in Pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="bordertop.md"><strong>Bordertop</strong></a><br/></td>
<td>Die Höhe der Fensterrahmen in Pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="captionheight.md"><strong>CaptionHeight</strong></a><br/></td>
<td>Die Höhe des normalen Beschriftungs Bereichs in Pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="colorbits.md"><strong>Colorbits</strong></a><br/></td>
<td>Die Anzahl der angrenzenden Farbbits für jedes Pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="intel.md"><strong>Intel</strong></a><br/></td>
<td>Die numerische Prozessor Ebene bei Ausführung auf einem Intel-Prozessor.<br/></td>
</tr>
<tr class="odd">
<td><a href="intel64.md"><strong>Intel64</strong></a><br/></td>
<td>Die numerische Prozessor Ebene bei Ausführung auf einem Itanium-Prozessor.<br/></td>
</tr>
<tr class="even">
<td><a href="msix64.md"><strong>Msix64</strong></a><br/></td>
<td>Die numerische Prozessor Ebene bei Ausführung auf einem x64-Prozessor.<br/></td>
</tr>
<tr class="odd">
<td><a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br/></td>
<td>Die Größe des installierten RAM in Megabyte.<br/></td>
</tr>
<tr class="even">
<td><a href="screenx.md"><strong>ScreenX</strong></a><br/></td>
<td>Die Breite des Bildschirms in Pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="screeny.md"><strong>Screeny</strong></a><br/></td>
<td>Die Höhe des Bildschirms in Pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="textheight.md"><strong>TextHeight</strong></a><br/></td>
<td>Die Höhe der Zeichen in logischen Einheiten.<br/></td>
</tr>
<tr class="odd">
<td><a href="virtualmemory.md"><strong>Virtualmemory</strong></a><br/></td>
<td>Die Menge des verfügbaren Auslagerungs Datei-Speicherplatzes in Megabyte.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="installation-status-properties"></a>Eigenschaften des Installations Status

In der folgenden Liste finden Sie Links zu weiteren Informationen zu Status Eigenschaften, die vom Installationsprogramm während der Installation aktualisiert werden.



| Eigenschaft                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Afterreboot**](afterreboot.md)<br/>                                 | Gibt an, dass die aktuelle Installation einem Neustart folgt, den die [ForceReboot-Aktion](forcereboot-action.md) aufruft.<br/>                                                                                                                                                |
| [**Costingcomplete**](costingcomplete.md)<br/>                         | Gibt an, ob der Speicherplatz in Anspruch ist.<br/>                                                                                                                                                                                                             |
| [**Installiert**](installed.md)<br/>                                     | Gibt an, dass ein Produkt bereits installiert ist.<br/>                                                                                                                                                                                                                |
| [**Msicheckcrcs**](msicheckcrcs.md)<br/>                               | Das Installationsprogramm führt ein CRC für Dateien nur aus, wenn die [**msicheckcrcs**](msicheckcrcs.md) -Eigenschaft festgelegt ist.<br/>                                                                                                                                                           |
| [**Msirestartmanagersessionkey**](msirestartmanagersessionkey.md)<br/> | Das Installationsprogramm legt diese Eigenschaft auf den Sitzungsschlüssel für die [Restart Manager](../rstmgr/restart-manager-portal.md) -Sitzung fest.<br/>                                                                                                                                                         |
| [**Msirunningelevated**](msirunningelevated-.md)<br/>                  | Der Installer legt den Wert dieser Eigenschaft auf 1 fest, wenn das Installationsprogramm mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird.<br/>                                                                                                                   |
| [**Msisystemrebootpending**](msisystemrebootpending.md)<br/>           | Der Installer legt diese Eigenschaft auf 1 fest, wenn zurzeit ein Neustart des Betriebssystems aussteht.<br/>                                                                                                                                                              |
| [**Msiuihidecancel**](msiuihidecancel.md)<br/>                         | Der Installer legt " [**msiuihidecancel**](msiuihidecancel.md) " auf 1 fest, wenn die interne Installations Ebene " **installuilevel \_ hidecancel**" umfasst.<br/>                                                                                                                   |
| [**Msiuiprogressonly**](msiuiprogressonly.md)<br/>                     | Der Installer legt [**msiuiprogressonly**](msiuiprogressonly.md) auf 1 fest, wenn die interne Installations Ebene den Wert von " **\_ instalssonly**" enthält.<br/>                                                                                                             |
| [**Msiuisourceresonly**](msiuisourceresonly.md)<br/>                   | [**Msiuisourceresonly**](msiuisourceresonly.md) auf 1 (eins), wenn die interne Installations Ebene " **installuilevel \_ sourceresonly**" enthält.<br/>                                                                                                                       |
| [**Nocompanyname**](nocompanyname.md)<br/>                             | Unterdrückt die automatische Einstellung der [**CompanyName**](companyname.md) -Eigenschaft.<br/>                                                                                                                                                                          |
| [**Nomen Name**](nousername.md)<br/>                                   | Unterdrückt die automatische Einstellung der [**username**](username.md) -Eigenschaft.<br/>                                                                                                                                                                                |
| [**Ausgabebereich**](outofdiskspace.md)<br/>                           | Nicht genügend Speicherplatz für die Installation.<br/>                                                                                                                                                                                                      |
| [**Outo-norbdiskspace**](outofnorbdiskspace.md)<br/>                   | Nicht genügend Speicherplatz mit Rollback.<br/>                                                                                                                                                                                                             |
| [**Vorab ausgewählten**](preselected.md)<br/>                                 | Features sind bereits ausgewählt.<br/>                                                                                                                                                                                                                                |
| [**Primaryvolumepath**](primaryvolumepath.md)<br/>                     | Das Installationsprogramm legt den Wert dieser Eigenschaft auf den Pfad des Volumes fest, das von der [**PRIMARYFOLDER**](primaryfolder.md) -Eigenschaft festgelegt wird.<br/>                                                                                                                  |
| [**Primaryvolumespaceavailable**](primaryvolumespaceavailable.md)<br/> | Das Installationsprogramm legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die auf dem Volume verfügbar sind, auf das die Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verweist.<br/>                                                      |
| [**Primaryvolumespaceremaineing**](primaryvolumespaceremaining.md)<br/> | Das Installationsprogramm legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der verbleibenden Bytes auf dem Volume darstellt, auf das die Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verweist, wenn alle derzeit ausgewählten Features installiert sind.<br/> |
| [**Primaryvolumespacerequired**](primaryvolumespacerequired.md)<br/>   | Das Installationsprogramm legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle aktuell ausgewählten Funktionen auf dem Volume erforderlich sind, auf das die Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verweist.<br/>                    |
| [**Productlanguage**](productlanguage.md)<br/>                         | Numerischer sprach Bezeichner (langid) für die Datenbank. Benötigten<br/>                                                                                                                                                                                             |
| [**Replacedinusefiles**](replacedinusefiles.md)<br/>                   | Legen Sie fest, ob das Installationsprogramm über eine Datei installiert wird, die in Gebrauch ist.<br/>                                                                                                                                                                                          |
| [**Zusetzen**](resume.md)<br/>                                           | Fortsetzen der Installation.<br/>                                                                                                                                                                                                                                         |
| [**Rollback deaktiviert**](rollbackdisabled.md)<br/>                       | Das Installationsprogramm legt diese Eigenschaft fest, wenn das Rollback deaktiviert ist.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Gibt die Benutzeroberflächen Ebene an.<br/>                                                                                                                                                                                                                           |
| [**Updaterarted**](updatestarted.md)<br/>                             | Wird festgelegt, wenn Änderungen am System für diese Installation begonnen haben.<br/>                                                                                                                                                                                              |
| [**Upgradingproductcode**](upgradingproductcode.md)<br/>               | Wird vom Installationsprogramm festgelegt, wenn ein Upgrade eine Anwendung entfernt.<br/>                                                                                                                                                                                                  |
| [**Versionmsi**](versionmsi.md)<br/>                                   | Das Installationsprogramm legt diese Eigenschaft auf die Version von Windows Installer fest, die während der Installation ausgeführt wird.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Betriebs System Eigenschaften

In der folgenden Liste finden Sie Links zu weiteren Informationen zu Betriebssystem Eigenschaften, die vom Installationsprogramm beim Start festgelegt werden.



| Eigenschaftsname                                                                             | Kurzbeschreibung                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Wird unter Windows 2000 festgelegt, wenn der Benutzer über Administratorrechte verfügt.<br/>                                                                                                                                                                                                                        |
| [**Computername**](computername.md)<br/>                                           | Der Computer Name des aktuellen Systems.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Auf Systemen, die Common Language Runtime Assemblys unterstützen, legt das Installationsprogramm den Wert dieser Eigenschaft auf die Dateiversion fusion.dll fest. Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn das Betriebssystem Common Language Runtime Assemblys nicht unterstützt.<br/>                   |
| [**Msintproducttype**](msintproducttype.md)<br/>                                   | Gibt den Windows-Produkttyp an.<br/>                                                                                                                                                                                                                                                  |
| [**Msintsuitebackoffice**](msintsuitebackoffice.md)<br/>                           | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft BackOffice-Komponenten installiert sind.<br/>                                                                                                                                      |
| [**Msintsuitedatacenter**](msintsuitedatacenter.md)<br/>                           | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn Windows 2000 Datacenter Server installiert ist.<br/>                                                                                                                                        |
| [**Msintsuiteenter Prise**](msintsuiteenterprise.md)<br/>                           | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn Windows 2000 Advanced Server installiert ist.<br/>                                                                                                                                          |
| [**Msintsuitepersonal**](msintsuitepersonal.md)<br/>                               | Unter Windows XP und neueren Betriebssystemen legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn das Betriebssystem Home (nicht Professional) ist.<br/>                                                                                                                                      |
| [**Msintsuitesmallbusiness**](msintsuitesmallbusiness.md)<br/>                     | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft Small Business Server installiert ist.<br/>                                                                                                                                       |
| [**Msintsuitesmallbusinessrestricted**](msintsuitesmallbusinessrestricted.md)<br/> | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft Small Business Server mit der eingeschränkten Client Lizenz installiert ist.<br/>                                                                                                   |
| [**Msintsuitewebserver**](msintsuitewebserver.md)<br/>                             | Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die [**msintsuitewebserver**](msintsuitewebserver.md) -Eigenschaft auf 1 (eins) fest, wenn die Web Edition von Windows Server 2003 installiert ist. Nur verfügbar für die Windows Server 2003-Version der Windows Installer.<br/> |
| [**Msitabletpc**](msitabletpc.md)<br/>                                             | Der Installer legt diese Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Auf Systemen, die Win32-Assemblys unterstützen, legt das Installationsprogramm den Wert dieser Eigenschaft auf die Dateiversion sxs.dll fest. Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn das Betriebssystem keine Win32-Assemblys unterstützt.<br/>                                                          |
| [**Oleadvtsupport**](oleadvtsupport.md)<br/>                                       | Legen Sie fest, ob OLE die Windows Installer unterstützt.<br/>                                                                                                                                                                                                                                           |
| [**Redirecteddllsupport**](redirecteddllsupport.md)<br/>                           | Der Installer legt die Eigenschaft [**redirecteddllsupport**](redirecteddllsupport.md) fest, wenn das System, das die Installation ausführt, [isolierte Komponenten](isolated-components.md)unterstützt.<br/>                                                                                              |
| [**Remoteadmints**](remoteadmints.md)<br/>                                         | Der Installer legt die [**remoteadmints**](remoteadmints.md) -Eigenschaft fest, wenn das System ein Remote Verwaltungs Server ist, auf dem der Terminal Server-Rollen Dienst ausgeführt wird.<br/>                                                                                                                   |
| [**Servicepacklevel**](servicepacklevel.md)<br/>                                   | Die Versionsnummer des Betriebssystems Service Pack.<br/>                                                                                                                                                                                                                             |
| [**Servicepacklevelminor**](servicepacklevelminor.md)<br/>                         | Die neben Versionsnummer des Betriebssystems Service Pack.<br/>                                                                                                                                                                                                                       |
| [**Sharedwindows**](sharedwindows.md)<br/>                                         | Wird festgelegt, wenn das System als freigegebene Fenster verwendet wird.<br/>                                                                                                                                                                                                                                  |
| [**Shelladvtsupport**](shelladvtsupport.md)<br/>                                   | Legen Sie fest, ob die Shell Funktions Werbung unterstützt.<br/>                                                                                                                                                                                                                                       |
| [**Systemlanguageid**](systemlanguageid.md)<br/>                                   | Standard sprach Bezeichner für das System.<br/>                                                                                                                                                                                                                                          |
| [**Terminalserver**](terminalserver.md)<br/>                                       | Festlegen, wenn das System ein Server ist, auf dem der Terminal Server-Rollen Dienst ausgeführt wird.<br/>                                                                                                                                                                                                            |
| [**Ttcsupport**](ttcsupport.md)<br/>                                               | Gibt an, ob das Betriebssystem die Verwendung von. TTC-Dateien (echte typschriftart Sammlungen) unterstützt.<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | Versionsnummer für das Windows-Betriebssystem.<br/>                                                                                                                                                                                                                                     |
| [**Versiondatabase**](versiondatabase.md)<br/>                                     | Numerische Datenbankversion der aktuellen Installation.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Versionsnummer für das Betriebssystem.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Versionsnummer für das Betriebssystem, wenn das System auf einem 64-Bit-Computer ausgeführt wird.<br/>                                                                                                                                                                                               |
| [**Windows-Build**](windowsbuild.md)<br/>                                          | Buildnummer des Betriebssystems.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Eigenschaften von Produktinformationen

In der folgenden Liste finden Sie Links zu weiteren Informationen zu produktspezifischen Eigenschaften, die in der Eigenschaften [Tabelle](property-table.md)angegeben sind.



| Eigenschaftsname                                                  | Kurzbeschreibung                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Arphelplink**](arphelplink.md)<br/>                  | Internet Adresse oder URL für technischen Support.<br/>                                                                                 |
| [**Arphelptelefon**](arphelptelephone.md)<br/>        | Telefonnummern für technischen Support.<br/>                                                                                               |
| [**Diskprompt**](diskprompt.md)<br/>                    | Zeichenfolge, die von einem Meldungs Feld angezeigt wird, das einen Datenträger auffordert<br/>                                                                     |
| [**Isadminpackage**](isadminpackage.md)<br/>            | Legen Sie diese Einstellung auf 1 (eins) fest, wenn die aktuelle Installation von einem Paket ausgeführt wird, das über eine administrative Installation erstellt wurde.<br/>           |
| [**Leftunit**](leftunit.md)<br/>                        | Platziert Einheiten auf der linken Seite der Zahl.<br/>                                                                                        |
| [**Hersteller**](manufacturer.md)<br/>                | Der Name des Anwendungs Herstellers. (Erforderlich)<br/>                                                                               |
| [**Mediasourcedir**](mediasourcedir.md)<br/>            | Der Installer legt diese Eigenschaft auf 1 (eins) fest, wenn bei der Installation eine Medienquelle verwendet wird, z. b. eine CD-ROM.<br/>                       |
| [**Msiinstanceguid**](msiinstanceguid.md)<br/>          | Das vorhanden sein dieser Eigenschaft gibt an, dass eine Transformation zum Ändern des Produktcodes für das Produkt registriert ist.<br/>                   |
| [**Msinewinstance**](msinewinstance.md)<br/>            | Diese Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit instanztransformationen an.<br/>                              |
| [**"Parametriproductcode"**](parentoriginaldatabase.md)<br/> | Das Installationsprogramm legt diese Eigenschaft für Installationen fest, die eine [parallele Installations](concurrent-installations.md) Aktion ausführt.<br/> |
| [**Pidtemplate**](pidtemplate.md)<br/>                  | Zeichenfolge, die als Vorlage für die [**PIDKEY**](pidkey.md) -Eigenschaft verwendet wird.<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Ein eindeutiger Bezeichner für eine bestimmte Produktversion. (Erforderlich)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Lesbarer Name einer Anwendung. (Erforderlich)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Legen Sie auf den installierten Zustand eines Produkts fest.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Das Zeichen folgen Format der Produktversion als numerischer Wert. (Erforderlich)<br/>                                                            |
| [**UpgradeCode auch**](upgradecode.md)<br/>                  | Eine GUID, die einen zusammenhängenden Satz von Produkten darstellt.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Aktualisierungs Eigenschaften für Zusammenfassungs Informationen

Die folgenden Eigenschaften werden nur durch Transformationen in MSP-Dateien festgelegt, die zum Aktualisieren des Datenstroms für Zusammenfassungs Informationen eines administrativen Images verwendet werden.



| Eigenschaft                                                              | BESCHREIBUNG                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Patchnewpackagecode**](patchnewpackagecode.md)<br/>         | Der Wert dieser Eigenschaft wird in die [**Revisionsnummer-Zusammenfassungs**](revision-number-summary.md) Eigenschaft geschrieben.<br/> |
| [**Patchnewsummarycomments**](patchnewsummarycomments.md)<br/> | Der Wert dieser Eigenschaft wird in die Eigenschaft für die [**Kommentar Zusammenfassung**](comments-summary.md) geschrieben.<br/>               |
| [**Patchnewsummarysubject**](patchnewsummarysubject.md)<br/>   | Der Wert dieser Eigenschaft wird in die [**Subject Summary**](subject-summary.md) -Eigenschaft geschrieben.<br/>                 |



 

## <a name="system-folder-properties"></a>Eigenschaften von System Ordnern

In der folgenden Liste finden Sie Links zu weiteren Informationen zu Systemordnern, die vom Installationsprogramm beim Setup festgelegt werden.



| Eigenschaft                                                        | BESCHREIBUNG                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Ordner "admintools"**](admintoolsfolder.md)<br/>         | Der vollständige Pfad zu dem Verzeichnis, das Verwaltungs Tools enthält.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | Der vollständige Pfad zum **roamingordner** für den aktuellen Benutzer.<br/>              |
| [**Commonappdatafolder**](commonappdatafolder.md)<br/>   | Der vollständige Pfad zu den Anwendungsdaten für alle Benutzer.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Der vollständige Pfad zum vordefinierten **64-Bit-Ordner für gemeinsame Dateien** .<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Der vollständige Pfad zum Ordner " **Gemeinsame Dateien** " für den aktuellen Benutzer.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | Der vollständige Pfad zum **Desktop** Ordner.<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | Der vollständige Pfad zum Ordner **Favoriten** für den aktuellen Benutzer.<br/>            |
| [**Fonsordner**](fontsfolder.md)<br/>                   | Der vollständige Pfad zum **Schriftarten** Ordner.<br/>                                     |
| [**Localappdatafolder**](localappdatafolder.md)<br/>     | Der vollständige Pfad zu dem Ordner, der lokale (nicht roaminganwendungen) Anwendungen enthält.<br/> |
| [**Mypicturesfolder**](mypicturesfolder.md)<br/>         | Der vollständige Pfad zum Ordner " **Bilder** ".<br/>                                  |
| [**"Netthoodfolder"**](nethoodfolder.md)<br/>               | Der vollständige Pfad zum Ordner " **netthood** ".<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Der vollständige Pfad zum Ordner " **Dokumente** " für den aktuellen Benutzer.<br/>            |
| [**Printhoodfolder**](printhoodfolder.md)<br/>           | Der vollständige Pfad zum Ordner **printhood** .<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Der vollständige Pfad zum vordefinierten Ordner für **64-Bit-Programmdateien** .<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | Der vollständige Pfad zum vordefinierten Ordner für **32-Bit-Programmdateien** .<br/>           |
| [**Programmmenufolder**](programmenufolder.md)<br/>       | Der vollständige Pfad zum **Programm Menü** Ordner.<br/>                              |
| [**Recentfolder**](recentfolder.md)<br/>                 | Der vollständige Pfad zum **aktuellen** Ordner.<br/>                                    |
| [**Ordner "SendTo"**](sendtofolder.md)<br/>                 | Der vollständige Pfad zum Ordner **SendTo** für den aktuellen Benutzer.<br/>               |
| [**Startmenü Ordner**](startmenufolder.md)<br/>           | Der vollständige Pfad zum **Startmenü** Ordner.<br/>                                |
| [**Startupfolder**](startupfolder.md)<br/>               | Der vollständige Pfad zum **Start** Ordner.<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Der vollständige Pfad zum Ordner für 16-Bit-System-DLLs.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Der vollständige Pfad zum vordefinierten Ordner " **System64** ".<br/>                       |
| [**Systemordner**](systemfolder.md)<br/>                 | Der vollständige Pfad zum **System** Ordner für den aktuellen Benutzer.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Der vollständige **Pfad zum temporären Ordner.**<br/>                                      |
| [**Vorlagenordner**](templatefolder.md)<br/>             | Der vollständige Pfad zum **Vorlagen** Ordner für den aktuellen Benutzer.<br/>             |
| [**Verzeichnis Windows befinden**](windowsfolder.md)<br/>               | Der vollständige Pfad zum **Windows** -Ordner.<br/>                                   |
| [**Windows Volume**](windowsvolume.md)<br/>               | Das Volume des **Windows** -Ordners.<br/>                                      |



 

## <a name="user-information-properties"></a>Eigenschaften von Benutzerinformationen

In der folgenden Liste finden Sie Links zu weiteren Informationen zu den vom Benutzer bereitgestellten Informationen.



| Eigenschaft                                                      | BESCHREIBUNG                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Adminproperties**](adminproperties.md)<br/>         | Liste der Eigenschaften, die während einer Verwaltungs Installation festgelegt werden.<br/>       |
| [**CompanyName**](companyname.md)<br/>                 | Der Name der Organisation des Benutzers, der die Installation ausführt.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Der Benutzername für den aktuell angemeldeten Benutzer.<br/>                           |
| [**Msihiddenproperties**](msihiddenproperties.md)<br/> | Liste der Eigenschaften, die verhindert werden, dass Sie in das Protokoll geschrieben werden.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Teil der vom Benutzer eingegebenen Produkt-ID.<br/>                                 |
| [**ProductID**](productid.md)<br/>                     | Vollständige Produkt-ID nach einer erfolgreichen Überprüfung.<br/>                               |
| [**Userlanguageid**](userlanguageid.md)<br/>           | Standardsprachen-ID des aktuellen Benutzers.<br/>                             |
| [**User**](username.md)<br/>                       | Der Benutzer, der die Installation ausführt.<br/>                                     |
| [**UserSID-Eigenschaft**](usersid.md)<br/>                | Wird vom Installer entsprechend der Sicherheits-ID (SID) des Benutzers festgelegt.<br/> |



 

 

 
