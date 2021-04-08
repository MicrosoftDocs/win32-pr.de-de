---
title: EC_WMT_INDEX_EVENT (Windows Media-Format 11 SDK)
description: EC \_ WMT- \_ Index \_ Ereignis
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK für Windows Media-Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF), EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039935"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="c603b-108">EC_WMT_INDEX_EVENT (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="c603b-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c603b-109">Wird vom SDK für den Windows Media-Format gesendet, wenn eine Anwendung den ASF-Writer verwendet, um Windows Media Video Dateien zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="c603b-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="c603b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c603b-110">Parameters</span></span>

<span data-ttu-id="c603b-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c603b-111">*lParam1*</span></span>

<span data-ttu-id="c603b-112">Kann eine der folgenden **WMT- \_ Status** Meldungen sein.</span><span class="sxs-lookup"><span data-stu-id="c603b-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="c603b-113">`Message`</span><span class="sxs-lookup"><span data-stu-id="c603b-113">Message</span></span>              | <span data-ttu-id="c603b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c603b-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="c603b-115">WMT \_ gestartet</span><span class="sxs-lookup"><span data-stu-id="c603b-115">WMT\_STARTED</span></span>         | <span data-ttu-id="c603b-116">Die Indizierung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="c603b-116">Indexing has begun.</span></span> <span data-ttu-id="c603b-117">*lParam2* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c603b-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="c603b-118">WMT \_ geschlossen</span><span class="sxs-lookup"><span data-stu-id="c603b-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="c603b-119">Die Indizierung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c603b-119">Indexing has been completed.</span></span> <span data-ttu-id="c603b-120">*lParam2* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c603b-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="c603b-121">WMT- \_ Index \_ Fortschritt</span><span class="sxs-lookup"><span data-stu-id="c603b-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="c603b-122">Die Indizierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c603b-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="c603b-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c603b-123">*lParam2*</span></span>

<span data-ttu-id="c603b-124">Wenn *lParam1* WMT \_ Closed oder WMT \_ gestartet ist, dann ist *lParam2* gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c603b-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="c603b-125">Wenn *lParam1* den WMT- \_ Index Status \_ hat, ist *lParam2* ein **DWORD** -Wert, der den Status als Prozentsatz der gesamten Downloadgröße ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="c603b-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c603b-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c603b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c603b-127">**DirectShow-qasf-Referenz**</span><span class="sxs-lookup"><span data-stu-id="c603b-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




