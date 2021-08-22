---
title: Media.isIdentical-Methode
description: Die isIdentical-Methode ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen identisch ist. | Media.isIdentical-Methode
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- isIdentical-Windows Media Player
- isIdentical-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , isIdentical-Methode
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
ms.openlocfilehash: 5147d6ccc72d570709ef6ad898bf52872909dc5e3800d9cc671c774510b45d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054638"
---
# <a name="mediaisidentical-method"></a>Media.isIdentical-Methode

Die **isIdentical-Methode** ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen identisch ist.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Medien* \[ In\]
</dt> <dd>

**Medienobjekt,** das mit dem aktuellen **Media-Objekt verglichen werden** soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **isIdentical,** um zu überprüfen, ob ein Medienelement mit dem Namen newMedia mit dem aktuellen Medienelement identisch ist. Wenn sie nicht identisch sind, wird das neue Medienelement abgespielt. Andernfalls wird das aktuelle Medium weiterhin unterbrechungsfrei abspielt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> </dl>

 

 





