---
title: MicrosoftDNS_ServerDomainContainment-Klasse
description: Jede Instanz der WMI-Klasse MicrosoftDNS \_ Server Association kann mehrere Instanzen der MicrosoftDNS- \_ Domänen Klasse enthalten.
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS-MicrosoftDNS_ServerDomainContainment Klasse
- DNS-MicrosoftDNS_ServerDomainContainment Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740265"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="063bd-105">MicrosoftDNS \_ serverdomaincontainment-Klasse</span><span class="sxs-lookup"><span data-stu-id="063bd-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="063bd-106">Jede Instanz der WMI-Klasse [**MicrosoftDNS \_ Server**](microsoftdns-server.md) Association kann mehrere Instanzen der [**MicrosoftDNS- \_ Domänen**](microsoftdns-domain.md) Klasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="063bd-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="063bd-107">Jede Instanz der **MicrosoftDNS- \_ Domänen** Klasse gehört zu einer einzelnen Instanz der **MicrosoftDNS- \_ Server** Klasse und ist so definiert, dass Sie für diesen Server schwach ist.</span><span class="sxs-lookup"><span data-stu-id="063bd-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="063bd-108">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="063bd-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="063bd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="063bd-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="063bd-110">Member</span><span class="sxs-lookup"><span data-stu-id="063bd-110">Members</span></span>

<span data-ttu-id="063bd-111">Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="063bd-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="063bd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="063bd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="063bd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="063bd-113">Properties</span></span>

<span data-ttu-id="063bd-114">Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="063bd-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="063bd-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="063bd-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063bd-116">Datentyp: **MicrosoftDNS- \_ Server**</span><span class="sxs-lookup"><span data-stu-id="063bd-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="063bd-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063bd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="063bd-118">Qualifizierer: Key, override ("GroupComponent"), min (1), Max (1)</span><span class="sxs-lookup"><span data-stu-id="063bd-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="063bd-119">Beschreibung: der DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="063bd-119">Description: The DNS Server.</span></span>

<span data-ttu-id="063bd-120">Geerbt von **CIM- \_ Komponente**.</span><span class="sxs-lookup"><span data-stu-id="063bd-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="063bd-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="063bd-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063bd-122">Datentyp: **MicrosoftDNS \_ Domain**</span><span class="sxs-lookup"><span data-stu-id="063bd-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="063bd-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063bd-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="063bd-124">Qualifizierer: Key, override ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="063bd-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="063bd-125">Beschreibung: Domäne, Zone, Cache oder roothints, die vom DNS-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="063bd-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="063bd-126">Geerbt von **CIM- \_ Komponente**.</span><span class="sxs-lookup"><span data-stu-id="063bd-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="063bd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="063bd-127">Remarks</span></span>

<span data-ttu-id="063bd-128">Die **MicrosoftDNS \_ serverdomaincontainment** -Klasse wird von der **CIM- \_ Komponenten** Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="063bd-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="063bd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="063bd-129">Requirements</span></span>



| <span data-ttu-id="063bd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="063bd-130">Requirement</span></span> | <span data-ttu-id="063bd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="063bd-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="063bd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="063bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="063bd-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="063bd-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="063bd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="063bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="063bd-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="063bd-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="063bd-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="063bd-136">Namespace</span></span><br/>                | <span data-ttu-id="063bd-137">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="063bd-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="063bd-138">MOF</span><span class="sxs-lookup"><span data-stu-id="063bd-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="063bd-139"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="063bd-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="063bd-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="063bd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063bd-141">**MicrosoftDNS \_ domaindomaincontainment**</span><span class="sxs-lookup"><span data-stu-id="063bd-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="063bd-142">**MicrosoftDNS \_ domainresourcerecordcontainment**</span><span class="sxs-lookup"><span data-stu-id="063bd-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="063bd-143">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="063bd-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





