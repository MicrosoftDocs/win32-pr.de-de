---
title: MicrosoftDNS_NSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Namen Server-Datensatz (NS) darstellt.
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- DNS-MicrosoftDNS_NSType Klasse
- DNS-MicrosoftDNS_NSType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957241"
---
# <a name="microsoftdns_nstype-class"></a><span data-ttu-id="ad4ef-105">MicrosoftDNS- \_ nstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad4ef-105">MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="ad4ef-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Namen Server-Datensatz (NS) darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Name Server (NS) record.</span></span>

<span data-ttu-id="ad4ef-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad4ef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad4ef-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a><span data-ttu-id="ad4ef-109">Member</span><span class="sxs-lookup"><span data-stu-id="ad4ef-109">Members</span></span>

<span data-ttu-id="ad4ef-110">Die **MicrosoftDNS- \_ nstype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ad4ef-110">The **MicrosoftDNS\_NSType** class has these types of members:</span></span>

-   [<span data-ttu-id="ad4ef-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ad4ef-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad4ef-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad4ef-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad4ef-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="ad4ef-113">Methods</span></span>

<span data-ttu-id="ad4ef-114">Die **MicrosoftDNS- \_ nstype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-114">The **MicrosoftDNS\_NSType** class has these methods.</span></span>



| <span data-ttu-id="ad4ef-115">Methode</span><span class="sxs-lookup"><span data-stu-id="ad4ef-115">Method</span></span>                             | <span data-ttu-id="ad4ef-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad4ef-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4ef-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ad4ef-118">Instanziiert einen DNS-NS-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem Host mit der Autorität für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-118">Instantiates a DNS NS Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the host with authority for the domain.</span></span> <span data-ttu-id="ad4ef-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ad4ef-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="ad4ef-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ad4ef-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-121">**Modify**</span></span>                         | <span data-ttu-id="ad4ef-122">Aktualisiert die TTL-und NS-Hosts auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-122">Updates the TTL and NS Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ad4ef-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ad4ef-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ad4ef-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="ad4ef-125">Qualifiers: Implemented</span></span><br/>                               |



 

### <a name="properties"></a><span data-ttu-id="ad4ef-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad4ef-126">Properties</span></span>

<span data-ttu-id="ad4ef-127">Die **MicrosoftDNS- \_ nstype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-127">The **MicrosoftDNS\_NSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad4ef-128">**NSHost**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-128">**NSHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad4ef-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad4ef-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad4ef-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad4ef-131">Autorisierender Host für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="ad4ef-131">Authoritative host for the domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad4ef-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad4ef-132">Requirements</span></span>



| <span data-ttu-id="ad4ef-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad4ef-133">Requirement</span></span> | <span data-ttu-id="ad4ef-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ad4ef-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4ef-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad4ef-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ad4ef-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad4ef-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ad4ef-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad4ef-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ad4ef-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad4ef-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ad4ef-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad4ef-139">Namespace</span></span><br/>                | <span data-ttu-id="ad4ef-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ad4ef-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ad4ef-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ad4ef-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad4ef-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ef-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4ef-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad4ef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4ef-144">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ nstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ad4ef-145">**Modify-Methode der MicrosoftDNS- \_ nstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-145">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="ad4ef-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="ad4ef-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





