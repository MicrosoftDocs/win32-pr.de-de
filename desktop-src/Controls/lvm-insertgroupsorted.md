---
title: LVM_INSERTGROUPSORTED Meldung (kommstrg. h)
description: Fügt eine Gruppe in eine geordnete Liste von Gruppen ein.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Windows-Steuerelemente für LVM_INSERTGROUPSORTED Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859149"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="950b7-104">LVM \_ insertgroupsortierte Nachricht</span><span class="sxs-lookup"><span data-stu-id="950b7-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="950b7-105">Fügt eine Gruppe in eine geordnete Liste von Gruppen ein.</span><span class="sxs-lookup"><span data-stu-id="950b7-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="950b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="950b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950b7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="950b7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="950b7-108">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">lvinsertgroupsortierte</a> -Struktur, die die einzufügende Gruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="950b7-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="950b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="950b7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="950b7-110">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="950b7-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950b7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="950b7-111">Return value</span></span>

<span data-ttu-id="950b7-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="950b7-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="950b7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="950b7-113">Remarks</span></span>

<span data-ttu-id="950b7-114">Die Reihenfolge der Liste basiert auf der ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="950b7-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="950b7-115">Die Reihenfolge wird durch die Anwendungs definierte Sortierfunktion " [**lvgroupcompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)" definiert, die durch den *wParam* -Parameter in der [**lvinsertgroupsortierten**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) -Struktur übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="950b7-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="950b7-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="950b7-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="950b7-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="950b7-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="950b7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="950b7-118">Requirements</span></span>



| <span data-ttu-id="950b7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="950b7-119">Requirement</span></span> | <span data-ttu-id="950b7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="950b7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="950b7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="950b7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="950b7-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="950b7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="950b7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="950b7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="950b7-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="950b7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="950b7-125">Header</span><span class="sxs-lookup"><span data-stu-id="950b7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="950b7-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="950b7-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="950b7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="950b7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="950b7-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="950b7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="950b7-129">**"Lvgroupcompare"**</span><span class="sxs-lookup"><span data-stu-id="950b7-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="950b7-130">**Lvinsertgroupsortierbar**</span><span class="sxs-lookup"><span data-stu-id="950b7-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

