---
title: MicrosoftDNS_DomainDomainContainment-Klasse
description: Die MicrosoftDNS- \_ domaindomaincontainment-Klasse wird für die Domänen Kapselung verwendet. DNS-Domänen können andere DNS-Domänen enthalten.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS-MicrosoftDNS_DomainDomainContainment Klasse
- DNS-MicrosoftDNS_DomainDomainContainment Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040853"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="a8dcb-105">MicrosoftDNS- \_ domaindomaincontainment-Klasse</span><span class="sxs-lookup"><span data-stu-id="a8dcb-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="a8dcb-106">Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse wird für die Domänen Kapselung verwendet. DNS-Domänen können andere DNS-Domänen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="a8dcb-107">Jede Instanz der [**MicrosoftDNS- \_ Domänen**](microsoftdns-domain.md) Klasse kann mehrere andere Instanzen der **MicrosoftDNS- \_ Domäne** enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="a8dcb-108">Eine Instanz eines **MicrosoftDNS- \_ Domänen** Objekts ist direkt in höchstens einer **MicrosoftDNS- \_ Domäne** der höheren Ebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="a8dcb-109">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8dcb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8dcb-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a8dcb-111">Member</span><span class="sxs-lookup"><span data-stu-id="a8dcb-111">Members</span></span>

<span data-ttu-id="a8dcb-112">Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a8dcb-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="a8dcb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8dcb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8dcb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8dcb-114">Properties</span></span>

<span data-ttu-id="a8dcb-115">Die **MicrosoftDNS- \_ domaindomaincontainment** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8dcb-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8dcb-117">Datentyp: **MicrosoftDNS \_ Domain**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="a8dcb-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8dcb-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8dcb-119">Qualifizierer: Key, Max (1), override ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="a8dcb-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="a8dcb-120">Beschreibung: eine Domäne, eine Zone, ein Cache oder eine roothints auf höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="a8dcb-121">Von CIM- \_ Komponente geerbt</span><span class="sxs-lookup"><span data-stu-id="a8dcb-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="a8dcb-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8dcb-123">Datentyp: **MicrosoftDNS \_ Domain**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="a8dcb-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a8dcb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8dcb-125">Qualifizierer: Key, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a8dcb-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="a8dcb-126">Beschreibung: die Domäne, die sich in einer Domäne, Zone, einem Cache oder in einer höheren Ebene befindet.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="a8dcb-127">Geerbt von CIM- \_ Komponente.</span><span class="sxs-lookup"><span data-stu-id="a8dcb-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8dcb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8dcb-128">Requirements</span></span>



| <span data-ttu-id="a8dcb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8dcb-129">Requirement</span></span> | <span data-ttu-id="a8dcb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a8dcb-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dcb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8dcb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dcb-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8dcb-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a8dcb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8dcb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dcb-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8dcb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8dcb-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8dcb-135">Namespace</span></span><br/>                | <span data-ttu-id="a8dcb-136">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="a8dcb-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a8dcb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a8dcb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8dcb-138"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8dcb-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8dcb-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8dcb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8dcb-140">**MicrosoftDNS \_ domainresourcerecordcontainment**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="a8dcb-141">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="a8dcb-142">**MicrosoftDNS \_ serverdomaincontainment**</span><span class="sxs-lookup"><span data-stu-id="a8dcb-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





