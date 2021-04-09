---
title: Requirements dprivileges (Requirements-privilegestype)-Element
description: Gibt die Berechtigungen an, die für die Aufgabe erforderlich sind.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Requirements dprivileges-Element Taskplaner
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106353"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="d5fb2-104">Requirements dprivileges (Requirements-privilegestype)-Element</span><span class="sxs-lookup"><span data-stu-id="d5fb2-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="d5fb2-105">Gibt die Berechtigungen an, die für die Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d5fb2-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="d5fb2-106">Das Element "Requirements **dprivileges** " wird durch den komplexen Typ "Requirements [**dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="d5fb2-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d5fb2-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d5fb2-107">Parent element</span></span>



| <span data-ttu-id="d5fb2-108">Element</span><span class="sxs-lookup"><span data-stu-id="d5fb2-108">Element</span></span>                                                                                  | <span data-ttu-id="d5fb2-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d5fb2-109">Derived from</span></span>                                                           | <span data-ttu-id="d5fb2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5fb2-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d5fb2-111">**Prinzipal (principaltype)**</span><span class="sxs-lookup"><span data-stu-id="d5fb2-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="d5fb2-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="d5fb2-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="d5fb2-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="d5fb2-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d5fb2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5fb2-114">Remarks</span></span>

<span data-ttu-id="d5fb2-115">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2:: Requirements dprivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d5fb2-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="d5fb2-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5fb2-116">Examples</span></span>

<span data-ttu-id="d5fb2-117">Der folgende XML-Code definiert die Verwendung eines Gruppen Bezeichners und der erforderlichen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="d5fb2-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="d5fb2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5fb2-118">Requirements</span></span>



| <span data-ttu-id="d5fb2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5fb2-119">Requirement</span></span> | <span data-ttu-id="d5fb2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d5fb2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d5fb2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5fb2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fb2-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5fb2-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d5fb2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5fb2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fb2-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5fb2-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5fb2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5fb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fb2-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d5fb2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





