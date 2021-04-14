---
title: Komplexer EventType-Typ
description: Definiert den Stamm Knoten des Ereignis Schemas.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType-Ereignisprotokoll (komplexer Typ)
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391586"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="e44f9-104">Komplexer EventType-Typ</span><span class="sxs-lookup"><span data-stu-id="e44f9-104">EventType Complex Type</span></span>

<span data-ttu-id="e44f9-105">Definiert den Stamm Knoten des Ereignis Schemas.</span><span class="sxs-lookup"><span data-stu-id="e44f9-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e44f9-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e44f9-106">Child elements</span></span>



| <span data-ttu-id="e44f9-107">Element</span><span class="sxs-lookup"><span data-stu-id="e44f9-107">Element</span></span>                                                                          | <span data-ttu-id="e44f9-108">type</span><span class="sxs-lookup"><span data-stu-id="e44f9-108">Type</span></span>                                                                               | <span data-ttu-id="e44f9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e44f9-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e44f9-110">**Binaryeventdata**</span><span class="sxs-lookup"><span data-stu-id="e44f9-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="e44f9-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e44f9-111">hexBinary</span></span>                                                                          | <span data-ttu-id="e44f9-112">Enthält die Ereignisdaten als binäres Blob.</span><span class="sxs-lookup"><span data-stu-id="e44f9-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="e44f9-113">Die Ereignisdaten werden als binäres Blob gerendert, wenn die Renderingfunktion die zum Decodieren des Ereignisses verwendeten Metadaten nicht finden kann.</span><span class="sxs-lookup"><span data-stu-id="e44f9-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e44f9-114">**Debug-Daten**</span><span class="sxs-lookup"><span data-stu-id="e44f9-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="e44f9-115">**Debug DataType**</span><span class="sxs-lookup"><span data-stu-id="e44f9-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="e44f9-116">Enthält die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="e44f9-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="e44f9-117">**EVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="e44f9-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="e44f9-118">**Eventdatatype**</span><span class="sxs-lookup"><span data-stu-id="e44f9-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="e44f9-119">Enthält die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e44f9-119">Contains the event data.</span></span> <span data-ttu-id="e44f9-120">Die Reihenfolge der Datenelemente in der Vorlage bestimmt das Layout der Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e44f9-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="e44f9-121">**Processingerrordata**</span><span class="sxs-lookup"><span data-stu-id="e44f9-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="e44f9-122">**Processingerrordatatype**</span><span class="sxs-lookup"><span data-stu-id="e44f9-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="e44f9-123">Enthält Details zu dem Fehler, der beim Versuch aufgetreten ist, das Ereignis zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="e44f9-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="e44f9-124">Dies kann vorkommen, wenn die Ereignisdaten nicht mit der Ereignisdaten Definition im Manifest identisch sind.</span><span class="sxs-lookup"><span data-stu-id="e44f9-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="e44f9-125">Die Ereignisdaten sind als binäres Blob enthalten.</span><span class="sxs-lookup"><span data-stu-id="e44f9-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="e44f9-126">**Renderinginfo**</span><span class="sxs-lookup"><span data-stu-id="e44f9-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="e44f9-127">**Renderinginfotype**</span><span class="sxs-lookup"><span data-stu-id="e44f9-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="e44f9-128">Enthält die gerenderten Meldungs Zeichenfolgen für das Ereignis (einschließlich der Meldungs Zeichenfolge des Ereignisses und der Meldungs Zeichenfolgen für alle Eigenschaften des Ereignisses, z. b. Ebene, Aufgabe und OpCode).</span><span class="sxs-lookup"><span data-stu-id="e44f9-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="e44f9-129">Dieser Abschnitt enthält nur Ereignisse, die mit dem [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="e44f9-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="e44f9-130">**System**</span><span class="sxs-lookup"><span data-stu-id="e44f9-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="e44f9-131">**Systempropertiestype**</span><span class="sxs-lookup"><span data-stu-id="e44f9-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="e44f9-132">Enthält Informationen, die den Anbieter und die Art der Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. den Prozess und die Thread-IDs, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e44f9-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="e44f9-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="e44f9-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="e44f9-134">**Userdatatype**</span><span class="sxs-lookup"><span data-stu-id="e44f9-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="e44f9-135">Enthält die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e44f9-135">Contains the event data.</span></span> <span data-ttu-id="e44f9-136">Der Abschnitt "Benutzerdaten" der Vorlage bestimmt das Layout der Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e44f9-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="e44f9-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e44f9-137">Remarks</span></span>

<span data-ttu-id="e44f9-138">In der Regel enthält dieser Abschnitt den Abschnitt " **EventData** " oder " **UserData** ".</span><span class="sxs-lookup"><span data-stu-id="e44f9-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="e44f9-139">Der **EventData** -Abschnitt wird verwendet, wenn die Vorlage keinen **UserData** -Abschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="e44f9-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44f9-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e44f9-140">Requirements</span></span>



| <span data-ttu-id="e44f9-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e44f9-141">Requirement</span></span> | <span data-ttu-id="e44f9-142">Wert</span><span class="sxs-lookup"><span data-stu-id="e44f9-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e44f9-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e44f9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e44f9-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e44f9-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e44f9-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e44f9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e44f9-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e44f9-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

