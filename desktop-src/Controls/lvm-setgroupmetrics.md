---
title: LVM_SETGROUPMETRICS Meldung (kommstrg. h)
description: Legt Informationen zur Anzeige von Gruppen fest.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- Windows-Steuerelemente für LVM_SETGROUPMETRICS Meldung
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340348"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="b828c-104">LVM- \_ setgroupmetrics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b828c-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="b828c-105">Legt Informationen zur Anzeige von Gruppen fest.</span><span class="sxs-lookup"><span data-stu-id="b828c-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="b828c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b828c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b828c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b828c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b828c-108">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b828c-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="b828c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b828c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b828c-110">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**lvgroupmetrics**</a> -Struktur, die die festzulegenden Metriken enthält.</span><span class="sxs-lookup"><span data-stu-id="b828c-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b828c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b828c-111">Return value</span></span>

<span data-ttu-id="b828c-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b828c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b828c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b828c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b828c-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="b828c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b828c-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b828c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b828c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b828c-116">Requirements</span></span>



| <span data-ttu-id="b828c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b828c-117">Requirement</span></span> | <span data-ttu-id="b828c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b828c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b828c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b828c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b828c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b828c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b828c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b828c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b828c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b828c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b828c-123">Header</span><span class="sxs-lookup"><span data-stu-id="b828c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b828c-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b828c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





