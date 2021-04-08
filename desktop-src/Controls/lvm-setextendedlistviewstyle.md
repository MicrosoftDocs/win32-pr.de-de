---
title: LVM_SETEXTENDEDLISTVIEWSTYLE Meldung (kommstrg. h)
description: Legt erweiterte Stile in Listenansicht-Steuerelementen fest. Sie können diese Nachricht explizit senden oder das "ListView"-und "ListView/ \_ \_ textendedlistviewstyleex"-Makro verwenden.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Windows-Steuerelemente für LVM_SETEXTENDEDLISTVIEWSTYLE Meldung
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949423"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="82e58-105">LVM- \_ Meldung "abtextendedlistviewstyle"</span><span class="sxs-lookup"><span data-stu-id="82e58-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="82e58-106">Legt erweiterte Stile in Listenansicht-Steuerelementen fest.</span><span class="sxs-lookup"><span data-stu-id="82e58-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="82e58-107">Sie können diese Nachricht explizit senden oder das " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) "-und "ListView/ [**\_ textendedlistviewstyleex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) "-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="82e58-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82e58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82e58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e58-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82e58-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82e58-110">**DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen.</span><span class="sxs-lookup"><span data-stu-id="82e58-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="82e58-111">Dieser Parameter kann eine Kombination aus [**erweiterten List-View Stilen**](extended-list-view-styles.md)sein.</span><span class="sxs-lookup"><span data-stu-id="82e58-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="82e58-112">Nur die erweiterten Stile in *wParam* werden geändert.</span><span class="sxs-lookup"><span data-stu-id="82e58-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="82e58-113">Alle anderen Stile werden unverändert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="82e58-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="82e58-114">Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="82e58-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="82e58-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82e58-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82e58-116">**DWORD** -Wert, der die festzulegenden erweiterten Listenansicht-Steuerelement Stile angibt.</span><span class="sxs-lookup"><span data-stu-id="82e58-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="82e58-117">Dieser Parameter kann eine Kombination aus [**erweiterten List-View Stilen**](extended-list-view-styles.md)sein.</span><span class="sxs-lookup"><span data-stu-id="82e58-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="82e58-118">Stile, die nicht festgelegt sind, aber in *wParam* angegeben sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="82e58-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e58-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82e58-119">Return value</span></span>

<span data-ttu-id="82e58-120">Gibt einen **DWORD** -Wert zurück, der die vorherigen erweiterten Listenansicht-Steuerelement Stile enthält.</span><span class="sxs-lookup"><span data-stu-id="82e58-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e58-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82e58-121">Remarks</span></span>

<span data-ttu-id="82e58-122">Mit dem *wParam* -Parameter können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="82e58-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="82e58-123">Wenn Sie z. b. [**LVS \_ Ex \_ FullRowSelect**](extended-list-view-styles.md) für *wParam* und 0 für *LPARAM* übergeben, werden die **LVS \_ Ex \_ FullRowSelect** -Stil gelöscht, aber alle anderen Stile bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="82e58-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="82e58-124">Aus Gründen der Abwärtskompatibilität wurde das ListView-Element " [**\_ abtextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) " nicht für die Verwendung von *wParam* aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="82e58-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="82e58-125">Wenn Sie den *wParam* -Wert verwenden möchten, verwenden Sie das ListView-Makro " [**\_ stextendecodlistviewstyleex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) ".</span><span class="sxs-lookup"><span data-stu-id="82e58-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="82e58-126">Wenn Sie diese Meldung verwenden, um die LVS-Zeichen für die [**\_ Post- \_ Kontrollkästchen**](extended-list-view-styles.md) festzulegen, werden alle zuvor festgelegten Status Bild Indizes verworfen.</span><span class="sxs-lookup"><span data-stu-id="82e58-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="82e58-127">Alle Kontrollkästchen werden mit dem Status "deaktiviert" initialisiert.</span><span class="sxs-lookup"><span data-stu-id="82e58-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="82e58-128">Der State Image Index ist in Bits 12 bis 15 des **State** -Members der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="82e58-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e58-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82e58-129">Requirements</span></span>



| <span data-ttu-id="82e58-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82e58-130">Requirement</span></span> | <span data-ttu-id="82e58-131">Wert</span><span class="sxs-lookup"><span data-stu-id="82e58-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82e58-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82e58-132">Minimum supported client</span></span><br/> | <span data-ttu-id="82e58-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82e58-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82e58-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82e58-134">Minimum supported server</span></span><br/> | <span data-ttu-id="82e58-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82e58-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82e58-136">Header</span><span class="sxs-lookup"><span data-stu-id="82e58-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="82e58-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e58-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





