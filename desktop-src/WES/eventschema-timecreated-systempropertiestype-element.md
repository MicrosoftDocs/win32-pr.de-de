---
title: TimeCreated-Element (systempropertiestype)
description: Der Zeitstempel, der angibt, wann das Ereignis protokolliert wurde.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- TimeCreated-Element (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956654"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="656ce-104">TimeCreated-Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="656ce-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="656ce-105">Der Zeitstempel, der angibt, wann das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="656ce-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="656ce-106">Das **TimeCreated** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="656ce-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="656ce-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="656ce-107">Attributes</span></span>



| <span data-ttu-id="656ce-108">Name</span><span class="sxs-lookup"><span data-stu-id="656ce-108">Name</span></span>       | <span data-ttu-id="656ce-109">type</span><span class="sxs-lookup"><span data-stu-id="656ce-109">Type</span></span>     | <span data-ttu-id="656ce-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="656ce-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="656ce-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="656ce-111">SystemTime</span></span> | <span data-ttu-id="656ce-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="656ce-112">dateTime</span></span> | <span data-ttu-id="656ce-113">Die Systemzeit, zu der das Ereignis protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="656ce-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="656ce-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656ce-114">Requirements</span></span>



| <span data-ttu-id="656ce-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="656ce-115">Requirement</span></span> | <span data-ttu-id="656ce-116">Wert</span><span class="sxs-lookup"><span data-stu-id="656ce-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="656ce-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="656ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="656ce-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="656ce-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="656ce-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="656ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="656ce-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="656ce-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="656ce-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="656ce-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="656ce-122">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="656ce-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="656ce-123">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="656ce-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





