---
description: Gibt die Liste der bevorzugten Netzwerkanbieter zum Zeitpunkt des Roamings an.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Dataroamingpartners (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353102"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="6b7de-103">Dataroamingpartners (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="6b7de-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="6b7de-104">Das **dataroamingpartners (mbnprofile)** -Element gibt die Liste der bevorzugten Netzwerkanbieter zum Zeitpunkt des Roamings an.</span><span class="sxs-lookup"><span data-stu-id="6b7de-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="6b7de-105">Der Mobile Breitbanddienst verwendet dieses Element, um beim Roaming das bevorzugte Netzwerk auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6b7de-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="6b7de-106">Das-Element hat das folgende untergeordnete Element, das mindestens einmal definiert werden muss, aber mehrmals definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b7de-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="6b7de-107">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="6b7de-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="6b7de-108">Dieses Element kann maximal ein Vorkommen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b7de-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="6b7de-109">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b7de-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6b7de-110">Das **dataroamingpartners** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="6b7de-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6b7de-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b7de-111">Child elements</span></span>



| <span data-ttu-id="6b7de-112">Element</span><span class="sxs-lookup"><span data-stu-id="6b7de-112">Element</span></span>                                                         | <span data-ttu-id="6b7de-113">type</span><span class="sxs-lookup"><span data-stu-id="6b7de-113">Type</span></span>                                                    | <span data-ttu-id="6b7de-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b7de-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="6b7de-115">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="6b7de-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="6b7de-116">**Provider Type**</span><span class="sxs-lookup"><span data-stu-id="6b7de-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="6b7de-117">Der Name und die Anbieter-ID eines Mobil Funk Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="6b7de-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6b7de-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b7de-118">Requirements</span></span>



| <span data-ttu-id="6b7de-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b7de-119">Requirement</span></span> | <span data-ttu-id="6b7de-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7de-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6b7de-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b7de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7de-122">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6b7de-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6b7de-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b7de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7de-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b7de-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6b7de-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b7de-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b7de-126">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="6b7de-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7de-127">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="6b7de-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="6b7de-128">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="6b7de-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7de-129">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="6b7de-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




