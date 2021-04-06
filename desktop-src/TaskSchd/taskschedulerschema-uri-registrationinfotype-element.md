---
title: URI (registrationinfotype)-Element
description: Gibt den URI der Aufgabe an.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- URI-Element Taskplaner
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743752"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="77d4c-104">URI (registrationinfotype)-Element</span><span class="sxs-lookup"><span data-stu-id="77d4c-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="77d4c-105">Gibt den URI der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="77d4c-105">Specifies the URI of the task.</span></span> <span data-ttu-id="77d4c-106">Mit diesem Element wird angegeben, wo die registrierte Aufgabe in der Hierarchie der Aufgaben Ordner abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="77d4c-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="77d4c-107">Das **URI** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="77d4c-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="77d4c-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="77d4c-108">Parent element</span></span>



| <span data-ttu-id="77d4c-109">Element</span><span class="sxs-lookup"><span data-stu-id="77d4c-109">Element</span></span>                                                                           | <span data-ttu-id="77d4c-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="77d4c-110">Derived from</span></span>                                                                         | <span data-ttu-id="77d4c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77d4c-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d4c-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="77d4c-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="77d4c-113">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="77d4c-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="77d4c-114">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="77d4c-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77d4c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77d4c-115">Remarks</span></span>

<span data-ttu-id="77d4c-116">Bei der Skripterstellung wird der URI der Aufgabe mithilfe der [**RegistrationInfo. Uri**](registrationinfo-uri.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="77d4c-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="77d4c-117">Bei der C++-Entwicklung wird der URI der Aufgabe mithilfe der [**iregistrationinfo:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="77d4c-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d4c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77d4c-118">Requirements</span></span>



| <span data-ttu-id="77d4c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77d4c-119">Requirement</span></span> | <span data-ttu-id="77d4c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="77d4c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77d4c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77d4c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77d4c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77d4c-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77d4c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77d4c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77d4c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77d4c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77d4c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77d4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d4c-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="77d4c-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="77d4c-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="77d4c-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





