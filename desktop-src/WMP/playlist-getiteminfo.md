---
title: Wiedergabe. getiteminfo-Methode
description: Die getiteminfo-Methode ruft den Wert eines Wiedergabelisten Attributs ab.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369944"
---
# <a name="playlistgetiteminfo-method"></a>Wiedergabe. getiteminfo-Methode

Die **getiteminfo** -Methode ruft den Wert eines Wiedergabelisten Attributs ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des abzurufenden Attributs enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

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

[**Wiedergabeliste. Einstellungs Element**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





