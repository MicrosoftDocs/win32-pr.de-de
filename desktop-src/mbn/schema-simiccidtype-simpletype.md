---
description: Definiert einen Typ für das simiccid-Element des mobilen Breitband Profils.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: einfacher simiccidtype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355488"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="42dd2-103">einfacher simiccidtype-Typ</span><span class="sxs-lookup"><span data-stu-id="42dd2-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="42dd2-104">Der einfache Typ **simiccidtype** definiert einen Typ für das [**simiccid-**](schema-simiccid-mbnprofile-element.md) Element des mobilen Breitband Profils.</span><span class="sxs-lookup"><span data-stu-id="42dd2-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="42dd2-105">Bei diesem Typ handelt es sich um eine Sammlung von Ziffern und/oder groß-und Kleinbuchstaben, mindestens ein Zeichen lang und höchstens 20 Zeichen lang.</span><span class="sxs-lookup"><span data-stu-id="42dd2-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="42dd2-106">Muster</span><span class="sxs-lookup"><span data-stu-id="42dd2-106">Patterns</span></span>

<span data-ttu-id="42dd2-107">Der einfache Typ **simiccidtype** ist ein Token, das durch das folgende Muster eingeschränkt wird:</span><span class="sxs-lookup"><span data-stu-id="42dd2-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="42dd2-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42dd2-108">Requirements</span></span>



| <span data-ttu-id="42dd2-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42dd2-109">Requirement</span></span> | <span data-ttu-id="42dd2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="42dd2-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="42dd2-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42dd2-111">Minimum supported client</span></span><br/> | <span data-ttu-id="42dd2-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="42dd2-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="42dd2-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42dd2-113">Minimum supported server</span></span><br/> | <span data-ttu-id="42dd2-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="42dd2-114">None supported</span></span><br/>                         |



 

 




