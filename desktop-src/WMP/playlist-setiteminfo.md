---
title: Playlist.setItemInfo-Methode
description: Die setItemInfo-Methode gibt den Wert eines Wiedergabelistenattributs an.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- setItemInfo-Methode Windows Media Player
- setItemInfo-Methode Windows Media Player , Playlist-Klasse
- Playlist-Klasse Windows Media Player , setItemInfo-Methode
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
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335747"
---
# <a name="playlistsetiteminfo-method"></a>Playlist.setItemInfo-Methode

Die **setItemInfo-Methode** gibt den Wert eines Wiedergabelistenattributs an.

## <a name="syntax"></a>Syntax


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des festzulegenden Attributs enthält. Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie im Windows Media Player [Attributverweis.](attribute-reference.md)

</dd> <dt>

*wert* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den neuen Wert für das Attribut enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine besondere Verwendung der **setItemInfo-Methode** besteht darin, die Elemente in der Wiedergabeliste mithilfe des SortAttribute-Attributs zu sortieren. Im folgenden JScript Beispiel wird eine Wiedergabeliste nach den Werten des UserLastPlayedTime-Attributs sortiert. Die Variablenwiedergabeliste ist ein Verweis auf ein **Wiedergabelistenobjekt.**


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Beispielcode, der diese Eigenschaft verwendet, finden Sie in der [attributeCount-Eigenschaft.](playlist-attributecount.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





