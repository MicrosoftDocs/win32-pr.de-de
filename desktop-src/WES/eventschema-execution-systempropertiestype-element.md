---
title: Execution (systempropertiestype)-Element
description: Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Ausführungs Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740360"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="bbc11-104">Execution (systempropertiestype)-Element</span><span class="sxs-lookup"><span data-stu-id="bbc11-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="bbc11-105">Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="bbc11-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="bbc11-106">Das **Execution** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="bbc11-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="bbc11-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="bbc11-107">Attributes</span></span>



| <span data-ttu-id="bbc11-108">Name</span><span class="sxs-lookup"><span data-stu-id="bbc11-108">Name</span></span>          | <span data-ttu-id="bbc11-109">type</span><span class="sxs-lookup"><span data-stu-id="bbc11-109">Type</span></span>         | <span data-ttu-id="bbc11-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbc11-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc11-111">Kernelzeit</span><span class="sxs-lookup"><span data-stu-id="bbc11-111">KernelTime</span></span>    | <span data-ttu-id="bbc11-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-112">unsignedInt</span></span>  | <span data-ttu-id="bbc11-113">Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Zeiteinheiten.</span><span class="sxs-lookup"><span data-stu-id="bbc11-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="bbc11-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="bbc11-114">ProcessID</span></span>     | <span data-ttu-id="bbc11-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-115">unsignedInt</span></span>  | <span data-ttu-id="bbc11-116">Gibt den Prozess an, der das Ereignis generiert hat</span><span class="sxs-lookup"><span data-stu-id="bbc11-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="bbc11-117">ProcessorId</span><span class="sxs-lookup"><span data-stu-id="bbc11-117">ProcessorID</span></span>   | <span data-ttu-id="bbc11-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="bbc11-118">unsignedByte</span></span> | <span data-ttu-id="bbc11-119">Die Identifikationsnummer für den Prozessor, der das Ereignis verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="bbc11-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="bbc11-120">Processortime</span><span class="sxs-lookup"><span data-stu-id="bbc11-120">ProcessorTime</span></span> | <span data-ttu-id="bbc11-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-121">unsignedInt</span></span>  | <span data-ttu-id="bbc11-122">Für private ETW-Sitzungen die verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks.</span><span class="sxs-lookup"><span data-stu-id="bbc11-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="bbc11-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="bbc11-123">SessionID</span></span>     | <span data-ttu-id="bbc11-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-124">unsignedInt</span></span>  | <span data-ttu-id="bbc11-125">Die Identifikationsnummer für die Terminal Server Sitzung, in der das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bbc11-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="bbc11-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="bbc11-126">ThreadID</span></span>      | <span data-ttu-id="bbc11-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-127">unsignedInt</span></span>  | <span data-ttu-id="bbc11-128">Gibt den Thread an, der das Ereignis generiert hat</span><span class="sxs-lookup"><span data-stu-id="bbc11-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="bbc11-129">Usertime</span><span class="sxs-lookup"><span data-stu-id="bbc11-129">UserTime</span></span>      | <span data-ttu-id="bbc11-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbc11-130">unsignedInt</span></span>  | <span data-ttu-id="bbc11-131">Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Zeiteinheiten.</span><span class="sxs-lookup"><span data-stu-id="bbc11-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="bbc11-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbc11-132">Requirements</span></span>



| <span data-ttu-id="bbc11-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbc11-133">Requirement</span></span> | <span data-ttu-id="bbc11-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bbc11-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbc11-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbc11-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc11-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbc11-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbc11-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbc11-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc11-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbc11-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbc11-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbc11-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbc11-140">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="bbc11-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbc11-141">**Systempropertiestype**</span><span class="sxs-lookup"><span data-stu-id="bbc11-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="bbc11-142">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="bbc11-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbc11-143">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="bbc11-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





