---
title: SecurityDescriptor (registrationinfotype)-Element
description: Gibt die Sicherheits Beschreibung der Aufgabe an.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- SecurityDescriptor-Element Taskplaner
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040280"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="995de-104">SecurityDescriptor (registrationinfotype)-Element</span><span class="sxs-lookup"><span data-stu-id="995de-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="995de-105">Gibt die Sicherheits Beschreibung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="995de-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="995de-106">Das **securityDescriptor** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="995de-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="995de-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="995de-107">Parent element</span></span>



| <span data-ttu-id="995de-108">Element</span><span class="sxs-lookup"><span data-stu-id="995de-108">Element</span></span>                                                                           | <span data-ttu-id="995de-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="995de-109">Derived from</span></span>                                                                         | <span data-ttu-id="995de-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="995de-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="995de-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="995de-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="995de-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="995de-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="995de-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="995de-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="995de-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="995de-114">Remarks</span></span>

<span data-ttu-id="995de-115">Bei der Skript Entwicklung wird die Sicherheits Beschreibung einer Aufgabe mithilfe der [**RegistrationInfo. securityDescriptor**](registrationinfo-securitydescriptor.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="995de-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="995de-116">Bei der C++-Entwicklung wird die Sicherheits Beschreibung einer Aufgabe mithilfe der [**iregistrationinfo:: securityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="995de-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="995de-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="995de-117">Requirements</span></span>



| <span data-ttu-id="995de-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="995de-118">Requirement</span></span> | <span data-ttu-id="995de-119">Wert</span><span class="sxs-lookup"><span data-stu-id="995de-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="995de-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="995de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="995de-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="995de-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="995de-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="995de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="995de-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="995de-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="995de-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="995de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995de-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="995de-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="995de-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="995de-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





