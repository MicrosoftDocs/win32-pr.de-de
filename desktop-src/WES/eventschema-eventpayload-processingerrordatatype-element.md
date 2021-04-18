---
title: EventPayload-Element (processingerrordatatype)
description: Enthält binäre Ereignisdaten für das Ereignis, das einen Fehler verursacht hat, als die Ereignisdaten verarbeitet wurden.
ms.assetid: 0ba72d72-8f43-40ca-b3ee-89fe27a4dd07
keywords:
- EventPayload-Element (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- EventPayload
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4dd20f95924282ae8cb0f1b0604c0e77d07766ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337494"
---
# <a name="eventpayload-processingerrordatatype-element"></a><span data-ttu-id="056e5-104">EventPayload-Element (processingerrordatatype)</span><span class="sxs-lookup"><span data-stu-id="056e5-104">EventPayload (ProcessingErrorDataType) Element</span></span>

<span data-ttu-id="056e5-105">Enthält binäre Ereignisdaten für das Ereignis, das einen Fehler verursacht hat, als die Ereignisdaten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="056e5-105">Contains binary event data for the event that caused an error when the event data was processed.</span></span>

``` syntax
<xs:element name="EventPayload"
    type="hexBinary"
 />
```

<span data-ttu-id="056e5-106">Das **eventPayload** -Element wird durch den komplexen Typ [**processingerrordatatype**](eventschema-processingerrordatatype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="056e5-106">The **EventPayload** element is defined by the [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="056e5-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="056e5-107">Requirements</span></span>



| <span data-ttu-id="056e5-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="056e5-108">Requirement</span></span> | <span data-ttu-id="056e5-109">Wert</span><span class="sxs-lookup"><span data-stu-id="056e5-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="056e5-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="056e5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="056e5-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056e5-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="056e5-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="056e5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="056e5-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056e5-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="056e5-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="056e5-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="056e5-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="056e5-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="056e5-116">**Processingerrordata (EventType)**</span><span class="sxs-lookup"><span data-stu-id="056e5-116">**ProcessingErrorData (EventType)**</span></span>](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





