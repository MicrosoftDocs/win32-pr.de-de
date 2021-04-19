---
title: HexInt64Type Simple Type (Ereignis Schema)
description: Definiert einen 8-Byte-hexadezimal-Typ. | HexInt64Type Simple Type (Ereignis Schema)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- HexInt64Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366417"
---
# <a name="hexint64type-simple-type-event-schema"></a><span data-ttu-id="c8cd9-105">HexInt64Type Simple Type (Ereignis Schema)</span><span class="sxs-lookup"><span data-stu-id="c8cd9-105">HexInt64Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="c8cd9-106">Definiert einen 8-Byte-hexadezimal-Typ.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="c8cd9-107">Muster</span><span class="sxs-lookup"><span data-stu-id="c8cd9-107">Patterns</span></span>

<span data-ttu-id="c8cd9-108">Der einfache **HexInt64Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="c8cd9-108">The **HexInt64Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="c8cd9-109">Der Wert kann zwischen einem und sechzehn hexadezimalen Zeichen (z. b. 0xA oder 0xac7bd361004fe190) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8cd9-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cd9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8cd9-110">Requirements</span></span>



| <span data-ttu-id="c8cd9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8cd9-111">Requirement</span></span> | <span data-ttu-id="c8cd9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c8cd9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8cd9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8cd9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cd9-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8cd9-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8cd9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8cd9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cd9-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8cd9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





