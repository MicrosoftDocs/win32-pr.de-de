---
description: Identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Provider-Element (dataroamingpartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129009"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="1e5a0-103">Provider-Element (dataroamingpartners)</span><span class="sxs-lookup"><span data-stu-id="1e5a0-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="1e5a0-104">Das **Provider-Element (dataroamingpartners)** identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.</span><span class="sxs-lookup"><span data-stu-id="1e5a0-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="1e5a0-105">Dieses Element verfügt über die folgenden untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1e5a0-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="1e5a0-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="1e5a0-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="1e5a0-108">Dieses Element kann im [**dataroamingpartners**](schema-dataroamingpartners-mbnprofile-element.md) -Element mehrmals definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e5a0-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="1e5a0-109">Sie muss mindestens einmal definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e5a0-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="1e5a0-110">Das **Provider** -Element wird durch das [**dataroamingpartners**](schema-dataroamingpartners-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="1e5a0-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5a0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e5a0-111">Requirements</span></span>



| <span data-ttu-id="1e5a0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e5a0-112">Requirement</span></span> | <span data-ttu-id="1e5a0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1e5a0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="1e5a0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e5a0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5a0-115">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e5a0-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="1e5a0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e5a0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5a0-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e5a0-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="1e5a0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e5a0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e5a0-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1e5a0-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="1e5a0-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1e5a0-122">**Dataroamingpartners (mbnprofile)**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




