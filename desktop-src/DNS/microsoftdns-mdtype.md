---
title: MicrosoftDNS_MDType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Agent für einen Domänen Eintrag (MD) darstellt.
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- DNS-MicrosoftDNS_MDType Klasse
- DNS-MicrosoftDNS_MDType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858876"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="fce8e-105">MicrosoftDNS- \_ mdtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="fce8e-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="fce8e-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Agent für einen Domänen Eintrag (MD) darstellt.</span><span class="sxs-lookup"><span data-stu-id="fce8e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="fce8e-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fce8e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce8e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce8e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="fce8e-109">Member</span><span class="sxs-lookup"><span data-stu-id="fce8e-109">Members</span></span>

<span data-ttu-id="fce8e-110">Die **MicrosoftDNS- \_ mdtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fce8e-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="fce8e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fce8e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fce8e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fce8e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fce8e-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="fce8e-113">Methods</span></span>

<span data-ttu-id="fce8e-114">Die **MicrosoftDNS- \_ mdtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fce8e-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="fce8e-115">Methode</span><span class="sxs-lookup"><span data-stu-id="fce8e-115">Method</span></span>                             | <span data-ttu-id="fce8e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fce8e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce8e-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="fce8e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fce8e-118">Instanziiert einen DNS MD-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name der Domäne, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und der Host des Mail-Agents.</span><span class="sxs-lookup"><span data-stu-id="fce8e-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="fce8e-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fce8e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fce8e-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="fce8e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fce8e-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="fce8e-121">**Modify**</span></span>                         | <span data-ttu-id="fce8e-122">Aktualisiert die TTL-und MD-Hosts auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fce8e-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fce8e-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="fce8e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fce8e-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fce8e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fce8e-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="fce8e-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="fce8e-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fce8e-126">Properties</span></span>

<span data-ttu-id="fce8e-127">Die **MicrosoftDNS- \_ mdtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fce8e-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fce8e-128">**Mdhost**</span><span class="sxs-lookup"><span data-stu-id="fce8e-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fce8e-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fce8e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fce8e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fce8e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fce8e-131">Der voll qualifizierte Domänen Name, der einen Host mit einem e-Mail-Agent angibt, der für die angegebene Domäne eine e-Mail liefern konnte</span><span class="sxs-lookup"><span data-stu-id="fce8e-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fce8e-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fce8e-132">Requirements</span></span>



| <span data-ttu-id="fce8e-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fce8e-133">Requirement</span></span> | <span data-ttu-id="fce8e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fce8e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce8e-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fce8e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fce8e-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fce8e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fce8e-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fce8e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fce8e-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fce8e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fce8e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="fce8e-139">Namespace</span></span><br/>                | <span data-ttu-id="fce8e-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="fce8e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fce8e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fce8e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fce8e-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fce8e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce8e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fce8e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce8e-144">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mdtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fce8e-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fce8e-145">**Modify-Methode der MicrosoftDNS- \_ mdtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fce8e-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="fce8e-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="fce8e-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





