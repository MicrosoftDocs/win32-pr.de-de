---
title: Playlistarray. Item-Methode
description: Die Item-Methode ruft die Wiedergabeliste am angegebenen Index ab.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- Element-Methoden Fenster Media Player
- Item-Methode, Windows Media Player, playlistarray-Klasse
- Playlistarray-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360931"
---
# <a name="playlistarrayitem-method"></a>Playlistarray. Item-Methode

Die **Item** -Methode ruft die Wiedergabeliste am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index der abzurufenden Wiedergabeliste enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playlistarray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





