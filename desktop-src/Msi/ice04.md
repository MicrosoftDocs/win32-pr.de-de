---
description: ICE04 überprüft, ob die Sequenznummer jeder Datei in der Tabelle Datei kleiner oder gleich der größten Sequenznummer in der LastSequence -Spalte der Media-Tabelle ist.
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

ICE04 überprüft, ob die Sequenznummer jeder Datei in der [Tabelle Datei](file-table.md) kleiner oder gleich der größten Sequenznummer in der LastSequence -Spalte der [Media-Tabelle ist.](media-table.md)

Jeder Datensatz in der Media-Tabelle stellt einen Datenträger auf dem Quellmedium dar, der alle Dateien mit einer Sequenznummer enthält, die kleiner oder gleich dem Wert in der LastSequence -Spalte und größer als der LastSequence-Wert im Datensatz des vorherigen Datenträgers ist.

## <a name="result"></a>Ergebnis

ICE04 gibt eine Fehlermeldung aus, wenn eine Datei mit einer Sequenznummer größer als die größte LastSequence-Nummer für das Quellmedium ist.

## <a name="example"></a>Beispiel

ICE04 würde den folgenden Fehler für das gezeigte Beispiel melden:

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

 

 



