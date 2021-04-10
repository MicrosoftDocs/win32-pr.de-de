---
title: UInt64Type Simple Type (eventmanifest-Schema)
description: Definiert einen Long-Typ ohne Vorzeichen.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040562"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="4b4dd-104">UInt64Type einfacher Typ</span><span class="sxs-lookup"><span data-stu-id="4b4dd-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="4b4dd-105">Definiert einen Long-Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-105">Defines an unsigned long type.</span></span> <span data-ttu-id="4b4dd-106">Der Wert kann als 8-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 18446744073709551615 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="4b4dd-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b4dd-107">Requirements</span></span>



| <span data-ttu-id="4b4dd-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b4dd-108">Requirement</span></span> | <span data-ttu-id="4b4dd-109">Wert</span><span class="sxs-lookup"><span data-stu-id="4b4dd-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b4dd-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b4dd-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4dd-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b4dd-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b4dd-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b4dd-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4dd-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b4dd-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





