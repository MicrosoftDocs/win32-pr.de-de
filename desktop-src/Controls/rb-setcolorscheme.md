---
title: RB_SETCOLORSCHEME Nachricht (Commctrl.h)
description: Legt die Farbschemainformationen für das Rebar-Steuerelement fest.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7715082a371c3632d8accb8fdf60bbac50d8d7d8182732d6a62c2dbb423c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169276"
---
# <a name="rb_setcolorscheme-message"></a>RB \_ SETCOLORSCHEME-Nachricht

Legt die Farbschemainformationen für das Rebar-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**COLORSCHEME-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) die die Farbschemainformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Das Steuerelement für die Neuleiste verwendet die Farbschemainformationen, wenn die 3D-Elemente im Steuerelement und in den Bändern gezeichnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)
</dt> </dl>

 

 





