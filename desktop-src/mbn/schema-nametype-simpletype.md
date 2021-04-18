---
description: Definiert einen Zeichen Folgentyp für das mobile Breitband Profil.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: einfacher nametype-Typ (mobiles Breitband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347788"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="2ccf3-103">einfacher nametype-Typ (mobiles Breitband)</span><span class="sxs-lookup"><span data-stu-id="2ccf3-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="2ccf3-104">Der einfache **nametype** -Typ definiert einen Zeichen Folgentyp für das mobile Breitband Profil.</span><span class="sxs-lookup"><span data-stu-id="2ccf3-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="2ccf3-105">Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 255 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="2ccf3-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="2ccf3-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ccf3-106">Requirements</span></span>



| <span data-ttu-id="2ccf3-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ccf3-107">Requirement</span></span> | <span data-ttu-id="2ccf3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2ccf3-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2ccf3-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ccf3-109">Minimum supported client</span></span><br/> | <span data-ttu-id="2ccf3-110">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2ccf3-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2ccf3-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ccf3-111">Minimum supported server</span></span><br/> | <span data-ttu-id="2ccf3-112">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2ccf3-112">None supported</span></span><br/>                         |



 

 




