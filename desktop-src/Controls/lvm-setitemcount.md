---
title: LVM_SETITEMCOUNT Meldung (kommstrg. h)
description: Bewirkt, dass das Listenansicht-Steuerelement Arbeitsspeicher für die angegebene Anzahl von Elementen zuweist oder die virtuelle Anzahl von Elementen in einem Steuerelement für die virtuelle Listenansicht festlegt.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Windows-Steuerelemente für LVM_SETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103227"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="14175-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="14175-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="14175-105">Bewirkt, dass das Listenansicht-Steuerelement Arbeitsspeicher für die angegebene Anzahl von Elementen zuweist oder die virtuelle Anzahl von Elementen in einem Steuerelement für die [virtuelle Listenansicht](list-view-controls-overview.md)festlegt.</span><span class="sxs-lookup"><span data-stu-id="14175-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="14175-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14175-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14175-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14175-108">Anzahl der Elemente, die das Listenansicht-Steuerelement letztendlich enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="14175-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="14175-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14175-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14175-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="14175-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="14175-111">Werte, die das Verhalten des Listenansicht-Steuer Elements nach dem Zurücksetzen der Element Anzahl angeben.</span><span class="sxs-lookup"><span data-stu-id="14175-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="14175-112">Dieser Wert kann eine Kombination folgender Werte sein:</span><span class="sxs-lookup"><span data-stu-id="14175-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="14175-113">Wert</span><span class="sxs-lookup"><span data-stu-id="14175-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="14175-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="14175-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="14175-115"><dt>**lvsicf \_ noinvalidateall**</dt></span><span class="sxs-lookup"><span data-stu-id="14175-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="14175-116">Das Listenansicht-Steuerelement wird nicht neu gezeichnet, es sei denn, die betroffenen Elemente sind aktuell in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="14175-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="14175-117"><dt>**lvsicf \_ NoScroll**</dt></span><span class="sxs-lookup"><span data-stu-id="14175-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="14175-118">Das Listenansicht-Steuerelement ändert die Bild Lauf Position nicht, wenn die Element Anzahl geändert wird.</span><span class="sxs-lookup"><span data-stu-id="14175-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14175-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14175-119">Return value</span></span>

<span data-ttu-id="14175-120">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="14175-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14175-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14175-121">Remarks</span></span>

<span data-ttu-id="14175-122">Wie der Arbeitsspeicher zugewiesen wird, hängt davon ab, wie das Listenansicht-Steuerelement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="14175-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="14175-123">Sie können diese Nachricht explizit senden oder das [**ListView- \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) /ListView-oder [**ListView \_ -/ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="14175-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="14175-124">Weitere Informationen finden Sie unter [virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="14175-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="14175-125">Wenn das Listenansicht-Steuerelement ohne den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil erstellt wurde, bewirkt das Senden dieser Nachricht, dass das Steuerelement seine internen Datenstrukturen für die angegebene Anzahl von Elementen zuweist.</span><span class="sxs-lookup"><span data-stu-id="14175-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="14175-126">Dadurch wird verhindert, dass das-Steuerelement die Datenstrukturen jedes Mal zuordnen muss, wenn ein Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="14175-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="14175-127">Wenn das Listenansicht-Steuerelement mit dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil (eine virtuelle Listenansicht) erstellt wurde, wird beim Senden dieser Nachricht die virtuelle Anzahl der im Steuerelement enthaltenen Elemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14175-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="14175-128">Der *LPARAM* -Parameter ist nur für Listenansicht-Steuerelemente vorgesehen, die den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) -und [**LVS- \_ Bericht**](list-view-window-styles.md) oder [**LVS- \_ Listen**](list-view-window-styles.md) Stile verwenden.</span><span class="sxs-lookup"><span data-stu-id="14175-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="14175-129">Wenn es sich bei der allgemeinen Steuerelement Listenansicht um eine virtualisierte Listenansicht ([**LVS-Besitzer \_ Daten**](list-view-window-styles.md)) handelt, gibt es in der Listenansicht einen Grenzwert von 100 Millionen Elementen.</span><span class="sxs-lookup"><span data-stu-id="14175-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="14175-130">In diesem Szenario gibt **LVM " \_ sstitemcount** " den Wert "false" zurück, wenn er einen *wParam* -Wert von 100.000.001 hat.</span><span class="sxs-lookup"><span data-stu-id="14175-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="14175-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14175-131">Requirements</span></span>



| <span data-ttu-id="14175-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14175-132">Requirement</span></span> | <span data-ttu-id="14175-133">Wert</span><span class="sxs-lookup"><span data-stu-id="14175-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14175-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14175-134">Minimum supported client</span></span><br/> | <span data-ttu-id="14175-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14175-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14175-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14175-136">Minimum supported server</span></span><br/> | <span data-ttu-id="14175-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14175-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14175-138">Header</span><span class="sxs-lookup"><span data-stu-id="14175-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="14175-139"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="14175-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

