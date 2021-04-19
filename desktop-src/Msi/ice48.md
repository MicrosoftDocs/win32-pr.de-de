---
description: ICE48 sucht nach Verzeichnissen, die auf lokale Pfade in der Eigenschaften Tabelle hart codiert sind.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363562"
---
# <a name="ice48"></a>ICE48

ICE48 sucht nach Verzeichnissen, die auf lokale Pfade in der [Eigenschaften Tabelle](property-table.md)hart codiert sind.

Verwenden Sie keine hart Codierung von Verzeichnis Pfaden zu lokalen Laufwerken, da sich die Computer in der Einrichtung des lokalen Laufwerks unterscheiden. Diese Vorgehensweise ist möglicherweise akzeptabel, wenn eine Anwendung auf einer großen Anzahl von Computern bereitgestellt wird, auf denen die relevanten Teile der Laufwerke identisch sind.

## <a name="result"></a>Ergebnis

ICE48 gibt eine Fehlermeldung aus, wenn ein Verzeichnis vorhanden ist, das in einem lokalen Pfad in der Eigenschaften Tabelle hart codiert ist.

## <a name="example"></a>Beispiel

ICE48 würde die folgende Warnung für das gezeigte Beispiel melden.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Verzeichnis Tabelle](directory-table.md) (partiell)



| Verzeichnis | Über \_ geordnetes Verzeichnis | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Eigenschaften Tabelle](property-table.md) (partiell)



| Eigenschaft | Wert      |
|----------|------------|
| Dir1     | d: \\ Quelle |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



