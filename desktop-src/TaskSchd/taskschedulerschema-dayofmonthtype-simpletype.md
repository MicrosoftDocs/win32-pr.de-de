---
title: Dateityp "dayof monthtype"
description: Definiert die möglichen Werte zum Angeben eines Monats Tags.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- der Typ "dayof monthtype" ist Taskplaner
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517504"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="420f6-104">Dateityp "dayof monthtype"</span><span class="sxs-lookup"><span data-stu-id="420f6-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="420f6-105">Definiert die möglichen Werte zum Angeben eines Monats Tags.</span><span class="sxs-lookup"><span data-stu-id="420f6-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="420f6-106">Muster</span><span class="sxs-lookup"><span data-stu-id="420f6-106">Patterns</span></span>

<span data-ttu-id="420f6-107">Der einfache Typ " **dayosmonthtype** " ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="420f6-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="420f6-108">Gibt den 1. bis zum 31. Tag des Monats oder immer den letzten Tag des Monats an.</span><span class="sxs-lookup"><span data-stu-id="420f6-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="420f6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="420f6-109">Requirements</span></span>



| <span data-ttu-id="420f6-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="420f6-110">Requirement</span></span> | <span data-ttu-id="420f6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="420f6-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="420f6-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="420f6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="420f6-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="420f6-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="420f6-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="420f6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="420f6-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="420f6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="420f6-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="420f6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420f6-117">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="420f6-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="420f6-118">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="420f6-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





