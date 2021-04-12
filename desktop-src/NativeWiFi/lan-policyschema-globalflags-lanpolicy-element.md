---
description: Enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: globalflags-Element (lanpolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216927"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="53e7c-103">globalflags-Element (lanpolicy)</span><span class="sxs-lookup"><span data-stu-id="53e7c-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="53e7c-104">Das globalflags-Element (lanpolicy) enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="53e7c-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="53e7c-105">Das **globalflags** -Element wird durch das [**lanpolicy**](lan-policyschema-lanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="53e7c-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="53e7c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53e7c-106">Child elements</span></span>



| <span data-ttu-id="53e7c-107">Element</span><span class="sxs-lookup"><span data-stu-id="53e7c-107">Element</span></span>                                                                           | <span data-ttu-id="53e7c-108">type</span><span class="sxs-lookup"><span data-stu-id="53e7c-108">Type</span></span>    | <span data-ttu-id="53e7c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e7c-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53e7c-110">**enableautoconfig**</span><span class="sxs-lookup"><span data-stu-id="53e7c-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="53e7c-111">boolean</span><span class="sxs-lookup"><span data-stu-id="53e7c-111">boolean</span></span> | <span data-ttu-id="53e7c-112">Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="53e7c-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53e7c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53e7c-113">Requirements</span></span>



| <span data-ttu-id="53e7c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53e7c-114">Requirement</span></span> | <span data-ttu-id="53e7c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53e7c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53e7c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53e7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53e7c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53e7c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53e7c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53e7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53e7c-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53e7c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53e7c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e7c-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="53e7c-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="53e7c-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="53e7c-122">**Lanpolicy**</span><span class="sxs-lookup"><span data-stu-id="53e7c-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="53e7c-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="53e7c-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="53e7c-124">**Lanpolicy**</span><span class="sxs-lookup"><span data-stu-id="53e7c-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




