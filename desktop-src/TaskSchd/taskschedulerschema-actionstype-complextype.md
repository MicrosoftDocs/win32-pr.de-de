---
title: komplexer aktionstype-Typ
description: Definiert die untergeordneten Elemente und das Attribut für das Actions-Element.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- komplexer aktionstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392085"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="fa02c-104">komplexer aktionstype-Typ</span><span class="sxs-lookup"><span data-stu-id="fa02c-104">actionsType Complex Type</span></span>

<span data-ttu-id="fa02c-105">Definiert die untergeordneten Elemente und das Attribut für das [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="fa02c-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="fa02c-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="fa02c-106">Attributes</span></span>



| <span data-ttu-id="fa02c-107">Name</span><span class="sxs-lookup"><span data-stu-id="fa02c-107">Name</span></span>    | <span data-ttu-id="fa02c-108">type</span><span class="sxs-lookup"><span data-stu-id="fa02c-108">Type</span></span>  | <span data-ttu-id="fa02c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa02c-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa02c-110">Kontext</span><span class="sxs-lookup"><span data-stu-id="fa02c-110">Context</span></span> | <span data-ttu-id="fa02c-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="fa02c-111">IDREF</span></span> | <span data-ttu-id="fa02c-112">Prinzipal Bezeichner des verwendeten, der der Sicherheitskontext für die Aktionen der Aufgabe ist.</span><span class="sxs-lookup"><span data-stu-id="fa02c-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fa02c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa02c-113">Requirements</span></span>



| <span data-ttu-id="fa02c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa02c-114">Requirement</span></span> | <span data-ttu-id="fa02c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fa02c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa02c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa02c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa02c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa02c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa02c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa02c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa02c-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa02c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa02c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa02c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa02c-121">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="fa02c-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="fa02c-122">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fa02c-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





