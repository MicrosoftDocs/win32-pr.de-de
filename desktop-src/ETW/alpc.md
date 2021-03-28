---
description: Diese Klasse ist die übergeordnete Klasse für erweiterte Ereignisse des lokalen Prozedur Aufrufes. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977728"
---
# <a name="alpc-class"></a><span data-ttu-id="f7d4c-104">ALPC-Klasse</span><span class="sxs-lookup"><span data-stu-id="f7d4c-104">ALPC class</span></span>

<span data-ttu-id="f7d4c-105">Diese Klasse ist die übergeordnete Klasse für erweiterte Ereignisse des lokalen Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="f7d4c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d4c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7d4c-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f7d4c-108">Member</span><span class="sxs-lookup"><span data-stu-id="f7d4c-108">Members</span></span>

<span data-ttu-id="f7d4c-109">Die **ALPC** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d4c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7d4c-110">Remarks</span></span>

<span data-ttu-id="f7d4c-111">Um erweiterte Aufruf Ereignisse für lokale Prozeduren in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ ALPC** in dem **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an</span><span class="sxs-lookup"><span data-stu-id="f7d4c-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="f7d4c-112">Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für ALPC-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**alpcguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="f7d4c-113">Verwenden Sie die folgenden Ereignis Typen, um beim Verarbeiten von Ereignissen das tatsächliche ALPC-Ereignis zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="f7d4c-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="f7d4c-114">Event type</span></span>           | <span data-ttu-id="f7d4c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7d4c-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d4c-116">Ereignistyp Wert, 33</span><span class="sxs-lookup"><span data-stu-id="f7d4c-116">Event type value, 33</span></span> | <span data-ttu-id="f7d4c-117">Sende Nachrichten Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-117">Send message event.</span></span> <span data-ttu-id="f7d4c-118">Die " [**ALPC \_ Send \_ Message**](alpc-send-message.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="f7d4c-119">Ereignistyp Wert, 34</span><span class="sxs-lookup"><span data-stu-id="f7d4c-119">Event type value, 34</span></span> | <span data-ttu-id="f7d4c-120">Nachrichten Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-120">Receive message event.</span></span> <span data-ttu-id="f7d4c-121">Die " [**ALPC \_ Receive \_ Message**](alpc-receive-message.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="f7d4c-122">Ereignistyp Wert, 35</span><span class="sxs-lookup"><span data-stu-id="f7d4c-122">Event type value, 35</span></span> | <span data-ttu-id="f7d4c-123">Warten auf Antwort Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-123">Wait for reply event.</span></span> <span data-ttu-id="f7d4c-124">Die [**ALPC \_ Wait \_ for \_ Reply**](alpc-wait-for-reply.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="f7d4c-125">Ereignistyp Wert, 36</span><span class="sxs-lookup"><span data-stu-id="f7d4c-125">Event type value, 36</span></span> | <span data-ttu-id="f7d4c-126">Warten Sie auf das neue Message-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-126">Wait for new message event.</span></span> <span data-ttu-id="f7d4c-127">Die [**ALPC- \_ Wartezeit \_ für die \_ neue \_**](alpc-wait-for-new-message.md) MOF-Nachrichten Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="f7d4c-128">Ereignistyp Wert, 37</span><span class="sxs-lookup"><span data-stu-id="f7d4c-128">Event type value, 37</span></span> | <span data-ttu-id="f7d4c-129">Warten Sie das wartende Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-129">Stop waiting event.</span></span> <span data-ttu-id="f7d4c-130">Die " [**ALPC \_ Unwait**](alpc-unwait.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7d4c-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="f7d4c-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7d4c-131">Requirements</span></span>



| <span data-ttu-id="f7d4c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7d4c-132">Requirement</span></span> | <span data-ttu-id="f7d4c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f7d4c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7d4c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7d4c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d4c-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7d4c-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7d4c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7d4c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d4c-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7d4c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

