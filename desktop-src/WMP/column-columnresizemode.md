---
title: COLUMN.columnResizeMode
description: Das columnResizeMode-Attribut gibt den Größenänderungsmodus für diese Spalte an oder ruft diesen ab.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN.columnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764000"
---
# <a name="columncolumnresizemode"></a>COLUMN.columnResizeMode

Das **columnResizeMode-Attribut** gibt den Größenänderungsmodus für diese Spalte an oder ruft diesen ab.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die einen der folgenden Werte enthält.



| Wert          | Beschreibung                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Standard. Die Spaltengröße wird so angepasst, dass alle Daten in der Spalte und der Kopfzeile berücksichtigt werden.                         |
| AutoizeData   | Die Spaltengröße wird so angepasst, dass nur alle Daten in der Spalte berücksichtigt werden.                                                 |
| Fest          | Die Spalte ist eine feste Größe.                                                                                    |
| Erstreckt sich      | Die Spaltengröße wird so geändert, dass der verbleibende Platz im **PLAYLIST-Steuerelement** verwendet wird, nachdem die Größe aller anderen Spalten geändert wurde. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COLUMN-Element**](column-element.md)
</dt> </dl>

 

 





