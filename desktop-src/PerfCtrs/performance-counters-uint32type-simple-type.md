---
description: Definiert einen ganzzahligen Typ ohne Vorzeichen.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: UInt32Type Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348611"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="a03bc-103">UInt32Type Simple Type (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="a03bc-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="a03bc-104">Definiert einen ganzzahligen Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a03bc-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="a03bc-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a03bc-105">Remarks</span></span>

<span data-ttu-id="a03bc-106">Sie können den Wert als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angeben.</span><span class="sxs-lookup"><span data-stu-id="a03bc-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="a03bc-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a03bc-107">Requirements</span></span>



| <span data-ttu-id="a03bc-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a03bc-108">Requirement</span></span> | <span data-ttu-id="a03bc-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a03bc-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a03bc-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a03bc-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a03bc-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a03bc-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a03bc-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a03bc-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a03bc-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a03bc-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




