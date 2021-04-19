---
title: Video. Windows less
description: Mit dem Fenster "Windows less" wird ein Wert angegeben oder abgerufen, der angibt, ob das Video Steuerelement Fenster-oder fensterlose Fenster enthält. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- Video. fensterlose Windows-Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370706"
---
# <a name="videowindowless"></a>Video. Windows less

Mit dem **Fenster "Windows less** " wird ein Wert angegeben oder abgerufen, der angibt, ob das Video Steuerelement Fenster-oder fensterlose Fenster enthält. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird, und anschließend schreibgeschützt.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| true  | Das Video Steuerelement ist fensterloser.        |
| false | Standard. Das Video Steuerelement wird angezeigt. |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein nicht rechteckiges Videofenster gewünscht ist oder wenn Sie einen Teil des Videofensters mit einem Bild abdecken möchten, muss dieses Attribut auf true festgelegt werden. Dadurch wird eine gewisse Leistung erzielt, um das erforderliche Clipping durchzuführen.

Die Video Wiedergabe ist für die nicht geklickte Wiedergabe optimiert. In diesem Fall wird das **fensterlose** Attribut auf false festgelegt, und das gesamte Video Rechteck wird immer angezeigt. Alle Bilder, die das Videofenster abdecken, werden ignoriert, und das Videofenster hat die oberste z-Reihenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video-Element**](video-element.md)
</dt> </dl>

 

 





