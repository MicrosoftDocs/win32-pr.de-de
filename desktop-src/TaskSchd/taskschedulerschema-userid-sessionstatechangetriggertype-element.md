---
title: UserID (sessionstatechangetriggertype)-Element
description: Enthält den Benutzer für die Terminal Server Sitzung. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
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
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518587"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="5c009-105">UserID (sessionstatechangetriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="5c009-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="5c009-106">Enthält den Benutzer für die Terminal Server Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5c009-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="5c009-107">Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.</span><span class="sxs-lookup"><span data-stu-id="5c009-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="5c009-108">Das **UserID** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="5c009-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5c009-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5c009-109">Parent element</span></span>



| <span data-ttu-id="5c009-110">Element</span><span class="sxs-lookup"><span data-stu-id="5c009-110">Element</span></span>                       | <span data-ttu-id="5c009-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="5c009-111">Derived from</span></span>                                                                                           | <span data-ttu-id="5c009-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c009-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c009-113">**Sessionstatechange-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="5c009-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="5c009-114">**sessionstatechangetriggertype**</span><span class="sxs-lookup"><span data-stu-id="5c009-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="5c009-115">Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="5c009-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c009-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c009-116">Remarks</span></span>

<span data-ttu-id="5c009-117">Informationen zur C++-Entwicklung finden Sie unter [**UserId-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="5c009-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="5c009-118">Informationen zur Skript Entwicklung finden Sie unter [**sessionstatechange-Benutzer-ID**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="5c009-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c009-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c009-119">Requirements</span></span>



| <span data-ttu-id="5c009-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c009-120">Requirement</span></span> | <span data-ttu-id="5c009-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5c009-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c009-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c009-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c009-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c009-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c009-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c009-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c009-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c009-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





