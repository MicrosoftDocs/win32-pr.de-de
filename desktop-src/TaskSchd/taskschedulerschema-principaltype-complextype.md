---
title: komplexer principaltype-Typ
description: Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungs Informationen für das Prinzipal Element.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- komplexer principaltype-Typ Taskplaner
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478168"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="26923-104">komplexer principaltype-Typ</span><span class="sxs-lookup"><span data-stu-id="26923-104">principalType Complex Type</span></span>

<span data-ttu-id="26923-105">Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungs Informationen für das [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) Element.</span><span class="sxs-lookup"><span data-stu-id="26923-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="26923-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26923-106">Child elements</span></span>



| <span data-ttu-id="26923-107">Element</span><span class="sxs-lookup"><span data-stu-id="26923-107">Element</span></span>                                                                                             | <span data-ttu-id="26923-108">type</span><span class="sxs-lookup"><span data-stu-id="26923-108">Type</span></span>                                                                                     | <span data-ttu-id="26923-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26923-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26923-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="26923-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="26923-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26923-111">string</span></span>                                                                                   | <span data-ttu-id="26923-112">Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="26923-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="26923-113">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="26923-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="26923-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="26923-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="26923-115">Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26923-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="26923-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="26923-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="26923-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="26923-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="26923-118">Gibt die Sicherheits Anmelde Methode an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26923-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="26923-119">**Processtokensidtype**</span><span class="sxs-lookup"><span data-stu-id="26923-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="26923-120">**processtokensidtype**</span><span class="sxs-lookup"><span data-stu-id="26923-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="26923-121">Gibt die Typen der Prozess Sicherheits-ID (SID) an, die von Tasks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="26923-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="26923-122">**Requirements-Privilegien**</span><span class="sxs-lookup"><span data-stu-id="26923-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="26923-123">**Requirements dprivilegestype**</span><span class="sxs-lookup"><span data-stu-id="26923-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="26923-124">Gibt die erforderlichen Berechtigungen zum Ausführen der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="26923-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="26923-125">**Ausführungs Ebene**</span><span class="sxs-lookup"><span data-stu-id="26923-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="26923-126">**runleveltype**</span><span class="sxs-lookup"><span data-stu-id="26923-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="26923-127">Gibt die Berechtigungsebene an, auf der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26923-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="26923-128">**UserID**</span><span class="sxs-lookup"><span data-stu-id="26923-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="26923-129">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="26923-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="26923-130">Gibt die Benutzer-ID an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26923-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="26923-131">Attributes</span><span class="sxs-lookup"><span data-stu-id="26923-131">Attributes</span></span>



| <span data-ttu-id="26923-132">Name</span><span class="sxs-lookup"><span data-stu-id="26923-132">Name</span></span> | <span data-ttu-id="26923-133">type</span><span class="sxs-lookup"><span data-stu-id="26923-133">Type</span></span> | <span data-ttu-id="26923-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26923-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="26923-135">id</span><span class="sxs-lookup"><span data-stu-id="26923-135">id</span></span>   | <span data-ttu-id="26923-136">id</span><span class="sxs-lookup"><span data-stu-id="26923-136">ID</span></span>   | <span data-ttu-id="26923-137">Gibt den Bezeichner des Prinzipals an.</span><span class="sxs-lookup"><span data-stu-id="26923-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="26923-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26923-138">Requirements</span></span>



| <span data-ttu-id="26923-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26923-139">Requirement</span></span> | <span data-ttu-id="26923-140">Wert</span><span class="sxs-lookup"><span data-stu-id="26923-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="26923-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26923-141">Minimum supported client</span></span><br/> | <span data-ttu-id="26923-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26923-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="26923-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26923-143">Minimum supported server</span></span><br/> | <span data-ttu-id="26923-144">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26923-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26923-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26923-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26923-146">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="26923-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="26923-147">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="26923-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





