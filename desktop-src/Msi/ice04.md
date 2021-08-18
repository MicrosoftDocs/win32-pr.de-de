---
description: ICE04 überprüft, ob die Sequenznummer jeder Datei in der Dateitabelle kleiner oder gleich der größten Sequenznummer in der Spalte LastSequence der Tabelle Media ist.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635662"
---
# <a name="ice04"></a>ICE04

ICE04 überprüft, ob die Sequenznummer jeder Datei in der [Dateitabelle](file-table.md) kleiner oder gleich der größten Sequenznummer in der LastSequence-Spalte der [Medientabelle](media-table.md)ist.

Jeder Datensatz in der Tabelle Media stellt einen Datenträger auf dem Quellmedium dar, der alle Dateien enthält, deren Sequenznummer kleiner oder gleich dem Wert in der Spalte LastSequence und größer als der LastSequence-Wert im Datensatz des vorherigen Datenträgers ist.

## <a name="result"></a>Ergebnis

ICE04 sendet eine Fehlermeldung, wenn eine Datei mit einer Sequenznummer vorhanden ist, die größer als die größte LastSequence-Nummer für das Quellmedium ist.

## <a name="example"></a>Beispiel

ICE04 meldet den folgenden Fehler für das gezeigte Beispiel:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Dateitabelle](file-table.md) (partiell)



| Datei   | Sequenz |
|--------|----------|
| Myfile | 210      |



 

[Medientabelle](media-table.md) (partiell)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



