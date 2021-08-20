---
title: RB_GETDROPTARGET Meldung (Commctrl.h)
description: Ruft den IDropTarget-Schnittstellenzeiger eines Rebar-Steuerelements ab.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793d2192ef65f193ff27d40cc14660c90d067034d8c1304e1bde1a354a4f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169610"
---
# <a name="rb_getdroptarget-message"></a>RB \_ GETDROPTARGET-Nachricht

Ruft den [**IDropTarget-Schnittstellenzeiger**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) eines Rebar-Steuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen [**IDropTarget-Zeiger,**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) der den Schnittstellenzeiger empfängt. Es liegt in der Verantwortung des Aufrufers, [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für diesen Zeiger aufzurufen, wenn er nicht mehr benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

