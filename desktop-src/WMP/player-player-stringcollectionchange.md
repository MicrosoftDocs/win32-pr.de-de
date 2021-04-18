---
title: Player. stringcollectionchange-Ereignis
description: Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert. | Player. stringcollectionchange-Ereignis
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Stringcollectionchange-Ereignisfenster Media Player
- Stringcollectionchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, stringcollectionchange-Ereignis
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
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357551"
---
# <a name="playerstringcollectionchange-event"></a>Player. stringcollectionchange-Ereignis

Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert.

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

*pdispstringcollection* 
</dt> <dd>

**StringCollection** -Objekt, das geändert wurde.

</dd> <dt>

*change* 
</dt> <dd>

Zahl (Long), die den Typ der Änderung angibt, die in der Zeichen folgen Auflistung aufgetreten ist. Enthält einen der folgenden Werte.



|        |                                    |
|--------|------------------------------------|
| Number | BESCHREIBUNG                        |
| 0      | Unbekannt (Kein gültiger Wert)       |
| 1      | Ein Element wurde eingefügt.              |
| 2      | Die Zeichen folgen Auflistung wurde geändert.     |
| 3      | Ein Element wurde gelöscht.               |
| 4      | Die Zeichen folgen Auflistung wurde gelöscht. |
| 5      | Massen Aktualisierungen werden gestartet.        |
| 6      | Massen Aktualisierungen wurden beendet.           |



 

</dd> <dt>

*lcollectionindex* 
</dt> <dd>

Zahl (Long), die den Index des geänderten Zeichen folgen-Sammel Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 





