---
title: Komplexer channelpublishingtype-Typ
description: Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird. | Komplexer channelpublishingtype-Typ
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Ereignisprotokoll des komplexen channelpublishingtype-Typs
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350631"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="13ca3-105">Komplexer channelpublishingtype-Typ</span><span class="sxs-lookup"><span data-stu-id="13ca3-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="13ca3-106">Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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

## <a name="child-elements"></a><span data-ttu-id="13ca3-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13ca3-107">Child elements</span></span>



| <span data-ttu-id="13ca3-108">Element</span><span class="sxs-lookup"><span data-stu-id="13ca3-108">Element</span></span>                                                                              | <span data-ttu-id="13ca3-109">type</span><span class="sxs-lookup"><span data-stu-id="13ca3-109">Type</span></span>                                                              | <span data-ttu-id="13ca3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13ca3-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13ca3-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="13ca3-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="13ca3-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="13ca3-113">Die Größe des Arbeitsspeichers in Kilobytes, die für jeden Puffer belegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="13ca3-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="13ca3-114">Wenn Sie eine relativ niedrige Ereignisrate erwarten, sollte die Größe des Puffers auf die Seitengröße des Arbeitsspeichers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13ca3-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="13ca3-115">Wenn erwartet wird, dass die Ereignisrate relativ hoch ist, sollten Sie eine größere Puffergröße angeben und die maximale Anzahl von Puffern erhöhen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="13ca3-116">Die Puffergröße wirkt sich auf die Rate aus, mit der Puffer aufgefüllt werden und geleert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="13ca3-117">Obwohl eine kleine Puffergröße weniger Arbeitsspeicher erfordert, erhöht sich die Rate, mit der Puffer geleert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="13ca3-118">Die Standardpuffergröße für analytische und Debugkanäle beträgt 4 KB, und für admin und Operational beträgt der Wert 64 KB.</span><span class="sxs-lookup"><span data-stu-id="13ca3-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="13ca3-119">**clocktype**</span><span class="sxs-lookup"><span data-stu-id="13ca3-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="13ca3-120">Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="13ca3-121">Sie können SYSTEMTIME oder QPC angeben.</span><span class="sxs-lookup"><span data-stu-id="13ca3-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="13ca3-122">SYSTEMTIME bietet einen Zeitstempel mit niedriger Auflösung (10 Millisekunden), ist aber vergleichsweise kostengünstiger.</span><span class="sxs-lookup"><span data-stu-id="13ca3-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="13ca3-123">Der Standardwert ist SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="13ca3-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="13ca3-124">Der Query Performance Counter (QPC) bietet einen Zeitstempel mit hoher Auflösung (100 nanoseconds), ist aber vergleichsweise kostengünstiger.</span><span class="sxs-lookup"><span data-stu-id="13ca3-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="13ca3-125">Wenn Sie über hohe Ereignis Raten verfügen oder wenn der Consumer Ereignisse aus unterschiedlichen Puffern zusammenfasst, sollten Sie QPC durchführen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="13ca3-126">**controlguid**</span><span class="sxs-lookup"><span data-stu-id="13ca3-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="13ca3-127">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="13ca3-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="13ca3-128">Gibt die Sitzungs-GUID für eine ETW-Sitzung an, die WPP-Ereignisse enthält.</span><span class="sxs-lookup"><span data-stu-id="13ca3-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="13ca3-129">Diese Einstellung ist nur für Kanäle vom Typ Debug zulässig.</span><span class="sxs-lookup"><span data-stu-id="13ca3-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="13ca3-130">Diese Kanäle können nicht vollständig aktiviert werden, wenn Schlüsselwörter auf NULL (0x0000000000000000) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="13ca3-131">Sie müssen mit Schlüsselwörtern aktiviert werden, die auf 0xFFFFFFFFFFFFFFFF festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="13ca3-132">**filemax**</span><span class="sxs-lookup"><span data-stu-id="13ca3-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="13ca3-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="13ca3-134">Die maximale Anzahl von Wiederholungen, die der Dienst beim Aktivieren des Kanals eine neue Protokolldatei erstellen soll (schließt den Neustart des Computers ein).</span><span class="sxs-lookup"><span data-stu-id="13ca3-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="13ca3-135">Wenn der Wert 0 oder 1 ist, überschreibt der Dienst die Protokolldatei jedes Mal, wenn der Kanal aktiviert ist und die vorherigen Ereignisse verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="13ca3-136">Wenn der Wert größer als 1 ist, erstellt der Dienst jedes Mal, wenn der Kanal aktiviert ist, eine neue Protokolldatei, um die Ereignisse beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="13ca3-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="13ca3-137">Der Standardwert ist 1, und der Höchstwert, den Sie angeben können, ist 16.</span><span class="sxs-lookup"><span data-stu-id="13ca3-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="13ca3-138">Der Dienst fügt eine dreistellige Dezimalzahl zwischen 0 und filemax 1 an jeden Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="13ca3-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="13ca3-139">Beispielsweise *filename*. ETL.xxx, wobei xxx die dreistellige Dezimalzahl ist.</span><span class="sxs-lookup"><span data-stu-id="13ca3-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="13ca3-140">Die Dateien befinden sich in% windir% \\ system32 \\ winevt \\ Logs.</span><span class="sxs-lookup"><span data-stu-id="13ca3-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="13ca3-141">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="13ca3-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="13ca3-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="13ca3-143">Eine Bitmaske, die die Kategorie der Ereignisse bestimmt, die in den Kanal geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="13ca3-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="13ca3-144">Wenn der Wert des Attributs " **Keywords** " den Wert 0 hat, werden alle Ereignisse, die der Anbieter schreibt, in den Kanal geschrieben. Andernfalls werden nur Ereignisse, die ein Schlüsselwort definiert haben, das in den **Schlüsselwörtern** Bitmaske enthalten ist, in den Channel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="13ca3-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="13ca3-145">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="13ca3-145">The default is 0.</span></span><br/> <span data-ttu-id="13ca3-146">Bei debugkanälen, bei denen das controlguid-Attribut festgelegt ist, muss das **Keywords** -Attribut auf 0xFFFFFFFFFFFFFFFF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13ca3-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="13ca3-147">Die Sitzung übergibt den Schlüsselwort Wert an den Anbieter, wenn er den Anbieter aktiviert.</span><span class="sxs-lookup"><span data-stu-id="13ca3-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="13ca3-148">**Schleifen**</span><span class="sxs-lookup"><span data-stu-id="13ca3-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="13ca3-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="13ca3-150">Die Wartezeit in Millisekunden, bevor die Puffer geleert werden.</span><span class="sxs-lookup"><span data-stu-id="13ca3-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="13ca3-151">Bei Null leert etw die Puffer, sobald Sie voll sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="13ca3-152">Bei einem Wert ungleich NULL leert etw alle Puffer, die Ereignisse auf Grundlage des Werts enthalten, auch wenn der Puffer nicht voll ist.</span><span class="sxs-lookup"><span data-stu-id="13ca3-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="13ca3-153">Normalerweise möchten Sie Puffer nur dann leeren, wenn Sie voll sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="13ca3-154">Wenn Sie die Puffer bereinigen, können Sie die Dateigröße der Protokolldatei mit dem nicht gefüllten Pufferbereich vergrößern.</span><span class="sxs-lookup"><span data-stu-id="13ca3-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="13ca3-155">Der Standardwert beträgt 1 Sekunde für Administrator-und Betriebs Protokolle und 5 Sekunden für analytische und Debugprotokolle.</span><span class="sxs-lookup"><span data-stu-id="13ca3-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="13ca3-156">**Level**</span><span class="sxs-lookup"><span data-stu-id="13ca3-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="13ca3-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="13ca3-158">Der Schweregrad der Ereignisse, die in den Kanal geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13ca3-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="13ca3-159">Der Dienst schreibt Ereignisse in den Kanal, der einen Ebenenwert hat, der kleiner oder gleich dem angegebenen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="13ca3-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="13ca3-160">Der Standardwert ist 0 (null), was bedeutet, dass Ereignisse mit beliebigen Ebenen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="13ca3-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="13ca3-161">Die Sitzung übergibt den Wert für die Ebene an den Anbieter, wenn Sie den Anbieter aktiviert.</span><span class="sxs-lookup"><span data-stu-id="13ca3-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="13ca3-162">**MaxBuffers**</span><span class="sxs-lookup"><span data-stu-id="13ca3-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="13ca3-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="13ca3-164">Die maximale Anzahl von Puffern, die für die Sitzung zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="13ca3-165">In der Regel ist dieser Wert die minimale Anzahl von Puffern plus 20.</span><span class="sxs-lookup"><span data-stu-id="13ca3-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="13ca3-166">Dieser Wert muss größer oder gleich dem für minbuffers angegebenen Wert sein.</span><span class="sxs-lookup"><span data-stu-id="13ca3-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="13ca3-167">Der Standardwert für die maximale Anzahl von Puffern für analytische und Debugkanäle beträgt 10 KB. für admin und Operational beträgt der Wert 64 KB.</span><span class="sxs-lookup"><span data-stu-id="13ca3-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="13ca3-168">**minbuffers**</span><span class="sxs-lookup"><span data-stu-id="13ca3-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="13ca3-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="13ca3-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="13ca3-170">Die Mindestanzahl an Puffern, die für die Sitzung zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="13ca3-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="13ca3-171">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="13ca3-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="13ca3-172">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="13ca3-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="13ca3-173">Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="13ca3-174">Wenn Sie die SID mit dem Ereignis einschließen möchten, legen Sie dieses Attribut auf "Publishing" fest.</span><span class="sxs-lookup"><span data-stu-id="13ca3-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="13ca3-175">Die SID wird auf der Grundlage der Thread Identität festgelegt, wenn das Ereignis geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="13ca3-176">Wenn Sie die SID nicht mit dem Ereignis einschließen möchten, legen Sie dieses Attribut auf "None" fest.</span><span class="sxs-lookup"><span data-stu-id="13ca3-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="13ca3-177">Der Standardwert ist "Publishing".</span><span class="sxs-lookup"><span data-stu-id="13ca3-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="13ca3-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13ca3-178">Remarks</span></span>

