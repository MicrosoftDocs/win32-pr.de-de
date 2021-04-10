---
description: Gibt die Anbieter-ID des Mobil Funknetzwerks an.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (ProviderType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214697"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="a13b4-103">ProviderID (ProviderType)-Element</span><span class="sxs-lookup"><span data-stu-id="a13b4-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="a13b4-104">Das **ProviderType-Element (ProviderType)** gibt die Anbieter-ID des Mobil Funk Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a13b4-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="a13b4-105">Das-Element ist eine Sequenz von Ziffern mit maximal 6 Ziffern.</span><span class="sxs-lookup"><span data-stu-id="a13b4-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="a13b4-106">Dieses Element ist im [**Provider**](schema-provider-dataroamingpartners-element.md) -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a13b4-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="a13b4-107">Das **ProviderID** -Element wird durch den komplexen [**ProviderType**](schema-providertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a13b4-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13b4-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a13b4-108">Requirements</span></span>



| <span data-ttu-id="a13b4-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a13b4-109">Requirement</span></span> | <span data-ttu-id="a13b4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a13b4-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a13b4-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a13b4-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a13b4-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a13b4-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a13b4-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a13b4-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a13b4-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a13b4-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a13b4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a13b4-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="a13b4-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a13b4-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a13b4-117">**Provider Type**</span><span class="sxs-lookup"><span data-stu-id="a13b4-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="a13b4-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a13b4-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a13b4-119">**Anbieter (dataroamingpartners)**</span><span class="sxs-lookup"><span data-stu-id="a13b4-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




