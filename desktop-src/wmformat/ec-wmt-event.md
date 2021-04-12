---
title: EC_WMT_EVENT (Windows Media-Format 11 SDK)
description: '\_WMT- \_ Ereignis für EC'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK für Windows Media-Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Digital Rights Management (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474856"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="d438f-110">EC_WMT_EVENT (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="d438f-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d438f-111">Wird vom SDK für den Windows Media-Format gesendet, wenn eine Anwendung den ASF-Reader-Filter verwendet, um von Digital Rights Management (DRM) geschützte ASF-Dateien wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="d438f-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="d438f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d438f-112">Parameters</span></span>

<span data-ttu-id="d438f-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d438f-113">*lParam1*</span></span>

<span data-ttu-id="d438f-114">Kann einen der folgenden WMT- \_ Status Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d438f-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="d438f-115">WMT- \_ Status Meldung</span><span class="sxs-lookup"><span data-stu-id="d438f-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="d438f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d438f-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d438f-117">WMT \_ keine \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="d438f-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="d438f-118">Die Datei ist mit der DRM-Version 1 geschützt, und die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d438f-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="d438f-119">WMT-Abruf \_ \_ Lizenz</span><span class="sxs-lookup"><span data-stu-id="d438f-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="d438f-120">Der Lizenz Erwerbs Vorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d438f-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="d438f-121">(Dies bedeutet nicht unbedingt, dass eine Lizenz erfolgreich erworben wurde.)</span><span class="sxs-lookup"><span data-stu-id="d438f-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="d438f-122">WMT \_ keine \_ Rechte \_ Ex</span><span class="sxs-lookup"><span data-stu-id="d438f-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="d438f-123">Die Datei ist mit der DRM-Version 7 geschützt, und die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d438f-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="d438f-124">WMT \_ erfordert \_ Individualisierung</span><span class="sxs-lookup"><span data-stu-id="d438f-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="d438f-125">Mit der Lizenz können nur Individual Anwendungen die angeforderte Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="d438f-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="d438f-126">WMT \_ Individual</span><span class="sxs-lookup"><span data-stu-id="d438f-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="d438f-127">Der Individualisierungsprozess wird jetzt ausgeführt oder wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d438f-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="d438f-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d438f-128">*lParam2*</span></span>

<span data-ttu-id="d438f-129">Ein Zeiger auf eine **am \_ WMT- \_ Ereignis \_ Daten** Struktur, die Informationen über das Ereignis im **pData** -Member-Zeiger enthält, sowie einen **HRESULT** -Statuscode, der vom SDK für den Windows Media-Format gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d438f-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="d438f-130">Der Wert von *lParam2* ist abhängig vom Wert von *lParam1*, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d438f-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="d438f-131">(Die "WM \_ "-Strukturen werden im Windows Media-Format-SDK definiert.)</span><span class="sxs-lookup"><span data-stu-id="d438f-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="d438f-132">Wenn lParam1...</span><span class="sxs-lookup"><span data-stu-id="d438f-132">If lParam1 is...</span></span>              | <span data-ttu-id="d438f-133">\_WMT- \_ Ereignis \_ Daten. pdata ist...</span><span class="sxs-lookup"><span data-stu-id="d438f-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d438f-134">WMT \_ keine \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="d438f-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="d438f-135">Ein Zeiger auf eine **WCHAR** -Zeichenfolge, die eine Challenge-URL enthält.</span><span class="sxs-lookup"><span data-stu-id="d438f-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="d438f-136">WMT-Abruf \_ \_ Lizenz</span><span class="sxs-lookup"><span data-stu-id="d438f-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="d438f-137">Ein Zeiger auf eine **WM- \_ get- \_ Lizenz \_ Daten** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d438f-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="d438f-138">WMT \_ keine \_ Rechte \_ Ex</span><span class="sxs-lookup"><span data-stu-id="d438f-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="d438f-139">Ein Zeiger auf eine **WM- \_ get- \_ Lizenz \_ Daten** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d438f-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="d438f-140">WMT \_ erfordert \_ Individualisierung</span><span class="sxs-lookup"><span data-stu-id="d438f-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="d438f-141">NULL.</span><span class="sxs-lookup"><span data-stu-id="d438f-141">NULL.</span></span>                                                       |
| <span data-ttu-id="d438f-142">WMT \_ Individual</span><span class="sxs-lookup"><span data-stu-id="d438f-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="d438f-143">Ein Zeiger auf eine **WM- \_ Individualisierungs \_ Status** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d438f-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="d438f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d438f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d438f-145">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="d438f-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="d438f-146">**DirectShow-qasf-Referenz**</span><span class="sxs-lookup"><span data-stu-id="d438f-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="d438f-147">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="d438f-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




