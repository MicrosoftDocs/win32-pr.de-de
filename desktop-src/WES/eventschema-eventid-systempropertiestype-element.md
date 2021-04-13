---
title: EventID-Element (systempropertiestype)
description: Der Bezeichner, den der Anbieter verwendet hat, um das Ereignis zu identifizieren.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- EventID-Element EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475597"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="2ca60-104">EventID-Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="2ca60-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="2ca60-105">Der Bezeichner, den der Anbieter verwendet hat, um das Ereignis zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2ca60-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2ca60-106">Das **EventID-** Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="2ca60-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca60-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ca60-107">Requirements</span></span>



| <span data-ttu-id="2ca60-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ca60-108">Requirement</span></span> | <span data-ttu-id="2ca60-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2ca60-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ca60-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ca60-110">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca60-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ca60-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ca60-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ca60-112">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca60-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ca60-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ca60-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ca60-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ca60-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="2ca60-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2ca60-116">**System (EventType)**</span><span class="sxs-lookup"><span data-stu-id="2ca60-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





