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
# <a name="tb_addbuttons-message"></a><span data-ttu-id="9ef5b-104">TB \_ AddButtons-Meldung</span><span class="sxs-lookup"><span data-stu-id="9ef5b-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="9ef5b-105">Fügt einer Symbolleiste eine oder mehrere Schaltflächen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ef5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef5b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ef5b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ef5b-108">Anzahl der hinzu zufügenden Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="9ef5b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ef5b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ef5b-110">Zeiger auf ein Array von [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Strukturen, die Informationen über die hinzu zufügenden Schaltflächen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="9ef5b-111">Es muss die gleiche Anzahl von Elementen im Array wie durch *wParam* angegebene Schaltflächen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef5b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ef5b-112">Return value</span></span>

<span data-ttu-id="9ef5b-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9ef5b-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef5b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ef5b-114">Remarks</span></span>

<span data-ttu-id="9ef5b-115">Wenn die Symbolleiste mit der Funktion " [**dashboardwindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellt wurde, müssen Sie die Meldung " [**TB \_ buttonstructsize**](tb-buttonstructsize.md) " vor dem Senden von **TB- \_ AddButtons** an die Symbolleiste senden.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="9ef5b-116">Eine Erläuterung zum Zuweisen von Bitmaps zu Symbolleisten-Schaltflächen aus einer oder mehreren Bildlisten finden Sie unter [**TB \_ SetImageList**](tb-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef5b-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="9ef5b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ef5b-117">Examples</span></span>

<span data-ttu-id="9ef5b-118">Der folgende Beispielcode fügt eine Symbolleiste mit der Standard-System Bitmap für Ansichts Schaltflächen drei Schaltflächen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="9ef5b-119">Die [**TB \_ AddBitmap**](tb-addbitmap.md) -Meldung gibt den Index des ersten Schaltflächen Bilds in der Bildliste zurück.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="9ef5b-120">Einzelne Bilder werden durch ihre Offsets von diesem Wert identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9ef5b-120">Individual images are identified by their offsets from that value.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9ef5b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ef5b-121">Requirements</span></span>



| <span data-ttu-id="9ef5b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ef5b-122">Requirement</span></span> | <span data-ttu-id="9ef5b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9ef5b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef5b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ef5b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef5b-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ef5b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ef5b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ef5b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef5b-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ef5b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ef5b-128">Header</span><span class="sxs-lookup"><span data-stu-id="9ef5b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef5b-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef5b-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9ef5b-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9ef5b-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9ef5b-131">**TB \_ Addbuttonsw** (Unicode) und **TB \_ addbuttonsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9ef5b-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9ef5b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ef5b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef5b-133">**Bild-/Indexwerte der Symbolleiste Standard**</span><span class="sxs-lookup"><span data-stu-id="9ef5b-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

