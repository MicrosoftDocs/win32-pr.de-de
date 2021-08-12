---
title: Player.StringCollectionChange-Ereignis
description: Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgensammlung ändert. | Player.StringCollectionChange-Ereignis
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- StringCollectionChange-Windows Media Player
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
ms.openlocfilehash: 5012cd94c14532eb94eb452c9c7aa20d50ffb8a447c2d14f56e8c6df02456849
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572418"
---
# <a name="playerstringcollectionchange-event"></a>Player.StringCollectionChange-Ereignis

Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgensammlung ändert.

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

Zahl (long) gibt den Typ der Änderung an, die an der Zeichenfolgensammlung aufgetreten ist. Schließt einen der folgenden Werte ein.



| Number | BESCHREIBUNG                        |
|--------|------------------------------------|
| 0      | Unbekannt (Kein gültiger Wert)       |
| 1      | Ein Element wurde eingefügt.              |
| 2      | Die Zeichenfolgensammlung wurde geändert.     |
| 3      | Ein Element wurde gelöscht.               |
| 4      | Die Zeichenfolgensammlung wurde löschen. |
| 5      | Massenaktualisierungen beginnen.        |
| 6      | Massenaktualisierungen wurden beendet.           |



 

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

 

 





