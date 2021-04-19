---
title: Wiedergabe. InsertItem-Methode
description: Die InsertItem-Methode fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- InsertItem-Methode, Windows-Media Player
- InsertItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, InsertItem-Methode
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367450"
---
# <a name="playlistinsertitem-method"></a>Wiedergabe. InsertItem-Methode

Die **InsertItem** -Methode fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.

## <a name="syntax"></a>Syntax


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index enthält, an dem das Element hinzugefügt werden soll.

</dd> <dt>

*Element* \[ in\]
</dt> <dd>

**Medien** Objekt, das eingefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Elemente nach dem eingefügten Element werden die Indexnummern um 1 erhöhen.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. Element**](playlist-item.md)
</dt> <dt>

[**Wiedergabeliste. RemoveItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





