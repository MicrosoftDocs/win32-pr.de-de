---
description: Der Windows Installer verfügt über die folgenden Standardaktionen.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Referenz zu Standardaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e88b4b60e3dd13dc4830a1ea4ba2d16a439546d1ced3dc2a8b7552780548d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627630"
---
# <a name="standard-actions-reference"></a>Referenz zu Standardaktionen

Der Windows Installer verfügt über die folgenden Standardaktionen.



| Name der Aktion                                                     | Kurze Beschreibung der Aktion                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMIN](admin-action.md)                                       | Eine Aktion der obersten Ebene, die für eine Administratorinstallation verwendet wird.                                                                                                                   |
| [Werben](advertise-action.md)                               | Eine Aktion der obersten Ebene, die aufgerufen wird, um angekündigte Komponenten zu installieren oder zu entfernen.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Überprüft, ob der von [**AVAILABLEFREEREG**](availablefreereg.md) angegebene freie Speicherplatz in der Registrierung vorhanden ist.                                                               |
| [AppSearch](appsearch-action.md)                               | Sucht nach früheren Versionen von Produkten und ermittelt, dass Upgrades installiert sind.                                                                                        |
| [BindImage](bindimage-action.md)                               | Bindet ausführbare Dateien an importierte DLLs.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Verwendet Dateisignaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert werden, bevor eine Upgradeinstallation ausgeführt wird.                                              |
| [CostFinalize](costfinalize-action.md)                         | Beendet den Kostenprozess für die interne Installation, der von der [CostInitialize-Aktion gestartet wurde.](costinitialize-action.md)                                                               |
| [CostInitialize](costinitialize-action.md)                     | Startet den Kostenprozess für die Installation.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Erstellt leere Ordner für Komponenten.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Erstellt Verknüpfungen.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Entfernt Systemdienste.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Deaktiviert das Rollback für den Rest der Installation.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Dupliziert Dateien, die von der InstallFiles-Aktion installiert wurden.                                                                                                                        |
| [Executeaction](executeaction-action.md)                       | Überprüft die [**EXECUTEACTION-Eigenschaft,**](executeaction.md) um zu bestimmen, welche Aktion der obersten Ebene die Ausführungssequenz startet, und führt dann diese Aktion aus.                          |
| [FileCost](filecost-action.md)                                 | Initialisiert die Berechnung der Datenträgerkosten mit dem Installationsprogramm. Die Datenträgerkosten werden erst abgeschlossen, wenn die Aktion CostFinalize ausgeführt wird.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Erkennt Übereinstimmungen zwischen der [Upgradetabelle und](upgrade-table.md) den installierten Produkten.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Wird in der Aktionssequenz verwendet, um den Benutzer während der Installation zur Eingabe eines Neustarts des Systems aufforderungen.                                                                           |
| [Installieren](install-action.md)                                   | Eine Aktion der obersten Ebene, die aufgerufen wird, um Komponenten zu installieren oder zu entfernen.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Kopiert die Installationsdatenbank auf den Administratorinstallationspunkt.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der letzten InstallFinalize-Aktion enthält. Beendet die Transaktion nicht.   |
| [InstallFiles](installfiles-action.md)                         | Kopiert Dateien aus der Quelle in das Zielverzeichnis.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der letzten InstallFinalize-Aktion enthält. Markiert das Ende einer Transaktion. |
| [InstallInitialize](installinitialize-action.md)               | Markiert den Anfang einer Transaktion.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | Mit der Aktion InstallSFPCatalogFile werden die Kataloge installiert, die von Windows für Windows Dateischutz verwendet werden.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Überprüft, ob alle Volumes mit zugeordneten Kosten über ausreichend Speicherplatz für die Installation verfügen.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Verarbeitet die [IsolatedComponent-Tabelle.](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Wertet eine Reihe von bedingten Anweisungen aus, die in der LaunchCondition-Tabelle enthalten sind und alle als TRUE ausgewertet werden müssen, bevor die Installation fortgesetzt werden kann.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migriert die aktuellen Featurezustände zur ausstehenden Installation.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Sucht vorhandene Dateien und verschiebt oder kopiert diese Dateien an einen neuen Speicherort.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Konfiguriert einen Dienst für das System. **[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt.<br/>                           |
| [MsiPublishAssemblies-Aktion](msipublishassemblies-action.md)  | Verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys, die installiert werden.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys, die entfernt werden.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Installiert die ODBC-Treiber, -Translators und -Datenquellen.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Registriert einen Dienst beim System.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Fragt die Patchtabelle ab, um zu bestimmen, welche Patches auf bestimmte Dateien angewendet werden, und führt dann das byteweise Patchen der Dateien aus.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registriert Komponenten, ihre Schlüsselpfade und Komponentenclients.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Gibt die in der PublishComponent-Tabelle angegebenen Komponenten an.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Schreibt den Featurestatus der einzelnen Features in die Systemregistrierung.                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Veröffentlicht Produktinformationen mit dem System.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Verwaltet die Registrierung von COM-Klasseninformationen beim System.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | Die Aktion RegisterComPlus registriert COM+-Anwendungen.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registriert Erweiterungsinformationen beim System.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registriert installierte Schriftarten beim System.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registriert MIME-Informationen beim System.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registriert Produktinformationen beim Installationsprogramm und speichert die Installationsdatenbank auf dem lokalen Computer.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registriert OLE ProgId-Informationen beim System.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registriert Typbibliotheken beim System.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registriert Benutzerinformationen, um den Benutzer eines Produkts zu identifizieren.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Löscht Dateien, die von der DuplicateFiles-Aktion installiert wurden.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Ändert die Werte von Umgebungsvariablen.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Entfernt installierte Versionen eines Produkts.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Entfernt Dateien, die zuvor von der InstallFiles-Aktion installiert wurden.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Entfernt leere Ordner, die mit komponenten verknüpft sind, die entfernt werden sollen.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Löscht .ini Dateiinformationen, die einer in der IniFile-Tabelle angegebenen Komponente zugeordnet sind.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Entfernt ODBC-Datenquellen, -Translators und -Treiber.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Entfernt die Registrierungsschlüssel einer Anwendung, die aus der Registrierungstabelle erstellt wurden.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Verwaltet das Entfernen einer angekündigten Verknüpfung, deren Funktion für die Deinstallation ausgewählt ist.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Bestimmt den Quellspeicherort und legt die [**SourceDir-Eigenschaft**](sourcedir.md) fest.                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Verwendet Dateisignaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert werden, bevor eine Upgradeinstallation ausgeführt wird.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Fordert den Benutzer am Ende der Installation zur Eingabe eines Systemneustarts auf.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Verarbeitet Module in der SelfReg-Tabelle und registriert sie, wenn sie installiert sind.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Aufheben der Registrierung der Module in der SelfReg-Tabelle, die für die Deinstallation festgelegt sind.                                                                                                  |
| [Sequenz](sequence-action.md)                                 | Führt die Aktionen in einer Tabelle aus, die von der [**SEQUENCE-Eigenschaft angegeben**](sequence.md) wird.                                                                                           |
| [SetODBCFolders-Aktion](setodbcfolders-action.md)              | Überprüft das System auf vorhandene ODBC-Treiber und legt das Zielverzeichnis für neue ODBC-Treiber fest.                                                                                   |
| [StartServices](startservices-action.md)                       | Startet Systemdienste.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Beendet Systemdienste.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Verwaltet die Nichtvertierung von Komponenten aus der PublishComponent-Tabelle und entfernt Informationen zu veröffentlichten Komponenten.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Entfernt die Zuordnungsinformationen zum Auswahlzustand und zur Featurekomponente aus der Systemregistrierung.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Verwaltet das Entfernen von COM-Klassen aus der Systemregistrierung.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | Die Aktion UnregisterComPlus entfernt COM+-Anwendungen aus der Registrierung.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Verwaltet das Entfernen erweiterungsbezogener Informationen aus dem System.                                                                                                         |
| [Aufheben der Registrierung vonFonts](unregisterfonts-action.md)                   | Entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Aufheben der Registrierung von MIME-bezogenen Informationen in der Systemregistrierung.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Verwaltet die Aufhebung der Registrierung von OLE ProgId-Informationen mit dem System.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Aufheben der Registrierung von Typbibliotheken beim System.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Legt [**die ProductID-Eigenschaft**](productid.md) auf den vollständigen Produktbezeichner fest.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Ändert die Werte von Umgebungsvariablen.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Schreibt .ini Dateiinformationen.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Richtet Registrierungsinformationen ein.                                                                                                                                                 |



 

 

 




