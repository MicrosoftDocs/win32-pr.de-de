---
title: TVM_SETAUTOSCROLLINFO Meldung (kommstrg. h)
description: Legt Informationen fest, die zum Bestimmen von Auto Bild Lauf Merkmalen verwendet werden. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "seetautoscrollinfo" senden.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Windows-Steuerelemente für TVM_SETAUTOSCROLLINFO Meldung
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338136"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="becc4-105">TVM- \_ Meldung "abtautoscrollinfo"</span><span class="sxs-lookup"><span data-stu-id="becc4-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="becc4-106">Legt Informationen fest, die zum Bestimmen von Auto Bild Lauf Merkmalen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="becc4-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="becc4-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ seetautoscrollinfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) " senden.</span><span class="sxs-lookup"><span data-stu-id="becc4-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="becc4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="becc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="becc4-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="becc4-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="becc4-110">Gibt Pixel pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="becc4-110">Specifies pixels per second.</span></span> <span data-ttu-id="becc4-111">Der Offset für den Bildlauf wird durch den *wParam* dividiert, um die Gesamtdauer des automatischen Bildlaufs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="becc4-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="becc4-112">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="becc4-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="becc4-113">Gibt das umzeichnungs Zeitintervall an.</span><span class="sxs-lookup"><span data-stu-id="becc4-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="becc4-114">Zeichnen Sie bei jedem abgefragten Intervall neu, bis der Artikel in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="becc4-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="becc4-115">Bei Angabe von *wParam* wird der Speicherort des Elements berechnet und ein Repaint-Vorgang durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="becc4-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="becc4-116">Legen Sie diesen Wert fest, um einen Smooth Scroll zu erstellen</span><span class="sxs-lookup"><span data-stu-id="becc4-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="becc4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="becc4-117">Return value</span></span>

<span data-ttu-id="becc4-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="becc4-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="becc4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="becc4-119">Remarks</span></span>

<span data-ttu-id="becc4-120">AutoScroll-Informationen werden verwendet, um einen Bildlauf in einem nicht sichtbaren Element durchführen.</span><span class="sxs-lookup"><span data-stu-id="becc4-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="becc4-121">Das Steuerelement muss über den erweiterten [**\_ \_ autohscroll**](tree-view-control-window-extended-styles.md) -Stil "TVs" verfügen.</span><span class="sxs-lookup"><span data-stu-id="becc4-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="becc4-122">Weitere Informationen zu erweiterten Stilen finden Sie unter Tree-View Steuerelement erweiterter Stile.</span><span class="sxs-lookup"><span data-stu-id="becc4-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="becc4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="becc4-123">Requirements</span></span>



| <span data-ttu-id="becc4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="becc4-124">Requirement</span></span> | <span data-ttu-id="becc4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="becc4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="becc4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="becc4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="becc4-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becc4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="becc4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="becc4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="becc4-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becc4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="becc4-130">Header</span><span class="sxs-lookup"><span data-stu-id="becc4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="becc4-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="becc4-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





