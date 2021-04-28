---
title: LM_GETIDEALHEIGHT-Nachricht (Commctrl.h)
description: 'LM_GETIDEALHEIGHT Meldung: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.'
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112398"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="52431-104">LM \_ GETIDEALHEIGHT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="52431-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="52431-105">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.</span><span class="sxs-lookup"><span data-stu-id="52431-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="52431-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52431-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52431-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="52431-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="52431-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="52431-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52431-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52431-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="52431-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52431-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52431-111">Return value</span></span>

<span data-ttu-id="52431-112">Ganze Zahl, die die bevorzugte Höhe des Linktexts in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="52431-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="52431-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52431-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52431-114">Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt.</span><span class="sxs-lookup"><span data-stu-id="52431-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="52431-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="52431-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52431-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52431-116">Requirements</span></span>



| <span data-ttu-id="52431-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52431-117">Requirement</span></span> | <span data-ttu-id="52431-118">Wert</span><span class="sxs-lookup"><span data-stu-id="52431-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52431-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52431-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52431-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52431-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52431-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52431-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52431-122">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52431-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52431-123">Header</span><span class="sxs-lookup"><span data-stu-id="52431-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52431-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="52431-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





