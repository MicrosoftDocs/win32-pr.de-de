---
title: LM_GETIDEALSIZE (Commctrl.h)
description: 'LM_GETIDEALSIZE Meldung: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112388"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="823e2-104">LM \_ GETIDEALSIZE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="823e2-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="823e2-105">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuerelements ab.</span><span class="sxs-lookup"><span data-stu-id="823e2-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="823e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="823e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="823e2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="823e2-108">Maximale Breite des Links in Pixel.</span><span class="sxs-lookup"><span data-stu-id="823e2-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="823e2-109">*lParam* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="823e2-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="823e2-110">Enthält nach der Rückgabe dieser Meldung einen Zeiger auf eine <a href="/previous-versions//dd145106(v=vs.85)">**SIZE-Struktur.**</a></span><span class="sxs-lookup"><span data-stu-id="823e2-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="823e2-111">Der **Cy-Member** dieser -Struktur gibt die ideale Höhe des Steuerelements für die gegebene Breite an.</span><span class="sxs-lookup"><span data-stu-id="823e2-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="823e2-112">Sie passt das **Cx-Member** an den tatsächlich benötigten Speicherplatz an.</span><span class="sxs-lookup"><span data-stu-id="823e2-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823e2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="823e2-113">Return value</span></span>

<span data-ttu-id="823e2-114">Eine ganze Zahl, die die bevorzugte Höhe des Linktexts in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="823e2-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="823e2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="823e2-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="823e2-116">Um diese API verwenden zu können, müssen Sie ein Manifest bereitstellen, das Comclt32.dll 6.0 angibt.</span><span class="sxs-lookup"><span data-stu-id="823e2-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="823e2-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="823e2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="823e2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="823e2-118">Requirements</span></span>



| <span data-ttu-id="823e2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="823e2-119">Requirement</span></span> | <span data-ttu-id="823e2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="823e2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="823e2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="823e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="823e2-122">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="823e2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="823e2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="823e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="823e2-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="823e2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="823e2-125">Header</span><span class="sxs-lookup"><span data-stu-id="823e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="823e2-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="823e2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

