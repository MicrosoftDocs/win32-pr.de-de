---
description: ICE04 überprüft, ob die Sequenznummer jeder Datei in der Dateitabelle kleiner oder gleich der größten Sequenznummer in der LastSequence-Spalte der Medien Tabelle ist.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960045"
---
# <a name="ice04"></a>ICE04

ICE04 überprüft, ob die Sequenznummer jeder Datei in der [Dateitabelle](file-table.md) kleiner oder gleich der größten Sequenznummer in der LastSequence-Spalte der [Medien Tabelle](media-table.md)ist.

Jeder Datensatz in der Medien Tabelle stellt einen Datenträger auf dem Quell Medium dar, der alle Dateien mit einer Sequenznummer enthält, die kleiner oder gleich dem Wert in der Spalte LastSequence ist, und größer als der LastSequence-Wert im Datensatz des vorangehenden Datenträgers.

## <a name="result"></a>Ergebnis

ICE04 gibt eine Fehlermeldung aus, wenn eine Datei mit einer Sequenznummer größer als die größte Last Sequenznummer für das Quell Medium ist.

## <a name="example"></a>Beispiel

ICE04 würde den folgenden Fehler für das gezeigte Beispiel melden:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Dateitabelle](file-table.md) (partiell)



| File   | Sequenz |
|--------|----------|
| MyFile | 210      |



 

[Medien Tabelle](media-table.md) (partiell)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



