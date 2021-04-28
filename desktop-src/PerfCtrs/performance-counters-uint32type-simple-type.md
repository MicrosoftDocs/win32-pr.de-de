---
description: 'UInt32Type Simple Type (Leistungsindikatoren): Definiert einen Ganzzahltyp ohne Vorzeichen.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Einfacher UInt32Type-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114578"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="6d64d-103">Einfacher UInt32Type-Typ (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="6d64d-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="6d64d-104">Definiert einen ganzzahligen Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="6d64d-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="6d64d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d64d-105">Remarks</span></span>

<span data-ttu-id="6d64d-106">Sie können den Wert als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angeben.</span><span class="sxs-lookup"><span data-stu-id="6d64d-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d64d-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d64d-107">Requirements</span></span>



| <span data-ttu-id="6d64d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d64d-108">Requirement</span></span> | <span data-ttu-id="6d64d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="6d64d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6d64d-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d64d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6d64d-111">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d64d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6d64d-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d64d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6d64d-113">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d64d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




