---
title: MicrosoftDNS_Cache-Klasse
description: Die MicrosoftDNS- \_ Cache Klasse beschreibt einen Cache, der auf einem DNS-Server vorhanden ist.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS-MicrosoftDNS_Cache Klasse
- DNS-MicrosoftDNS_Cache Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040618"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="3758f-105">MicrosoftDNS- \_ Cache Klasse</span><span class="sxs-lookup"><span data-stu-id="3758f-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="3758f-106">Die **MicrosoftDNS- \_ Cache** Klasse beschreibt einen Cache, der auf einem DNS-Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3758f-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="3758f-107">Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen.</span><span class="sxs-lookup"><span data-stu-id="3758f-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="3758f-108">Die **MicrosoftDNS- \_ Cache** Klasse ist ein Container für die Ressourcen Datensätze, die vom DNS-Server zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3758f-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="3758f-109">Verwechseln Sie dies nicht mit einer Cache Datei, die Root-Hinweise enthält.</span><span class="sxs-lookup"><span data-stu-id="3758f-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="3758f-110">Jede Instanz der **MicrosoftDNS \_** -Klasse muss genau einem DNS-Server zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3758f-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="3758f-111">Sie ist möglicherweise mehreren Instanzen der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) oder der [**MicrosoftDNS- \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3758f-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="3758f-112">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="3758f-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3758f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3758f-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="3758f-114">Member</span><span class="sxs-lookup"><span data-stu-id="3758f-114">Members</span></span>

<span data-ttu-id="3758f-115">Die **MicrosoftDNS- \_ Cache** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3758f-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="3758f-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="3758f-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3758f-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="3758f-117">Methods</span></span>

<span data-ttu-id="3758f-118">Die **MicrosoftDNS- \_ Cache** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3758f-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="3758f-119">Methode</span><span class="sxs-lookup"><span data-stu-id="3758f-119">Method</span></span>                   | <span data-ttu-id="3758f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3758f-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3758f-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="3758f-121">**ClearCache**</span></span>           | <span data-ttu-id="3758f-122">Löscht den DNS-Server Cache von Ressourcen Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="3758f-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="3758f-123">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="3758f-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="3758f-124">**Getchilshedname**</span><span class="sxs-lookup"><span data-stu-id="3758f-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="3758f-125">Ruft den Distinguished Name für die Zone ab.</span><span class="sxs-lookup"><span data-stu-id="3758f-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="3758f-126">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="3758f-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="3758f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3758f-127">Requirements</span></span>



| <span data-ttu-id="3758f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3758f-128">Requirement</span></span> | <span data-ttu-id="3758f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3758f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3758f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3758f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3758f-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3758f-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3758f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3758f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3758f-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3758f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3758f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3758f-134">Namespace</span></span><br/>                | <span data-ttu-id="3758f-135">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="3758f-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3758f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3758f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3758f-137"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3758f-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3758f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3758f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3758f-139">**MicrosoftDNS- \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="3758f-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="3758f-140">**ClearCache-Methode der MicrosoftDNS- \_ Cache Klasse**</span><span class="sxs-lookup"><span data-stu-id="3758f-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="3758f-141">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Cache Klasse**</span><span class="sxs-lookup"><span data-stu-id="3758f-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





