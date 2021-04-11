---
description: Definiert einen Zeichen Folgentyp für das iconfilepath-Element im mobilen Breitband Profil.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: einfacher iconfiletype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129013"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="2785e-103">einfacher iconfiletype-Typ</span><span class="sxs-lookup"><span data-stu-id="2785e-103">iconFileType Simple Type</span></span>

<span data-ttu-id="2785e-104">Der einfache **iconfiletype** -Typ definiert einen Zeichen Folgentyp für das [**iconfilepath**](schema-iconfilepath-mbnprofile-element.md) -Element im mobilen Breitband Profil.</span><span class="sxs-lookup"><span data-stu-id="2785e-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="2785e-105">Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 1024 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="2785e-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="2785e-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2785e-106">Requirements</span></span>



| <span data-ttu-id="2785e-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2785e-107">Requirement</span></span> | <span data-ttu-id="2785e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2785e-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2785e-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2785e-109">Minimum supported client</span></span><br/> | <span data-ttu-id="2785e-110">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2785e-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2785e-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2785e-111">Minimum supported server</span></span><br/> | <span data-ttu-id="2785e-112">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2785e-112">None supported</span></span><br/>                         |



 

 




