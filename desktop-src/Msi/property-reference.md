---
description: 'In diesem Abschnitt werden die eigenschaften aufgeführt, die vom Windows definiert werden:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Eigenschaftenverweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38f952632609090c69b85786c6aef64243d420b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481566"
---
# <a name="property-reference"></a>Eigenschaftenverweis

In diesem Abschnitt werden die eigenschaften aufgeführt, die vom Windows definiert werden:

-   [Eigenschaften des Komponentenspeicherorts](#component-location-properties)
-   [Konfigurationseigenschaften](#configuration-properties)
-   [Datums-, Uhrzeiteigenschaften](#date-time-properties)
-   [Eigenschaften der Featureinstallationsoptionen](#feature-installation-options-properties)
-   [Hardwareeigenschaften](#hardware-properties)
-   [Installationsstatuseigenschaften](#installation-status-properties)
-   [Betriebssystemeigenschaften](#operating-system-properties)
-   [Produktinformationseigenschaften](#product-information-properties)
-   [Updateeigenschaften für Zusammenfassungsinformationen](#summary-information-update-properties)
-   [Systemordnereigenschaften](#system-folder-properties)
-   [Benutzerinformationseigenschaften](#user-information-properties)

Zusätzliche Eigenschaften können durch erstellungsdaten oder benutzerdefinierte Aktionen angegeben werden. Eigenschaften mit Namen, die keine Kleinbuchstaben enthalten, sind öffentliche Eigenschaften und können in der Befehlszeile angegeben werden.

Informationen zu den Werten des Registrierungsschlüssels **Deinstallieren,** die von den Installereigenschaften bereitgestellt werden, finden Sie unter [Deinstallieren des Registrierungsschlüssels.](uninstall-registry-key.md)

## <a name="component-location-properties"></a>Eigenschaften des Komponentenspeicherorts

Die folgende Liste enthält Links zu weitere Informationen zu den Eigenschaften des Komponentenspeicherorts.



| Eigenschaft                                                            | BESCHREIBUNG                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | Das Installationsprogramm legt diese Eigenschaft auf die aus der Datenbank gestartete Datenbank, die Datenbank in der Quelle oder die zwischengespeicherte Datenbank fest.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | Das Installationsprogramm legt diese Eigenschaft für Installationen fest, die von einer Gleichzeitige [Installation ausgeführt](concurrent-installations.md) werden.<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Stammverzeichnis, das die Quelldateien enthält.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Gibt das Stammzielverzeichnis für die Installation an. Während einer [Administratorinstallation](administrative-installation.md) ist diese Eigenschaft der Speicherort zum Kopieren des Installationspakets.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

Die folgende Liste enthält Links zu weiteren Informationen zu anderen konfigurierbaren Eigenschaften.



| Eigenschaft                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AKTION**](action.md)<br/>                                                     | Die erste Aktion wird aufgerufen, nachdem das Installationsprogramm initialisiert wurde.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Bestimmt, wo Konfigurationsinformationen gespeichert werden.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | URL des Updatekanals für eine Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Stellt Kommentare für das **Hinzufügen oder Entfernen von Programmen** in **Systemsteuerung.**<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Stellt kontakt für das **Hinzufügen oder Entfernen von Programmen** in **Systemsteuerung.**<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Vollqualifizierter Pfad zum primären Ordner einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Deaktiviert Funktionen, die ein Produkt ändern.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Deaktiviert Funktionen, die ein Produkt entfernen.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Deaktiviert die Schaltfläche **Reparieren** im Assistenten Programme.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Gibt das primäre Symbol für das Installationspaket an.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Stellt eine **ReadMe für** das **Hinzufügen oder Entfernen von Programmen** in Systemsteuerung. <br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Geschätzte Größe einer Anwendung in Kilobyte.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Verhindert die Anzeige einer Anwendung in der **Liste Programme hinzufügen oder** entfernen.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | URL für die Startseite einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | URL für Informationen zum Anwendungsupdate.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Registrierungsspeicherplatz (in Kilobytes), der für eine Anwendung erforderlich ist. Wird von [der AllocateRegistrySpace-Aktion verwendet.](allocateregistryspace-action.md)<br/>                                                                                                                                                                                                                                              |
| [**CCP \_ DRIVE**](ccp-drive.md)<br/>                                              | Der Stammpfad für das Qualifizieren von Produkten für KPEs.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Standardschriftart, die für Steuerelemente verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Legen Sie fest, um die Generierung der spezifischen Tastenkombinationen zu deaktivieren, die [installation-on-demand unterstützen.](installation-on-demand.md)<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Verhindert, dass das Installationsprogramm Medienquellen wie CD-ROMs als gültige Quellen für das Produkt registriert.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Deaktiviert das Rollback für die aktuelle Konfiguration.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Aktion der obersten Ebene, die von ExecuteAction initiiert wird.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Ausführungsmodus, den das Installationsprogramm ausführt.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Verbessert die Installationsleistung in bestimmten OEM-Szenarien.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Anfängliche Ebene, auf der Features installiert werden.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Die Benutzeroberflächenebene ist auf "Basic" begrenzt.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Liste der zu protokollierten Aktionsnamen.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Diese Eigenschaft muss auf den relativen Pfad festgelegt werden, wenn sich das Installationspaket nicht im Stammverzeichnis der CD-ROM befindet.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Diese optionale Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungsspeicherorte, an denen die Anwendung die Einstellungen und Einstellungen eines Benutzers speichert. Verfügbar mit Windows Installer 4.0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Deaktivieren Sie die eingebettete Benutzeroberfläche für die Installation.<br/> **[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Reduzieren Sie die Zeit, die zum Installieren eines großen Installationspakets Windows Installer erforderlich ist.<br/> **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Fordert an, dass Windows Installer das Paket nur für den aktuellen Benutzer installiert.<br/> **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Legen Sie diese Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die [**DISABLEMEDIA-Eigenschaft**](-disablemedia.md) festgelegt.<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Legen Sie diese Eigenschaft in der Befehlszeile oder in der Eigenschaftentabelle auf [](small-updates.md) 1 [](minor-upgrades.md) (eins) fest, um die Upgradekomponentenregeln bei kleinen Updates und kleineren Upgrades eines bestimmten Produkts anzuwenden. [](property-table.md) Verfügbar ab Windows Installer 3.0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Wenn diese Eigenschaft auf 1 festgelegt wurde, kann das Installationsprogramm die Registrierung redundanter Komponenten aufheben und deinstallieren, um zu verhindern, dass verwaiste Komponenten auf dem Computer zurückgelassen werden.<br/> **[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Ermöglicht dem Autor, einen primären Ordner für eine Installation zu bestimmen. Wird verwendet, um die Werte für die [**Eigenschaften PrimaryVolumePath,**](primaryvolumepath.md) [**PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)und [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) zu bestimmen.<br/> |
| [**Privilegiert**](privileged.md)<br/>                                             | Führt eine Installation mit erhöhten Rechten aus.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Aktion, wenn nicht genügend Speicherplatz für die Installation vorhanden ist.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**NEUSTART**](reboot.md)<br/>                                                     | Erzwingt oder unterdrückt einen Neustart.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Unterdrückt die Anzeige von Aufforderungen für Neustarts für den Benutzer. Alle erforderlichen Neustarts werden automatisch ausgeführt.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Standardlaufwerk für eine Installation.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Eine Tabelle mit dem Sequenztabellenschema.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Bewirkt, dass kurze Dateinamen verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**VERWANDELT**](transforms.md)<br/>                                             | Liste der Transformationen, die auf eine Datenbank angewendet werden sollen.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informiert das Installationsprogramm darüber, dass sich die Transformationen für ein Produkt an der Quelle befinden.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | Durch Festlegen [**der TRANSFORMSECURE-Eigenschaft**](transformssecure.md) auf 1 (eins) wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Benutzercomputer an einem Speicherort zwischengespeichert werden sollen, an dem der Benutzer keinen Schreibzugriff hat.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | Das Installationsprogramm legt den Wert dieser Eigenschaft auf den vollständigen Pfad der Protokolldatei fest, wenn die Protokollierung aktiviert wurde. Diese Eigenschaft ist ab Windows Installer 4.0 verfügbar.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Legt den Standardprotokollierungsmodus für das Windows Installer-Paket fest. Diese Eigenschaft ist ab Windows Installer 4.0 verfügbar.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Legen Sie diese Eigenschaft auf 1 fest, um an fordern, dass das Installationsprogramm die tatsächlichen Benutzerinformationen verwendet, wenn die [**AdminUser-Eigenschaft festgelegt**](adminuser.md) wird. Diese Eigenschaft ist ab Windows Installer 4.0 verfügbar.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Datums-, Uhrzeiteigenschaften

Die [**Datums-**](date.md) [**und Uhrzeiteigenschaften**](time.md) sind Liveeigenschaften, die das Installationsprogramm beim Extrahieren von Daten fest legt.



| Eigenschaft                        | BESCHREIBUNG                  |
|---------------------------------|------------------------------|
| [**Datum**](date.md)<br/> | Das aktuelle Datum.<br/> |
| [**Time**](time.md)<br/> | Die aktuelle Zeit.<br/> |



 

## <a name="feature-installation-options-properties"></a>Eigenschaften der Featureinstallationsoptionen

Die folgende Liste enthält Links zu zusätzlichen Informationen zu den Eigenschaften der Featureinstallationsoptionen.



| Eigenschaft                                                                | BESCHREIBUNG                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Liste der Features, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Liste der Features, die lokal installiert werden sollen.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Liste der Features, die aus der Quelle ausgeführt werden sollen.<br/>                                                                                                                                |
| [**WERBEN**](advertise.md)<br/>                               | Liste der Features, die angekündigt werden sollen.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Liste der Komponenten, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Liste der Komponenten-IDs, die lokal installiert werden sollen.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Liste der Komponenten-IDs, die von Quellmedien ausgeführt werden.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Liste der Dateischlüssel für Dateien, die in der Standardkonfiguration installiert werden sollen.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Liste der Dateischlüssel für Dateien, die lokal ausgeführt werden sollen.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Liste der Dateischlüssel, die auf dem Quellmedium ausgeführt werden sollen.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | Durch festlegen dieser Eigenschaft wird das Patchen einer Anwendung durch den am wenigsten privilegierten Benutzer (LEAST Privileged User, LUA) verhindert.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Liste der Patches, die während der Installation entfernt werden sollen.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Gibt an, ob das Paket die [Funktionen Restart Manager](../rstmgr/restart-manager-portal.md) oder [FilesInUse](filesinuse-dialog.md) verwendet.<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Gibt an, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren und neu gestartet werden sollen, um die Installation des Updates zu aktivieren.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Gibt an, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren werden sollen, um die Installation des Updates zu aktivieren.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | Durch Festlegen dieser Eigenschaft werden Patches entfernt.<br/>                                                                                                                                 |
| [**PATCH**](patch.md)<br/>                                       | Durch Festlegen dieser Eigenschaft wird ein Patch angewendet.<br/>                                                                                                                                 |
| [**INSTALLIEREN**](reinstall.md)<br/>                               | Liste der funktionen, die neu installiert werden sollen.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Eine Zeichenfolge, die Buchstaben enthält, die den Typ der neu durchzuführenden Neuinstallation angeben.<br/>                                                                                          |
| [**ENTFERNEN**](remove.md)<br/>                                     | Liste der funktionen, die entfernt werden sollen.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Hardwareeigenschaften

In der folgenden Liste sind die Hardwareeigenschaften aufgeführt, die Windows Installer beim Start festlegen.




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <a href="alpha.md"><strong>Alpha</strong></a><br /> | Die numerische Prozessorebene, wenn auf einem Alphaprozessor ausgeführt wird.<br /><blockquote>[!Note]<br />Diese Eigenschaft ist veraltet, die Alphaplattform wird von Windows Installer nicht unterstützt.</blockquote><br /> | 
| <a href="borderside.md"><strong>BorderSide</strong></a><br /> | Die Breite des Fensterrahmens in Pixel.<br /> | 
| <a href="bordertop.md"><strong>BorderTop</strong></a><br /> | Die Höhe des Fensterrahmens in Pixel.<br /> | 
| <a href="captionheight.md"><strong>CaptionHeight</strong></a><br /> | Die Höhe des normalen Beschriftungsbereichs in Pixel.<br /> | 
| <a href="colorbits.md"><strong>ColorBits</strong></a><br /> | Die Anzahl benachbarter Farbbits für jedes Pixel.<br /> | 
| <a href="intel.md"><strong>Intel</strong></a><br /> | Die numerische Prozessorebene bei Ausführung auf einem Intel-Prozessor.<br /> | 
| <a href="intel64.md"><strong>Intel64</strong></a><br /> | Die numerische Prozessorebene bei Ausführung auf einem Itanium-Prozessor.<br /> | 
| <a href="msix64.md"><strong>Msix64</strong></a><br /> | Die numerische Prozessorebene bei Ausführung auf einem x64-Prozessor.<br /> | 
| <a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br /> | Die Größe des installierten RAM in Megabyte.<br /> | 
| <a href="screenx.md"><strong>ScreenX</strong></a><br /> | Die Breite des Bildschirms in Pixel.<br /> | 
| <a href="screeny.md"><strong>Screeny</strong></a><br /> | Die Höhe des Bildschirms in Pixel.<br /> | 
| <a href="textheight.md"><strong>TextHeight</strong></a><br /> | Die Höhe von Zeichen in logischen Einheiten.<br /> | 
| <a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br /> | Die Menge des verfügbaren Seitendateispeicherplatzes in Megabyte.<br /> | 




 

## <a name="installation-status-properties"></a>Installationsstatuseigenschaften

Die folgende Liste enthält Links zu weiteren Informationen zu Statuseigenschaften, die während der Installation vom Installationsprogramm aktualisiert werden.



| Eigenschaft                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Gibt an, dass die aktuelle Installation nach einem Neustart erfolgt, den die [ForceReboot-Aktion](forcereboot-action.md) aufruft.<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Gibt an, ob die Speicherplatzkosten vollständig sind.<br/>                                                                                                                                                                                                             |
| [**Installiert**](installed.md)<br/>                                     | Gibt an, dass ein Produkt bereits installiert ist.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | Das Installationsprogramm führt nur dann eine CRC für Dateien durch, wenn die [**MSICHECKCRCS-Eigenschaft**](msicheckcrcs.md) festgelegt ist.<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | Der Installer legt diese Eigenschaft auf den Sitzungsschlüssel für die [Neustart-Manager-Sitzung](../rstmgr/restart-manager-portal.md) fest.<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | Der Installer legt den Wert dieser Eigenschaft auf 1 fest, wenn das Installationsprogramm mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird.<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | Der Installer legt diese Eigenschaft auf 1 fest, wenn ein Neustart des Betriebssystems derzeit aussteht.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | Der Installer legt [**MsiUIHideCancel**](msiuihidecancel.md) auf 1 fest, wenn die interne Installationsebene **INSTALLUILEVEL \_ HIDECANCEL** enthält.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | Der Installer legt [**MsiUIProgressOnly**](msiuiprogressonly.md) auf 1 fest, wenn die interne Installationsebene **INSTALLUILEVEL \_ PROGRESSONLY** enthält.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) auf 1 (eins), wenn die interne Installationsebene **INSTALLUILEVEL \_ SOURCERESONLY** enthält.<br/>                                                                                                                       |
| [**NOCOMPANYNAME**](nocompanyname.md)<br/>                             | Unterdrückt die automatische Einstellung der [**COMPANYNAME-Eigenschaft.**](companyname.md)<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | Unterdrückt die automatische Einstellung der [**USERNAME-Eigenschaft.**](username.md)<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Nicht genügend Speicherplatz für die Installation.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Nicht genügend Speicherplatz mit deaktivierten Rollbacks.<br/>                                                                                                                                                                                                             |
| [**Vorgewählten**](preselected.md)<br/>                                 | Features sind bereits ausgewählt.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | Der Installer legt den Wert dieser Eigenschaft auf den Pfad des Volumes fest, das von der [**PRIMARYFOLDER-Eigenschaft**](primaryfolder.md) festgelegt wird.<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | Der Installer legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der bytes darstellt, die auf dem Volume verfügbar sind, auf das die [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verweist.<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | Der Installer legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der bytes darstellt, die auf dem Volume verbleiben, auf das die [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verweist, wenn alle derzeit ausgewählten Features installiert sind.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | Der Installer legt den Wert dieser Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle derzeit ausgewählten Features auf dem Volume erforderlich sind, auf das die [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verweist.<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Numerischer Sprachbezeichner (LANGID) für die Datenbank. (ERFORDERLICH)<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Legen Sie fest, ob das Installationsprogramm über eine Datei installiert wird, die verwendet wird.<br/>                                                                                                                                                                                          |
| [**FORTSETZEN**](resume.md)<br/>                                           | Die Installation wurde fortgesetzt.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | Das Installationsprogramm legt diese Eigenschaft fest, wenn das Rollback deaktiviert ist.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Gibt die Benutzeroberflächenebene an.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Legen Sie fest, wenn Änderungen am System für diese Installation begonnen haben.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Wird vom Installationsprogramm festgelegt, wenn eine Anwendung durch ein Upgrade entfernt wird.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | Das Installationsprogramm legt diese Eigenschaft auf die Version von Windows Installer fest, die während der Installation ausgeführt wird.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Betriebssystemeigenschaften

Die folgende Liste enthält Links zu weiteren Informationen zu Betriebssystemeigenschaften, die der Installer beim Start festlegt.



| Eigenschaftsname                                                                             | Kurzbeschreibung                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adminuser**](adminuser.md)<br/>                                                 | Legen Sie auf Windows 2000 fest, wenn der Benutzer über Administratorrechte verfügt.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Computername des aktuellen Systems.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Auf Systemen, die Common Language Runtime-Assemblys unterstützen, legt der Installer den Wert dieser Eigenschaft auf die Dateiversion von fusion.dll fest. Der Installer legt diese Eigenschaft nicht fest, wenn das Betriebssystem keine Common Language Runtime-Assemblys unterstützt.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Gibt den Windows Produkttyp an.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | Unter Windows Betriebssystemen 2000 und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft BackOffice-Komponenten installiert sind.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | Unter Windows Betriebssystemen 2000 und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn Windows 2000 Datacenter Server installiert ist.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | Unter Windows Betriebssystemen 2000 und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn Windows 2000 Advanced Server installiert ist.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | Auf Windows XP-Betriebssystemen und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn das Betriebssystem Home (nicht Professional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | Unter Windows Betriebssystemen 2000 und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft Small Business Server installiert ist.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | Unter Windows Betriebssystemen 2000 und höher legt der Installer diese Eigenschaft nur dann auf 1 (eins) fest, wenn Microsoft Small Business Server mit der restriktiven Clientlizenz installiert ist.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | Unter Windows Betriebssystemen 2000 und höher legt der Installer die [**MsiNTSuiteWebServer-Eigenschaft**](msintsuitewebserver.md) auf 1 (eins) fest, wenn die Webedition von Windows Server 2003 installiert ist. Nur verfügbar mit Windows Server 2003 des Windows Installers.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | Das Installationsprogramm legt diese Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition installiert ist.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Auf Systemen, die Win32-Assemblys unterstützen, legt der Installer den Wert dieser Eigenschaft auf die Dateiversion der sxs.dll. Das Installationsprogramm setzt diese Eigenschaft nicht, wenn das Betriebssystem Win32-Assemblys nicht unterstützt.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Legen Sie fest, ob OLE den Windows unterstützt.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | Das Installationsprogramm legt die [**RedirectedDllSupport-Eigenschaft**](redirecteddllsupport.md) fest, wenn das System, das die Installation vorsteuert, [isolierte Komponenten unterstützt.](isolated-components.md)<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | Das Installationsprogramm legt die [**RemoteAdminTS-Eigenschaft**](remoteadmints.md) fest, wenn das System ein Remoteverwaltungsserver ist, auf dem der Terminalserver-Rollendienst ausgeführt wird.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Die Versionsnummer des Betriebssystem-Service Packs.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Die Nebenversionsnummer des Betriebssystem-Service Packs.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Legen Sie fest, wenn das System als freigegebene Windows.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Legen Sie fest, ob die Shell Feature-Werbung unterstützt.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Standardsprachbezeichner für das System.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Wird festgelegt, wenn das System ein Server ist, auf dem der Terminalserver-Rollendienst ausgeführt wird.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Gibt an, ob das Betriebssystem die Verwendung von TTC-Dateien (True Type Font Collections) unterstützt.<br/>                                                                                                                                                                                            |
| [**Version9x**](version9x.md)<br/>                                                 | Versionsnummer für das Windows Betriebssystem.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Numerische Datenbankversion der aktuellen Installation.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Versionsnummer für das Betriebssystem.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Versionsnummer für das Betriebssystem, wenn das System auf einem 64-Bit-Computer ausgeführt wird.<br/>                                                                                                                                                                                               |
| [**Windows Build**](windowsbuild.md)<br/>                                          | Buildnummer des Betriebssystems.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Produktinformationseigenschaften

Die folgende Liste enthält Links zu weitere Informationen zu produktspezifischen Eigenschaften, die in der [Eigenschaftentabelle angegeben sind.](property-table.md)



| Eigenschaftsname                                                  | Kurzbeschreibung                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Internetadresse oder URL für technischen Support.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Telefonnummern des technischen Support.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Zeichenfolge, die von einem Meldungsfeld angezeigt wird, das zur Eingabe eines Datenträgers aufgefordert wird.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Legen Sie auf 1 (eins) fest, wenn die aktuelle Installation von einem Paket ausgeführt wird, das über eine Administratorinstallation erstellt wurde.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Platziert Einheiten links von der Zahl.<br/>                                                                                        |
| [**Hersteller**](manufacturer.md)<br/>                | Name des Anwendungsherstellers. (Erforderlich)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | Das Installationsprogramm legt diese Eigenschaft auf 1 (eins) fest, wenn die Installation eine Medienquelle verwendet, z. B. eine CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | Das Vorhandensein dieser Eigenschaft gibt an, dass eine Änderungstransformation des Produktcodes für das Produkt registriert ist.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Diese Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit Instanztransformationen an.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | Das Installationsprogramm legt diese Eigenschaft für Installationen fest, die von einer [Gleichzeitige Installation](concurrent-installations.md) ausgeführt werden.<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Zeichenfolge, die als Vorlage für die [**PIDKEY-Eigenschaft verwendet**](pidkey.md) wird.<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Ein eindeutiger Bezeichner für eine bestimmte Produktversion. (Erforderlich)<br/>                                                                 |
| [**Productname**](productname.md)<br/>                  | Lesbarer Name einer Anwendung. (Erforderlich)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Legen Sie auf den installierten Zustand eines Produkts fest.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Das Zeichenfolgenformat der Produktversion als numerischer Wert. (Erforderlich)<br/>                                                            |
| [**Upgradecode**](upgradecode.md)<br/>                  | Eine GUID, die einen verknüpften Satz von Produkten darstellt.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Updateeigenschaften für Zusammenfassungsinformationen

Die folgenden Eigenschaften werden nur von Transformationen in MSP-Dateien festgelegt, die zum Aktualisieren des Zusammenfassungsinformationsstreams eines administrativen Images verwendet werden.



| Eigenschaft                                                              | BESCHREIBUNG                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | Der Wert dieser Eigenschaft wird in die [**Revision number Summary-Eigenschaft**](revision-number-summary.md) geschrieben.<br/> |
| [**PATCH PATCH PATCHPATCHUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | Der Wert dieser Eigenschaft wird in die [**Comments Summary-Eigenschaft**](comments-summary.md) geschrieben.<br/>               |
| [**PATCH PATCHUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | Der Wert dieser Eigenschaft wird in die [**Subject Summary-Eigenschaft**](subject-summary.md) geschrieben.<br/>                 |



 

## <a name="system-folder-properties"></a>Systemordnereigenschaften

Die folgende Liste enthält Links zu weiteren Informationen zu Systemordnern, die das Installationsprogramm beim Setup festlegt.



| Eigenschaft                                                        | BESCHREIBUNG                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | Der vollständige Pfad zum Verzeichnis, das Verwaltungstools enthält.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | Der vollständige Pfad zum **Roamingordner** für den aktuellen Benutzer.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | Der vollständige Pfad zu Anwendungsdaten für alle Benutzer.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Der vollständige Pfad zum vordefinierten **64-Bit-Ordner "Allgemeine Dateien".**<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Der vollständige Pfad zum Ordner **Allgemeine Dateien** für den aktuellen Benutzer.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | Der vollständige Pfad zum **Ordner Desktop.**<br/>                                   |
| [**FavoritenOrdner**](favoritesfolder.md)<br/>           | Der vollständige Pfad zum Ordner **Favoriten** für den aktuellen Benutzer.<br/>            |
| [**SchriftartenOrdner**](fontsfolder.md)<br/>                   | Der vollständige Pfad zum Ordner **Schriftarten.**<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | Der vollständige Pfad zu dem Ordner, der lokale Anwendungen (ohneRoaming) enthält.<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | Der vollständige Pfad zum Ordner **Bilder.**<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | Der vollständige Pfad zum **Ordner NetHood.**<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Der vollständige Pfad zum Ordner **Dokumente** für den aktuellen Benutzer.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | Der vollständige Pfad zum Ordner **PrintHood.**<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Der vollständige Pfad zum vordefinierten **64-Bit-Ordner "Programme".**<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | Der vollständige Pfad zum vordefinierten **32-Bit-Ordner "Programme".**<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | Der vollständige Pfad zum Ordner **Programmmenü.**<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Der vollständige Pfad zum Ordner **Zuletzt verwendet.**<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | Der vollständige Pfad zum Ordner **SendTo** für den aktuellen Benutzer.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | Der vollständige Pfad zum **Ordner Startmenü.**<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Der vollständige Pfad zum **Startordner.**<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Der vollständige Pfad zum Ordner für 16-Bit-System-DLLs.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Der vollständige Pfad zum vordefinierten **Ordner System64.**<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | Der vollständige Pfad zum **Ordner System** für den aktuellen Benutzer.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Der vollständige Pfad zum Ordner **Temp.**<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | Der vollständige Pfad zum **Vorlagenordner** für den aktuellen Benutzer.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | Der vollständige Pfad zum **Ordner Windows.**<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | Das Volume des **ordners Windows.**<br/>                                      |



 

## <a name="user-information-properties"></a>Benutzerinformationseigenschaften

Die folgende Liste enthält Links zu weiteren Informationen zu vom Benutzer bereitgestellten Informationen.



| Eigenschaft                                                      | BESCHREIBUNG                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Liste der Eigenschaften, die während einer Administratorinstallation festgelegt werden.<br/>       |
| [**COMPANYNAME**](companyname.md)<br/>                 | Organisationsname des Benutzers, der die Installation ausführt.<br/>            |
| [**Logonuser**](logonuser.md)<br/>                     | Benutzername für den Benutzer, der derzeit angemeldet ist.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Liste der Eigenschaften, die verhindert werden, dass sie in das Protokoll geschrieben werden.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Teil der Produkt-ID, die der Benutzer eingibt.<br/>                                 |
| [**Productid**](productid.md)<br/>                     | Vollständige Produkt-ID nach erfolgreicher Überprüfung.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Standardsprachbezeichner des aktuellen Benutzers.<br/>                             |
| [**NUTZERNAME**](username.md)<br/>                       | Benutzer, der die Installation ausführt.<br/>                                     |
| [**UserSID-Eigenschaft**](usersid.md)<br/>                | Wird vom Installationsprogramm entsprechend der Sicherheits-ID (SID) des Benutzers festgelegt.<br/> |



 

 

 
