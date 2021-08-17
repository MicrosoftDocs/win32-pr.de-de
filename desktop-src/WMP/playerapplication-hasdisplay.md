---
title: PlayerApplication.hasDisplay
description: Die hasDisplay-Eigenschaft ruft einen Wert ab, der angibt, ob das Video über das Remote-Player-Steuerelement angezeigt werden kann.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication.hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cffddc08c154ced6d7cb72b18642b5ebb4960e539e5682d1cf6e8518b74831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747359"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

Die **hasDisplay-Eigenschaft** ruft einen Wert ab, der angibt, ob das Video über das Remote-Player-Steuerelement angezeigt werden kann.

## <a name="syntax"></a>Syntax

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **schreibgeschützter boolescher** Wert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur beim Remoting des Windows Media Player-Steuerelements verwendet.

Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, video kann jedoch nur an einer Stelle gleichzeitig angezeigt werden, entweder im vollständigen Modus des Players oder in einem der Remote-Windows Media Player-Steuerelemente. Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das Steuerelement ist, über das Video angezeigt werden kann.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PlayerApplication-Objekt**](playerapplication-object.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





