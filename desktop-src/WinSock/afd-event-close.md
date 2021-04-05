---
description: Winsock-Netzwerkablaufverfolgungs-Ereignis für SocketClose.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751488"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="7caf4-103">Ereignis zum Schließen von AFD- \_ Ereignissen \_</span><span class="sxs-lookup"><span data-stu-id="7caf4-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="7caf4-104">Das Ereignis für die **AFD- \_ Ereignis \_ Schließung** ist ein Winsock-Netzwerk Ablauf Verfolgungs Ereignis für den socketschließ Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7caf4-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="7caf4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7caf4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7caf4-106">*Enterexit*</span><span class="sxs-lookup"><span data-stu-id="7caf4-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf4-107">Informationen zu diesem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7caf4-107">Information on this event.</span></span>

<span data-ttu-id="7caf4-108">In der folgenden Tabelle sind die möglichen Werte für den Parameter " *enterexit* " aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="7caf4-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="7caf4-109">Wert</span><span class="sxs-lookup"><span data-stu-id="7caf4-109">Value</span></span>                                                                        | <span data-ttu-id="7caf4-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7caf4-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7caf4-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7caf4-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7caf4-112">Der Start einer Winsock-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7caf4-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7caf4-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7caf4-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7caf4-114">Die Winsock-Anforderung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7caf4-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7caf4-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7caf4-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7caf4-116">Der Winsock-AFD-Treiber hat eine interne Aktion ausgeführt (z. b. eine Verbindung abgebrochen).</span><span class="sxs-lookup"><span data-stu-id="7caf4-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="7caf4-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7caf4-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7caf4-118">Der TCP/IP-Treiber hat dieses Ereignis verursacht.</span><span class="sxs-lookup"><span data-stu-id="7caf4-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="7caf4-119">Dies weist normalerweise auf eine Daten Benachrichtigung hin.</span><span class="sxs-lookup"><span data-stu-id="7caf4-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="7caf4-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7caf4-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="7caf4-121">Der Winsock-AFD-Treiber hat dieses Ereignis ausgelöst (z. b. das Festlegen einer Socketoption).</span><span class="sxs-lookup"><span data-stu-id="7caf4-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7caf4-122">*Location*</span><span class="sxs-lookup"><span data-stu-id="7caf4-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf4-123">Ein privates Feld, das intern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7caf4-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="7caf4-124">*Prozess*</span><span class="sxs-lookup"><span data-stu-id="7caf4-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf4-125">Die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Adresse des Prozesses, der den zugehörigen Socket besitzt.</span><span class="sxs-lookup"><span data-stu-id="7caf4-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="7caf4-126">Dies ist eine nicht transparente Struktur, die als Prozess Objekt für einen Prozess dient.</span><span class="sxs-lookup"><span data-stu-id="7caf4-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="7caf4-127">Weitere Informationen finden Sie in der Dokumentation zum Windows-Treiberkit für die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7caf4-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7caf4-128">*Endpunkt*</span><span class="sxs-lookup"><span data-stu-id="7caf4-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf4-129">Die AFD- \_ Endpunkt Adresse des Sockets.</span><span class="sxs-lookup"><span data-stu-id="7caf4-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="7caf4-130">*Status*</span><span class="sxs-lookup"><span data-stu-id="7caf4-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="7caf4-131">Der NTSTATUS-Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7caf4-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7caf4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7caf4-132">Remarks</span></span>

<span data-ttu-id="7caf4-133">Das Ereignis für die **AFD- \_ Ereignis \_ Schließung** wird nachverfolgt, wenn ein Winsock-Netzwerk Vorgang einen Socket schließt.</span><span class="sxs-lookup"><span data-stu-id="7caf4-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="7caf4-134">Der Kanal für dieses Ereignis ist Winsock-AFD.</span><span class="sxs-lookup"><span data-stu-id="7caf4-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="7caf4-135">Die Ebene für dieses Ereignis dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="7caf4-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="7caf4-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7caf4-136">Requirements</span></span>



| <span data-ttu-id="7caf4-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7caf4-137">Requirement</span></span> | <span data-ttu-id="7caf4-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7caf4-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7caf4-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7caf4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7caf4-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7caf4-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7caf4-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7caf4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7caf4-142">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7caf4-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7caf4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7caf4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7caf4-144">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="7caf4-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7caf4-145">**Ereignis \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="7caf4-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="7caf4-146">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="7caf4-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7caf4-147">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="7caf4-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="7caf4-148">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="7caf4-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

