---
title: PLAYERAPPLICATION.hasDisplay-Attribut
description: Das hasDisplay-Attribut ruft einen Wert ab, der angibt, ob das Video über das Remotesteuerelement Windows Media Player angezeigt werden kann.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION.hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571943"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

Das **hasDisplay-Attribut** ruft einen Wert ab, der angibt, ob das Video über das Remotesteuerelement Windows Media Player angezeigt werden kann.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein schreibgeschützter **boolescher** Wert.



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| True  | Das Video kann angezeigt werden.    |
| Falsch | Das Video kann nicht angezeigt werden. |



 

## <a name="remarks"></a>Hinweise

Dieses Attribut wird nur beim Remoting des Windows Media Player-Steuerelements verwendet.

Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, video kann jedoch nur an einer Stelle gleichzeitig angezeigt werden, entweder im vollständigen Modus des Players oder in einem der Remotesteuerelemente. Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das Steuerelement ist, über das Video angezeigt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYERAPPLICATION-Element**](playerapplication-element.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





