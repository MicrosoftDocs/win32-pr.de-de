---
title: HexInt16Type einfacher Typ
description: Definiert einen 2-Byte-hexadezimal-Typ.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478663"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="ae30a-104">HexInt16Type einfacher Typ</span><span class="sxs-lookup"><span data-stu-id="ae30a-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="ae30a-105">Definiert einen 2-Byte-hexadezimal-Typ.</span><span class="sxs-lookup"><span data-stu-id="ae30a-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="ae30a-106">Muster</span><span class="sxs-lookup"><span data-stu-id="ae30a-106">Patterns</span></span>

<span data-ttu-id="ae30a-107">Der einfache **HexInt16Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="ae30a-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="ae30a-108">Der Wert kann zwischen einem und vier hexadezimal Zeichen (z. b. 0xA oder 0xac7b) enthalten.</span><span class="sxs-lookup"><span data-stu-id="ae30a-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae30a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae30a-109">Requirements</span></span>



| <span data-ttu-id="ae30a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae30a-110">Requirement</span></span> | <span data-ttu-id="ae30a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ae30a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae30a-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae30a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae30a-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae30a-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae30a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae30a-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





