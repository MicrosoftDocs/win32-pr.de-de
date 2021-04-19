---
title: Wiedergabemethode.
description: Die Methode "stiteminfo" gibt den Wert eines Wiedergabelisten Attributs an.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369302"
---
# <a name="playlistsetiteminfo-method"></a>Wiedergabemethode.

Die Methode " **stiteminfo** " gibt den Wert eines Wiedergabelisten Attributs an.

## <a name="syntax"></a>Syntax


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** mit dem Namen des festzulegenden Attributs. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den neuen Wert für das Attribut enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine besondere Verwendung der Methode "Methode" **ist das Sortieren** der Elemente in der Wiedergabeliste mithilfe des SortAttribute-Attributs. Im folgenden JScript-Beispiel wird eine Wiedergabeliste nach den Werten des userlastplayedtime-Attributs sortiert. Die Variablen Wiedergabeliste ist ein Verweis auf ein **Wiedergabe** Listen Objekt.


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](playlist-attributecount.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. getiteminfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





