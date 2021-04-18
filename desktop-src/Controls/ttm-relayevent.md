---
title: TTM_RELAYEVENT Meldung (kommstrg. h)
description: Übergibt eine Maus Nachricht zur Verarbeitung an ein QuickInfo-Steuerelement.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Windows-Steuerelemente für TTM_RELAYEVENT Meldung
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
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353249"
---
# <a name="ttm_relayevent-message"></a>TTM \_ relayevent-Nachricht

Übergibt eine Maus Nachricht zur Verarbeitung an ein QuickInfo-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein. **Windows 7 und höher:** Wenn die Position der QuickInfo von der Cursorposition versetzt ist (damit Sie nicht durch einen Finger oder ein Zeigegerät behindert wird), kann dieser Parameter zusätzliche Informationen enthalten, die aus der [**WM- \_ mousettverschiebungmeldung**](/windows/desktop/inputdev/wm-mousemove) entnommen werden. Rufen Sie diese zusätzlichen Informationen mit [**getMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)ab.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die zu relaynachricht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Ein QuickInfo-Steuerelement verarbeitet nur die folgenden Nachrichten, die von der **TTM \_ Relay** -Meldung an das Steuerelement weitergegeben werden

-   WM \_ lbuttondown
-   WM- \_ lbuttonup
-   WM- \_ mbuttondown
-   WM- \_ mbuttonup
-   WM- \_ mouseelmove
-   WM- \_ ncmouummove
-   WM- \_ rbuttondown
-   WM- \_ rbuttonup

Alle anderen Nachrichten werden ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

