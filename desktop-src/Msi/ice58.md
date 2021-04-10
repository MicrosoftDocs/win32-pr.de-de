---
description: ICE58 prüft, ob die Medien Tabelle nicht mehr als 80 Zeilen enthält.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960347"
---
# <a name="ice58"></a>ICE58

ICE58 prüft, ob die [Medien Tabelle](media-table.md) nicht mehr als 80 Zeilen enthält.

## <a name="result"></a>Ergebnis

Von ICE58 gemeldete Warnungen bewirken, dass die Installation fehlschlägt, es sei denn, das Paket wird mit Windows Installer 2,0 oder höher installiert. Ab Windows Installer 2,0 wird die Beschränkung auf mehr als 80 Medien Tabelleneinträge entfernt. Es wird keine Warnung ausgegeben, wenn die [**Zusammenfassungs**](page-count-summary.md) Eigenschaft für die Seitenzählung des Pakets größer oder gleich 150 ist. Pakete des Schemas 200 oder höher können nur von Windows Installer 2,0 oder höher installiert werden.

## <a name="example"></a>Beispiel

ICE58 meldet die folgenden Fehler und Warnungen für das gezeigte Beispiel.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Um diesen Fehler zu beheben, entfernen Sie nicht verwendete Medien Tabelleneinträge, konsolidieren Sie Medien Tabelleneinträge, die auf die gleichen Medien verweisen, und packen Sie die Anwendung neu, um das erforderliche Medium zu verringern.

[Medien Tabelle](media-table.md) (partiell)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



