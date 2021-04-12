---
title: komplexer registrationinfotype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das RegistrationInfo-Element.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- komplexer registrationinfotype-Typ Taskplaner
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956761"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="7c184-104">komplexer registrationinfotype-Typ</span><span class="sxs-lookup"><span data-stu-id="7c184-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="7c184-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="7c184-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7c184-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c184-106">Child elements</span></span>



| <span data-ttu-id="7c184-107">Element</span><span class="sxs-lookup"><span data-stu-id="7c184-107">Element</span></span>                                                                                           | <span data-ttu-id="7c184-108">type</span><span class="sxs-lookup"><span data-stu-id="7c184-108">Type</span></span>     | <span data-ttu-id="7c184-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c184-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c184-110">**Autor**</span><span class="sxs-lookup"><span data-stu-id="7c184-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="7c184-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-111">string</span></span>   | <span data-ttu-id="7c184-112">Gibt den Autor der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7c184-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="7c184-113">**Datum**</span><span class="sxs-lookup"><span data-stu-id="7c184-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="7c184-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="7c184-114">dateTime</span></span> | <span data-ttu-id="7c184-115">Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7c184-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="7c184-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c184-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="7c184-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-117">string</span></span>   | <span data-ttu-id="7c184-118">Gibt die Beschreibung des Tasks an.</span><span class="sxs-lookup"><span data-stu-id="7c184-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="7c184-119">**Dokumentation**</span><span class="sxs-lookup"><span data-stu-id="7c184-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="7c184-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-120">string</span></span>   | <span data-ttu-id="7c184-121">Gibt jede zusätzliche Dokumentation für den Task an.</span><span class="sxs-lookup"><span data-stu-id="7c184-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="7c184-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7c184-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="7c184-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-123">string</span></span>   | <span data-ttu-id="7c184-124">Gibt die Sicherheits Beschreibung der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7c184-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="7c184-125">**Ausgangs**</span><span class="sxs-lookup"><span data-stu-id="7c184-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="7c184-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-126">string</span></span>   | <span data-ttu-id="7c184-127">Gibt an, woher die Aufgabe stammt.</span><span class="sxs-lookup"><span data-stu-id="7c184-127">Specifies where the task originated from.</span></span> <span data-ttu-id="7c184-128">Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7c184-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="7c184-129">**RT**</span><span class="sxs-lookup"><span data-stu-id="7c184-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="7c184-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="7c184-130">anyURI</span></span>   | <span data-ttu-id="7c184-131">Gibt den URI der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7c184-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="7c184-132">**Version**</span><span class="sxs-lookup"><span data-stu-id="7c184-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="7c184-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c184-133">string</span></span>   | <span data-ttu-id="7c184-134">Gibt die Versionsnummer der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7c184-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="7c184-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c184-135">Requirements</span></span>



| <span data-ttu-id="7c184-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c184-136">Requirement</span></span> | <span data-ttu-id="7c184-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7c184-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c184-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c184-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7c184-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c184-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c184-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c184-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7c184-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c184-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c184-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c184-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c184-143">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="7c184-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7c184-144">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="7c184-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





