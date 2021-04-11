---
title: Komplexer channelloggingtype-Typ
description: Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob Sie sequenziell oder zirkulär ist. | Komplexer channelloggingtype-Typ
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Ereignisprotokoll für komplexen channelloggingtype-Typ
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132269"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="30a96-105">Komplexer channelloggingtype-Typ</span><span class="sxs-lookup"><span data-stu-id="30a96-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="30a96-106">Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob Sie sequenziell oder zirkulär ist.</span><span class="sxs-lookup"><span data-stu-id="30a96-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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

## <a name="child-elements"></a><span data-ttu-id="30a96-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30a96-107">Child elements</span></span>



| <span data-ttu-id="30a96-108">Element</span><span class="sxs-lookup"><span data-stu-id="30a96-108">Element</span></span>                                                                         | <span data-ttu-id="30a96-109">type</span><span class="sxs-lookup"><span data-stu-id="30a96-109">Type</span></span>                                                              | <span data-ttu-id="30a96-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30a96-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30a96-111">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="30a96-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="30a96-112">boolean</span><span class="sxs-lookup"><span data-stu-id="30a96-112">boolean</span></span>                                                           | <span data-ttu-id="30a96-113">Bestimmt, ob eine neue Protokolldatei erstellt wird, wenn die aktuelle Protokolldatei die maximale Größe erreicht.</span><span class="sxs-lookup"><span data-stu-id="30a96-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="30a96-114">Legen Sie diese Einstellung auf **true** fest, um anzufordern, dass der Dienst eine neue Datei erstellt, wenn die Protokolldatei die maximale Größe erreicht. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="30a96-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="30a96-115">Sie können die [**Automatische Sicherung**](eventmanifestschema-autobackup-channelloggingtype-element.md) nur auf **true** festlegen, wenn die [**Beibehaltung**](eventmanifestschema-retention-channelloggingtype-element.md) auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="30a96-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="30a96-116">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="30a96-116">The default is **false**.</span></span><br/> <span data-ttu-id="30a96-117">Es gibt keine Beschränkung für die Anzahl der Sicherungsdateien, die vom Dienst erstellt werden können (nur durch den verfügbaren Speicherplatz beschränkt).</span><span class="sxs-lookup"><span data-stu-id="30a96-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="30a96-118">Die Sicherungs Dateinamen weisen die Form Archive-*ChannelName* - *Zeitstempel*. evtx auf und befinden sich im Ordner% windir% \\ system32 \\ winevt \\ Logs.</span><span class="sxs-lookup"><span data-stu-id="30a96-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="30a96-119">**MaxSize**</span><span class="sxs-lookup"><span data-stu-id="30a96-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="30a96-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="30a96-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="30a96-121">Die maximale Größe der Protokolldatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="30a96-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="30a96-122">Der Standardwert (und der minimale Wert) ist 1 MB.</span><span class="sxs-lookup"><span data-stu-id="30a96-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="30a96-123">Wenn die physische Protokoll Größe kleiner ist als die konfigurierte maximale Größe, und im Protokoll ist zusätzlicher Speicherplatz erforderlich, um Ereignisse zu speichern, weist der Dienst einen weiteren Speicherblock zu, auch wenn die resultierende physische Größe des Protokolls größer als die konfigurierte maximale Größe ist.</span><span class="sxs-lookup"><span data-stu-id="30a96-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="30a96-124">Der Dienst ordnet Blöcke von 1 MB zu, sodass die physische Größe auf bis zu 1 MB größer als die konfigurierte maximale Größe anwachsen kann.</span><span class="sxs-lookup"><span data-stu-id="30a96-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="30a96-125">**zurück**</span><span class="sxs-lookup"><span data-stu-id="30a96-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="30a96-126">boolean</span><span class="sxs-lookup"><span data-stu-id="30a96-126">boolean</span></span>                                                           | <span data-ttu-id="30a96-127">Bestimmt, ob die Protokolldatei eine sequenzielle oder zirkuläre Protokolldatei ist.</span><span class="sxs-lookup"><span data-stu-id="30a96-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="30a96-128">Legen Sie für eine sequenzielle Protokolldatei auf **true** und **false** für eine zirkuläre Protokolldatei fest.</span><span class="sxs-lookup"><span data-stu-id="30a96-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="30a96-129">Der Standardwert lautet " **false** " für Administrator-und Betriebskanal Typen und für analytische und debugkanaltypen " **true** "</span><span class="sxs-lookup"><span data-stu-id="30a96-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="30a96-130">Zum Abfragen eines zirkulären Protokolls müssen Sie zunächst den Kanal deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="30a96-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="30a96-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30a96-131">Remarks</span></span>

<span data-ttu-id="30a96-132">Sie können das **MaxSize** -Attribut für einen beliebigen Kanaltyp angeben.</span><span class="sxs-lookup"><span data-stu-id="30a96-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="30a96-133">Sie können das Attribut für die **Automatische Sicherung** nur für die Typen "admin" und "Operational Channel" angeben.</span><span class="sxs-lookup"><span data-stu-id="30a96-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="30a96-134">Sie können das **Beibehaltungs** Attribut auf "false" (zirkuläre Protokollierung) für Administrator-und Betriebskanal Typen festlegen.</span><span class="sxs-lookup"><span data-stu-id="30a96-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="30a96-135">Sie können das **Beibehaltungs** Attribut auf "false" (zirkuläre Protokollierung) für analytische und debugkanaltypen festlegen, aber um die Ereignisse im Windows-Ereignisanzeige anzuzeigen, müssen Sie den Kanal zunächst deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="30a96-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="30a96-136">Beachten Sie Folgendes: Wenn Sie den Kanal erneut aktivieren, werden die Ereignisse aus dem Kanal entfernt.</span><span class="sxs-lookup"><span data-stu-id="30a96-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a96-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30a96-137">Requirements</span></span>



| <span data-ttu-id="30a96-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30a96-138">Requirement</span></span> | <span data-ttu-id="30a96-139">Wert</span><span class="sxs-lookup"><span data-stu-id="30a96-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30a96-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30a96-140">Minimum supported client</span></span><br/> | <span data-ttu-id="30a96-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a96-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30a96-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30a96-142">Minimum supported server</span></span><br/> | <span data-ttu-id="30a96-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30a96-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





