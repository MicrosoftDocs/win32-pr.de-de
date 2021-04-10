---
description: Definiert einen Typ für das abonniert-Element des mobilen Breitband Profils.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: einfacher Typ des abonniert-Typs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041707"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="56b09-103">einfacher Typ des abonniert-Typs</span><span class="sxs-lookup"><span data-stu-id="56b09-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="56b09-104">Der einfache Typ " **abonniert Type** " definiert einen Typ für das " [**abonniert**](schema-subscriberid-mbnprofile-element.md) "-Element des mobilen Breitband Profils.</span><span class="sxs-lookup"><span data-stu-id="56b09-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="56b09-105">Dieser Typ ist eine Auflistung von einem oder mehreren Zeichen.</span><span class="sxs-lookup"><span data-stu-id="56b09-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="56b09-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56b09-106">Requirements</span></span>



| <span data-ttu-id="56b09-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56b09-107">Requirement</span></span> | <span data-ttu-id="56b09-108">Wert</span><span class="sxs-lookup"><span data-stu-id="56b09-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="56b09-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56b09-109">Minimum supported client</span></span><br/> | <span data-ttu-id="56b09-110">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="56b09-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="56b09-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56b09-111">Minimum supported server</span></span><br/> | <span data-ttu-id="56b09-112">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="56b09-112">None supported</span></span><br/>                         |



 

 




