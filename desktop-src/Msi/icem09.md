---
description: ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4d2af38903d2e704d49b48f932818d8dfaeeb1e12588c007d4af05c297642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894490"
---
# <a name="icem09"></a>ICEM09

ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet. Hierzu wird überprüft, ob keine Komponente im Modul ein Verzeichnis in einem vordefinierten Systemverzeichnis wie "ProgramFilesFolder" oder "StartMenuFolder" installiert. Stattdessen sollten Module Verzeichnisse mit eindeutigen Namen (erstellt mit der Benennungskonvention für Mergemodule) und benutzerdefinierte Aktionen verwenden, um das entsprechende Zielverzeichnis als Ziel zu verwenden. Dieser Ansatz verhindert, dass Module mit einer vorhandenen Verzeichnisstruktur in der endgültigen Datenbank in Konflikt geraten. ICEM09 überprüft, ob die benutzerdefinierten Aktionen, die für diese Technik erforderlich sind, entweder nicht vorhanden sind (sodass das Mergetool sie generieren kann) oder in der richtigen Form vorhanden sind (sodass sie erwartungsgemäß funktionieren).

Fehler beim Beheben einer Warnung oder eines Fehlers, die von ICEM09 gemeldet werden, kann zu Problemen für die Clients Ihres Mergemoduls führen. Verzeichnistabellenzeilen mit Primärschlüsseln wie ProgramFilesFolder sind häufig in einer Datenbank vorhanden. Wenn Komponenten in Ihrem Modul daher direkt in vordefinierten Verzeichnissen wie ProgramFilesFolder installiert werden, können die Verzeichniseinträge im Modul mit bereits vorhandenen Zeilen in Konflikt stehen. Diese Bedingung erfordert, dass der Benutzer Ihres Moduls die Quelldateien aus Ihrem Modul aufteilt, um dem vorhandenen Quellverzeichnis zu entsprechen.

## <a name="result"></a>Ergebnis

ICEM09 meldet einen Fehler oder eine Warnung, wenn eine Modulkomponente ein Verzeichnis in einem vordefinierten Systemverzeichnis installiert, was zu einem möglichen Namenskonflikt mit der vorhandenen Verzeichnisstruktur führt.

## <a name="example"></a>Beispiel

ICEM09 sendet die folgenden Warnungen für ein Modul, das die angezeigten Datenbankeinträge enthält.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Benennen Sie das Mergemodulverzeichnis um, damit es nicht mit einer Windows Installer-Eigenschaft übereinstimmt und daher eindeutig ist. Legen Sie dann eine Eigenschaft mit dem gleichen Namen auf den Wert des Windows Installer-Verzeichnisses fest. Wenn die Verzeichnisauflösung erfolgt, hat das Verzeichnis eine Eigenschaft mit dem gleichen Namen, sodass der Installationsspeicherort des Verzeichnisses der Wert der Eigenschaft ist. Dateien werden vom unterschiedlichen Quellspeicherort an denselben Zielspeicherort verschoben. Dieser Prozess sollte die Zusammenführungskonflikte vollständig entfernen.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Wenn die Aktion nicht die Sequenznummer 1 hat, wird sie möglicherweise nicht früh genug in der Sequenz mit der Zieldatenbank zusammengeführt, um effektiv zu funktionieren.

Um diese Warnung zu beheben, legen Sie die Sequenznummer auf 1 fest. Beachten Sie, dass die meisten aktuellen Mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur Zusammenführungszeit generieren, sodass es nicht immer erforderlich ist, die Aktionen explizit im Mergemodul zu erstellen.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Da die CustomAction-Spalte der Primärschlüssel der CustomAction-Tabelle ist, generieren einige Mergetools möglicherweise doppelte Aktionen, da sich der Name der vorab erstellten Aktion unterscheidet.

Um diese Warnung zu beheben, benennen Sie die Aktion mit dem Zielverzeichnis. Beachten Sie, dass die meisten aktuellen Mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur Zusammenführungszeit generieren, sodass es nicht immer erforderlich ist, die Aktionen explizit im Mergemodul zu erstellen.

[Verzeichnistabelle](directory-table.md)



| Verzeichnis          | \_Übergeordnetes Verzeichnis | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | Ein          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Komponententabelle](component-table.md)



| Komponente               | Verzeichnis          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | StartMenuFolder    |
| Component3.<GUID> | AppDataFolder      |
| Component4.<GUID> | MyPicturesFolder   |



 

[CustomAction-Tabelle](customaction-table.md)



| CustomAction                 | type | `Source`                       | Ziel              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder.<GUID> | 51   | StartMenuFolder.<GUID> | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[Tabelle "ModuleInstallExecuteSequence"](moduleinstallexecutesequence-table.md)



| Aktion                       | Sequenz | BaseAction | Danach | Bedingung |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz zum Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



