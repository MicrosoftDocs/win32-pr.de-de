---
title: Author (registrationinfotype)-Element
description: Gibt den Autor der Aufgabe an.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Author-Element Taskplaner
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956686"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="a334f-104">Author (registrationinfotype)-Element</span><span class="sxs-lookup"><span data-stu-id="a334f-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="a334f-105">Gibt den Autor der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="a334f-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="a334f-106">Das **Author** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="a334f-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a334f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a334f-107">Parent element</span></span>



| <span data-ttu-id="a334f-108">Element</span><span class="sxs-lookup"><span data-stu-id="a334f-108">Element</span></span>                                                                           | <span data-ttu-id="a334f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a334f-109">Derived from</span></span>                                                                         | <span data-ttu-id="a334f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a334f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a334f-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="a334f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="a334f-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="a334f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="a334f-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="a334f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a334f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a334f-114">Remarks</span></span>

<span data-ttu-id="a334f-115">Bei der Skripterstellung wird der Autor der Aufgabe mithilfe der [**RegistrationInfo. Author**](registrationinfo-author.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a334f-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="a334f-116">Bei der C++-Entwicklung wird der Autor der Aufgabe mithilfe der [**iregistrationinfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a334f-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a334f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a334f-117">Examples</span></span>

<span data-ttu-id="a334f-118">Der folgende XML-Code definiert den Autor einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a334f-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="a334f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a334f-119">Requirements</span></span>



| <span data-ttu-id="a334f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a334f-120">Requirement</span></span> | <span data-ttu-id="a334f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a334f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a334f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a334f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a334f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a334f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a334f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a334f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a334f-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a334f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a334f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a334f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a334f-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a334f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a334f-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a334f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





