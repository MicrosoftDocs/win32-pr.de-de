---
title: guidtype Simple Type (Taskplaner)
description: Definiert das Muster für gültige GUIDs.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- guidtype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105374"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="20054-104">guidtype Simple Type (Taskplaner)</span><span class="sxs-lookup"><span data-stu-id="20054-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="20054-105">Definiert das Muster für gültige GUIDs.</span><span class="sxs-lookup"><span data-stu-id="20054-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="20054-106">Muster</span><span class="sxs-lookup"><span data-stu-id="20054-106">Patterns</span></span>

<span data-ttu-id="20054-107">Der einfache **guidtype** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="20054-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="20054-108">Eine eindeutige 128-Bit-Zahl.</span><span class="sxs-lookup"><span data-stu-id="20054-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="20054-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20054-109">Requirements</span></span>



| <span data-ttu-id="20054-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20054-110">Requirement</span></span> | <span data-ttu-id="20054-111">Wert</span><span class="sxs-lookup"><span data-stu-id="20054-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20054-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20054-112">Minimum supported client</span></span><br/> | <span data-ttu-id="20054-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20054-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="20054-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20054-114">Minimum supported server</span></span><br/> | <span data-ttu-id="20054-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20054-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20054-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20054-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20054-117">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="20054-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="20054-118">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="20054-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





