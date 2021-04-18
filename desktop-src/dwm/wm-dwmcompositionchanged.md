---
title: WM_DWMCOMPOSITIONCHANGED Meldung (Winuser. h)
description: Informiert alle Fenster der obersten Ebene darüber, dass die Desktopfenster-Manager-Komposition (DWM) aktiviert oder deaktiviert wurde.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED Meldung Desktopfenster-Manager
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
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339971"
---
# <a name="wm_dwmcompositionchanged-message"></a>WM \_ dwmcompositionchanged-Meldung

Informiert alle Fenster der obersten Ebene darüber, dass die Desktopfenster-Manager-Komposition (DWM) aktiviert oder deaktiviert wurde.

> [!Note]  
> Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von den videomodusänderungen nicht gesendet wird.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

Die [**dwmiscompositionaktivierte**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) -Funktion kann verwendet werden, um den aktuellen Kompositions Status zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

