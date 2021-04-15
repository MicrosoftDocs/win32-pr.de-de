---
title: Berechtigungs Element ("Requirements dprivilegestype")
description: Gibt das Recht einer Aufgabe an, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Berechtigungs Element Taskplaner
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478387"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="ec378-104">Berechtigungs Element ("Requirements dprivilegestype")</span><span class="sxs-lookup"><span data-stu-id="ec378-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="ec378-105">Gibt das Recht einer Aufgabe an, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="ec378-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="ec378-106">Das **Privileg** -Element wird durch den komplexen Typ "Requirements [**dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="ec378-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ec378-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ec378-107">Parent element</span></span>



| <span data-ttu-id="ec378-108">Element</span><span class="sxs-lookup"><span data-stu-id="ec378-108">Element</span></span>                                                                                             | <span data-ttu-id="ec378-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ec378-109">Derived from</span></span>                                                                             | <span data-ttu-id="ec378-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec378-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec378-111">**Requirements-Privilegien**</span><span class="sxs-lookup"><span data-stu-id="ec378-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="ec378-112">**Requirements dprivilegestype**</span><span class="sxs-lookup"><span data-stu-id="ec378-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="ec378-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec378-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ec378-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec378-114">Remarks</span></span>

<span data-ttu-id="ec378-115">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2:: Requirements dprivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ec378-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ec378-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec378-116">Examples</span></span>

<span data-ttu-id="ec378-117">Der folgende XML-Code definiert ein settings-Element, das das Recht eines Tasks angibt, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="ec378-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="ec378-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec378-118">Requirements</span></span>



| <span data-ttu-id="ec378-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec378-119">Requirement</span></span> | <span data-ttu-id="ec378-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ec378-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ec378-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec378-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec378-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec378-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ec378-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec378-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec378-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec378-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec378-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec378-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec378-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ec378-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





