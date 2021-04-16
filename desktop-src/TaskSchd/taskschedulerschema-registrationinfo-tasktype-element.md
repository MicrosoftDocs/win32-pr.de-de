---
title: RegistrationInfo (TaskType)-Element
description: Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- Registrierungsinformationen Taskplaner, XML-Element
- RegistrationInfo-Element Taskplaner
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477784"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="84512-105">RegistrationInfo (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="84512-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="84512-106">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="84512-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="84512-107">Das **RegistrationInfo** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="84512-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="84512-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="84512-108">Parent element</span></span>



| <span data-ttu-id="84512-109">Element</span><span class="sxs-lookup"><span data-stu-id="84512-109">Element</span></span>                                          | <span data-ttu-id="84512-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="84512-110">Derived from</span></span>                                                 | <span data-ttu-id="84512-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84512-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="84512-112">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="84512-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="84512-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="84512-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="84512-114">Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84512-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="84512-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84512-115">Child elements</span></span>



| <span data-ttu-id="84512-116">Element</span><span class="sxs-lookup"><span data-stu-id="84512-116">Element</span></span>                                                                                                                  | <span data-ttu-id="84512-117">type</span><span class="sxs-lookup"><span data-stu-id="84512-117">Type</span></span>     | <span data-ttu-id="84512-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84512-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84512-119">**Autor (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="84512-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-120">string</span></span>   | <span data-ttu-id="84512-121">Gibt den Autor der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="84512-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="84512-122">**Date (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="84512-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="84512-123">dateTime</span></span> | <span data-ttu-id="84512-124">Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="84512-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="84512-125">**Description (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="84512-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-126">string</span></span>   | <span data-ttu-id="84512-127">Gibt die Beschreibung des Tasks an.</span><span class="sxs-lookup"><span data-stu-id="84512-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="84512-128">**Dokumentation (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="84512-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-129">string</span></span>   | <span data-ttu-id="84512-130">Gibt jede zusätzliche Dokumentation für den Task an.</span><span class="sxs-lookup"><span data-stu-id="84512-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="84512-131">**SecurityDescriptor (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="84512-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-132">string</span></span>   | <span data-ttu-id="84512-133">Gibt die Sicherheits Beschreibung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="84512-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="84512-134">**Quelle (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="84512-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-135">string</span></span>   | <span data-ttu-id="84512-136">Gibt an, woher die Aufgabe stammt.</span><span class="sxs-lookup"><span data-stu-id="84512-136">Specifies where the task originated from.</span></span> <span data-ttu-id="84512-137">Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="84512-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="84512-138">**URI (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="84512-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="84512-139">anyURI</span></span>   | <span data-ttu-id="84512-140">Gibt den URI der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="84512-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="84512-141">**Version (registrationinfotype)**</span><span class="sxs-lookup"><span data-stu-id="84512-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="84512-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="84512-142">string</span></span>   | <span data-ttu-id="84512-143">Gibt die Versionsnummer der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="84512-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="84512-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84512-144">Remarks</span></span>

<span data-ttu-id="84512-145">Bei der Skripterstellung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="84512-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="84512-146">Bei der C++-Entwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo)angegeben.</span><span class="sxs-lookup"><span data-stu-id="84512-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="84512-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84512-147">Requirements</span></span>



| <span data-ttu-id="84512-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84512-148">Requirement</span></span> | <span data-ttu-id="84512-149">Wert</span><span class="sxs-lookup"><span data-stu-id="84512-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84512-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84512-150">Minimum supported client</span></span><br/> | <span data-ttu-id="84512-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84512-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84512-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84512-152">Minimum supported server</span></span><br/> | <span data-ttu-id="84512-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84512-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84512-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84512-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84512-155">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="84512-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="84512-156">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="84512-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





