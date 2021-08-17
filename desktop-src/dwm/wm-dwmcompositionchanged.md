---
title: WM_DWMCOMPOSITIONCHANGED Meldung (Winuser.h)
description: Informiert alle Fenster der obersten Ebene, dass Desktopfenster-Manager Komposition (DWM) aktiviert oder deaktiviert wurde.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973c69e114882041fc300ca6dee9c96efe121ee7bbf10875ed58ed3c269772c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118794"
---
# <a name="wm_dwmcompositionchanged-message"></a>WM \_ DWMCOMPOSITIONCHANGED-Nachricht

Informiert alle Fenster der obersten Ebene, dass Desktopfenster-Manager Komposition (DWM) aktiviert oder deaktiviert wurde.

> [!Note]  
> Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von Videomodusänderungen nicht gesendet wird.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

Die [**DwmIsCompositionEnabled-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) kann verwendet werden, um den aktuellen Kompositionszustand zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

