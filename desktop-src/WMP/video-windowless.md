---
title: VIDEO.windowless
description: Das fensterlose Attribut gibt einen Wert an, der angibt, ob das Video-Steuerelement fensterlos oder fensterlos ist, oder ruft einen Wert ab. Das heißt, ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder abgeschnitten werden kann.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO.windowless Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98aefde5aab9837f220ccb7df254e6a592e0d5e9d41de43291b2ab73e287321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931740"
---
# <a name="videowindowless"></a>VIDEO.windowless

Das **fensterlose** Attribut gibt einen Wert an, der angibt, ob das Video-Steuerelement fensterlos oder fensterlos ist, oder ruft einen Wert ab. Das heißt, ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher Wert,** der zur Entwurfszeit angegeben und danach schreibgeschützt ist.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| true  | Das Videosteuerelement ist fensterlos.        |
| false | Standard. Das Videosteuerelement wird eingeblendet. |



 

## <a name="remarks"></a>Hinweise

Wenn ein nicht rechteckiges Videofenster gewünscht ist oder Sie einen Teil des Videofensters mit einem Bild abdecken möchten, muss dieses Attribut auf TRUE festgelegt werden. Dadurch wird die Leistung für die erforderlichen Ausschneidefunktionen geerkt.

Die Videowiedergabe ist für die nicht angepasste Wiedergabe optimiert. In diesem Fall wird das **Attribut ohne Fenster** auf FALSE festgelegt, und das gesamte Videorechteck wird immer angezeigt. Alle Bilder, die das Videofenster abdecken, werden ignoriert, und das Videofenster weist die höchste Z-Reihenfolge auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VIDEO-Element**](video-element.md)
</dt> </dl>

 

 





