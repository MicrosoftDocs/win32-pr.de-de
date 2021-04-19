---
title: UInt8Type einfacher Typ
description: Definiert einen Byte-Typ ohne Vorzeichen.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- UInt8Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342014"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="5849a-104">UInt8Type einfacher Typ</span><span class="sxs-lookup"><span data-stu-id="5849a-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="5849a-105">Definiert einen Byte-Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5849a-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="5849a-106">Der Wert kann als 1-Byte-Ganzzahl oder Hexadezimalwert im Bereich zwischen 0 und 255 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5849a-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5849a-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5849a-107">Requirements</span></span>



| <span data-ttu-id="5849a-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5849a-108">Requirement</span></span> | <span data-ttu-id="5849a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5849a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5849a-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5849a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5849a-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5849a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5849a-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5849a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5849a-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5849a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





