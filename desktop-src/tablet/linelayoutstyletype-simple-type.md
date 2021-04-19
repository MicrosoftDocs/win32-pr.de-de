---
description: Definiert die gültigen Werte für das Style-Attribut des linelayout-Elements.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Einfacher linelayoutstyletype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349698"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="4b22f-103">Einfacher linelayoutstyletype-Typ</span><span class="sxs-lookup"><span data-stu-id="4b22f-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="4b22f-104">Definiert die gültigen Werte für das **Style** -Attribut des [linelayout-Elements](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="4b22f-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="4b22f-105">Muster</span><span class="sxs-lookup"><span data-stu-id="4b22f-105">Patterns</span></span>

<span data-ttu-id="4b22f-106">Der einfache Typ **linelayoutstyletype** ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="4b22f-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="4b22f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b22f-107">Remarks</span></span>

<span data-ttu-id="4b22f-108">Gültige Werte für das **Style** -Attribut des [linelayout-Elements](linelayout-element.md) sind:</span><span class="sxs-lookup"><span data-stu-id="4b22f-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="4b22f-109">Keine</span><span class="sxs-lookup"><span data-stu-id="4b22f-109">None</span></span>
-   <span data-ttu-id="4b22f-110">Basis</span><span class="sxs-lookup"><span data-stu-id="4b22f-110">Solid</span></span>
-   <span data-ttu-id="4b22f-111">Strich</span><span class="sxs-lookup"><span data-stu-id="4b22f-111">Dash</span></span>
-   <span data-ttu-id="4b22f-112">Punkt</span><span class="sxs-lookup"><span data-stu-id="4b22f-112">Dot</span></span>
-   <span data-ttu-id="4b22f-113">DashDot</span><span class="sxs-lookup"><span data-stu-id="4b22f-113">DashDot</span></span>
-   <span data-ttu-id="4b22f-114">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="4b22f-114">DashDotDot</span></span>
-   <span data-ttu-id="4b22f-115">Double</span><span class="sxs-lookup"><span data-stu-id="4b22f-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="4b22f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b22f-116">Requirements</span></span>



| <span data-ttu-id="4b22f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b22f-117">Requirement</span></span> | <span data-ttu-id="4b22f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4b22f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4b22f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b22f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b22f-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b22f-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b22f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b22f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b22f-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4b22f-122">None supported</span></span><br/>                                     |



 

 




