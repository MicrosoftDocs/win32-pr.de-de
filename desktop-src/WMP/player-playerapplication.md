---
title: Player. playerapplication
description: Die playerapplication-Eigenschaft ruft das playerapplication-Objekt ab, wenn ein Remotes Windows Media Player-Steuerelement ausgeführt wird.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerapplication-Windows-Media Player
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
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369517"
---
# <a name="playerplayerapplication"></a>Player. playerapplication

Die **playerapplication** -Eigenschaft ruft das **playerapplication** -Objekt ab, wenn ein Remotes Windows Media Player-Steuerelement ausgeführt wird.

## <a name="syntax"></a>Syntax

**playerapplication**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Schreib geschütztes **playerapplication** -Objekt oder der NULL-Wert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur verwendet, wenn das Windows Media playercontrol-Element Remoting verwendet wird. Wenn der Wert NULL ist, wird das Windows Media playercontrol nicht in den Remote Modus eingebettet.

Auf diese Eigenschaft kann nur in C++-Code oder in Skriptcode in Skins über die globale Variable playerapplication zugegriffen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Globale Attribute**](global-attributes.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Playerapplication-Objekt**](playerapplication-object.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





