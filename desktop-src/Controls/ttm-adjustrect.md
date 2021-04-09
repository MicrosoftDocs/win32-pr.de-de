---
title: TTM_ADJUSTRECT Meldung (kommstrg. h)
description: Berechnet das Textanzeige Rechteck eines QuickInfo-Steuer Elements aus dem Fenster Rechteck oder das QuickInfo-Fenster Rechteck, das zum Anzeigen eines angegebenen Textanzeige Rechtecks erforderlich ist.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Windows-Steuerelemente für TTM_ADJUSTRECT Meldung
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956492"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="31d35-104">TTM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="31d35-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="31d35-105">Berechnet das Textanzeige Rechteck eines QuickInfo-Steuer Elements aus dem Fenster Rechteck oder das QuickInfo-Fenster Rechteck, das zum Anzeigen eines angegebenen Textanzeige Rechtecks erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="31d35-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="31d35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31d35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31d35-108">Wert, der angibt, welcher Vorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31d35-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="31d35-109">**True** gibt an, dass *LPARAM* zum Angeben eines Textanzeige Rechtecks verwendet wird und das entsprechende Fenster Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="31d35-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="31d35-110">Wenn **false**, wird *LPARAM* zum Angeben eines Fenster Rechtecks verwendet, und das entsprechende Textanzeige Rechteck wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="31d35-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="31d35-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31d35-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31d35-112">**Rect** -Struktur, um entweder ein QuickInfo-Fenster Rechteck oder ein Textanzeige Rechteck zu halten.</span><span class="sxs-lookup"><span data-stu-id="31d35-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d35-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d35-113">Return value</span></span>

<span data-ttu-id="31d35-114">Gibt einen Wert ungleich 0 (null) zurück, wenn das Rechteck erfolgreich angepasst wurde, und gibt NULL zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="31d35-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d35-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d35-115">Remarks</span></span>

<span data-ttu-id="31d35-116">Diese Meldung ist besonders nützlich, wenn Sie ein QuickInfo-Steuerelement verwenden möchten, um den vollständigen Text einer Zeichenfolge anzuzeigen, die in der Regel abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="31d35-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="31d35-117">Sie wird häufig mit ListView-und TreeView-Steuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="31d35-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="31d35-118">Normalerweise senden Sie diese Nachricht als Antwort auf einen TTN-Benachrichtigungs Code [ \_ anzeigen](ttn-show.md) , damit Sie das QuickInfo-Steuerelement ordnungsgemäß positionieren können.</span><span class="sxs-lookup"><span data-stu-id="31d35-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="31d35-119">Das QuickInfo-Fenster Rechteck ist etwas größer als das Textanzeige Rechteck, das die QuickInfo-Zeichenfolge umschließt.</span><span class="sxs-lookup"><span data-stu-id="31d35-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="31d35-120">Der Fenster Ursprung wird auch nach links vom Ursprung des Textanzeige Rechtecks verschoben.</span><span class="sxs-lookup"><span data-stu-id="31d35-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="31d35-121">Zum Positionieren des Textanzeige Rechtecks müssen Sie das entsprechende Fenster Rechteck berechnen und dieses Rechteck verwenden, um die QuickInfo zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="31d35-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="31d35-122">**TTM \_** "Anpassungen" verarbeitet diese Berechnung für Sie.</span><span class="sxs-lookup"><span data-stu-id="31d35-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="31d35-123">Wenn Sie " *wParam* " auf " **true**" festlegen, nimmt die Größe und Position des gewünschten QuickInfo-Textanzeige Rechtecks an, und die Größe und Position des QuickInfo-Fensters wird zurück **gegeben, um \_** den Text an der angegebenen Position anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31d35-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="31d35-124">Wenn Sie " *wParam* " auf " **false**" festlegen, können Sie ein QuickInfo-Fenster Rechteck angeben, und die Größe und Position des Text Rechtecks werden von **TTM \_** "-Wert-",</span><span class="sxs-lookup"><span data-stu-id="31d35-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="31d35-125">Das folgende Code Fragment veranschaulicht die Verwendung der **TTM- \_** Nachricht, um ein QuickInfo-Steuerelement zu positionieren, um den vollständigen Text der Zeichenfolge eines Steuer Elements anstelle einer abgeschnittene Zeichenfolge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31d35-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="31d35-126">Die von der Anwendung definierte **getmyitemrect** -Funktion gibt das Text Rechteck zurück, das benötigt wird, um den QuickInfo-Text direkt über die abgeschnittene Zeichenfolge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31d35-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="31d35-127">Die Details, wie diese Funktion implementiert wird, hängen vom jeweiligen Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="31d35-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="31d35-128">**TTM \_** Mithilfe von "" wird "" "" ""</span><span class="sxs-lookup"><span data-stu-id="31d35-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="31d35-129">Er gibt ein entsprechend großes und positioniertes Fenster Rechteck zurück, das dann verwendet wird, um das QuickInfo-Fenster zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="31d35-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="31d35-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d35-130">Requirements</span></span>



| <span data-ttu-id="31d35-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d35-131">Requirement</span></span> | <span data-ttu-id="31d35-132">Wert</span><span class="sxs-lookup"><span data-stu-id="31d35-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31d35-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d35-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31d35-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d35-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31d35-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d35-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31d35-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d35-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31d35-137">Header</span><span class="sxs-lookup"><span data-stu-id="31d35-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d35-138"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d35-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





