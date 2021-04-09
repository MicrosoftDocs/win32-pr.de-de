---
title: LM_GETIDEALHEIGHT Meldung (kommstrg. h)
description: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- Windows-Steuerelemente für LM_GETIDEALHEIGHT Meldung
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858659"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="d2a95-104">LM- \_ getidealheight-Meldung</span><span class="sxs-lookup"><span data-stu-id="d2a95-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="d2a95-105">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="d2a95-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2a95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2a95-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2a95-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d2a95-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2a95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2a95-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2a95-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d2a95-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a95-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2a95-111">Return value</span></span>

<span data-ttu-id="d2a95-112">Eine ganze Zahl, die die bevorzugte Höhe des linktexts in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2a95-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a95-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2a95-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2a95-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="d2a95-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d2a95-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d2a95-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2a95-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2a95-116">Requirements</span></span>



| <span data-ttu-id="d2a95-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2a95-117">Requirement</span></span> | <span data-ttu-id="d2a95-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a95-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a95-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2a95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a95-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2a95-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2a95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a95-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a95-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2a95-123">Header</span><span class="sxs-lookup"><span data-stu-id="d2a95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a95-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a95-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





