---
title: RB_SETPALETTE Nachricht (Commctrl.h)
description: Legt die aktuelle Palette des Rebar-Steuerelements fest.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434940"
---
# <a name="rb_setpalette-message"></a>RB \_ SETPALETTE-Meldung

Legt die aktuelle Palette des Rebar-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Eine **HPALETTE,** die die neue Palette angibt, die das Neuleistensteuerelement verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine **HPALETTE** zurück, die die vorherige Palette des Rebar-Steuerelements angibt.

## <a name="remarks"></a>Hinweise

Es liegt in der Verantwortung der Anwendung, die diese Nachricht sendet, die in dieser Nachricht übergebene **HPALETTE** zu löschen (siehe [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Das Steuerelement für die Neuleiste löscht keinen **HPALETTE-Satz** mit dieser Meldung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

