---
title: Komplexer systempropertiestype-Typ
description: Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. die Prozess-und Thread-IDs.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Ereignisprotokoll für komplexen systempropertiestype-Typ
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742721"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="69e1f-104">Komplexer systempropertiestype-Typ</span><span class="sxs-lookup"><span data-stu-id="69e1f-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="69e1f-105">Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. die Prozess-und Thread-IDs.</span><span class="sxs-lookup"><span data-stu-id="69e1f-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
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
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="69e1f-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69e1f-106">Child elements</span></span>



| <span data-ttu-id="69e1f-107">Element</span><span class="sxs-lookup"><span data-stu-id="69e1f-107">Element</span></span>                                                                         | <span data-ttu-id="69e1f-108">type</span><span class="sxs-lookup"><span data-stu-id="69e1f-108">Type</span></span>                                                        | <span data-ttu-id="69e1f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69e1f-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69e1f-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="69e1f-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="69e1f-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="69e1f-111">anyURI</span></span>                                                      | <span data-ttu-id="69e1f-112">Der Kanal, auf dem das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="69e1f-113">**Computer**</span><span class="sxs-lookup"><span data-stu-id="69e1f-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="69e1f-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="69e1f-114">string</span></span>                                                      | <span data-ttu-id="69e1f-115">Der Name des Computers, auf dem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="69e1f-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="69e1f-116">**Ungs**</span><span class="sxs-lookup"><span data-stu-id="69e1f-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="69e1f-117">Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="69e1f-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="69e1f-118">**EventID**</span><span class="sxs-lookup"><span data-stu-id="69e1f-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="69e1f-119">Der Bezeichner, den der Anbieter verwendet hat, um das Ereignis zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69e1f-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="69e1f-120">**Eventrecordid**</span><span class="sxs-lookup"><span data-stu-id="69e1f-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="69e1f-121">Die Datensatznummer, die dem Ereignis bei der Protokollierung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="69e1f-122">**Ausführung**</span><span class="sxs-lookup"><span data-stu-id="69e1f-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="69e1f-123">Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="69e1f-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="69e1f-124">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="69e1f-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="69e1f-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="69e1f-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="69e1f-126">Eine Bitmaske der Schlüsselwörter, die im Ereignis definiert sind.</span><span class="sxs-lookup"><span data-stu-id="69e1f-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="69e1f-127">Schlüsselwörter werden verwendet, um Ereignis Typen zu klassifizieren (z. b. Ereignisse, die dem Lesen von Daten zugeordnet sind).</span><span class="sxs-lookup"><span data-stu-id="69e1f-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="69e1f-128">**Geringen**</span><span class="sxs-lookup"><span data-stu-id="69e1f-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="69e1f-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="69e1f-129">unsignedByte</span></span>                                                | <span data-ttu-id="69e1f-130">Der im Ereignis definierte Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="69e1f-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="69e1f-131">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="69e1f-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="69e1f-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="69e1f-132">unsignedByte</span></span>                                                | <span data-ttu-id="69e1f-133">Der im Ereignis definierte Opcode.</span><span class="sxs-lookup"><span data-stu-id="69e1f-133">The opcode defined in the event.</span></span> <span data-ttu-id="69e1f-134">Task und Opcode werden typlogisch verwendet, um die Position in der Anwendung zu identifizieren, von der das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="69e1f-135">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="69e1f-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="69e1f-136">Identifiziert den Anbieter, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="69e1f-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="69e1f-137">Die Attribute **Name** und **GUID** sind enthalten, wenn der Anbieter ein Instrumentierungs Manifest zum Definieren der Ereignisse verwendet hat. Andernfalls wird das **eventSourceName** -Attribut eingeschlossen, wenn das Ereignis von einem Legacy Ereignis Anbieter (mit der [Ereignis Protokollierungs](/windows/desktop/EventLog/event-logging) -API) protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="69e1f-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="69e1f-138">**Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="69e1f-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="69e1f-139">Identifiziert den Benutzer, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="69e1f-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="69e1f-140">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="69e1f-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="69e1f-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="69e1f-141">unsignedShort</span></span>                                               | <span data-ttu-id="69e1f-142">Die im Ereignis definierte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="69e1f-142">The task defined in the event.</span></span> <span data-ttu-id="69e1f-143">Task und Opcode werden in der Regel verwendet, um die Position in der Anwendung zu identifizieren, von der das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="69e1f-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="69e1f-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="69e1f-145">Der Zeitstempel, der angibt, wann das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="69e1f-146">Der Zeitstempel schließt entweder das **SYSTEMTIME** -Attribut oder das **rawtime** -Attribut ein.</span><span class="sxs-lookup"><span data-stu-id="69e1f-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="69e1f-147">**Version**</span><span class="sxs-lookup"><span data-stu-id="69e1f-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="69e1f-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="69e1f-148">unsignedByte</span></span>                                                | <span data-ttu-id="69e1f-149">Die Versionsnummer der Ereignis Definition.</span><span class="sxs-lookup"><span data-stu-id="69e1f-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="69e1f-150">Attributes</span><span class="sxs-lookup"><span data-stu-id="69e1f-150">Attributes</span></span>



