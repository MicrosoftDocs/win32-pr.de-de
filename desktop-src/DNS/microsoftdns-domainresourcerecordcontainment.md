---
title: MicrosoftDNS_DomainResourceRecordContainment-Klasse
description: Die MicrosoftDNS- \_ domainresourcerecordcontainment-Klasse wird für die RR-Kapselung verwendet; jede Instanz der MicrosoftDNS- \_ Domäne kann mehrere Instanzen der MicrosoftDNS \_ resourcerecord-Klasse enthalten.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS-MicrosoftDNS_DomainResourceRecordContainment Klasse
- DNS-MicrosoftDNS_DomainResourceRecordContainment Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476755"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="59155-105">MicrosoftDNS- \_ domainresourcerecordcontainment-Klasse</span><span class="sxs-lookup"><span data-stu-id="59155-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="59155-106">Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse wird für die RR-Kapselung verwendet; jede Instanz der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) kann mehrere Instanzen der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="59155-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="59155-107">Jede Instanz der **MicrosoftDNS \_ resourcerecord** -Klasse gehört zu einer einzelnen Instanz der **MicrosoftDNS- \_ Domänen** Klasse und ist so definiert, dass Sie für diese Instanz schwach ist.</span><span class="sxs-lookup"><span data-stu-id="59155-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="59155-108">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="59155-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="59155-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="59155-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="59155-110">Member</span><span class="sxs-lookup"><span data-stu-id="59155-110">Members</span></span>

<span data-ttu-id="59155-111">Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="59155-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="59155-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59155-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59155-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59155-113">Properties</span></span>

<span data-ttu-id="59155-114">Die **MicrosoftDNS- \_ domainresourcerecordcontainment** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="59155-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59155-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="59155-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59155-116">Datentyp: **MicrosoftDNS \_ Domain**</span><span class="sxs-lookup"><span data-stu-id="59155-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="59155-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59155-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59155-118">Qualifizierer: Key, override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="59155-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="59155-119">Beschreibung: Zone, Cache, roothints oder Domäne, die direkt den Ressourcen Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="59155-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="59155-120">Von CIM- \_ Komponente geerbt</span><span class="sxs-lookup"><span data-stu-id="59155-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="59155-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="59155-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59155-122">Datentyp: **MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="59155-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="59155-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59155-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59155-124">Qualifizierer: Key, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="59155-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="59155-125">Beschreibung: der Ressourcen Daten Satz in Domäne, Zone, Cache oder roothints.</span><span class="sxs-lookup"><span data-stu-id="59155-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="59155-126">Geerbt von CIM- \_ Komponente.</span><span class="sxs-lookup"><span data-stu-id="59155-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59155-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59155-127">Requirements</span></span>



| <span data-ttu-id="59155-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59155-128">Requirement</span></span> | <span data-ttu-id="59155-129">Wert</span><span class="sxs-lookup"><span data-stu-id="59155-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59155-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59155-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59155-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59155-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="59155-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59155-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59155-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59155-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="59155-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="59155-134">Namespace</span></span><br/>                | <span data-ttu-id="59155-135">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="59155-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="59155-136">MOF</span><span class="sxs-lookup"><span data-stu-id="59155-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59155-137"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="59155-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59155-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59155-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59155-139">**MicrosoftDNS \_ serverdomaincontainment**</span><span class="sxs-lookup"><span data-stu-id="59155-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="59155-140">**MicrosoftDNS \_ domaindomaincontainment**</span><span class="sxs-lookup"><span data-stu-id="59155-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="59155-141">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="59155-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





