---
title: Playerapplication. hasdisplay
description: Die hasdisplay-Eigenschaft ruft einen Wert ab, der angibt, ob Videos über das Remote Player-Steuerelement angezeigt werden können.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Playerapplication. hasdisplay-Windows-Media Player
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
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358353"
---
# <a name="playerapplicationhasdisplay"></a>Playerapplication. hasdisplay

Die **hasdisplay** -Eigenschaft ruft einen Wert ab, der angibt, ob Videos über das Remote Player-Steuerelement angezeigt werden können.

## <a name="syntax"></a>Syntax

*playerapplication*. **hasdisplay**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Schreib geschützter **boolescher** Wert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur verwendet, wenn das Windows Media Player-Steuerelement Remoting ist.

Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, aber Video kann nur jeweils an einer Stelle angezeigt werden, entweder im vollständigen Modus des Players oder in einem der remoten Windows Media Player-Steuerelemente. Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das aktuelle Steuerelement ist, durch das Video angezeigt werden kann.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playerapplication-Objekt**](playerapplication-object.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





