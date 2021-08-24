---
description: ICE94 überprüft die Tabelle "Shortcut", "Featuretabelle" und "MsiAssembly" und gibt eine Warnung aus, wenn es nichtvertierte Verknüpfungen gibt, die auf eine Assemblydatei im globalen Assemblycache verweisen.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd203fe35b6bedc7d36f3e5a5c18fc6a235d3e65924b41909803e67ab79337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894890"
---
# <a name="ice94"></a>ICE94

ICE94 überprüft die Tabelle ["Shortcut",](shortcut-table.md) ["Featuretabelle"](feature-table.md)und ["MsiAssembly"](msiassembly-table.md) und gibt eine Warnung aus, wenn es nichtvertierte Verknüpfungen gibt, die auf eine Assemblydatei im globalen Assemblycache verweisen. Wenn der Eintrag im Feld Ziel der Verknüpfungstabelle kein Feature in der Featuretabelle ist, wird die Verknüpfung nicht rückgängig machen. Wenn der Eintrag im Feld Komponente der Verknüpfungstabelle auch in der Tabelle MsiAssembly aufgeführt ist, zeigt die Verknüpfung \_ auf eine Assemblydatei. Wenn der Eintrag im Feld \_ Dateianwendung in der MsiAssembly-Tabelle leer ist, befindet sich die Assemblydatei im globalen Assemblycache.

## <a name="result"></a>Ergebnis

ICE94 gibt die folgende Warnung aus.



| ICE94-Warnung                                                                                | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Die nicht angekündigte Verknüpfung \[ "2" \] verweist auf eine Assemblydatei im globalen Assemblycache. | Eine nichtvertierte Verknüpfung ist ein Zeiger auf eine Assemblydatei im globalen Assemblycache. |



 

## <a name="example"></a>Beispiel

ICE94 meldet den folgenden Fehler für das Beispiel:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Komponente\_ | Ziel    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Featuretabelle](feature-table.md) (partiell)



| Komponente  |
|----------|
| feature1 |



 

[MsiAssembly-Tabelle](msiassembly-table.md) (partiell)



| Komponente\_ | \_Dateianwendung |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



