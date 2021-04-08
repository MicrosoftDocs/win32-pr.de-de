---
title: komplexer idletriggertype-Typ
description: Definiert den Basistyp für das idleauslöserelement.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- komplexer idletriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97868d5b13f224bc55661b681246be29f3a4a20b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740448"
---
# <a name="idletriggertype-complex-type"></a><span data-ttu-id="94c60-104">komplexer idletriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="94c60-104">idleTriggerType Complex Type</span></span>

<span data-ttu-id="94c60-105">Definiert den Basistyp für das [**idleauslöserelement**](taskschedulerschema-idletrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="94c60-105">Defines the base type for the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="94c60-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94c60-106">Requirements</span></span>



| <span data-ttu-id="94c60-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94c60-107">Requirement</span></span> | <span data-ttu-id="94c60-108">Wert</span><span class="sxs-lookup"><span data-stu-id="94c60-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94c60-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94c60-109">Minimum supported client</span></span><br/> | <span data-ttu-id="94c60-110">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94c60-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94c60-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94c60-111">Minimum supported server</span></span><br/> | <span data-ttu-id="94c60-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94c60-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94c60-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94c60-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c60-114">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="94c60-114">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="94c60-115">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="94c60-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





