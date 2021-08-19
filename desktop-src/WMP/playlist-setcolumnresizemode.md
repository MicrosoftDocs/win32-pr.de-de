---
title: PLAYLIST.setColumnResizeMode
description: Die setColumnResizeMode-Methode gibt an, wie sich die indizierte Spalte selbst formatiert.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST.setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335802"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST.setColumnResizeMode

Die **setColumnResizeMode-Methode** gibt an, wie die größe der indizierten Spalte selbst ist.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Spalte*
</dt> <dd>

**Zahl** (**long**), die den Index der zu ändernden Spalte angibt.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modus*
</dt> <dd>

**Eine Zeichenfolge,** die den Größenmodus angibt. Enthält einen der folgenden Werte.



| Wert          | Beschreibung                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutoizeHeader | Die Größe der Spalte wird so geändert, dass alle Daten sowohl in der Spalte als auch im Header berücksichtigt werden.                                  |
| AutoizeData   | Die Größe der Spalte wird so geändert, dass nur alle Daten in der Spalte berücksichtigt werden.                                                 |
| Fest          | Die Spalte ist eine feste Größe.                                                                                    |
| Erstreckt sich      | Die Größe der Spalte wird so geändert, dass der verbleibende Speicherplatz im **PLAYLIST-Element** verwendet wird, nachdem die Größe aller anderen Spalten geändert wurde. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> </dl>

 

 





