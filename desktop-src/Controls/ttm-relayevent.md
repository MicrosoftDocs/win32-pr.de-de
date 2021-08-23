---
title: TTM_RELAYEVENT (Commctrl.h)
description: Übergibt eine Mausnachricht zur Verarbeitung an ein QuickInfo-Steuerelement.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051a0b7ab8ecd93b15ceb9187eefd6f566b55d653b751889cd29acec58366716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166363"
---
# <a name="ttm_relayevent-message"></a>TTM \_ RELAYEVENT-Nachricht

Übergibt eine Mausnachricht zur Verarbeitung an ein QuickInfo-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein. **Windows 7 und höher:** Wenn die Position der QuickInfo von der Cursorposition versetzt wird (um nicht durch einen Finger oder ein Zeigegerät blockiert zu werden), kann dieser Parameter zusätzliche Informationen aus der [**WM \_ MOUSEMOVE-Meldung**](/windows/desktop/inputdev/wm-mousemove) enthalten. Rufen Sie diese zusätzlichen Informationen mit [**GetMessageExtraInfo ab.**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MSG-Struktur,**](/windows/win32/api/winuser/ns-winuser-msg) die die zu sendende Nachricht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Ein QuickInfo-Steuerelement verarbeitet nur die folgenden Nachrichten, die von der **TTM \_ RELAYEVENT-Nachricht an das Steuerelement übergeben** werden:

-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEMOVE
-   WM \_ NCMOUSEMOVE
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP

Alle anderen Nachrichten werden ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

