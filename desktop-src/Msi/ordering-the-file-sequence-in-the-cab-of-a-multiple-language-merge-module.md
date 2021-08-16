---
description: Mergemodule, Sprachtransformationen und Cab-Dateien mit mehreren Sprachen müssen so erstellt werden, dass die Reihenfolge der Dateien mit der in der Dateitabelle angegebenen Reihenfolge übereinstimmt.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Sortieren der Dateisequenz im CAB eines Mergemoduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942807"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Sortieren der Dateisequenz im CAB eines Mergemoduls mit mehreren Sprachen

Mergemodule, Sprachtransformationen und Cab-Dateien in mehreren Sprachen müssen so erstellt werden, dass die Reihenfolge der Dateien im .cab mit der Installationsreihenfolge der in der [Dateitabelle](file-table.md)angegebenen Dateien übereinstimmt, auch nach der Anwendung der Sprachtransformation. Wenn die Reihenfolge im Modul und im .cab nicht übereinstimmt, kann das Mergemodul nicht verwendet werden.

Weisen Sie jeder Datei im Modul eine eindeutige Sequenznummer zu, die unabhängig von ihrer Sprache ist, und verwenden Sie dann immer diese Sequenznummer für die Datei. Verwenden Sie dieselbe Sequenz, wenn Sie die Cab-Datei erstellen und eine Sprachtransformation erstellen.

Da das Installationsprogramm nur die in der [Dateitabelle](file-table.md)aufgeführten Dateien installiert, ermöglicht die Verwendung einer globalen Dateisequenz im Cab, [dateitabellen](file-table.md)und sprachtransformation dem Mergetool das Überspringen aller zusätzlichen Dateien, die im Schränk gespeichert sind, die nicht in der [Dateitabelle](file-table.md)aufgeführt sind. Andere Dateien sind möglicherweise im Cab vorhanden, dürfen aber nicht in der [Dateitabelle](file-table.md)aufgeführt werden. Beispielsweise kann ein Modul, das Code.dll, English.dat, German.dat und French.dat installiert, die folgende globale Dateisequenzreihenfolge verwenden.



| Datei        | Sequenz |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |
| German.Dat  | 3        |
| French.Dat  | 4        |



 

Sprachtransformationen können dann erstellt werden, um die [Dateitabelle](file-table.md) des Moduls für Englisch, Deutsch oder Französisch zu ändern.

[Dateitabelle](file-table.md) (teilweise für Englisch)



| Datei        | Sequenz |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |



 

[Dateitabelle](file-table.md) (teilweise für Deutsch)



| Datei       | Sequenz |
|------------|----------|
| Code.Dll   | 1        |
| German.Dat | 3        |



 

[Dateitabelle](file-table.md) (teilweise für Französisch)



| Datei       | Sequenz |
|------------|----------|
| Code.Dll   | 1        |
| French.Dat | 4        |



 

Weitere Informationen finden Sie unter [Authoring a Language Transform for a Multiple Language Merge Module (Erstellen einer Sprachtransformation für ein Mergemodul mit mehreren Sprachen)](authoring-a-language-transform-for-a-multiple-language-merge-module.md) und [Authoring Merge Module File Tables (Erstellen von Mergemoduldateitabellen).](authoring-merge-module-file-tables.md)

 

 



