---
title: komplexer Typ "Requirements dprivilegestype"
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Requirements dprivileges (Requirements dprivilegestype)-Element.
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- komplexer Typ "Requirements dprivilegestype" Taskplaner
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479227"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="eb14c-104">komplexer Typ "Requirements dprivilegestype"</span><span class="sxs-lookup"><span data-stu-id="eb14c-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="eb14c-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Requirements [**dprivileges (Requirements dprivilegestype)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="eb14c-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="eb14c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb14c-106">Child elements</span></span>



| <span data-ttu-id="eb14c-107">Element</span><span class="sxs-lookup"><span data-stu-id="eb14c-107">Element</span></span>                                                                           | <span data-ttu-id="eb14c-108">type</span><span class="sxs-lookup"><span data-stu-id="eb14c-108">Type</span></span>                                                                  | <span data-ttu-id="eb14c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb14c-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="eb14c-110">**Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="eb14c-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="eb14c-111">**PrivilegeType**</span><span class="sxs-lookup"><span data-stu-id="eb14c-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="eb14c-112">Gibt die erforderlichen Berechtigungen für den Task an.</span><span class="sxs-lookup"><span data-stu-id="eb14c-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="eb14c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb14c-113">Requirements</span></span>



| <span data-ttu-id="eb14c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb14c-114">Requirement</span></span> | <span data-ttu-id="eb14c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="eb14c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="eb14c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb14c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eb14c-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb14c-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="eb14c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb14c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eb14c-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb14c-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb14c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb14c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb14c-121">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="eb14c-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="eb14c-122">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="eb14c-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





