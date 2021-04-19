---
title: HexInt32Type Simple Type (eventmanifest-Schema)
description: Definiert einen 4-Byte-hexadezimal-Typ. | HexInt32Type Simple Type (eventmanifest-Schema)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
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
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353309"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="19680-105">HexInt32Type Simple Type (eventmanifest-Schema)</span><span class="sxs-lookup"><span data-stu-id="19680-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="19680-106">Definiert einen 4-Byte-hexadezimal-Typ.</span><span class="sxs-lookup"><span data-stu-id="19680-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="19680-107">Muster</span><span class="sxs-lookup"><span data-stu-id="19680-107">Patterns</span></span>

<span data-ttu-id="19680-108">Der einfache **HexInt32Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="19680-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="19680-109">Der Wert kann zwischen 1 und acht hexadezimal Zeichen (z. b. 0xA oder 0xac7bd361) enthalten.</span><span class="sxs-lookup"><span data-stu-id="19680-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="19680-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19680-110">Requirements</span></span>



| <span data-ttu-id="19680-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19680-111">Requirement</span></span> | <span data-ttu-id="19680-112">Wert</span><span class="sxs-lookup"><span data-stu-id="19680-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19680-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19680-113">Minimum supported client</span></span><br/> | <span data-ttu-id="19680-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19680-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19680-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19680-115">Minimum supported server</span></span><br/> | <span data-ttu-id="19680-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19680-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





