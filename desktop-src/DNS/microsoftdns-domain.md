---
title: MicrosoftDNS_Domain-Klasse
description: Die MicrosoftDNS- \_ Domänen Klasse stellt eine Domäne in einer DNS-Hierarchie dar.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS-MicrosoftDNS_Domain Klasse
- DNS-MicrosoftDNS_Domain Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103707"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="66260-105">MicrosoftDNS- \_ Domänen Klasse</span><span class="sxs-lookup"><span data-stu-id="66260-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="66260-106">Die **MicrosoftDNS- \_ Domänen** Klasse stellt eine Domäne in einer DNS-Hierarchie dar.</span><span class="sxs-lookup"><span data-stu-id="66260-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="66260-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="66260-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66260-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="66260-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="66260-109">Member</span><span class="sxs-lookup"><span data-stu-id="66260-109">Members</span></span>

<span data-ttu-id="66260-110">Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66260-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="66260-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="66260-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="66260-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66260-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="66260-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="66260-113">Methods</span></span>

<span data-ttu-id="66260-114">Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="66260-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="66260-115">Methode</span><span class="sxs-lookup"><span data-stu-id="66260-115">Method</span></span>                   | <span data-ttu-id="66260-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66260-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="66260-117">**Getchilshedname**</span><span class="sxs-lookup"><span data-stu-id="66260-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="66260-118">Ruft den Distinguished Name DS für die Zone ab.</span><span class="sxs-lookup"><span data-stu-id="66260-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="66260-119">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="66260-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="66260-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66260-120">Properties</span></span>

<span data-ttu-id="66260-121">Die **MicrosoftDNS- \_ Domänen** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66260-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66260-122">**Container Name**</span><span class="sxs-lookup"><span data-stu-id="66260-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66260-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66260-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66260-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66260-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66260-125">Der Name des Containers der Domäne, bei dem es sich um eine Zone, einen Cache oder einen roothin handelt.</span><span class="sxs-lookup"><span data-stu-id="66260-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="66260-126">In Fällen, in denen es sich bei dem Container um eine Zone (eine Instanz der [**MicrosoftDNS- \_ Zonen**](microsoftdns-zone.md) Klasse) handelt, enthält diese Eigenschaft den voll qualifizierten Namen der Zone.</span><span class="sxs-lookup"><span data-stu-id="66260-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="66260-127">Wenn der Container die Stammzone ist, sollte die Zeichenfolge \\ . \\ verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66260-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="66260-128">In Fällen, in denen es sich bei dem Container um den DNS-Cache von Ressourcen Einträgen handelt (eine Instanz der [**MicrosoftDNS- \_ Cache**](microsoftdns-cache.md) Klasse), wird diese Eigenschaft auf \\ die Zeichenfolge festgelegt. Cache \\ .</span><span class="sxs-lookup"><span data-stu-id="66260-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="66260-129">Wenn es sich bei dem Container um roothints handelt (eine Instanz der [**MicrosoftDNS-Klasse \_ roothints**](microsoftdns-roothints.md) ), sollte diese Eigenschaft auf festgelegt werden. \\ Roothints \\ .</span><span class="sxs-lookup"><span data-stu-id="66260-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="66260-130">**Dnsservername**</span><span class="sxs-lookup"><span data-stu-id="66260-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66260-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66260-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66260-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66260-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66260-133">Der voll qualifizierte Domänen Name oder die IP-Adresse des DNS-Servers, der die Domäne enthält.</span><span class="sxs-lookup"><span data-stu-id="66260-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="66260-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="66260-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66260-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66260-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66260-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66260-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66260-137">Der voll qualifizierte Domänen Name der Domäne.</span><span class="sxs-lookup"><span data-stu-id="66260-137">FQDN of the domain.</span></span>

<span data-ttu-id="66260-138">Für Instanzen von DNS-Cache oder roothints werden die Zeichen folgen \\ . Cache \\ und \\ .. Es sollten roothints \\ verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66260-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66260-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66260-139">Requirements</span></span>



| <span data-ttu-id="66260-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66260-140">Requirement</span></span> | <span data-ttu-id="66260-141">Wert</span><span class="sxs-lookup"><span data-stu-id="66260-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66260-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66260-142">Minimum supported client</span></span><br/> | <span data-ttu-id="66260-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66260-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="66260-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66260-144">Minimum supported server</span></span><br/> | <span data-ttu-id="66260-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66260-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66260-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="66260-146">Namespace</span></span><br/>                | <span data-ttu-id="66260-147">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="66260-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="66260-148">MOF</span><span class="sxs-lookup"><span data-stu-id="66260-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66260-149"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66260-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66260-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66260-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66260-151">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Domänen Klasse**</span><span class="sxs-lookup"><span data-stu-id="66260-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





