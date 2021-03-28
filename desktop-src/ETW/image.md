---
description: Diese Klasse ist die übergeordnete Klasse für Image-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Image-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979872"
---
# <a name="image-class"></a><span data-ttu-id="91861-104">Image-Klasse</span><span class="sxs-lookup"><span data-stu-id="91861-104">Image class</span></span>

<span data-ttu-id="91861-105">Diese Klasse ist die übergeordnete Klasse für Image-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="91861-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="91861-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="91861-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="91861-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91861-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="91861-108">Member</span><span class="sxs-lookup"><span data-stu-id="91861-108">Members</span></span>

<span data-ttu-id="91861-109">Die **Image** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="91861-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="91861-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91861-110">Remarks</span></span>

<span data-ttu-id="91861-111">Um Bild Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Ablaufverfolgungsflag für das Ereignis Ablaufverfolgungsflag im **enableflags** -Member der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91861-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="91861-112">Ereignisablaufverfolgungslistener können eine spezielle Verarbeitung für Bild Lade Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**imageloadguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="91861-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="91861-113">Verwenden Sie die folgenden Ereignis Typen, um Bild Lade Ereignisse beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="91861-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="91861-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="91861-114">Event type</span></span>                                                          | <span data-ttu-id="91861-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91861-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91861-116">**Ereignis \_ \_ \_ Laden von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="91861-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="91861-117">Bild Lade Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-117">Image load event.</span></span> <span data-ttu-id="91861-118">Wird generiert, wenn eine DLL oder eine ausführbare Datei geladen wird.</span><span class="sxs-lookup"><span data-stu-id="91861-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="91861-119">Der Anbieter generiert nur ein Ereignis zum ersten Mal, wenn eine bestimmte dll geladen wird.</span><span class="sxs-lookup"><span data-stu-id="91861-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="91861-120">Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="91861-121">**Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)</span><span class="sxs-lookup"><span data-stu-id="91861-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="91861-122">Bild Entlade Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-122">Image unload event.</span></span> <span data-ttu-id="91861-123">Wird generiert, wenn eine DLL oder eine ausführbare Datei entladen wird.</span><span class="sxs-lookup"><span data-stu-id="91861-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="91861-124">Der Anbieter generiert nur ein Ereignis für den letzten Zeitpunkt, an dem eine bestimmte DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="91861-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="91861-125">Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="91861-126">**Ereignis \_ Ablauf Verfolgungs \_ Typen- \_ DC- \_ Start**(Ereignistyp Wert ist 3)</span><span class="sxs-lookup"><span data-stu-id="91861-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="91861-127">Start Ereignis für die Datensammlung.</span><span class="sxs-lookup"><span data-stu-id="91861-127">Data collection start event.</span></span> <span data-ttu-id="91861-128">Listet alle geladenen Bilder am Anfang der Ablauf Verfolgung auf.</span><span class="sxs-lookup"><span data-stu-id="91861-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="91861-129">Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="91861-130">**Ereignis \_ Trace- \_ Typ- \_ DC- \_ Ende**(Ereignistyp Wert ist 4)</span><span class="sxs-lookup"><span data-stu-id="91861-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="91861-131">Ereignis zum Beenden der Datensammlung.</span><span class="sxs-lookup"><span data-stu-id="91861-131">Data collection end event.</span></span> <span data-ttu-id="91861-132">Listet alle geladenen Bilder am Ende der Ablauf Verfolgung auf.</span><span class="sxs-lookup"><span data-stu-id="91861-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="91861-133">Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="91861-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="91861-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91861-134">Requirements</span></span>



| <span data-ttu-id="91861-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91861-135">Requirement</span></span> | <span data-ttu-id="91861-136">Wert</span><span class="sxs-lookup"><span data-stu-id="91861-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91861-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91861-137">Minimum supported client</span></span><br/> | <span data-ttu-id="91861-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91861-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91861-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91861-139">Minimum supported server</span></span><br/> | <span data-ttu-id="91861-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91861-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91861-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91861-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91861-142">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="91861-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="91861-143">**Laden von Bildern \_**</span><span class="sxs-lookup"><span data-stu-id="91861-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="91861-144">**Bild \_ v0**</span><span class="sxs-lookup"><span data-stu-id="91861-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="91861-145">**Bild \_ v1**</span><span class="sxs-lookup"><span data-stu-id="91861-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
