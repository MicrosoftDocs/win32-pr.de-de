---
title: Player.playerApplication
description: Die playerApplication-Eigenschaft ruft das PlayerApplication-Objekt ab, wenn Windows Media Player remote ausgeführt wird.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player.playerApplication-Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995850"
---
# <a name="playerplayerapplication"></a>Player.playerApplication

Die **playerApplication-Eigenschaft** ruft das **PlayerApplication-Objekt** ab, wenn Windows Media Player remote ausgeführt wird.

## <a name="syntax"></a>Syntax

**playerApplication**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein schreibgeschütztes **PlayerApplication-Objekt** oder der NULL-Wert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur beim Remoting des Windows Media Playercontrol verwendet. Wenn der Wert NULL ist, Windows Media Playercontrol nicht in den Remotemodus eingebettet.

Auf diese Eigenschaft kann nur in C++-Code oder skriptcode in Skins über die globale PlayerApplication-Variable zugegriffen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Globale Attribute**](global-attributes.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**PlayerApplication-Objekt**](playerapplication-object.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





