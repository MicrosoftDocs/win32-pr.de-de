---
title: Media. isidentical-Methode
description: Die isidentical-Methode ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist. | Media. isidentical-Methode
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, isidentical-Methode
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358603"
---
# <a name="mediaisidentical-method"></a>Media. isidentical-Methode

Die **isidentical** -Methode ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Medien* \[ in\]
</dt> <dd>

**Medien** Objekt, das mit dem aktuellen **Medien** Objekt verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **isidentical** , um zu überprüfen, ob ein Medien Element mit dem Namen newmedia mit dem aktuellen Medien Element identisch ist. Wenn Sie nicht identisch sind, wird das neue Medien Element wiedergegeben. Andernfalls wird das aktuelle Medium weiterhin ununterbrochen abgespielt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 





