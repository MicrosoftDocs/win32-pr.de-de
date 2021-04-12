---
description: ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216942"
---
# <a name="icem09"></a>ICEM09

ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet. Dies geschieht, indem überprüft wird, ob keine Komponente im Modul ein Verzeichnis in einem vordefinierten System Verzeichnis installiert, wie z. b. "ProgramFilesFolder" oder "StartMenuFolder". Stattdessen sollten Module Verzeichnisse mit eindeutigen Namen verwenden (erstellt mit der Benennungs Konvention für das Mergemodul) und benutzerdefinierte Aktionen verwenden, um das entsprechende Zielverzeichnis als Ziel zu verwenden. Bei diesem Ansatz wird verhindert, dass Module in Konflikt mit einer vorhandenen Verzeichnisstruktur in der endgültigen Datenbank stehen. ICEM09 prüft, ob die für diese Technik benötigten benutzerdefinierten Aktionen entweder nicht vorhanden sind (damit das Mergetool Sie generieren kann) oder in der richtigen Form vorhanden sind (sodass Sie erwartungsgemäß funktionieren).

Wenn eine Warnung oder ein Fehler, der von ICEM09 gemeldet wurde, nicht behoben werden kann, können Probleme für die Clients des Mergemoduls auftreten. Verzeichnis Tabellenzeilen mit primär Schlüsseln, z. b. ProgramFilesFolder, sind häufig in einer Datenbank vorhanden. Wenn Komponenten in Ihrem Modul direkt in vordefinierten Verzeichnissen (z. b. ProgramFilesFolder) installiert werden, können die Verzeichniseinträge im Modul also mit bereits vorhandenen Zeilen kollidieren. Diese Bedingung erfordert, dass der Benutzer des Moduls die Quelldateien aus dem Modul aufteilen muss, damit es dem vorhandenen Quellverzeichnis entspricht.

## <a name="result"></a>Ergebnis

ICEM09 meldet einen Fehler oder eine Warnung, wenn eine Modul Komponente ein Verzeichnis in einem vordefinierten System Verzeichnis installiert, wodurch ein möglicher namens Konflikt mit der vorhandenen Verzeichnisstruktur verursacht wird.

## <a name="example"></a>Beispiel

ICEM09 veröffentlicht die folgenden Warnungen für ein Modul, das die angezeigten Datenbankeinträge enthält.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Benennen Sie das mergemodulverzeichnis um, sodass es nicht mit einer Windows Installer-Eigenschaft identisch ist und daher eindeutig ist. Legen Sie dann eine Eigenschaft mit demselben Namen auf den Wert des Windows Installer Verzeichnisses fest. Wenn die Verzeichnis Auflösung stattfindet, hat das Verzeichnis eine Eigenschaft mit demselben Namen, sodass der Installationsort des Verzeichnisses der Wert der Eigenschaft ist. Dateien werden vom unterschiedlichen Quell Speicherort an denselben Ziel Speicherort verschoben. Bei diesem Prozess sollten die Mergekonflikte vollständig entfernt werden.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Wenn die Aktion nicht die Sequenznummer 1 hat, wird Sie möglicherweise nicht früh genug in der Zieldatenbank zusammengeführt, um effektiv arbeiten zu können.

Legen Sie die Sequenznummer auf 1 fest, um diese Warnung zu beheben. Beachten Sie, dass die meisten aktuellen mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur mergezeit generieren, sodass es nicht immer notwendig ist, die Aktionen explizit im Mergemodul zu verfassen.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Da die CustomAction-Spalte der Primärschlüssel der CustomAction-Tabelle ist, können einige Merge-Tools doppelte Aktionen generieren, da der vordefinierte Aktionsname anders ist.

Um diese Warnung zu beheben, benennen Sie die Aktion mit dem Zielverzeichnis. Beachten Sie, dass die meisten aktuellen mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur mergezeit generieren, sodass es nicht immer notwendig ist, die Aktionen explizit im Mergemodul zu verfassen.

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis          | Über \_ geordnetes Verzeichnis | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| Startmenü Ordner    | Directory2        | b:c        |
| AppDataFolder      | Directory3        | D          |
| Mypicturesfolder   | Directory4        | E          |



 

[Komponenten Tabelle](component-table.md)



| Komponente               | Verzeichnis          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | Startmenü Ordner    |
| Component3.<GUID> | AppDataFolder      |
| Component4.<GUID> | Mypicturesfolder   |



 

[Tabelle "CustomAction"](customaction-table.md)



| CustomAction                 | type | `Source`                       | Ziel              |
|------------------------------|------|------------------------------|---------------------|
| Startmenü Folder.<GUID> | 51   | Startmenü Folder.<GUID> | \[Startmenü Ordner\] |
| Myappdatafolderaction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[Moduleinstallexecutesequence-Tabelle](moduleinstallexecutesequence-table.md)



| Aktion                       | Sequenz | Baseaction | Nach | Bedingung |
|------------------------------|----------|------------|-------|-----------|
| Startmenü Folder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



