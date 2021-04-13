---
description: Definiert einen Zeichen Folgentyp für das ProviderName-Element im mobilen Breitband Profil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: providernametype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526021"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="a01c2-103">providernametype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="a01c2-103">providerNameType Simple Type</span></span>

<span data-ttu-id="a01c2-104">Der einfache Typ **providernametype** definiert einen Zeichen Folgentyp für das [**providerName**](schema-providername-providertype-element.md) -Element im mobilen Breitband Profil.</span><span class="sxs-lookup"><span data-stu-id="a01c2-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="a01c2-105">Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 20 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="a01c2-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a01c2-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a01c2-106">Requirements</span></span>



| <span data-ttu-id="a01c2-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a01c2-107">Requirement</span></span> | <span data-ttu-id="a01c2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a01c2-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a01c2-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a01c2-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a01c2-110">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a01c2-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a01c2-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a01c2-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a01c2-112">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a01c2-112">None supported</span></span><br/>                         |



 

 




