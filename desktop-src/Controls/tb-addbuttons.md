---
title: TB_ADDBUTTONS Nachricht (Commctrl.h)
description: Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd3a5a15ac1983d93ca161dae20876159e5f633cf580d485686d67889276747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168523"
---
# <a name="tb_addbuttons-message"></a>TB \_ ADDBUTTONS-Nachricht

Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der hinzuzufügenden Schaltflächen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**TBBUTTON-Strukturen,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) die Informationen zu den hinzuzufügenden Schaltflächen enthalten. Es muss die gleiche Anzahl von Elementen im Array vorhanden sein wie durch *wParam* angegebene Schaltflächen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die Symbolleiste mit der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) erstellt wurde, müssen Sie die [**TB \_ BUTTONSTRUCTSIZE-Nachricht**](tb-buttonstructsize.md) an die Symbolleiste senden, bevor **Sie TB \_ ADDBUTTONS** senden.

Unter [**TB \_ SETIMAGELIST**](tb-setimagelist.md) erfahren Sie, wie Sie Symbolleistenschaltflächen aus einer oder mehreren Bildlisten Bitmaps zuweisen.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode fügt einer Symbolleiste drei Schaltflächen hinzu, wobei die Standardsystembitmap für Ansichtsschaltflächen verwendet wird. Die [**\_ TB-ADDBITMAP-Nachricht**](tb-addbitmap.md) gibt den Index des ersten Schaltflächenbilds in der Bildliste zurück. Einzelne Bilder werden durch ihre Offsets von diesem Wert identifiziert.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ ADDBUTTONSW** (Unicode) und **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Symbolleiste Standardschaltfläche – Bildindexwerte**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

