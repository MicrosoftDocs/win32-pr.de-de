---
title: GroupId-Element (principaltype)
description: Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen dieser Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- GroupId-Element Taskplaner
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040871"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="c3bbd-104">GroupId-Element (principaltype)</span><span class="sxs-lookup"><span data-stu-id="c3bbd-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="c3bbd-105">Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen dieser Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="c3bbd-106">Das **GroupID** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c3bbd-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c3bbd-107">Parent element</span></span>



| <span data-ttu-id="c3bbd-108">Element</span><span class="sxs-lookup"><span data-stu-id="c3bbd-108">Element</span></span>                                                                  | <span data-ttu-id="c3bbd-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="c3bbd-109">Derived from</span></span>                                                           | <span data-ttu-id="c3bbd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3bbd-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c3bbd-111">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="c3bbd-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="c3bbd-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="c3bbd-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="c3bbd-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c3bbd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3bbd-114">Remarks</span></span>

<span data-ttu-id="c3bbd-115">Sie können nicht gleichzeitig einen Gruppen Bezeichner und eine Benutzer-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="c3bbd-116">Geben Sie entweder die Elemente [**UserID**](taskschedulerschema-userid-principaltype-element.md) oder **GroupID** an, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="c3bbd-117">Bei der Skript Entwicklung wird der Gruppen Bezeichner des Prinzipals mit der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="c3bbd-118">Bei der C++-Entwicklung wird der Gruppen Bezeichner des Prinzipals mithilfe der [**IPrincipal:: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c3bbd-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3bbd-119">Examples</span></span>

<span data-ttu-id="c3bbd-120">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die dieses Element verwendet, finden Sie unter [Logon-auslöserbeispiel (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="c3bbd-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bbd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3bbd-121">Requirements</span></span>



| <span data-ttu-id="c3bbd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3bbd-122">Requirement</span></span> | <span data-ttu-id="c3bbd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bbd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3bbd-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3bbd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bbd-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3bbd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3bbd-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3bbd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bbd-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3bbd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3bbd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3bbd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bbd-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c3bbd-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





