---
title: Version (registrationinfotype)-Element
description: Gibt die Versionsnummer der Aufgabe an.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Versions Element Taskplaner
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337718"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="f5899-104">Version (registrationinfotype)-Element</span><span class="sxs-lookup"><span data-stu-id="f5899-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="f5899-105">Gibt die Versionsnummer der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="f5899-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="f5899-106">Das **Versions** Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="f5899-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f5899-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f5899-107">Parent element</span></span>



| <span data-ttu-id="f5899-108">Element</span><span class="sxs-lookup"><span data-stu-id="f5899-108">Element</span></span>                                                                           | <span data-ttu-id="f5899-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f5899-109">Derived from</span></span>                                                                         | <span data-ttu-id="f5899-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5899-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5899-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="f5899-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="f5899-112">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="f5899-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="f5899-113">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="f5899-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f5899-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5899-114">Remarks</span></span>

<span data-ttu-id="f5899-115">Bei der Skripterstellung wird die Version einer Aufgabe mithilfe der [**RegistrationInfo. Version**](registrationinfo-version.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5899-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="f5899-116">Bei der C++-Entwicklung wird die Version einer Aufgabe mithilfe der [**iregistrationinfo:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5899-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f5899-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5899-117">Examples</span></span>

<span data-ttu-id="f5899-118">Der folgende XML-Code definiert die Version einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="f5899-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="f5899-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5899-119">Requirements</span></span>



| <span data-ttu-id="f5899-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5899-120">Requirement</span></span> | <span data-ttu-id="f5899-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f5899-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5899-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5899-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5899-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5899-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5899-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5899-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5899-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5899-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5899-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5899-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5899-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f5899-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f5899-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f5899-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