<span data-ttu-id="13ca3-179">Sie können diese Veröffentlichungsinformationen für analytische und debugkanaltypen oder für jeden Kanal angeben, der die benutzerdefinierte Isolation angibt.</span><span class="sxs-lookup"><span data-stu-id="13ca3-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="13ca3-180">Obwohl Sie Ebenen und Schlüsselwörter angeben können, sollten Sie berücksichtigen, dass es sich hierbei um die einzigen Ereignisse handelt, die Sie vom Anbieter für diesen Kanal erhalten.</span><span class="sxs-lookup"><span data-stu-id="13ca3-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="13ca3-181">Wenn ein Puffer voll ist, leert etw den Puffer in die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="13ca3-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="13ca3-182">Wenn die Puffer schneller ausgefüllt werden, als Sie geleert werden können, werden neue Puffer zugewiesen und dem Pufferpool der Sitzung hinzugefügt, bis die maximale Anzahl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="13ca3-183">Über diesen Grenzwert hinaus verwirft die Sitzung eingehende Ereignisse, bis ein Puffer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="13ca3-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ca3-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13ca3-184">Requirements</span></span>



| <span data-ttu-id="13ca3-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13ca3-185">Requirement</span></span> | <span data-ttu-id="13ca3-186">Wert</span><span class="sxs-lookup"><span data-stu-id="13ca3-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13ca3-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13ca3-187">Minimum supported client</span></span><br/> | <span data-ttu-id="13ca3-188">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13ca3-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="13ca3-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13ca3-189">Minimum supported server</span></span><br/> | <span data-ttu-id="13ca3-190">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13ca3-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





