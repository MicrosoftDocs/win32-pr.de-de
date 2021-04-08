---
title: Komplexer eventdatatype-Typ
description: Definiert die Ereignisdaten Elemente und-Strukturen, die die Ereignisdaten enthalten.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Ereignisprotokoll des komplexen eventdatatype-Typs
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740376"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="e24ce-104">Komplexer eventdatatype-Typ</span><span class="sxs-lookup"><span data-stu-id="e24ce-104">EventDataType Complex Type</span></span>

<span data-ttu-id="e24ce-105">Definiert die Ereignisdaten Elemente und-Strukturen, die die Ereignisdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="e24ce-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e24ce-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e24ce-106">Child elements</span></span>



| <span data-ttu-id="e24ce-107">Element</span><span class="sxs-lookup"><span data-stu-id="e24ce-107">Element</span></span>                                                              | <span data-ttu-id="e24ce-108">type</span><span class="sxs-lookup"><span data-stu-id="e24ce-108">Type</span></span>                                                               | <span data-ttu-id="e24ce-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e24ce-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e24ce-110">**Binary**</span><span class="sxs-lookup"><span data-stu-id="e24ce-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="e24ce-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e24ce-111">hexBinary</span></span>                                                          | <span data-ttu-id="e24ce-112">Ein binäres Daten-BLOB für Ereignisse, die mithilfe der [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging)geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e24ce-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="e24ce-113">**Complexdata**</span><span class="sxs-lookup"><span data-stu-id="e24ce-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="e24ce-114">**Complexdatatype**</span><span class="sxs-lookup"><span data-stu-id="e24ce-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="e24ce-115">Eine-Struktur, die in der Vorlage für das-Ereignis definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e24ce-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="e24ce-116">**Daten**</span><span class="sxs-lookup"><span data-stu-id="e24ce-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="e24ce-117">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e24ce-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="e24ce-118">Ein Datenelement der obersten Ebene, das in der Vorlage für das-Ereignis definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e24ce-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="e24ce-119">Attributes</span><span class="sxs-lookup"><span data-stu-id="e24ce-119">Attributes</span></span>



| <span data-ttu-id="e24ce-120">Name</span><span class="sxs-lookup"><span data-stu-id="e24ce-120">Name</span></span> | <span data-ttu-id="e24ce-121">type</span><span class="sxs-lookup"><span data-stu-id="e24ce-121">Type</span></span>   | <span data-ttu-id="e24ce-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e24ce-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="e24ce-123">Name</span><span class="sxs-lookup"><span data-stu-id="e24ce-123">Name</span></span> | <span data-ttu-id="e24ce-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e24ce-124">string</span></span> | <span data-ttu-id="e24ce-125">Der Name der Vorlage, die die Datenelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="e24ce-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e24ce-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e24ce-126">Remarks</span></span>

<span data-ttu-id="e24ce-127">Die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion rendert Arrays und Strukturen als binäre Blob.</span><span class="sxs-lookup"><span data-stu-id="e24ce-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24ce-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e24ce-128">Requirements</span></span>



| <span data-ttu-id="e24ce-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e24ce-129">Requirement</span></span> | <span data-ttu-id="e24ce-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e24ce-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e24ce-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e24ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e24ce-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e24ce-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e24ce-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e24ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e24ce-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e24ce-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

