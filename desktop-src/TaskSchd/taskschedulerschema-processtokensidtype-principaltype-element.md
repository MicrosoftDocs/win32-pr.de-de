---
title: Processtokensidtype (principaltype)-Element
description: Gibt den Typ der Prozess Sicherheits Identifizierung (SID) der Aufgabe an.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Processtokensidtype-Element Taskplaner
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104631"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="ef13a-104">Processtokensidtype (principaltype)-Element</span><span class="sxs-lookup"><span data-stu-id="ef13a-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="ef13a-105">Gibt den Typ der Prozess Sicherheits Identifizierung (SID) der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="ef13a-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="ef13a-106">Das **processtokensidtype** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ef13a-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ef13a-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ef13a-107">Parent element</span></span>



| <span data-ttu-id="ef13a-108">Element</span><span class="sxs-lookup"><span data-stu-id="ef13a-108">Element</span></span>                                                                  | <span data-ttu-id="ef13a-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ef13a-109">Derived from</span></span>                                                           | <span data-ttu-id="ef13a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef13a-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ef13a-111">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="ef13a-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="ef13a-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="ef13a-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="ef13a-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="ef13a-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ef13a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef13a-114">Remarks</span></span>

<span data-ttu-id="ef13a-115">Bei der C++-Entwicklung wird der Prozess-SID-Typ mithilfe der [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ef13a-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ef13a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef13a-116">Examples</span></span>

<span data-ttu-id="ef13a-117">Der folgende XML-Code definiert den Prozess-SID-Typ der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ef13a-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="ef13a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef13a-118">Requirements</span></span>



| <span data-ttu-id="ef13a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef13a-119">Requirement</span></span> | <span data-ttu-id="ef13a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ef13a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef13a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef13a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef13a-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef13a-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ef13a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef13a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef13a-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef13a-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef13a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef13a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef13a-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ef13a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





