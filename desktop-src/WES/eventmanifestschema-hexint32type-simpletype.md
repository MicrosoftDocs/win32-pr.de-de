---
title: UInt32Type simple-Typ (Windows-Ereignisprotokoll)
description: Definiert einen ganzzahligen Typ ohne Vorzeichen.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949828"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="8de2c-104">UInt32Type simple-Typ (Windows-Ereignisprotokoll)</span><span class="sxs-lookup"><span data-stu-id="8de2c-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="8de2c-105">Definiert einen ganzzahligen Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="8de2c-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="8de2c-106">Der Wert kann als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich zwischen 0 und 4.294.967.295 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8de2c-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="8de2c-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8de2c-107">Requirements</span></span>



| <span data-ttu-id="8de2c-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8de2c-108">Requirement</span></span> | <span data-ttu-id="8de2c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8de2c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8de2c-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8de2c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8de2c-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8de2c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8de2c-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8de2c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8de2c-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8de2c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





