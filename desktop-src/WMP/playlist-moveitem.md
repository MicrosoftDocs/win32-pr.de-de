---
title: Playlist. muveitem-Methode
description: Die Methode "muveitem" ändert den Speicherort eines Elements in der Wiedergabeliste.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Windows-Media Player für die Windows-
- muveitem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Methode "muveitem"
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354776"
---
# <a name="playlistmoveitem-method"></a>Playlist. muveitem-Methode

Die Methode " **muveitem** " ändert den Speicherort eines Elements in der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldIndex* \[ in\]
</dt> <dd>

Die **Zahl** (**Long**), die den alten Index enthält.

</dd> <dt>

" *nwindex* \[ " in\]
</dt> <dd>

**Zahl** (**Long**), die den neuen Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In der Bibliothek gespeicherte Wiedergabelisten können sich außerhalb des Steuer Elements ändern. Achten Sie darauf, alle entsprechenden Wiedergabelisten bezogenen Ereignisse zu überwachen und zu verarbeiten, sodass die Reihenfolge der Elemente in der Wiedergabeliste nicht unerwartet geändert wird.

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

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





