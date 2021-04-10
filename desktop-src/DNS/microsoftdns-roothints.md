---
title: MicrosoftDNS_RootHints-Klasse
description: Die MicrosoftDNS- \_ Klasse roothints beschreibt die in einer Cache Datei auf einem DNS-Server gespeicherten roothints. Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS-MicrosoftDNS_RootHints Klasse
- DNS-MicrosoftDNS_RootHints Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104157"
---
# <a name="microsoftdns_roothints-class"></a><span data-ttu-id="15ef0-106">MicrosoftDNS- \_ Klasse "roothints"</span><span class="sxs-lookup"><span data-stu-id="15ef0-106">MicrosoftDNS\_RootHints class</span></span>

<span data-ttu-id="15ef0-107">Die **MicrosoftDNS-Klasse \_ roothints** beschreibt die in einer Cache Datei auf einem DNS-Server gespeicherten roothints.</span><span class="sxs-lookup"><span data-stu-id="15ef0-107">The **MicrosoftDNS\_RootHints** class describes the RootHints stored in a Cache file on a DNS Server.</span></span> <span data-ttu-id="15ef0-108">Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen.</span><span class="sxs-lookup"><span data-stu-id="15ef0-108">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span>

<span data-ttu-id="15ef0-109">**MicrosoftDNS \_ Roothints** ist ein Container für die Ressourcen Datensätze, die vom DNS-Server in einer Cache Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="15ef0-109">**MicrosoftDNS\_RootHints** is a container for the resource records stored by the DNS Server in a Cache file.</span></span> <span data-ttu-id="15ef0-110">Jede Instanz der **MicrosoftDNS-Klasse \_ roothints** muss genau einem DNS-Server zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="15ef0-110">Every instance of the **MicrosoftDNS\_RootHints** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="15ef0-111">Sie ist möglicherweise mehreren Instanzen der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="15ef0-111">It may be associated with multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

<span data-ttu-id="15ef0-112">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="15ef0-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ef0-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="15ef0-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="15ef0-114">Member</span><span class="sxs-lookup"><span data-stu-id="15ef0-114">Members</span></span>

<span data-ttu-id="15ef0-115">Die **MicrosoftDNS-Klasse \_ roothints** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="15ef0-115">The **MicrosoftDNS\_RootHints** class has these types of members:</span></span>

-   [<span data-ttu-id="15ef0-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="15ef0-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15ef0-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="15ef0-117">Methods</span></span>

<span data-ttu-id="15ef0-118">Die **MicrosoftDNS-Klasse \_ roothints** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="15ef0-118">The **MicrosoftDNS\_RootHints** class has these methods.</span></span>



| <span data-ttu-id="15ef0-119">Methode</span><span class="sxs-lookup"><span data-stu-id="15ef0-119">Method</span></span>                        | <span data-ttu-id="15ef0-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15ef0-120">Description</span></span>                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ef0-121">**Getchilshedname**</span><span class="sxs-lookup"><span data-stu-id="15ef0-121">**GetDistinguishedName**</span></span>      | <span data-ttu-id="15ef0-122">Ruft den Distinguished Name für die Zone ab.</span><span class="sxs-lookup"><span data-stu-id="15ef0-122">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="15ef0-123">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="15ef0-123">Qualifiers: Implemented</span></span><br/>   |
| <span data-ttu-id="15ef0-124">**"Schreibbackroothintdatafile"**</span><span class="sxs-lookup"><span data-stu-id="15ef0-124">**WriteBackRootHintDatafile**</span></span> | <span data-ttu-id="15ef0-125">Schreibt die roothints zurück in die DNS-Cache Datei.</span><span class="sxs-lookup"><span data-stu-id="15ef0-125">Writes the RootHints back to the DNS Cache file.</span></span> <br/> <span data-ttu-id="15ef0-126">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="15ef0-126">Qualifiers: Implemented</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15ef0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15ef0-127">Requirements</span></span>



| <span data-ttu-id="15ef0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15ef0-128">Requirement</span></span> | <span data-ttu-id="15ef0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="15ef0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15ef0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15ef0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15ef0-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15ef0-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="15ef0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15ef0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15ef0-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15ef0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15ef0-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="15ef0-134">Namespace</span></span><br/>                | <span data-ttu-id="15ef0-135">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="15ef0-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="15ef0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="15ef0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15ef0-137"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="15ef0-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ef0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15ef0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ef0-139">**MicrosoftDNS- \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="15ef0-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="15ef0-140">**"Write-backroothintdatafile"-Methode der MicrosoftDNS- \_ Klasse "roothints"**</span><span class="sxs-lookup"><span data-stu-id="15ef0-140">**WriteBackRootHintDatafile Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[<span data-ttu-id="15ef0-141">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Klasse "roothints"**</span><span class="sxs-lookup"><span data-stu-id="15ef0-141">**GetDistinguishedName Method of the MicrosoftDNS\_RootHints Class**</span></span>](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





