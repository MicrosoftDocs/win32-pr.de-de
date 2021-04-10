---
title: HexInt32Type Simple Type (Ereignis Schema)
description: Definiert einen 4-Byte-hexadezimal-Typ. | HexInt32Type Simple Type (Ereignis Schema)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- HexInt32Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961372"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="532fd-105">HexInt32Type Simple Type (Ereignis Schema)</span><span class="sxs-lookup"><span data-stu-id="532fd-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="532fd-106">Definiert einen 4-Byte-hexadezimal-Typ.</span><span class="sxs-lookup"><span data-stu-id="532fd-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="532fd-107">Muster</span><span class="sxs-lookup"><span data-stu-id="532fd-107">Patterns</span></span>

<span data-ttu-id="532fd-108">Der einfache **HexInt32Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="532fd-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="532fd-109">Der Wert kann zwischen 1 und acht hexadezimal Zeichen (z. b. 0xA oder 0xac7bd361) enthalten.</span><span class="sxs-lookup"><span data-stu-id="532fd-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="532fd-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="532fd-110">Requirements</span></span>



| <span data-ttu-id="532fd-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="532fd-111">Requirement</span></span> | <span data-ttu-id="532fd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="532fd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="532fd-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="532fd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="532fd-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="532fd-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="532fd-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="532fd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="532fd-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="532fd-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





