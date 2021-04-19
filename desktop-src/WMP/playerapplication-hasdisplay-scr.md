---
title: Playerapplication. hasdisplay-Attribut
description: Das hasdisplay-Attribut Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Playerapplication. hasdisplay-Windows-Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372335"
---
# <a name="playerapplicationhasdisplay"></a>Playerapplication. hasdisplay

Das **hasdisplay** -Attribut Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Schreib geschützter **boolescher** Wert.



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| True  | Das Video kann angezeigt werden.    |
| False | Das Video kann nicht angezeigt werden. |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird nur verwendet, wenn das Windows Media Player-Steuerelement Remoting ist.

Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, aber Video kann nur jeweils an einer Stelle angezeigt werden, entweder im vollständigen Modus des Players oder in einem der Remote Steuerelemente. Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das aktuelle Steuerelement ist, durch das Video angezeigt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playerapplication-Element**](playerapplication-element.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





