---
title: komplexer Typ von "aktionbasetype"
description: Definiert das ID-Attribut für alle Elemente dieses Typs.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- komplexer Typ von "aktionbasetype" Taskplaner
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105890"
---
# <a name="actionbasetype-complex-type"></a><span data-ttu-id="e7563-104">komplexer Typ von "aktionbasetype"</span><span class="sxs-lookup"><span data-stu-id="e7563-104">actionBaseType Complex Type</span></span>

<span data-ttu-id="e7563-105">Definiert das ID-Attribut für alle Elemente dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="e7563-105">Defines the Id attribute for all elements of this type.</span></span>

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e7563-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="e7563-106">Attributes</span></span>



| <span data-ttu-id="e7563-107">Name</span><span class="sxs-lookup"><span data-stu-id="e7563-107">Name</span></span> | <span data-ttu-id="e7563-108">type</span><span class="sxs-lookup"><span data-stu-id="e7563-108">Type</span></span> | <span data-ttu-id="e7563-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7563-109">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="e7563-110">id</span><span class="sxs-lookup"><span data-stu-id="e7563-110">id</span></span>   | <span data-ttu-id="e7563-111">id</span><span class="sxs-lookup"><span data-stu-id="e7563-111">ID</span></span>   | <span data-ttu-id="e7563-112">Die ID der Aktion, die von der Aufgabe ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7563-112">Id of the action performed by the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e7563-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7563-113">Requirements</span></span>



| <span data-ttu-id="e7563-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7563-114">Requirement</span></span> | <span data-ttu-id="e7563-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e7563-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7563-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7563-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7563-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7563-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7563-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7563-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7563-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7563-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7563-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7563-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7563-121">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="e7563-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="e7563-122">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e7563-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





