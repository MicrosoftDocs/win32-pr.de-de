---
title: Binary (templateitemtype)-Element
description: Enthält die Binärdaten, die von der Ereignisprotokoll-API bereitgestellt werden.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- Ereignisprotokoll für das binäre Element
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338783"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="6773a-104">Binary (templateitemtype)-Element</span><span class="sxs-lookup"><span data-stu-id="6773a-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="6773a-105">Enthält die Binärdaten, die von der [Ereignisprotokoll](/windows/desktop/EventLog/event-logging) -API bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6773a-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6773a-106">Das **Binary** -Element wird durch den komplexen Typ [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="6773a-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="6773a-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="6773a-107">Attributes</span></span>



| <span data-ttu-id="6773a-108">Name</span><span class="sxs-lookup"><span data-stu-id="6773a-108">Name</span></span> | <span data-ttu-id="6773a-109">type</span><span class="sxs-lookup"><span data-stu-id="6773a-109">Type</span></span>   | <span data-ttu-id="6773a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6773a-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="6773a-111">name</span><span class="sxs-lookup"><span data-stu-id="6773a-111">name</span></span> | <span data-ttu-id="6773a-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6773a-112">string</span></span> | <span data-ttu-id="6773a-113">Der Name, der den Binärdaten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6773a-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6773a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6773a-114">Requirements</span></span>



| <span data-ttu-id="6773a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6773a-115">Requirement</span></span> | <span data-ttu-id="6773a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6773a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6773a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6773a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6773a-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6773a-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6773a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6773a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6773a-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6773a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6773a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6773a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="6773a-122">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="6773a-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="6773a-123">**Vorlage (templatelisttype)**</span><span class="sxs-lookup"><span data-stu-id="6773a-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

