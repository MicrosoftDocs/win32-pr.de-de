---
title: Source-Element (registrationinfotype)
description: Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Quell Element Taskplaner
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391630"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="51831-105">Source-Element (registrationinfotype)</span><span class="sxs-lookup"><span data-stu-id="51831-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="51831-106">Gibt an, woher die Aufgabe stammt.</span><span class="sxs-lookup"><span data-stu-id="51831-106">Specifies where the task originated from.</span></span> <span data-ttu-id="51831-107">Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="51831-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="51831-108">Das **Source** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="51831-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="51831-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="51831-109">Parent element</span></span>



| <span data-ttu-id="51831-110">Element</span><span class="sxs-lookup"><span data-stu-id="51831-110">Element</span></span>                                                                           | <span data-ttu-id="51831-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="51831-111">Derived from</span></span>                                                                         | <span data-ttu-id="51831-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51831-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51831-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="51831-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="51831-114">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="51831-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="51831-115">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="51831-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="51831-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51831-116">Remarks</span></span>

<span data-ttu-id="51831-117">Bei der Skripterstellung wird die Quelle einer Aufgabe mithilfe der [**RegistrationInfo. Source**](registrationinfo-source.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="51831-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="51831-118">Bei der C++-Entwicklung wird die Quelle einer Aufgabe mithilfe der [**iregistrationinfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="51831-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51831-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51831-119">Requirements</span></span>



| <span data-ttu-id="51831-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51831-120">Requirement</span></span> | <span data-ttu-id="51831-121">Wert</span><span class="sxs-lookup"><span data-stu-id="51831-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51831-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51831-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51831-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51831-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51831-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51831-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51831-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51831-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51831-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51831-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51831-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="51831-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="51831-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="51831-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





