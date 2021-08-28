---
description: ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30542ead9a47ab5e92074227b1ae47fa6de0e643
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887392"
---
# <a name="icem09"></a>ICEM09

ICEM09 überprüft, ob das Mergemodul vordefinierte Verzeichnisse sicher verarbeitet. Hierzu wird überprüft, ob keine Komponente im Modul ein Verzeichnis in einem vordefinierten Systemverzeichnis wie "ProgramFilesFolder" oder "StartMenuFolder" installiert. Stattdessen sollten Module Verzeichnisse mit eindeutigen Namen verwenden (die mit der Benennungskonvention für Mergemodule erstellt wurden) und benutzerdefinierte Aktionen verwenden, um das entsprechende Zielverzeichnis als Ziel zu verwenden. Dieser Ansatz verhindert, dass Module mit einer vorhandenen Verzeichnisstruktur in der endgültigen Datenbank in Konflikt stehen. ICEM09 überprüft, ob die benutzerdefinierten Aktionen, die für diese Technik erforderlich sind, entweder nicht vorhanden sind (sodass sie vom Mergetool generiert werden können) oder in der richtigen Form vorhanden sind (damit sie erwartungsgemäß funktionieren).

Wenn eine von ICEM09 gemeldete Warnung oder ein Fehler nicht behoben werden kann, kann dies zu Problemen für die Clients Ihres Mergemoduls führen. Verzeichnistabellenzeilen mit Primärschlüsseln wie ProgramFilesFolder sind häufig in einer Datenbank vorhanden. Wenn Komponenten in Ihrem Modul direkt in vordefinierten Verzeichnissen wie ProgramFilesFolder installiert werden, können die Verzeichniseinträge im Modul daher mit bereits vorhandenen Zeilen kollidieren. Diese Bedingung würde erfordern, dass der Benutzer Ihres Moduls die Quelldateien aus Ihrem Modul aufteilt, damit sie mit dem vorhandenen Quellverzeichnis übereinstimmen.

## <a name="result"></a>Ergebnis

ICEM09 meldet einen Fehler oder eine Warnung, wenn eine Modulkomponente ein Verzeichnis in einem vordefinierten Systemverzeichnis installiert, was einen möglichen Namenskonflikt mit der vorhandenen Verzeichnisstruktur verursacht.

## <a name="example"></a>Beispiel

ICEM09 stellt die folgenden Warnungen für ein Modul mit den angezeigten Datenbankeinträgen zur Verfügung.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Benennen Sie das Mergemodulverzeichnis um, damit es nicht mit einer Windows Installer-Eigenschaft übereinstimmen und daher eindeutig ist. Legen Sie dann eine Eigenschaft mit demselben Namen auf den Wert des Windows Installer-Verzeichnisses fest. Wenn die Verzeichnisauflösung erfolgt, verfügt das Verzeichnis über eine Eigenschaft mit demselben Namen, sodass der Installationsspeicherort des Verzeichnisses der Wert der Eigenschaft ist. Dateien werden vom eindeutigen Quellspeicherort an denselben Zielspeicherort bewegt. Dieser Prozess sollte die Zusammenführungskonflikte vollständig entfernen.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Wenn die Aktion nicht die Sequenznummer 1 auf hat, wird sie möglicherweise nicht früh genug in der Sequenz mit der Zieldatenbank zusammengeführt, um effektiv zu funktionieren.

Um diese Warnung zu beheben, legen Sie die Sequenznummer auf 1 fest. Beachten Sie, dass die meisten aktuellen Mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur Mergezeit generieren, sodass es nicht immer erforderlich ist, die Aktionen explizit im Mergemodul zu erstellen.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Da die CustomAction-Spalte der Primärschlüssel der CustomAction-Tabelle ist, generieren einige Mergetools möglicherweise doppelte Aktionen, da der Name der vorab generierten Aktion anders ist.

Um diese Warnung zu beheben, benennen Sie die Aktion mit dem Zielverzeichnis. Beachten Sie, dass die meisten aktuellen Mergetools (aber nicht einige ältere Versionen) diese benutzerdefinierten Aktionen zur Zusammenführungszeit generieren, sodass es nicht immer erforderlich ist, die Aktionen explizit im Mergemodul zu erstellen.

[Verzeichnistabelle](directory-table.md)



| Verzeichnis          | Übergeordnetes \_ Verzeichnis | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Komponententabelle](component-table.md)



| Komponente               | Verzeichnis          |
|-------------------------|--------------------|
| Komponente1. &lt; GUID&gt; | ProgramFilesFolder |
| Komponente2. &lt; GUID&gt; | StartMenuFolder    |
| Komponente3. &lt; GUID&gt; | AppDataFolder      |
| Komponente 4. &lt; GUID&gt; | MyPicturesFolder   |



 

[CustomAction-Tabelle](customaction-table.md)



| CustomAction                 | Typ | `Source`                       | Ziel              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder. &lt; GUID&gt; | 51   | StartMenuFolder. &lt; GUID&gt; | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder. &lt; GUID&gt;   | \[AppDataFolder\]   |



 

[ModuleInstallExecuteSequence-Tabelle](moduleinstallexecutesequence-table.md)



| Aktion                       | Sequenz | BaseAction | Danach | Bedingung |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder. &lt; GUID&gt; | 100      |            |       |           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



