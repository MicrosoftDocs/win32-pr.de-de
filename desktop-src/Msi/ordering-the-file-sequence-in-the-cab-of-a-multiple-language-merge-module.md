---
description: Mergemodule, sprach Transformationen und CAB-Dateien mit mehreren Sprachen müssen so verfasst werden, dass die Reihenfolge der Dateien mit der in der Dateitabelle angegebenen Reihenfolge übereinstimmt.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Anordnen der Datei Sequenz im CAB eines Moduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218529"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Anordnen der Datei Sequenz im CAB eines Moduls mit mehreren Sprachen

Mergemodule, sprach Transformationen und CAB-Dateien mit mehreren Sprachen müssen so verfasst werden, dass die Reihenfolge der Dateien in der CAB-Datei mit der Installations Reihenfolge der in der [Dateitabelle](file-table.md)angegebenen Dateien übereinstimmt, auch nach der Anwendung der sprach Transformation. Wenn die Reihenfolge im Modul und im CAB nicht stimmt, kann das Mergemodul nicht verwendet werden.

Weisen Sie jeder Datei im Modul eine eindeutige Sequenznummer zu, die unabhängig von Ihrer Sprache ist, und verwenden Sie dann immer diese Sequenznummer für die Datei. Verwenden Sie dieselbe Sequenz, wenn Sie die CAB-Datei erstellen und eine sprach Transformation erstellen.

Da das Installationsprogramm nur die Dateien installiert, die in der [Dateitabelle](file-table.md)aufgeführt sind, ermöglicht die Verwendung einer globalen Datei Sequenz in CAB, [File Table](file-table.md)und Language Transform dem Merge-Tool das Überspringen zusätzlicher Dateien, die in der CAB-Datei gespeichert sind, die nicht in der [Dateitabelle](file-table.md)aufgeführt sind. Möglicherweise sind andere Dateien in der CAB-Datei vorhanden, Sie dürfen jedoch nicht in der [Dateitabelle](file-table.md)aufgeführt werden. Ein Modul, das Code.dll, English. dat, Deutsch. dat und Französisch. dat installiert, kann beispielsweise die folgende globale Datei Sequenz Reihenfolge verwenden.



| File        | Sequenz |
|-------------|----------|
| Code.Dll    | 1        |
| Englisch. dat | 2        |
| Deutsch. dat  | 3        |
| Französisch. dat  | 4        |



 

Sprach Transformationen können dann erstellt werden, um die [Dateitabelle](file-table.md) des Moduls für Englisch, Deutsch oder Französisch zu ändern.

[Dateitabelle](file-table.md) (partiell für Englisch)



| File        | Sequenz |
|-------------|----------|
| Code.Dll    | 1        |
| Englisch. dat | 2        |



 

[Dateitabelle](file-table.md) (partiell für Deutsch)



| File       | Sequenz |
|------------|----------|
| Code.Dll   | 1        |
| Deutsch. dat | 3        |



 

[Dateitabelle](file-table.md) (teilweise für Französisch)



| File       | Sequenz |
|------------|----------|
| Code.Dll   | 1        |
| Französisch. dat | 4        |



 

Weitere Informationen finden Sie unter [Erstellen einer sprach Transformation für ein Mergemodul mehrerer Sprachen](authoring-a-language-transform-for-a-multiple-language-merge-module.md) und [Erstellen von Mergemodul-Datei Tabellen](authoring-merge-module-file-tables.md).

 

 



