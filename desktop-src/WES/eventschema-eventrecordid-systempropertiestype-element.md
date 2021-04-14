---
title: Eventrecordid-Element (systempropertiestype)
description: Die Datensatznummer, die dem Ereignis bei der Protokollierung zugewiesen wurde.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- Eventrecordid-Element EventLog
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391587"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="427a8-104">Eventrecordid-Element (systempropertiestype)</span><span class="sxs-lookup"><span data-stu-id="427a8-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="427a8-105">Die Datensatznummer, die dem Ereignis bei der Protokollierung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="427a8-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="427a8-106">Das **eventrecordid** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="427a8-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="427a8-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="427a8-107">Requirements</span></span>



| <span data-ttu-id="427a8-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="427a8-108">Requirement</span></span> | <span data-ttu-id="427a8-109">Wert</span><span class="sxs-lookup"><span data-stu-id="427a8-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="427a8-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="427a8-110">Minimum supported client</span></span><br/> | <span data-ttu-id="427a8-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="427a8-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="427a8-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="427a8-112">Minimum supported server</span></span><br/> | <span data-ttu-id="427a8-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="427a8-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





