---
title: Display Name (principaltype)-Element
description: Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Display Name-Element Taskplaner
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519135"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="728be-104">Display Name (principaltype)-Element</span><span class="sxs-lookup"><span data-stu-id="728be-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="728be-105">Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="728be-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="728be-106">Das **Display Name** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="728be-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="728be-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="728be-107">Parent element</span></span>



| <span data-ttu-id="728be-108">Element</span><span class="sxs-lookup"><span data-stu-id="728be-108">Element</span></span>                                                                  | <span data-ttu-id="728be-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="728be-109">Derived from</span></span>                                                           | <span data-ttu-id="728be-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="728be-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="728be-111">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="728be-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="728be-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="728be-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="728be-113">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="728be-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="728be-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="728be-114">Remarks</span></span>

<span data-ttu-id="728be-115">Bei der Skripterstellung wird der Anzeige Name des Prinzipals mit der [**Principal. Display Name**](principal-displayname.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="728be-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="728be-116">Bei der C++-Entwicklung wird der Anzeige Name des Prinzipals mithilfe der [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="728be-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="728be-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728be-117">Examples</span></span>

<span data-ttu-id="728be-118">Der folgende XML-Code definiert eine mithilfe eines Gruppen Bezeichners und eines anzeigen Amens.</span><span class="sxs-lookup"><span data-stu-id="728be-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="728be-119">Der folgende XML-Code definiert einen Prinzipal mithilfe eines Benutzer Bezeichners und eines anzeigen Amens.</span><span class="sxs-lookup"><span data-stu-id="728be-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="728be-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="728be-120">Requirements</span></span>



| <span data-ttu-id="728be-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="728be-121">Requirement</span></span> | <span data-ttu-id="728be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="728be-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="728be-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="728be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="728be-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728be-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="728be-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="728be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="728be-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728be-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="728be-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="728be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728be-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="728be-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





