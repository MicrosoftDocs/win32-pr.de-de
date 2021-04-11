---
title: Imsrdpinputsink-Schnittstelle
description: Eingabe Senke für Remote Desktop.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Imsrdpinputsink-Schnittstelle Remotedesktopdienste
- Imsrdpinputsink-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949626"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="79e91-105">Imsrdpinputsink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="79e91-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="79e91-106">Eingabe Senke für Remote Desktop.</span><span class="sxs-lookup"><span data-stu-id="79e91-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="79e91-107">Member</span><span class="sxs-lookup"><span data-stu-id="79e91-107">Members</span></span>

<span data-ttu-id="79e91-108">Die **imsrdpinputsink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="79e91-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="79e91-109">**Imsrdpinputsink** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79e91-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="79e91-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="79e91-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79e91-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="79e91-111">Methods</span></span>

<span data-ttu-id="79e91-112">Die **imsrdpinputsink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="79e91-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="79e91-113">Methode</span><span class="sxs-lookup"><span data-stu-id="79e91-113">Method</span></span>                                                               | <span data-ttu-id="79e91-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e91-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="79e91-115">[**Addtouchinput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="79e91-116">Fügt Berührungs Eingaben hinzu.</span><span class="sxs-lookup"><span data-stu-id="79e91-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="79e91-117">[**Begintouchframe**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="79e91-118">Beginn des Berührungs Rahmens.</span><span class="sxs-lookup"><span data-stu-id="79e91-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="79e91-119">[**Endtouchframe**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="79e91-120">Ende des Berührungs Rahmens.</span><span class="sxs-lookup"><span data-stu-id="79e91-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="79e91-121">[**Sendkeyboarde Vent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="79e91-122">Sendet ein Tastaturereignis.</span><span class="sxs-lookup"><span data-stu-id="79e91-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="79e91-123">[**Sendmouslibuttonevent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="79e91-124">Sendet das Maustasten Ereignis.</span><span class="sxs-lookup"><span data-stu-id="79e91-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="79e91-125">[**Sendmoussmuveevent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="79e91-126">Sendet das MouseMove-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="79e91-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="79e91-127">[**Sendmouserwheelevent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="79e91-128">Sendet ein Mausrad Ereignis.</span><span class="sxs-lookup"><span data-stu-id="79e91-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="79e91-129">[**Sendsyncevent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79e91-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="79e91-130">Sendet ein Synchronisierungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="79e91-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="79e91-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79e91-131">Requirements</span></span>



| <span data-ttu-id="79e91-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79e91-132">Requirement</span></span> | <span data-ttu-id="79e91-133">Wert</span><span class="sxs-lookup"><span data-stu-id="79e91-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e91-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79e91-134">Minimum supported client</span></span><br/> | <span data-ttu-id="79e91-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79e91-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="79e91-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79e91-136">Minimum supported server</span></span><br/> | <span data-ttu-id="79e91-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79e91-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="79e91-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="79e91-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="79e91-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e91-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e91-140">DLL</span><span class="sxs-lookup"><span data-stu-id="79e91-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e91-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e91-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79e91-142">IID</span><span class="sxs-lookup"><span data-stu-id="79e91-142">IID</span></span><br/>                      | <span data-ttu-id="79e91-143">IID \_ imsrdpinputsink ist definiert als 4606850e-76a7-4e28-a47e-c7174f 619351</span><span class="sxs-lookup"><span data-stu-id="79e91-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

