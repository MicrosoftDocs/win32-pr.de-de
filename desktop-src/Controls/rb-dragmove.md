---
title: RB_DRAGMOVE (Commctrl.h)
description: Aktualisiert die Ziehposition im Rebar-Steuerelement nach einer vorherigen RB \_ BEGINDRAG-Meldung.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409722"
---
# <a name="rb_dragmove-message"></a>RB \_ DRAGMOVE-Nachricht

Aktualisiert die Ziehposition im Rebar-Steuerelement nach einer vorherigen [**RB \_ BEGINDRAG-Meldung.**](rb-begindrag.md)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD-Wert,** der die neuen Mauskoordinaten enthält. Die horizontale Koordinate ist im [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und die vertikale Koordinate im [**HIWORD enthalten.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Wenn Sie (DWORD)-1 übergeben, verwendet das Steuerelement für die Leiste die Position der Maus beim letzten Mal, wenn der Thread des Steuerelements [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder PeekMessage genannt [**wird.**](/windows/desktop/DevNotes/-peekmessage)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 

