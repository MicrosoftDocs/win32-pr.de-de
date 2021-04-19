---
description: Definiert einen 4-Byte-hexadezimal-Typ.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: HexInt32Type Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359040"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="fe27e-103">HexInt32Type Simple Type (Leistungsindikatoren)</span><span class="sxs-lookup"><span data-stu-id="fe27e-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="fe27e-104">Definiert einen 4-Byte-hexadezimal-Typ.</span><span class="sxs-lookup"><span data-stu-id="fe27e-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fe27e-105">Muster</span><span class="sxs-lookup"><span data-stu-id="fe27e-105">Patterns</span></span>

<span data-ttu-id="fe27e-106">Der einfache Typ " **HexInt32Type** " ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="fe27e-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="fe27e-107">Der Wert kann zwischen 1 und acht hexadezimal Zeichen (z. b. 0xA oder 0xac7bd361) enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe27e-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe27e-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe27e-108">Requirements</span></span>



| <span data-ttu-id="fe27e-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe27e-109">Requirement</span></span> | <span data-ttu-id="fe27e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="fe27e-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe27e-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe27e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fe27e-112">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe27e-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe27e-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe27e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fe27e-114">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe27e-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




