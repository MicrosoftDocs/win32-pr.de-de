---
description: Initiiert die Kommunikation mit einem Ereignis Anbieter unter Verwendung eines eingeschränkten Satzes von Abfragen.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Iwbemeventsink-Schnittstelle (wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364123"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="f2de3-103">Iwbemeventsink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f2de3-103">IWbemEventSink interface</span></span>

<span data-ttu-id="f2de3-104">Die **iwbemeventsink** -Schnittstelle initiiert die Kommunikation mit einem Ereignis Anbieter unter Verwendung eines eingeschränkten Satzes von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f2de3-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="f2de3-105">Diese Schnittstelle erweitert [**iwbebobjectsink**](iwbemobjectsink.md)und bietet neue Methoden für Sicherheit und Leistung.</span><span class="sxs-lookup"><span data-stu-id="f2de3-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="f2de3-106">Weitere Informationen zum Verwenden dieser Schnittstelle finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md) und [Sichern von WMI-Ereignissen](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="f2de3-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="f2de3-107">Member</span><span class="sxs-lookup"><span data-stu-id="f2de3-107">Members</span></span>

<span data-ttu-id="f2de3-108">Die **iwbemeventsink** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f2de3-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="f2de3-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f2de3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f2de3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f2de3-110">Methods</span></span>

<span data-ttu-id="f2de3-111">Die **iwbemeventsink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f2de3-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="f2de3-112">Methode</span><span class="sxs-lookup"><span data-stu-id="f2de3-112">Method</span></span>                                                                | <span data-ttu-id="f2de3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2de3-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="f2de3-114">**Getrestrictedsink**</span><span class="sxs-lookup"><span data-stu-id="f2de3-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="f2de3-115">Wird vom Consumer aufgerufen, um eingeschränkte Ereignis Abfragen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f2de3-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="f2de3-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="f2de3-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="f2de3-117">Überprüft den Status der Ereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="f2de3-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="f2de3-118">**Setbatchingparameters**</span><span class="sxs-lookup"><span data-stu-id="f2de3-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="f2de3-119">Wird vom Consumer aufgerufen, um Batch Verarbeitungsparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f2de3-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="f2de3-120">**Setsink Security**</span><span class="sxs-lookup"><span data-stu-id="f2de3-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="f2de3-121">Wird verwendet, um die Sicherheits Beschreibung für eine Ereignis Senke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f2de3-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="f2de3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2de3-122">Remarks</span></span>

<span data-ttu-id="f2de3-123">Wenn Sie eine Ereignis-Abonnement-Senke ([**iwbewbjectsink**](iwbemobjectsink.md) oder **iwbemeventsink**) implementieren, sollten Sie in den Methoden des Sink-Objekts nicht WMI aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2de3-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="f2de3-124">Beispielsweise kann das Aufrufen von [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) zum Abbrechen der Senke in einer Implementierung von [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) den WMI-Status beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f2de3-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="f2de3-125">Um ein Ereignis Abonnement abzubrechen, legen Sie ein Flag fest, und rufen Sie **IWbemServices:: cancelasynccall** von einem anderen Thread oder Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="f2de3-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="f2de3-126">Bei Implementierungen, die sich nicht auf eine Ereignis Senke beziehen, wie z. b. Object-, enum-und Abfrage-Abruf Werte, können Sie einen Rückruf in WMI durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="f2de3-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="f2de3-127">Sink-Implementierungen sollten die Ereignis Benachrichtigung innerhalb von 100 MS verarbeiten, weil der WMI-Thread, der die Ereignis Benachrichtigung übermittelt, erst dann andere Aufgaben ausführen kann, wenn die Verarbeitung des Sink-Objekts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f2de3-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="f2de3-128">Wenn für die Benachrichtigung eine große Menge an Verarbeitung erforderlich ist, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f2de3-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2de3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2de3-129">Requirements</span></span>



| <span data-ttu-id="f2de3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2de3-130">Requirement</span></span> | <span data-ttu-id="f2de3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f2de3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2de3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2de3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2de3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2de3-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="f2de3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2de3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2de3-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2de3-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="f2de3-136">Header</span><span class="sxs-lookup"><span data-stu-id="f2de3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2de3-137"><dt>Wbemprov. h (Include wbemittell. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2de3-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f2de3-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2de3-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2de3-139"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2de3-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f2de3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f2de3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2de3-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2de3-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f2de3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2de3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2de3-143">COM-API für WMI</span><span class="sxs-lookup"><span data-stu-id="f2de3-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




