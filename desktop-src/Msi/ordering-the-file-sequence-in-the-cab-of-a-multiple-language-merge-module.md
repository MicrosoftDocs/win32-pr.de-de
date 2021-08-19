---
description: Mergemodule für mehrere Sprachen, Sprachtransformationen und Schränkdateien müssen so verfasst werden, dass die Reihenfolge der Dateien der in der Tabelle Datei angegebenen Reihenfolge entspricht.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Reihenfolge der Dateisequenz in der CAB-Datei eines Mergemoduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942807"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Reihenfolge der Dateisequenz in der CAB-Datei eines Mergemoduls mit mehreren Sprachen

Mergemodule für mehrere Sprachen, Sprachtransformationen und Schränkdateien müssen so verfasst werden, dass die Reihenfolge der Dateien in der .cab der Installations reihenfolge der in der Dateitabelle angegebenen Dateien [entspricht,](file-table.md)auch nach der Anwendung der Sprachtransformation. Wenn die Reihenfolge im Modul und im .cab nicht übereinstimmen, kann das Mergemodul nicht verwendet werden.

Weisen Sie jeder Datei im Modul eine eindeutige Sequenznummer zu, die unabhängig von ihrer Sprache ist, und verwenden Sie diese Sequenznummer dann immer für die Datei. Verwenden Sie dieselbe Sequenz, wenn Sie die Schränkdatei erstellen und eine Sprachtransformation erstellen.

Da das Installationsprogramm nur die in der Dateitabelle aufgeführten Dateien [installiert,](file-table.md)ermöglicht die Verwendung einer globalen Dateisequenz in der Schränkungs-, Dateitabellen- und Sprachtransformation dem Mergetool das Überspringen zusätzlicher Dateien, die im Schränk gespeichert sind und nicht in der Dateitabelle aufgeführt [sind.](file-table.md) [](file-table.md) Andere Dateien sind möglicherweise in der Schränkung vorhanden, dürfen aber nicht in der [Dateitabelle aufgeführt werden.](file-table.md) Beispielsweise kann ein Modul, das Code.dll, English.dat, German.dat und French.dat installiert, die folgende globale Dateisequenzreihenfolge verwenden.



| Datei        | Sequenz |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |
| German.Dat  | 3        |
| French.Dat  | 4        |



 

Sprachtransformationen können dann zum Ändern der [Dateitabelle](file-table.md) des Moduls für Englisch, Deutsch oder Französisch verfasst werden.

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



 

[Dateitabelle](file-table.md) (partiell für Französisch)



| Datei       | Sequenz |
|------------|----------|
| Code.Dll   | 1        |
| French.Dat | 4        |



 

Weitere Informationen finden Sie unter [Erstellen einer Sprachtransformation für ein](authoring-a-language-transform-for-a-multiple-language-merge-module.md) Mergemodul mit mehreren Sprachen und Erstellen von [Mergemodul-Dateitabellen.](authoring-merge-module-file-tables.md)

 

 



