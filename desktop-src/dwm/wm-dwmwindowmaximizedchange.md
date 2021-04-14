---
title: WM_DWMWINDOWMAXIMIZEDCHANGE Meldung (Winuser. h)
description: Wird gesendet, wenn ein aus Desktopfenster-Manager (DWM) zusammengesetztes Fenster maximiert ist.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391949"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>WM \_ dwmwindowmaximizedchange-Meldung

Wird gesendet, wenn ein aus Desktopfenster-Manager (DWM) zusammengesetztes Fenster maximiert ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Legen Sie diese Einstellung auf "true" fest, um anzugeben, dass das Fenster maximiert ist.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

