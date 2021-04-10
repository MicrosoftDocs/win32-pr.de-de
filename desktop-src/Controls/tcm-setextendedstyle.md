---
title: TCM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt die erweiterten Stile fest, die vom Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des tabstrg-Formats "tabctrl"/ \_ textendedstyle senden.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Windows-Steuerelemente für TCM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040630"
---
# <a name="tcm_setextendedstyle-message"></a><span data-ttu-id="c3a37-105">TCM-Nachricht "- \_ textendedstyle"</span><span class="sxs-lookup"><span data-stu-id="c3a37-105">TCM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="c3a37-106">Legt die erweiterten Stile fest, die vom Registerkarten-Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3a37-106">Sets the extended styles that the tab control will use.</span></span> <span data-ttu-id="c3a37-107">Sie können diese Nachricht explizit oder mithilfe des tabstrg-Formats " [**tabctrl"/ \_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) senden.</span><span class="sxs-lookup"><span data-stu-id="c3a37-107">You can send this message explicitly or by using the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3a37-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3a37-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a37-110">Ein **DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c3a37-110">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="c3a37-111">Nur die erweiterten Stile in *wParam* werden geändert.</span><span class="sxs-lookup"><span data-stu-id="c3a37-111">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="c3a37-112">Alle anderen Stile werden unverändert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c3a37-112">All other styles will be maintained as they are.</span></span> <span data-ttu-id="c3a37-113">Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="c3a37-113">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="c3a37-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3a37-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a37-115">Ein Wert, der die erweiterten Registerkarten-Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="c3a37-115">Value specifying the extended tab control styles.</span></span> <span data-ttu-id="c3a37-116">Dieser Wert ist eine Kombination aus [erweiterten](tab-control-extended-styles.md)Formatvorlagen des Register Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c3a37-116">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a37-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3a37-117">Return value</span></span>

<span data-ttu-id="c3a37-118">Gibt einen **DWORD** -Wert zurück, der das vorherige Registerkarten-Steuerelement erweiterte Stile enthält.</span><span class="sxs-lookup"><span data-stu-id="c3a37-118">Returns a **DWORD** value that contains the previous tab control extended styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a37-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3a37-119">Remarks</span></span>

<span data-ttu-id="c3a37-120">Mit dem *wParam* -Parameter können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c3a37-120">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="c3a37-121">Wenn Sie z. b. [**TCS \_ Ex- \_ flatseparatoren**](tab-control-extended-styles.md) für *wParam* und 0 für *LPARAM* übergeben, wird der **TCS \_ Ex- \_ flatseparators** -Stil gelöscht, aber alle anderen Stile bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="c3a37-121">For example, if you pass [**TCS\_EX\_FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **TCS\_EX\_FLATSEPARATORS** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="c3a37-122">Aus Gründen der Abwärtskompatibilität wurde das [**tabstrg \* \_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) -Makro nicht so aktualisiert, dass *dwexmask* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3a37-122">For backward compatibility reasons, the [**TabCtrl\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) macro has not been updated to use *dwExMask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a37-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3a37-123">Requirements</span></span>



| <span data-ttu-id="c3a37-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3a37-124">Requirement</span></span> | <span data-ttu-id="c3a37-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c3a37-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a37-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3a37-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a37-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3a37-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3a37-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3a37-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a37-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3a37-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3a37-130">Header</span><span class="sxs-lookup"><span data-stu-id="c3a37-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a37-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a37-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a37-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3a37-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a37-133">**TCM \_ getextendecodstyle**</span><span class="sxs-lookup"><span data-stu-id="c3a37-133">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
</dt> </dl>

 

 





