---
description: Die folgenden Tabellen sind in einem Standardzusammenführungsmodul erforderlich.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Zusammenführen von Moduldatenbanktabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201b4af776ae0b68fd4330dca8240390e5731950fdaba5a734f48d887db5be84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580640"
---
# <a name="merge-module-database-tables"></a>Zusammenführen von Moduldatenbanktabellen

Die folgenden Tabellen sind in einem Standardzusammenführungsmodul erforderlich.



| Tabellenname                                       | Kommentar                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Komponente](component-table.md)                 | (ERFORDERLICH)                                                                                       |
| [Verzeichnis](directory-table.md)                 | (ERFORDERLICH)                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | (ERFORDERLICH)                                                                                       |
| [File](file-table.md)                           | (ERFORDERLICH)                                                                                       |
| [Modulesignature](modulesignature-table.md)     | (ERFORDERLICH) Zusammengeführt mit der Installer-Datenbank. Listet die Informationen auf, die ein Mergemodul identifizieren. |
| [ModuleComponents](modulecomponents-table.md)   | (ERFORDERLICH) Zusammengeführt mit der Installer-Datenbank. Listet alle Komponenten im Mergemodul auf.     |



 

Die folgenden Tabellen treten nur in Mergemodulen oder anderen Installerdatenbanken auf, die bereits mit einem Mergemodul kombiniert wurden.



| Tabellenname                                     | Kommentar                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | Zusammengeführt mit der Installer-Datenbank. Listet andere Mergemodule auf, die für dieses Mergemodul erforderlich sind.                |
| [ModuleExclusion](moduleexclusion-table.md)   | Zusammengeführt mit der Installer-Datenbank. Listet andere Mergemodule auf, die mit diesem Mergemodul nicht kompatibel sind. |



 

Die folgenden ModuleSequence-Tabellen treten nur in Mergemodulen auf.



| Tabellenname                                                             | Kommentar                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | Führt Aktionen in der [AdminUISequence-Tabelle zusammen.](adminuisequence-table.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | Führt Aktionen in der [AdminExecuteSequence-Tabelle zusammen.](adminexecutesequence-table.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | Verwenden Sie diese Tabelle nicht. Weitere Informationen finden Sie in der [Tabelle AdvtUISequence.](advtuisequence-table.md) |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | Führt Aktionen in der [Tabelle AdvtExecuteSequence zusammen.](advtexecutesequence-table.md)       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | Listet Tabellen im Modul auf, die nicht mit der .msi zusammengeführt werden.                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | Führt Aktionen in der [InstallUISequence-Tabelle zusammen.](installuisequence-table.md)           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | Führt Aktionen in der [InstallExecuteSequence-Tabelle zusammen.](installexecutesequence-table.md) |



 

Die folgenden Tabellen sind in jedem konfigurierbaren Mergemodul erforderlich. Mergemod.dll 2.0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen. Weitere Informationen finden Sie unter [Konfigurierbare Mergemodule.](configurable-merge-modules.md)



| Tabellenname                                                 | Kommentar                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ModuleSubsmodultabelle](modulesubstitution-table.md)   | (ERFORDERLICH) Diese Tabelle wird nicht mit der Zielinstallationsdatenbank zusammengeführt. Gibt die konfigurierbaren Felder in der Zieldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder zur Verfügung. |
| [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) | (ERFORDERLICH) Diese Tabelle wird nicht mit der Zielinstallationsdatenbank zusammengeführt. Identifiziert die konfigurierbaren Attribute des Moduls.                                                                 |



 

Die folgenden Installationstabellen können nicht in einem Standardzusammenführungsmodul auftreten.

-   [BBControl](bbcontrol-table.md)
-   [Billboard](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [Fehler](error-table.md)
-   [Feature](feature-table.md)
-   [LaunchCondition-Tabelle](launchcondition-table.md)
-   [Medien](media-table.md)
-   [Patch](patch-table.md)
-   [Upgrade](upgrade-table.md)

Die folgenden Installationstabellen sind in Mergemodulen optional.

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Klasse](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [Steuerung](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Dialogfeld](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [DuplicateFile](duplicatefile-table.md)
-   [Umgebung](environment-table.md)
-   [EventMapping](eventmapping-table.md)
-   [Erweiterung](extension-table.md)
-   [Schriftart](font-table.md)
-   [Symbol:](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [Mime](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCAttribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [ProgID-Tabelle](progid-table.md)
-   [Eigenschaft](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Registrierungstabelle](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [ServiceInstall](serviceinstall-table.md)
-   [Tastenkombination](shortcut-table.md)
-   [Signature](signature-table.md)
-   [TextStyle](textstyle-table.md)
-   [Typelib](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verb](verb-table.md)

 

 



