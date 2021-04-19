---
title: einfacher runleveltype-Typ
description: Definiert die möglichen Werte für das Runlevel-Element (principaltype).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- einfacher runleveltype-Typ Taskplaner
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342863"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="18871-104">einfacher runleveltype-Typ</span><span class="sxs-lookup"><span data-stu-id="18871-104">runLevelType Simple Type</span></span>

<span data-ttu-id="18871-105">Definiert die möglichen Werte für das [**Runlevel-Element (principaltype)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="18871-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="18871-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="18871-106">Enumeration values</span></span>

<span data-ttu-id="18871-107">Der einfache **runleveltype** -Typ definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="18871-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="18871-108">Wert</span><span class="sxs-lookup"><span data-stu-id="18871-108">Value</span></span>            | <span data-ttu-id="18871-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18871-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="18871-110">Leastprivilege</span><span class="sxs-lookup"><span data-stu-id="18871-110">LeastPrivilege</span></span>   | <span data-ttu-id="18871-111">Tasks werden mit den geringsten Berechtigungen (LUA) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18871-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="18871-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="18871-112">HighestAvailable</span></span> | <span data-ttu-id="18871-113">Tasks werden mit den höchsten Berechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18871-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="18871-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18871-114">Requirements</span></span>



| <span data-ttu-id="18871-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18871-115">Requirement</span></span> | <span data-ttu-id="18871-116">Wert</span><span class="sxs-lookup"><span data-stu-id="18871-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18871-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18871-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18871-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18871-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18871-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18871-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18871-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18871-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