| <span data-ttu-id="69e1f-151">Name</span><span class="sxs-lookup"><span data-stu-id="69e1f-151">Name</span></span>              | <span data-ttu-id="69e1f-152">type</span><span class="sxs-lookup"><span data-stu-id="69e1f-152">Type</span></span>                                                | <span data-ttu-id="69e1f-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69e1f-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e1f-154">Aktivitäts-ID</span><span class="sxs-lookup"><span data-stu-id="69e1f-154">ActivityID</span></span>        | [<span data-ttu-id="69e1f-155">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="69e1f-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="69e1f-156">Ein-Globally Unique Identifier, der die aktuelle Aktivität bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="69e1f-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="69e1f-157">Die mit diesem Bezeichner veröffentlichten Ereignisse sind Teil derselben Aktivität.</span><span class="sxs-lookup"><span data-stu-id="69e1f-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="69e1f-158">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="69e1f-158">EventSourceName</span></span>   | <span data-ttu-id="69e1f-159">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="69e1f-159">string</span></span>                                              | <span data-ttu-id="69e1f-160">Der Name der Ereignis Quelle, die das Ereignis veröffentlicht hat (wenn die Ereignis Quelle von der Legacy- [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API stammt).</span><span class="sxs-lookup"><span data-stu-id="69e1f-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="69e1f-161">GUID</span><span class="sxs-lookup"><span data-stu-id="69e1f-161">Guid</span></span>              | [<span data-ttu-id="69e1f-162">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="69e1f-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="69e1f-163">Der Globally Unique Identifier, der den Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="69e1f-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="69e1f-164">Kernelzeit</span><span class="sxs-lookup"><span data-stu-id="69e1f-164">KernelTime</span></span>        | <span data-ttu-id="69e1f-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-165">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-166">Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Zeiteinheiten.</span><span class="sxs-lookup"><span data-stu-id="69e1f-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="69e1f-167">Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im processortime-Member.</span><span class="sxs-lookup"><span data-stu-id="69e1f-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="69e1f-168">Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="69e1f-169">Name</span><span class="sxs-lookup"><span data-stu-id="69e1f-169">Name</span></span>              | <span data-ttu-id="69e1f-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="69e1f-170">anyURI</span></span>                                              | <span data-ttu-id="69e1f-171">Der Name des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="69e1f-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="69e1f-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="69e1f-172">ProcessID</span></span>         | <span data-ttu-id="69e1f-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-173">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-174">Gibt den Prozess an, der das Ereignis generiert hat</span><span class="sxs-lookup"><span data-stu-id="69e1f-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="69e1f-175">ProcessorId</span><span class="sxs-lookup"><span data-stu-id="69e1f-175">ProcessorID</span></span>       | <span data-ttu-id="69e1f-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="69e1f-176">unsignedByte</span></span>                                        | <span data-ttu-id="69e1f-177">Die Identifikationsnummer für den Prozessor, der das Ereignis verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="69e1f-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="69e1f-178">Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="69e1f-179">Processortime</span><span class="sxs-lookup"><span data-stu-id="69e1f-179">ProcessorTime</span></span>     | <span data-ttu-id="69e1f-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-180">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-181">Für private ETW-Sitzungen die verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks.</span><span class="sxs-lookup"><span data-stu-id="69e1f-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="69e1f-182">Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="69e1f-183">Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="69e1f-183">Qualifiers</span></span>        | <span data-ttu-id="69e1f-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="69e1f-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="69e1f-185">Ein Legacy Anbieter verwendet eine 32-Bit-Nummer, um seine Ereignisse zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69e1f-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="69e1f-186">Wenn das Ereignis von einem Legacy Anbieter protokolliert wird, enthält der Wert des **EventID-** Elements die nieder wertigen 16 Bits des Ereignis Bezeichners, und das **qualifiziererattribut** enthält die höherwertigen 16 Bits des Ereignis Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="69e1f-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="69e1f-187">Rawtime</span><span class="sxs-lookup"><span data-stu-id="69e1f-187">RawTime</span></span>           | <span data-ttu-id="69e1f-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="69e1f-188">unsignedLong</span></span>                                        | <span data-ttu-id="69e1f-189">Der rohzeit Stempel Wert. das Format des Zeitstempels hängt von der Zeit Quelle ab, die zum Erfassen der Ablauf Verfolgung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69e1f-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="69e1f-190">Der unformatierte Zeitstempel bietet eine höhere Genauigkeit als die Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="69e1f-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="69e1f-191">Die gerenderte Ereignis Ausgabe enthält nur eine unformatierte Zeit, wenn Sie TraceRpt.exe mit dem Schalter-RTS verwenden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="69e1f-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="69e1f-192">RelatedActivityID</span></span> | [<span data-ttu-id="69e1f-193">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="69e1f-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="69e1f-194">Ein-Globally Unique Identifier, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="69e1f-195">Die zugehörigen Ereignisse haben dann diesen Bezeichner als ActivityId-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="69e1f-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="69e1f-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="69e1f-196">SessionID</span></span>         | <span data-ttu-id="69e1f-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-197">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-198">Die Identifikationsnummer für die Terminal Server Sitzung, in der das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="69e1f-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="69e1f-199">Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="69e1f-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="69e1f-200">SystemTime</span></span>        | <span data-ttu-id="69e1f-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="69e1f-201">dateTime</span></span>                                            | <span data-ttu-id="69e1f-202">Die Systemzeit, zu der das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e1f-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="69e1f-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="69e1f-203">ThreadID</span></span>          | <span data-ttu-id="69e1f-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-204">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-205">Gibt den Thread an, der das Ereignis generiert hat</span><span class="sxs-lookup"><span data-stu-id="69e1f-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="69e1f-206">UserID</span><span class="sxs-lookup"><span data-stu-id="69e1f-206">UserID</span></span>            | <span data-ttu-id="69e1f-207">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="69e1f-207">string</span></span>                                              | <span data-ttu-id="69e1f-208">Die Sicherheits-ID (SID) des Benutzers in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="69e1f-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="69e1f-209">Usertime</span><span class="sxs-lookup"><span data-stu-id="69e1f-209">UserTime</span></span>          | <span data-ttu-id="69e1f-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1f-210">unsignedInt</span></span>                                         | <span data-ttu-id="69e1f-211">Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Zeiteinheiten.</span><span class="sxs-lookup"><span data-stu-id="69e1f-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="69e1f-212">Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im processortime-Member.</span><span class="sxs-lookup"><span data-stu-id="69e1f-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="69e1f-213">Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69e1f-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="69e1f-214">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69e1f-214">Remarks</span></span>

<span data-ttu-id="69e1f-215">Standardmäßig enthält das Ereignis den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) eines Computers.</span><span class="sxs-lookup"><span data-stu-id="69e1f-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="69e1f-216">Wenn Sie anstelle des FQDN den NetBIOS-Namen verwenden möchten, müssen Sie unter dem folgenden Registrierungsschlüssel einen DWORD-Registrierungs Wert mit dem Namen "compatflags" erstellen und den Wert von "compatflags" auf "0x2" festlegen.</span><span class="sxs-lookup"><span data-stu-id="69e1f-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="69e1f-217">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69e1f-217">Requirements</span></span>



| <span data-ttu-id="69e1f-218">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69e1f-218">Requirement</span></span> | <span data-ttu-id="69e1f-219">Wert</span><span class="sxs-lookup"><span data-stu-id="69e1f-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69e1f-220">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69e1f-220">Minimum supported client</span></span><br/> | <span data-ttu-id="69e1f-221">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e1f-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69e1f-222">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69e1f-222">Minimum supported server</span></span><br/> | <span data-ttu-id="69e1f-223">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e1f-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

