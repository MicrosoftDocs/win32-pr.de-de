---
title: TB_ADDBUTTONS Meldung (kommstrg. h)
description: Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Windows-Steuerelemente für TB_ADDBUTTONS Meldung
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
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957254"
---
# <a name="tb_addbuttons-message"></a>TB \_ AddButtons-Meldung

Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der hinzu zufügenden Schaltflächen.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Strukturen, die Informationen über die hinzu zufügenden Schaltflächen enthalten. Es muss die gleiche Anzahl von Elementen im Array wie durch *wParam* angegebene Schaltflächen vorhanden sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn die Symbolleiste mit der Funktion " [**dashboardwindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellt wurde, müssen Sie die Meldung " [**TB \_ buttonstructsize**](tb-buttonstructsize.md) " vor dem Senden von **TB- \_ AddButtons** an die Symbolleiste senden.

Eine Erläuterung zum Zuweisen von Bitmaps zu Symbolleisten-Schaltflächen aus einer oder mehreren Bildlisten finden Sie unter [**TB \_ SetImageList**](tb-setimagelist.md) .

## <a name="examples"></a>Beispiele

Der folgende Beispielcode fügt eine Symbolleiste mit der Standard-System Bitmap für Ansichts Schaltflächen drei Schaltflächen hinzu. Die [**TB \_ AddBitmap**](tb-addbitmap.md) -Meldung gibt den Index des ersten Schaltflächen Bilds in der Bildliste zurück. Einzelne Bilder werden durch ihre Offsets von diesem Wert identifiziert.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ Addbuttonsw** (Unicode) und **TB \_ addbuttonsa** (ANSI)<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bild-/Indexwerte der Symbolleiste Standard**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

