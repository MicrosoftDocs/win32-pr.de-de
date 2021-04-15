---
title: LVM_SCROLL Meldung (kommstrg. h)
description: Scrollt den Inhalt eines Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ scrollmakros senden.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Windows-Steuerelemente für LVM_SCROLL Meldung
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477559"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="2fb9a-105">LVM- \_ scrollnachricht</span><span class="sxs-lookup"><span data-stu-id="2fb9a-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="2fb9a-106">Scrollt den Inhalt eines Listenansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="2fb9a-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView- \_ scrollmakros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) senden.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fb9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fb9a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fb9a-110">Der Wert vom Typ " **int** ", der den horizontalen Bildlauf in Pixel relativ zur aktuellen Position des Listen Ansichts Inhalts angibt.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="2fb9a-111">Wenn sich das Listenansicht-Steuerelement in der Listenansicht befindet, wird dieser Wert auf die nächste Anzahl von Pixeln aufgerundet, die eine ganze Spalte bilden.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="2fb9a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fb9a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fb9a-113">Der Wert vom Typ " **int** ", der den vertikalen Bildlauf in Pixel relativ zur aktuellen Position des Listen Ansichts Inhalts angibt.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb9a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fb9a-114">Return value</span></span>

<span data-ttu-id="2fb9a-115">Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb9a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb9a-116">Remarks</span></span>

<span data-ttu-id="2fb9a-117">Wenn sich das Listenansicht-Steuerelement in der Berichtsansicht befindet, kann das Steuerelement nur vertikal in Zeilen Inkrementen gescrollt werden.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="2fb9a-118">Daher wird der *LPARAM* -Parameter auf die nächste Anzahl von Pixeln gerundet, die ein ganzes Zeilen Inkrement bilden.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="2fb9a-119">Wenn z. b. die Höhe einer Linie 16 Pixel und 8 für *LPARAM* überschritten wird, wird die Liste um 16 Pixel (1 Zeile) gescrollt.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="2fb9a-120">Wenn für *LPARAM* der Wert 7 festgelegt wird, wird für die Liste der Bildlauf mit 0 Pixel (0 Zeilen) durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fb9a-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb9a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fb9a-121">Requirements</span></span>



| <span data-ttu-id="2fb9a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fb9a-122">Requirement</span></span> | <span data-ttu-id="2fb9a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2fb9a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb9a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fb9a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb9a-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fb9a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fb9a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fb9a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb9a-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fb9a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fb9a-128">Header</span><span class="sxs-lookup"><span data-stu-id="2fb9a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb9a-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb9a-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





