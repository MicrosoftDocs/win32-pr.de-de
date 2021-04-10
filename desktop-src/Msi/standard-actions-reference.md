---
description: Der Windows Installer verfügt über die folgenden Standard Aktionen.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Referenz zu Standard Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5104c39639ff2bc7b504996467cf707eb52bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215563"
---
# <a name="standard-actions-reference"></a>Referenz zu Standard Aktionen

Der Windows Installer verfügt über die folgenden Standard Aktionen.



| Name der Aktion                                                     | Kurze Beschreibung der Aktion                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMIN](admin-action.md)                                       | Eine Aktion der obersten Ebene, die für eine administrative Installation verwendet wird.                                                                                                                   |
| [Benen](advertise-action.md)                               | Eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von angekündigten Komponenten aufgerufen wird.                                                                                                         |
| [Zuordnung von "Zuweisung"](allocateregistryspace-action.md)       | Überprüft, ob der durch [**availablefreereg**](availablefreereg.md) angegebene freie Speicherplatz in der Registrierung vorhanden ist.                                                               |
| [AppSearch](appsearch-action.md)                               | Sucht nach früheren Produktversionen und bestimmt, ob Upgrades installiert sind.                                                                                        |
| [BindImage](bindimage-action.md)                               | Bindet ausführbare Dateien an importierte DLLs.                                                                                                                                           |
| [Ccpsearch](ccpsearch-action.md)                               | Verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.                                              |
| [Costfinalize](costfinalize-action.md)                         | Beendet den internen Installationskosten Prozess, der von der [costinitialize-Aktion](costinitialize-action.md)gestartet wurde.                                                               |
| [Costinitialize](costinitialize-action.md)                     | Startet den Installationskosten Prozess.                                                                                                                                      |
| ["Kreatefolders"](createfolders-action.md)                       | Erstellt leere Ordner für-Komponenten.                                                                                                                                         |
| ["Kreateshortcuts"](createshortcuts-action.md)                   | Erstellt Verknüpfungen.                                                                                                                                                            |
| [Delta Service Services](deleteservices-action.md)                     | Entfernt Systemdienste.                                                                                                                                                      |
| [DISABLEROLLBACK](disablerollback-action.md)                   | Deaktiviert das Rollback für den Rest der Installation.                                                                                                                      |
| [Duplicatefiles](duplicatefiles-action.md)                     | Dupliziert Dateien, die von der InstallFiles-Aktion installiert wurden.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Überprüft die [**ExecuteAction**](executeaction.md) -Eigenschaft, um zu bestimmen, welche Aktion der obersten Ebene die Ausführungssequenz startet, und führt diese Aktion aus.                          |
| [Datei Kosten](filecost-action.md)                                 | Initialisiert die Berechnung der Datenträger Kosten mit dem Installationsprogramm. Die Datenträger Kosten werden erst abgeschlossen, wenn die costfinalize-Aktion ausgeführt wird.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Erkennt die Übereinstimmung zwischen der [upgradetabelle](upgrade-table.md) und den installierten Produkten.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Wird in der Aktions Sequenz verwendet, um den Benutzer zur Eingabe eines Neustarts des Systems während der Installation aufzufordern.                                                                           |
| [Installieren](install-action.md)                                   | Eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von Komponenten aufgerufen wird.                                                                                                                    |
| [Installadminpackage](installadminpackage-action.md)           | Kopiert die Installer-Datenbank in den administrativen Installations Punkt.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallFinalize-Aktion enthält. Beendet die Transaktion nicht.   |
| [InstallFiles](installfiles-action.md)                         | Kopiert Dateien aus der Quelle in das Zielverzeichnis.                                                                                                                    |
| [InstallFinalize wurde](installfinalize-action.md)                   | Führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallFinalize-Aktion enthält. Markiert das Ende einer Transaktion. |
| [Installinitialisieren](installinitialize-action.md)               | Markiert den Anfang einer Transaktion.                                                                                                                                         |
| [Installsfpcatalogfile](installsfpcatalogfile-action.md)       | Mit der Aktion installsfpcatalogfile werden die von Windows Me für den Windows-Datei Schutz verwendeten Kataloge installiert.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Mit dieser Option wird überprüft, ob alle Volumes mit attributierten Kosten über ausreichend Speicherplatz für die Installation verfügen.                                                                                   |
| [Isolatecomponents](isolatecomponents-action.md)               | Verarbeitet die [isolatedcomponent-Tabelle](isolatedcomponent-table.md) .                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Wertet einen Satz von Bedingungs Anweisungen aus, die in der LaunchCondition-Tabelle enthalten sind, die alle als true ausgewertet werden müssen, bevor die Installation fortgesetzt werden kann                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migriert die aktuellen Funktions Zustände zur ausstehenden Installation.                                                                                                                  |
| ["Muvefiles"](movefiles-action.md)                               | Hiermit werden vorhandene Dateien lokalisiert und an einen neuen Speicherort verschoben oder kopiert.                                                                                                     |
| [Msikonfigurireservices](msiconfigureservices-action.md)         | Konfiguriert einen Dienst für das System. **[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.<br/>                           |
| [Msipublishassemblyaktion](msipublishassemblies-action.md)  | Verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die installiert werden.                                                                |
| [Msiunpublishassemblys](msiunpublishassemblies-action.md)     | Verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die entfernt werden.                                                                  |
| [Installodbc](installodbc-action.md)                           | Installiert die ODBC-Treiber,-Konvertierer und-Datenquellen.                                                                                                                     |
| [Installdienste](installservices-action.md)                   | Registriert einen Dienst beim System.                                                                                                                                          |
| [Patchdateien](patchfiles-action.md)                             | Fragt die patchtabelle ab, um zu bestimmen, welche Patches auf bestimmte Dateien angewendet werden, und führt dann das Byte Weise Patchen der Dateien aus.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registriert Komponenten, Ihre Schlüssel Pfade und Komponenten Clients.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Gibt die in der Tabelle PublishComponent angegebenen Komponenten an.                                                                                                            |
| [Publishfeatures](publishfeatures-action.md)                   | Schreibt den Funktionsstatus der einzelnen Funktionen in die Systemregistrierung.                                                                                                             |
| [Publishproduct](publishproduct-action.md)                     | Veröffentlicht Produktinformationen mit dem System.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Verwaltet die Registrierung von COM-Klassen Informationen mit dem System.                                                                                                            |
| [Registercomplus](registercomplus-action.md)                   | Die registercomplus-Aktion registriert com+-Anwendungen.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registriert Erweiterungs bezogene Informationen beim System.                                                                                                                      |
| [Register Fonts](registerfonts-action.md)                       | Registriert installierte Schriftarten beim System.                                                                                                                                    |
| [Registermimeinfo](registermimeinfo-action.md)                 | Registriert MIME-Informationen beim System.                                                                                                                                   |
| [Register Product](registerproduct-action.md)                   | Registriert Produktinformationen beim Installer und speichert die Installer-Datenbank auf dem lokalen Computer.                                                                     |
| [Registerprogidinfo](registerprogidinfo-action.md)             | Registriert OLE-ProgID-Informationen beim System.                                                                                                                             |
| [Registertypelibraries](registertypelibraries-action.md)       | Registriert Typbibliotheken beim System.                                                                                                                                     |
| [Register User](registeruser-action.md)                         | Registriert Benutzerinformationen, um den Benutzer eines Produkts zu identifizieren.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Löscht Dateien, die von der duplicatefiles-Aktion installiert wurden.                                                                                                                         |
| [Removeumgebfäden](removeenvironmentstrings-action.md) | Ändert die Werte von Umgebungsvariablen.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Entfernt installierte Versionen eines Produkts.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Entfernt Dateien, die zuvor von der InstallFiles-Aktion installiert wurden.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Entfernt leere Ordner, die mit den zu entfernenden Komponenten verknüpft sind.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Löscht ini-Dateiinformationen, die einer in der IniFile-Tabelle angegebenen Komponente zugeordnet sind.                                                                                     |
| [Removeodbc](removeodbc-action.md)                             | Entfernt ODBC-Datenquellen,-Konvertierer und-Treiber.                                                                                                                          |
| [Removeregistryvalues](removeregistryvalues-action.md)         | Entfernt die Registrierungsschlüssel einer Anwendung, die aus der Registrierungs Tabelle erstellt wurden.                                                                                            |
| [Removeshortcuts](removeshortcuts-action.md)                   | Verwaltet das Entfernen einer angekündigten Verknüpfung, deren Funktion für die Deinstallation ausgewählt ist.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Bestimmt den Quell Speicherort und legt die [**SourceDir**](sourcedir.md) -Eigenschaft fest.                                                                                          |
| [RMCCPSEARCH](rmccpsearch-action.md)                           | Verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.                                              |
| [Schedulereboot](schedulereboot-action.md)                     | Fordert den Benutzer zur Eingabe eines Systemneustarts am Ende der Installation auf.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Verarbeitet Module in der Tabelle selfreg und registriert Sie, wenn Sie installiert sind.                                                                                              |
| [Selfunregmodules](selfunregmodules-action.md)                 | Hebt die Registrierung der Module in der selfreg-Tabelle auf, die für die Installation festgelegt sind.                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | Führt die Aktionen in einer Tabelle aus, die von der [**Sequence**](sequence.md) -Eigenschaft angegeben wird.                                                                                           |
| ["Stodbcfolders"-Aktion](setodbcfolders-action.md)              | Überprüft das System auf vorhandene ODBC-Treiber und legt das Zielverzeichnis für neue ODBC-Treiber fest.                                                                                   |
| [Startdienste](startservices-action.md)                       | Startet Systemdienste.                                                                                                                                                       |
| [Stop Services](stopservices-action.md)                         | Beendet Systemdienste.                                                                                                                                                        |
| [Unpublishcomponents](unpublishcomponents-action.md)           | Verwaltet die nicht Ankündigung von Komponenten aus der PublishComponent-Tabelle und entfernt Informationen zu veröffentlichten Komponenten.                                                 |
| [Nicht publishfeatures](unpublishfeatures-action.md)               | Entfernt die Zustellungs Status-und featurekomponentenzuordnungsinformationen aus der Systemregistrierung.                                                                               |
| [Unregisterclassinfo](unregisterclassinfo-action.md)           | Verwaltet das Entfernen von COM-Klassen aus der Systemregistrierung.                                                                                                                  |
| [Unregistercomplus](unregistercomplus-action.md)               | Die unregistercomplus-Aktion entfernt com+-Anwendungen aus der Registrierung.                                                                                                     |
| [Unregisterextensioninfo](unregisterextensioninfo-action.md)   | Verwaltet das Entfernen von Erweiterungs bezogenen Informationen aus dem System.                                                                                                         |
| [Unregisterfonts](unregisterfonts-action.md)                   | Entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.                                                                                                       |
| [Unregistermimeinfo](unregistermimeinfo-action.md)             | Hebt die Registrierung von MIME-bezogenen Informationen aus der Systemregistrierung auf.                                                                                                                |
| [Unregisterprogidinfo](unregisterprogidinfo-action.md)         | Verwaltet die Aufhebung der Registrierung von OLE ProgID-Informationen mit dem System.                                                                                                         |
| [Unregistertypelibraries](unregistertypelibraries-action.md)   | Hebt die Registrierung der Typbibliotheken beim System auf.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Legt die [**ProductID-**](productid.md) Eigenschaft auf den vollständigen Produkt Bezeichner fest.                                                                                                  |
| [Write-Umgebungs Zeichenfolgen](writeenvironmentstrings-action.md)   | Ändert die Werte von Umgebungsvariablen.                                                                                                                                 |
| ["Write"-Werte](writeinivalues-action.md)                     | Schreibt Informationen der INI-Datei.                                                                                                                                                 |
| ["Schreibegistryvalues"](writeregistryvalues-action.md)           | Richtet Registrierungsinformationen ein.                                                                                                                                                 |



 

 

 




