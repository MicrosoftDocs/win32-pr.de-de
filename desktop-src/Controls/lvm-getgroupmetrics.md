---
title: LVM_GETGROUPMETRICS Meldung (kommstrg. h)
description: Ruft Informationen zur Anzeige von Gruppen ab.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- Windows-Steuerelemente für LVM_GETGROUPMETRICS Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956994"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="d6819-104">LVM \_ getgroupmetrics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d6819-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="d6819-105">Ruft Informationen zur Anzeige von Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="d6819-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6819-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6819-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6819-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d6819-108">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d6819-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="d6819-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6819-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d6819-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**lvgroupmetrics**</a> -Struktur, die die abgerufenen Metriken empfängt.</span><span class="sxs-lookup"><span data-stu-id="d6819-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6819-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6819-111">Return value</span></span>

<span data-ttu-id="d6819-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6819-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6819-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6819-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6819-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="d6819-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d6819-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d6819-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6819-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6819-116">Requirements</span></span>



| <span data-ttu-id="d6819-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6819-117">Requirement</span></span> | <span data-ttu-id="d6819-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d6819-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6819-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6819-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6819-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6819-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6819-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6819-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6819-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6819-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6819-123">Header</span><span class="sxs-lookup"><span data-stu-id="d6819-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6819-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6819-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





