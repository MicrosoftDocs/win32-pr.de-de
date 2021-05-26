---
title: Player.StringCollectionChange-Ereignis
description: Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert. | Player.StringCollectionChange-Ereignis
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- StringCollectionChange-Ereignis Windows Media Player
- StringCollectionChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , StringCollectionChange-Ereignis
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424090"
---
# <a name="playerstringcollectionchange-event"></a>Player.StringCollectionChange-Ereignis

Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert.

## <a name="syntax"></a>Syntax


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

**StringCollection-Objekt,** das geändert wurde.

</dd> <dt>

*change* 
</dt> <dd>

Zahl (long), die den Typ der Änderung angibt, die an der Zeichenfolgenauflistung vorgenommen wurde. Enthält einen der folgenden Werte.



| Number | BESCHREIBUNG                        |
|--------|------------------------------------|
| 0      | Unbekannt (Kein gültiger Wert)       |
| 1      | Ein Element wurde eingefügt.              |
| 2      | Die Zeichenfolgenauflistung wurde geändert.     |
| 3      | Ein Element wurde gelöscht.               |
| 4      | Die Zeichenfolgenauflistung wurde gelöscht. |
| 5      | Massenaktualisierungen beginnen.        |
| 6      | Massenupdates wurden beendet.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Zahl (long), die den Index des geänderten Zeichenfolgensammlungselements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





