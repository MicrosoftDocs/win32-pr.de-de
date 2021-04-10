---
title: Provider-Element (systempropertiestype)
description: Identifiziert den Anbieter, der das Ereignis protokolliert hat.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Anbieter Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040261"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="27d2f-104">Provider-Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="27d2f-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="27d2f-105">Identifiziert den Anbieter, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="27d2f-105">Identifies the provider that logged the event.</span></span>

``` syntax
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
```

<span data-ttu-id="27d2f-106">Das **Provider** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="27d2f-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="27d2f-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="27d2f-107">Attributes</span></span>



| <span data-ttu-id="27d2f-108">Name</span><span class="sxs-lookup"><span data-stu-id="27d2f-108">Name</span></span>            | <span data-ttu-id="27d2f-109">type</span><span class="sxs-lookup"><span data-stu-id="27d2f-109">Type</span></span>                                                | <span data-ttu-id="27d2f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27d2f-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d2f-111">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="27d2f-111">EventSourceName</span></span> | <span data-ttu-id="27d2f-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27d2f-112">string</span></span>                                              | <span data-ttu-id="27d2f-113">Der Name der Ereignis Quelle, die das Ereignis veröffentlicht hat (wenn die Ereignis Quelle von der Legacy- [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API stammt).</span><span class="sxs-lookup"><span data-stu-id="27d2f-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="27d2f-114">GUID</span><span class="sxs-lookup"><span data-stu-id="27d2f-114">Guid</span></span>            | [<span data-ttu-id="27d2f-115">**Guidtype**</span><span class="sxs-lookup"><span data-stu-id="27d2f-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="27d2f-116">Der Globally Unique Identifier, der den Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27d2f-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="27d2f-117">Name</span><span class="sxs-lookup"><span data-stu-id="27d2f-117">Name</span></span>            | <span data-ttu-id="27d2f-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="27d2f-118">anyURI</span></span>                                              | <span data-ttu-id="27d2f-119">Der Name des Ereignis Anbieters, der das Ereignis protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="27d2f-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="27d2f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27d2f-120">Requirements</span></span>



| <span data-ttu-id="27d2f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27d2f-121">Requirement</span></span> | <span data-ttu-id="27d2f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="27d2f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27d2f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27d2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27d2f-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27d2f-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27d2f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27d2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27d2f-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27d2f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27d2f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27d2f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="27d2f-128">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="27d2f-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="27d2f-129">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="27d2f-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

