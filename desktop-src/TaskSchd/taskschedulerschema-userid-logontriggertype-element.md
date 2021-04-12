---
title: UserID-Element (logontriggertype)
description: Der Bezeichner des Benutzers. Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserID-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519108"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="fd7d4-105">UserID-Element (logontriggertype)</span><span class="sxs-lookup"><span data-stu-id="fd7d4-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="fd7d4-106">Der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-106">Identifier of the user.</span></span> <span data-ttu-id="fd7d4-107">Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="fd7d4-108">Das **UserID** -Element wird durch den komplexen [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fd7d4-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="fd7d4-109">Parent element</span></span>



| <span data-ttu-id="fd7d4-110">Element</span><span class="sxs-lookup"><span data-stu-id="fd7d4-110">Element</span></span>                                                                       | <span data-ttu-id="fd7d4-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="fd7d4-111">Derived from</span></span>                                                                 | <span data-ttu-id="fd7d4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd7d4-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="fd7d4-113">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="fd7d4-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="fd7d4-114">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="fd7d4-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="fd7d4-115">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fd7d4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd7d4-116">Remarks</span></span>

<span data-ttu-id="fd7d4-117">Bei der Skripterstellung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**logonauslöst. UserID**](logontrigger-userid.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="fd7d4-118">Bei der C++-Entwicklung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**iLogon-Eigenschaft:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd7d4-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="fd7d4-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd7d4-119">Examples</span></span>

<span data-ttu-id="fd7d4-120">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Logon-Vorgang angibt, finden Sie unter [Logon-auslöserbeispiel (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="fd7d4-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7d4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd7d4-121">Requirements</span></span>



| <span data-ttu-id="fd7d4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd7d4-122">Requirement</span></span> | <span data-ttu-id="fd7d4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fd7d4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd7d4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd7d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7d4-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7d4-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd7d4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd7d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7d4-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7d4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd7d4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd7d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7d4-129">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="fd7d4-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fd7d4-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fd7d4-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





