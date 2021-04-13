---
title: LM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Windows-Steuerelemente für LM_GETIDEALSIZE Meldung
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
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475207"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="a2eaa-104">LM- \_ getidealsize-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a2eaa-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="a2eaa-105">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2eaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2eaa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2eaa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a2eaa-108">Maximale Breite des Links in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="a2eaa-109">*LPARAM* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2eaa-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="a2eaa-110">Wenn diese Nachricht zurückgegeben wird, enthält Sie einen Zeiger auf eine <a href="/previous-versions//dd145106(v=vs.85)">**Größen**</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="a2eaa-111">Der **CY** -Member dieser Struktur gibt die ideale Höhe des Steuer Elements für die angegebene Breite an.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="a2eaa-112">Der **CX** -Member wird an den tatsächlich benötigten Speicherplatz angepasst.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2eaa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2eaa-113">Return value</span></span>

<span data-ttu-id="a2eaa-114">Eine ganze Zahl, die die bevorzugte Höhe des linktexts in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2eaa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2eaa-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2eaa-116">Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="a2eaa-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a2eaa-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a2eaa-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2eaa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2eaa-118">Requirements</span></span>



| <span data-ttu-id="a2eaa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2eaa-119">Requirement</span></span> | <span data-ttu-id="a2eaa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a2eaa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eaa-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2eaa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2eaa-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2eaa-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2eaa-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2eaa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2eaa-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2eaa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2eaa-125">Header</span><span class="sxs-lookup"><span data-stu-id="a2eaa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2eaa-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2eaa-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

