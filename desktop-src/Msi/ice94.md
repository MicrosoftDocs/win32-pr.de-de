---
description: ICE94 überprüft die Verknüpfungs Tabelle, die Featuretabelle und die MsiAssembly-Tabelle und gibt eine Warnung aus, wenn nicht angekündigte Verknüpfungen vorhanden sind, die auf eine Assemblydatei im globalen Assemblycache verweisen.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217651"
---
# <a name="ice94"></a>ICE94

ICE94 überprüft die Verknüpfungs [Tabelle](shortcut-table.md), die [Featuretabelle](feature-table.md)und die [MsiAssembly-Tabelle](msiassembly-table.md) und gibt eine Warnung aus, wenn nicht angekündigte Verknüpfungen vorhanden sind, die auf eine Assemblydatei im globalen Assemblycache verweisen. Wenn der Eintrag im Feld Ziel der Verknüpfungs Tabelle kein Feature in der Featuretabelle ist, wird die Verknüpfung nicht angekündigt. Wenn der Eintrag im Feld Komponente \_ der Verknüpfungs Tabelle auch in der Tabelle MsiAssembly aufgeführt ist, verweist die Verknüpfung auf eine Assemblydatei. Wenn der Eintrag im Feld "Datei \_ Anwendung" in der Tabelle "MsiAssembly" leer ist, befindet sich die Assemblydatei im globalen Assemblycache.

## <a name="result"></a>Ergebnis

ICE94 gibt die folgende Warnung aus.



| ICE94-Warnung                                                                                | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Die nicht angekündigte Verknüpfung ' \[ 2 \] ' verweist auf eine Assemblydatei im globalen Assemblycache. | Eine nicht angekündigte Verknüpfung verweist auf eine Assemblydatei im globalen Assemblycache. |



 

## <a name="example"></a>Beispiel

ICE94 meldet den folgenden Fehler für das Beispiel:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Komponente\_ | Ziel    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | Feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion  |
|----------|
| Feature1 |



 

[MsiAssembly-Tabelle](msiassembly-table.md) (partiell)



| Komponente\_ | Datei \_ Anwendung |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



