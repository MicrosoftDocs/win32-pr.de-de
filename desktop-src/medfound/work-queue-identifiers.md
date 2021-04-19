---
description: Die folgenden Konstanten identifizieren die Standard-Media Foundation Arbeits Warteschlangen.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Arbeitswarteschlangen-IDs (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367980"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="00f5c-103">Bezeichner der Arbeits Warteschlange</span><span class="sxs-lookup"><span data-stu-id="00f5c-103">Work Queue Identifiers</span></span>

<span data-ttu-id="00f5c-104">Die folgenden Konstanten identifizieren die Standard-Media Foundation Arbeits Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="00f5c-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="00f5c-105">Anwendungen sollten die mfasync- \_ Rückruf \_ Warteschlange \_ Multithreaded verwenden oder eine Arbeits Warteschlange verwenden, die von [**mflocksharedworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) abgerufen wird, wenn Sie die Ausführungs Priorität steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="00f5c-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="00f5c-106">Beachten Sie, dass sich die Standard Prioritäten der Plattform für die Arbeits Warteschlange dynamisch ändern können, wenn eine Anwendung [**registerplatformwithmmcss**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)aufruft.</span><span class="sxs-lookup"><span data-stu-id="00f5c-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="00f5c-107">Weitere Informationen zu Arbeits Warteschlangen finden Sie unter [Arbeits Warteschlangen](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="00f5c-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="00f5c-108">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="00f5c-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="00f5c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00f5c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="00f5c-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-111">In den meisten Fällen sollten Anwendungen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>verwenden.</span><span class="sxs-lookup"><span data-stu-id="00f5c-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="00f5c-112">Diese Arbeits Warteschlange wird für synchrone Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="00f5c-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="00f5c-113">Die Verwendung der Standard Arbeits Warteschlange kann das Risiko eines Deadlocks darstellen.</span><span class="sxs-lookup"><span data-stu-id="00f5c-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="00f5c-114">Anwendungen können eine private synchrone Warteschlange oberhalb der multithreadwarteschlange erstellen, indem Sie <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MF belegereserialworkqueue</strong></a>verwenden.</span><span class="sxs-lookup"><span data-stu-id="00f5c-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="00f5c-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-116">Nicht für allgemeine Anwendungs Verwendung.</span><span class="sxs-lookup"><span data-stu-id="00f5c-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="00f5c-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-118">Nicht für allgemeine Anwendungs Verwendung.</span><span class="sxs-lookup"><span data-stu-id="00f5c-118">Not for general application use.</span></span><br/> <span data-ttu-id="00f5c-119">Diese Arbeits Warteschlange wird intern für e/a-Vorgänge wie das Lesen von Dateien und das Lesen aus dem Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="00f5c-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="00f5c-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-121">Nicht für allgemeine Anwendungs Verwendung.</span><span class="sxs-lookup"><span data-stu-id="00f5c-121">Not for general application use.</span></span><br/> <span data-ttu-id="00f5c-122">Diese Arbeits Warteschlange wird für regelmäßige Rückrufe und geplante Arbeitselemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="00f5c-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="00f5c-123">Die folgenden Funktionen stellen Arbeitsaufgaben in diese Warteschlange:</span><span class="sxs-lookup"><span data-stu-id="00f5c-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="00f5c-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>Mfaddperiodiccallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="00f5c-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="00f5c-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MF scheduleworkitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="00f5c-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="00f5c-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MF scheduleworkitemex</strong></a></span><span class="sxs-lookup"><span data-stu-id="00f5c-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="00f5c-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005 bei der</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-128">Diese Multithread-Arbeits Warteschlange sollte in den meisten Fällen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00f5c-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="00f5c-129">Diese Arbeits Warteschlange wird für asynchrone Vorgänge in Media Foundation verwendet.</span><span class="sxs-lookup"><span data-stu-id="00f5c-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="00f5c-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="00f5c-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00f5c-131">Nicht für allgemeine Anwendungs Verwendung.</span><span class="sxs-lookup"><span data-stu-id="00f5c-131">Not for general application use.</span></span> <span data-ttu-id="00f5c-132">Anwendungen sollten stattdessen <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>verwenden.</span><span class="sxs-lookup"><span data-stu-id="00f5c-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="00f5c-133">Außerdem werden die folgenden Konstanten in Verbindung mit Arbeits Warteschlangen verwendet.</span><span class="sxs-lookup"><span data-stu-id="00f5c-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="00f5c-134">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="00f5c-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="00f5c-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00f5c-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="00f5c-136"><dt>**Mfasync \_ Rückruf \_ Warteschlange nicht \_ definiert**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="00f5c-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="00f5c-137">Nicht definierte Arbeits Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="00f5c-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="00f5c-138"><dt>**Mfasync \_ \_ \_ Private \_ Maske der Rückruf Warteschlange**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="00f5c-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="00f5c-139">Bitmaske zur Unterscheidung von Platt Form Arbeitswarteschlangen von den durch Aufrufen von [**mfbelegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)erstellten.</span><span class="sxs-lookup"><span data-stu-id="00f5c-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="00f5c-140">Für eine Arbeits Warteschlange, die von [**MF belegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)erstellt wurde, ist der folgende Wert ungleich 0 (null):</span><span class="sxs-lookup"><span data-stu-id="00f5c-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="00f5c-141"><dt>**Mfasync \_ Rückruf \_ Warteschlange \_ alle**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="00f5c-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="00f5c-142">Alle Platt Form Arbeitswarteschlangen.</span><span class="sxs-lookup"><span data-stu-id="00f5c-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="00f5c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00f5c-143">Requirements</span></span>



| <span data-ttu-id="00f5c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00f5c-144">Requirement</span></span> | <span data-ttu-id="00f5c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="00f5c-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f5c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00f5c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="00f5c-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00f5c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00f5c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00f5c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="00f5c-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00f5c-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00f5c-150">Header</span><span class="sxs-lookup"><span data-stu-id="00f5c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f5c-151"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00f5c-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00f5c-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00f5c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00f5c-153">Media Foundation Konstanten</span><span class="sxs-lookup"><span data-stu-id="00f5c-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="00f5c-154">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="00f5c-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="00f5c-155">Arbeits Warteschlangen und Threading</span><span class="sxs-lookup"><span data-stu-id="00f5c-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




