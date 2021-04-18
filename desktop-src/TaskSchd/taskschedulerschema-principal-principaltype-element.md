---
title: Principal (principaltype)-Element
description: Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Principal-Element Taskplaner
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340312"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="65058-104">Principal (principaltype)-Element</span><span class="sxs-lookup"><span data-stu-id="65058-104">Principal (principalType) Element</span></span>

<span data-ttu-id="65058-105">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="65058-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="65058-106">Mit diesen Anmelde Informationen wird der Sicherheitskontext definiert, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65058-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="65058-107">Das **Principal** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="65058-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="65058-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="65058-108">Parent element</span></span>



| <span data-ttu-id="65058-109">Element</span><span class="sxs-lookup"><span data-stu-id="65058-109">Element</span></span>                                                               | <span data-ttu-id="65058-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="65058-110">Derived from</span></span>                                                             | <span data-ttu-id="65058-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65058-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="65058-112">**Principals**</span><span class="sxs-lookup"><span data-stu-id="65058-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="65058-113">**principalstype**</span><span class="sxs-lookup"><span data-stu-id="65058-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="65058-114">Gibt die dem Task zugeordneten Sicherheits Prinzipale an.</span><span class="sxs-lookup"><span data-stu-id="65058-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="65058-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65058-115">Child elements</span></span>



| <span data-ttu-id="65058-116">Element</span><span class="sxs-lookup"><span data-stu-id="65058-116">Element</span></span>                                                                      | <span data-ttu-id="65058-117">type</span><span class="sxs-lookup"><span data-stu-id="65058-117">Type</span></span>                                                          | <span data-ttu-id="65058-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65058-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65058-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="65058-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="65058-120">**string**</span><span class="sxs-lookup"><span data-stu-id="65058-120">**string**</span></span>                                                    | <span data-ttu-id="65058-121">Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="65058-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="65058-122">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="65058-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="65058-123">**string**</span><span class="sxs-lookup"><span data-stu-id="65058-123">**string**</span></span>                                                    | <span data-ttu-id="65058-124">Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="65058-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="65058-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="65058-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="65058-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="65058-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="65058-127">Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="65058-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="65058-128">**UserID**</span><span class="sxs-lookup"><span data-stu-id="65058-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="65058-129">**string**</span><span class="sxs-lookup"><span data-stu-id="65058-129">**string**</span></span>                                                    | <span data-ttu-id="65058-130">Gibt die Benutzer-ID an, die erforderlich ist, um dem Prinzipal zugeordnete Tasks auszuführen</span><span class="sxs-lookup"><span data-stu-id="65058-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="65058-131">Attributes</span><span class="sxs-lookup"><span data-stu-id="65058-131">Attributes</span></span>



| <span data-ttu-id="65058-132">Name</span><span class="sxs-lookup"><span data-stu-id="65058-132">Name</span></span> | <span data-ttu-id="65058-133">type</span><span class="sxs-lookup"><span data-stu-id="65058-133">Type</span></span> | <span data-ttu-id="65058-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65058-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="65058-135">Id</span><span class="sxs-lookup"><span data-stu-id="65058-135">Id</span></span>   | <span data-ttu-id="65058-136">id</span><span class="sxs-lookup"><span data-stu-id="65058-136">ID</span></span>   | <span data-ttu-id="65058-137">Der Bezeichner der Prinzipal Definition.</span><span class="sxs-lookup"><span data-stu-id="65058-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65058-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65058-138">Remarks</span></span>

<span data-ttu-id="65058-139">Bei der Skripterstellung werden die Sicherheits Anmelde Informationen für einen Prinzipal mithilfe des [**Prinzipal**](principal.md) Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="65058-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="65058-140">Bei der C++-Entwicklung werden die Sicherheits Anmelde Informationen für einen Prinzipal mithilfe der [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) -Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="65058-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="65058-141">Die oben aufgeführten untergeordneten Elemente werden durch den komplexen Typ " [**principaltype**](taskschedulerschema-principaltype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="65058-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="65058-142">Informationen zur Sequenzierung für diese untergeordneten Elemente finden Sie unter [**principaltype**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="65058-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="65058-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65058-143">Examples</span></span>

<span data-ttu-id="65058-144">Im folgenden XML-Code wird ein Prinzipal mit einer Benutzer-ID definiert.</span><span class="sxs-lookup"><span data-stu-id="65058-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="65058-145">Der folgende XML-Code definiert einen Prinzipal mit einem Gruppen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="65058-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="65058-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65058-146">Requirements</span></span>



| <span data-ttu-id="65058-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65058-147">Requirement</span></span> | <span data-ttu-id="65058-148">Wert</span><span class="sxs-lookup"><span data-stu-id="65058-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65058-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65058-149">Minimum supported client</span></span><br/> | <span data-ttu-id="65058-150">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65058-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65058-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65058-151">Minimum supported server</span></span><br/> | <span data-ttu-id="65058-152">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65058-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65058-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65058-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65058-154">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="65058-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





