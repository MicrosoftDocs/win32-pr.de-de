---
title: weektype simple-Typ
description: Definiert die Werte, die im Week-Element verwendet werden können.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- weektype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103278"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="25ec1-104">weektype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="25ec1-104">weekType Simple Type</span></span>

<span data-ttu-id="25ec1-105">Definiert die Werte, die im [**Week**](taskschedulerschema-week-weekstype-element.md) -Element verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="25ec1-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="25ec1-106">Muster</span><span class="sxs-lookup"><span data-stu-id="25ec1-106">Patterns</span></span>

<span data-ttu-id="25ec1-107">Der einfache **weektype** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="25ec1-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="25ec1-108">Gibt den ersten bis zur vierten Woche des Monats (1-4) oder immer die letzte Woche des Monats an.</span><span class="sxs-lookup"><span data-stu-id="25ec1-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ec1-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25ec1-109">Requirements</span></span>



| <span data-ttu-id="25ec1-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25ec1-110">Requirement</span></span> | <span data-ttu-id="25ec1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="25ec1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25ec1-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25ec1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="25ec1-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ec1-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25ec1-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25ec1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="25ec1-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25ec1-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25ec1-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25ec1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ec1-117">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="25ec1-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="25ec1-118">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="25ec1-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





