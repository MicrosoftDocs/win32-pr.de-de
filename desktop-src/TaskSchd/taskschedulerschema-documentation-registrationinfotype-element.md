---
title: Documentation-Element (registrationinfotype)
description: Gibt jede zusätzliche Dokumentation für den Task an.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Documentation-Element Taskplaner
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346540"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="730d9-104">Documentation-Element (registrationinfotype)</span><span class="sxs-lookup"><span data-stu-id="730d9-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="730d9-105">Gibt jede zusätzliche Dokumentation für den Task an.</span><span class="sxs-lookup"><span data-stu-id="730d9-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="730d9-106">Das **Documentation** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="730d9-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="730d9-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="730d9-107">Parent element</span></span>



| <span data-ttu-id="730d9-108">Element</span><span class="sxs-lookup"><span data-stu-id="730d9-108">Element</span></span>                                                                           | <span data-ttu-id="730d9-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="730d9-109">Derived from</span></span>                                                                         | <span data-ttu-id="730d9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="730d9-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="730d9-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="730d9-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="730d9-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="730d9-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="730d9-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="730d9-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="730d9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="730d9-114">Remarks</span></span>

<span data-ttu-id="730d9-115">Bei Skript Anwendungen wird mithilfe der-Eigenschaft [**RegistrationInfo.Doc**](registrationinfo-documentation.md) -Eigenschaft die zusätzliche Aufgaben Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="730d9-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="730d9-116">Für C++-Anwendungen wird mithilfe der [**iregistrationinfo::D ocumentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) -Eigenschaft eine zusätzliche Aufgaben Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="730d9-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="730d9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="730d9-117">Requirements</span></span>



| <span data-ttu-id="730d9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="730d9-118">Requirement</span></span> | <span data-ttu-id="730d9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="730d9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="730d9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="730d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="730d9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="730d9-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="730d9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="730d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="730d9-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="730d9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="730d9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="730d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730d9-125">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="730d9-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





