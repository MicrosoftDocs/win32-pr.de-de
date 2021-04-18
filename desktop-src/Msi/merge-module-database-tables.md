---
description: Die folgenden Tabellen sind in einem standardmäßigen Mergemodul erforderlich.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Modul Datenbanktabellen zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351432"
---
# <a name="merge-module-database-tables"></a>Modul Datenbanktabellen zusammenführen

Die folgenden Tabellen sind in einem standardmäßigen Mergemodul erforderlich.



| Tabellenname                                       | Kommentar                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Komponente](component-table.md)                 | Benötigten                                                                                       |
| [Verzeichnis](directory-table.md)                 | Benötigten                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | Benötigten                                                                                       |
| [File](file-table.md)                           | Benötigten                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | Benötigten In der Installer-Datenbank zusammengeführt. Listet die Informationen auf, die ein Mergemodul identifizieren. |
| [Modulecomponents](modulecomponents-table.md)   | Benötigten In der Installer-Datenbank zusammengeführt. Listet alle Komponenten im Mergemodul auf.     |



 

Die folgenden Tabellen treten nur in Mergemodulen oder anderen Installer-Datenbanken auf, die bereits mit einem Mergemodul kombiniert wurden.



| Tabellenname                                     | Kommentar                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Moduleabhängigkeit](moduledependency-table.md) | In der Installer-Datenbank zusammengeführt. Listet andere für dieses Mergemodul erforderliche Mergemodule auf.                |
| [Moduleausschluss](moduleexclusion-table.md)   | In der Installer-Datenbank zusammengeführt. Listet andere Mergemodule auf, die mit diesem Mergemodul nicht kompatibel sind. |



 

Die folgenden modulesequence-Tabellen treten nur in Mergemodulen auf.



| Tabellenname                                                             | Kommentar                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Moduleadminuisequence](moduleadminuisequence-table.md)               | Führt Aktionen in der [Tabelle AdminUISequence](adminuisequence-table.md)zusammen.               |
| [Moduleadminexecutesequence](moduleadminexecutesequence-table.md)     | Führt Aktionen in der [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)zusammen.     |
| [Moduleadvtuisequence](moduleadvtuisequence-table.md)                 | Verwenden Sie diese Tabelle nicht. Weitere Informationen finden Sie unter [advtuisequence Table](advtuisequence-table.md). |
| [Moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)       | Führt Aktionen in der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)zusammen.       |
| [Moduleignoretable](moduleignoretable-table.md)                       | Listet die Tabellen im Modul auf, die nicht in der MSI-Datei zusammengeführt werden.                        |
| [Moduleinstalluisequence](moduleinstalluisequence-table.md)           | Führt Aktionen in der [Tabelle "InstallUISequence](installuisequence-table.md)" aus.           |
| [Moduleinstallexecutesequence](moduleinstallexecutesequence-table.md) | Führt Aktionen in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)zusammen. |



 

Die folgenden Tabellen sind in jedem konfigurierbaren Mergemodul erforderlich. Zum Erstellen eines konfigurierbaren Mergemoduls ist Mergemod.dll 2,0 oder höher erforderlich. Weitere Informationen finden Sie unter [konfigurierbare Mergemodule](configurable-merge-modules.md).



| Tabellenname                                                 | Kommentar                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ModuleSubstitution-Tabelle](modulesubstitution-table.md)   | Benötigten Diese Tabelle wird nicht in der Ziel Installations Datenbank zusammengeführt. Gibt die konfigurierbaren Felder in der Zieldatenbank an und stellt eine Vorlage für die Konfiguration der einzelnen Felder bereit. |
| [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) | Benötigten Diese Tabelle wird nicht in der Ziel Installations Datenbank zusammengeführt. Identifiziert die konfigurierbaren Attribute des Moduls.                                                                 |



 

Die folgenden Installer-Tabellen können nicht in einem standardmäßigen Mergemodul auftreten.

-   [Bbcontrol](bbcontrol-table.md)
-   [Billboard](billboard-table.md)
-   [Ccpsearch](ccpsearch-table.md)
-   [Fehler](error-table.md)
-   [Feature](feature-table.md)
-   [LaunchCondition-Tabelle](launchcondition-table.md)
-   [Medien](media-table.md)
-   [Patch](patch-table.md)
-   [Upgrade](upgrade-table.md)

Die folgenden Installer-Tabellen sind optional in Mergemodulen.

-   [Action Text](actiontext-table.md)
-   ["AdminExecuteSequence"](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Advtuisequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Klasse](class-table.md)
-   [ComboBox](combobox-table.md)
-   [Complocator](complocator-table.md)
-   [Steuerung](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Dialogfeld](dialog-table.md)
-   [Drlocator](drlocator-table.md)
-   [Duplicatefile](duplicatefile-table.md)
-   [Umgebung](environment-table.md)
-   [Tabelle EventMapping](eventmapping-table.md)
-   [Erweiterung](extension-table.md)
-   [Schriftart](font-table.md)
-   [Symbol:](icon-table.md)
-   [INIFILE](inifile-table.md)
-   [Inilocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [Medi](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [Odbcatcher Tribute](odbcattribute-table.md)
-   [ODBCDatasource](odbcdatasource-table.md)
-   [Odbcdriver](odbcdriver-table.md)
-   [Odbcsourceattribute](odbcsourceattribute-table.md)
-   [Odbctranslator](odbctranslator-table.md)
-   [ProgID-Tabelle](progid-table.md)
-   [Eigenschaft](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Registrierungs Tabelle](registry-table.md)
-   [Reglocator](reglocator-table.md)
-   [RemoveFile aktualisieren](removefile-table.md)
-   [Removeinifile](removeinifile-table.md)
-   [Removeregistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [Selfreg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [Serviceingestall](serviceinstall-table.md)
-   [Tastenkombination](shortcut-table.md)
-   [Signature](signature-table.md)
-   [Textart](textstyle-table.md)
-   [Export der Typbibliothek](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verb](verb-table.md)

 

 



