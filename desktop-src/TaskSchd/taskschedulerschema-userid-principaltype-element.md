---
title: UserID (principaltype)-Element
description: Gibt die Benutzer-ID an, die erforderlich ist, um die dem Prinzipal zugeordneten Tasks auszuführen
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392220"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="a66d6-104">UserID (principaltype)-Element</span><span class="sxs-lookup"><span data-stu-id="a66d6-104">UserId (principalType) Element</span></span>

<span data-ttu-id="a66d6-105">Gibt die Benutzer-ID an, die erforderlich ist, um die dem Prinzipal zugeordneten Tasks auszuführen</span><span class="sxs-lookup"><span data-stu-id="a66d6-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="a66d6-106">Das **UserID** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a66d6-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a66d6-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a66d6-107">Parent element</span></span>



| <span data-ttu-id="a66d6-108">Element</span><span class="sxs-lookup"><span data-stu-id="a66d6-108">Element</span></span>                                                                  | <span data-ttu-id="a66d6-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a66d6-109">Derived from</span></span>                                                           | <span data-ttu-id="a66d6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a66d6-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="a66d6-111">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="a66d6-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="a66d6-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="a66d6-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="a66d6-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="a66d6-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a66d6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a66d6-114">Remarks</span></span>

<span data-ttu-id="a66d6-115">Das **UserID** -Element und das [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Element werden verwendet, um den Benutzer zu definieren, der zum Ausführen dieser Aufgaben erforderlich ist, die diesen Prinzipal verwenden.</span><span class="sxs-lookup"><span data-stu-id="a66d6-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="a66d6-116">Sie können nicht gleichzeitig eine Benutzer-ID und einen Gruppen Bezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="a66d6-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="a66d6-117">Geben Sie entweder das **UserID** -oder das [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) -Element an, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="a66d6-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="a66d6-118">Bei der Skripterstellung wird die Benutzer-ID mithilfe der [**Principal. UserID**](principal-userid.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a66d6-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="a66d6-119">Bei der C++-Entwicklung wird der Benutzer Bezeichner mithilfe der [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a66d6-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a66d6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a66d6-120">Examples</span></span>

<span data-ttu-id="a66d6-121">Der folgende XML-Code definiert ein Prinzip mithilfe eines Benutzer Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="a66d6-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="a66d6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a66d6-122">Requirements</span></span>



| <span data-ttu-id="a66d6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a66d6-123">Requirement</span></span> | <span data-ttu-id="a66d6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a66d6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a66d6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a66d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a66d6-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a66d6-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a66d6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a66d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a66d6-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a66d6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a66d6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a66d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66d6-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a66d6-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





