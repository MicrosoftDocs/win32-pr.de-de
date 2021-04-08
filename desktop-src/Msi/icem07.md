---
description: ICEM07 überprüft, ob die Reihenfolge der Dateien in der Sequenz Tabelle mit der Reihenfolge der Dateien in MergeModule.CABinet übereinstimmt.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865767"
---
# <a name="icem07"></a>ICEM07

ICEM07 überprüft, ob die Reihenfolge der Dateien in der Sequenz Tabelle mit der Reihenfolge der Dateien in [MergeModule.CABinet](mergemodule-cabinet.md)übereinstimmt.

Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb

## <a name="result"></a>Ergebnis

ICEM07 gibt einen Fehler aus, wenn die Reihenfolge der Dateien in der Dateitabelle nicht der Reihenfolge in der CAB-Datei entspricht.

## <a name="example"></a>Beispiel

IC0M07 würde die folgende Fehlermeldung für das gezeigte Beispiel veröffentlichen.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Dateitabelle](file-table.md)



| File          | Sequenz |
|---------------|----------|
| Die-Flea. *Guid1* | 1        |
| FileB. *Guid1* | 8        |
| Filec. *Guid1* | 52       |



 

Eingebettetes [MergeModule.CABinet](mergemodule-cabinet.md)



| File          |
|---------------|
| Die-Flea. *Guid1* |
| Filec. *Guid1* |
| Fassung. *Guid1* |
| FileB. *Guid1* |



 

Obwohl die Datei Sequenznummern in der Dateitabelle nicht aufeinander folgen müssen und zusätzliche Dateien in der CAB-Datei vorhanden sein können, muss die relative Sequenz aller Dateien in der Dateitabelle mit der Reihenfolge in [MergeModule.CABinet](mergemodule-cabinet.md)identisch sein. Um diesen Fehler zu beheben, ändern Sie die Sequenznummer von fileB nach filec, damit Sie der Datei Reihenfolge in der CAB-Datei entspricht, oder erstellen Sie das CAB mit den Dateien in der richtigen Reihenfolge neu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



