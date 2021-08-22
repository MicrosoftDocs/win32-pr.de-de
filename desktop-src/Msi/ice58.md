---
description: ICE58 überprüft, ob ihre Media-Tabelle nicht mehr als 80 Zeilen enthält.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528230"
---
# <a name="ice58"></a>ICE58

ICE58 überprüft, ob Ihre [Media-Tabelle](media-table.md) nicht mehr als 80 Zeilen enthält.

## <a name="result"></a>Ergebnis

Warnungen, die von ICE58 gemeldet werden, führen dazu, dass die Installation fehlschlägt, es sei denn, das Paket wird mit Windows Installer 2.0 oder höher installiert. Ab Windows Installer 2.0 wird die Einschränkung auf mehr als 80 Medientabelleneinträge entfernt. Es wird keine Warnung ausgegeben, wenn die [**Page Count Summary-Eigenschaft**](page-count-summary.md) des Pakets größer oder gleich 150 ist. Pakete mit Schema 200 oder höher können nur von Windows Installer 2.0 oder höher installiert werden.

## <a name="example"></a>Beispiel

ICE58 meldet die folgenden Fehler und Warnungen für das gezeigte Beispiel.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Um diesen Fehler zu beheben, entfernen Sie alle nicht verwendeten Medientabelleneinträge, konsolidieren Sie Medientabelleneinträge, die auf dasselbe Medium verweisen, und packen Sie Ihre Anwendung neu, um die erforderlichen Medien zu reduzieren.

[Medientabelle](media-table.md) (partiell)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



