---
title: HexInt8Type einfacher Typ
description: Definiert einen hexadezimalen 1-Byte-Typ.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- HexInt8Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479203"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="2dd9d-104">HexInt8Type einfacher Typ</span><span class="sxs-lookup"><span data-stu-id="2dd9d-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="2dd9d-105">Definiert einen hexadezimalen 1-Byte-Typ.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="2dd9d-106">Muster</span><span class="sxs-lookup"><span data-stu-id="2dd9d-106">Patterns</span></span>

<span data-ttu-id="2dd9d-107">Der einfache **HexInt8Type** -Typ ist eine [Zeichenfolge](/dotnet/api/system.string) , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="2dd9d-108">Der Wert kann zwischen 1 und zwei hexadezimal Zeichen (z. b. 0xA oder 0xac) enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd9d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dd9d-109">Requirements</span></span>



| <span data-ttu-id="2dd9d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dd9d-110">Requirement</span></span> | <span data-ttu-id="2dd9d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="2dd9d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2dd9d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2dd9d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd9d-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dd9d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2dd9d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2dd9d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd9d-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dd9d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

