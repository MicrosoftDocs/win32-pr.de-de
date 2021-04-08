---
title: Description-Element (registrationinfotype)
description: Gibt die Beschreibung des Tasks an.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Description-Element Taskplaner
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740824"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="262d1-104">Description-Element (registrationinfotype)</span><span class="sxs-lookup"><span data-stu-id="262d1-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="262d1-105">Gibt die Beschreibung des Tasks an.</span><span class="sxs-lookup"><span data-stu-id="262d1-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="262d1-106">Das **Description** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="262d1-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="262d1-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="262d1-107">Parent element</span></span>



| <span data-ttu-id="262d1-108">Element</span><span class="sxs-lookup"><span data-stu-id="262d1-108">Element</span></span>                                                                           | <span data-ttu-id="262d1-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="262d1-109">Derived from</span></span>                                                                         | <span data-ttu-id="262d1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="262d1-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="262d1-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="262d1-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="262d1-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="262d1-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="262d1-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="262d1-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="262d1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="262d1-114">Remarks</span></span>

<span data-ttu-id="262d1-115">Bei der Skripterstellung wird die Beschreibung einer Aufgabe mithilfe der [**RegistrationInfo. Description**](registrationinfo-description.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="262d1-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="262d1-116">Bei der C++-Entwicklung wird die Beschreibung einer Aufgabe mithilfe der [**iregistrationinfo::D escription**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="262d1-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="262d1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="262d1-117">Requirements</span></span>



| <span data-ttu-id="262d1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="262d1-118">Requirement</span></span> | <span data-ttu-id="262d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="262d1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="262d1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="262d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="262d1-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="262d1-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="262d1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="262d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="262d1-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="262d1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="262d1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="262d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262d1-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="262d1-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="262d1-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="262d1-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





