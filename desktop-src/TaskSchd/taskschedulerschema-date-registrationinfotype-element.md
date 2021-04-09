---
title: Date (registrationinfotype)-Element
description: Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Date-Element Taskplaner
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104636"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="d837f-104">Date (registrationinfotype)-Element</span><span class="sxs-lookup"><span data-stu-id="d837f-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="d837f-105">Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="d837f-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="d837f-106">Das **Date** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d837f-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d837f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d837f-107">Parent element</span></span>



| <span data-ttu-id="d837f-108">Element</span><span class="sxs-lookup"><span data-stu-id="d837f-108">Element</span></span>                                                                           | <span data-ttu-id="d837f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d837f-109">Derived from</span></span>                                                                         | <span data-ttu-id="d837f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d837f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d837f-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="d837f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="d837f-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="d837f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="d837f-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d837f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d837f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d837f-114">Remarks</span></span>

<span data-ttu-id="d837f-115">Bei der Skripterstellung wird das Registrierungsdatum einer Aufgabe mithilfe der [**RegistrationInfo. Date**](registrationinfo-date.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="d837f-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="d837f-116">Bei der C++-Entwicklung wird das Registrierungsdatum einer Aufgabe mithilfe der [**iregistrationinfo::D Ate**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="d837f-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d837f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d837f-117">Requirements</span></span>



| <span data-ttu-id="d837f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d837f-118">Requirement</span></span> | <span data-ttu-id="d837f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d837f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d837f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d837f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d837f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d837f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d837f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d837f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d837f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d837f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d837f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d837f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d837f-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d837f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d837f-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d837f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





