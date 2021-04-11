---
description: Definiert einen Typ für das ProviderID-Element des mobilen Breitband Profils.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: provideridtype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129008"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="adde3-103">provideridtype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="adde3-103">providerIdType Simple Type</span></span>

<span data-ttu-id="adde3-104">Der einfache Typ **provideridtype** definiert einen Typ für das [**ProviderID**](schema-providerid-providertype-element.md) -Element des mobilen Breitband Profils.</span><span class="sxs-lookup"><span data-stu-id="adde3-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="adde3-105">Bei diesem Typ handelt es sich um eine Sammlung von Ziffern, die mindestens eine Ziffer lang und höchstens 6 Ziffern lang sind.</span><span class="sxs-lookup"><span data-stu-id="adde3-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="adde3-106">Muster</span><span class="sxs-lookup"><span data-stu-id="adde3-106">Patterns</span></span>

<span data-ttu-id="adde3-107">Der einfache Typ **provideridtype** ist ein Token, das durch das folgende Muster eingeschränkt wird:</span><span class="sxs-lookup"><span data-stu-id="adde3-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="adde3-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adde3-108">Requirements</span></span>



| <span data-ttu-id="adde3-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adde3-109">Requirement</span></span> | <span data-ttu-id="adde3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="adde3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="adde3-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adde3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="adde3-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="adde3-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="adde3-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adde3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="adde3-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="adde3-114">None supported</span></span><br/>                         |



 

 




