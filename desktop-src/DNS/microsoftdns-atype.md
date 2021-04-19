---
title: MicrosoftDNS_AType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Host Adresseintrag (a) darstellt.
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS-MicrosoftDNS_AType Klasse
- DNS-MicrosoftDNS_AType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342434"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="2c161-105">MicrosoftDNS- \_ aType-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c161-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="2c161-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Host Adresseintrag (a) darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c161-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="2c161-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2c161-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c161-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c161-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="2c161-109">Member</span><span class="sxs-lookup"><span data-stu-id="2c161-109">Members</span></span>

<span data-ttu-id="2c161-110">Die **MicrosoftDNS- \_ aType** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c161-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="2c161-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="2c161-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c161-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c161-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c161-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="2c161-113">Methods</span></span>

<span data-ttu-id="2c161-114">Die **MicrosoftDNS- \_ aType** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2c161-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="2c161-115">Methode</span><span class="sxs-lookup"><span data-stu-id="2c161-115">Method</span></span>                             | <span data-ttu-id="2c161-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c161-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c161-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="2c161-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="2c161-118">Instanziiert eine Host Adresse (a) RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name, die Klasse (Standard = in), der Gültigkeitsdauer Wert und die IP-Adresse des Hosts.</span><span class="sxs-lookup"><span data-stu-id="2c161-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="2c161-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c161-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="2c161-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="2c161-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="2c161-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="2c161-121">**Modify**</span></span>                         | <span data-ttu-id="2c161-122">Aktualisiert die Gültigkeitsdauer und die IP-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c161-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="2c161-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="2c161-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="2c161-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="2c161-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="2c161-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="2c161-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="2c161-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c161-126">Properties</span></span>

<span data-ttu-id="2c161-127">Die **MicrosoftDNS- \_ aType** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c161-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c161-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="2c161-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c161-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c161-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c161-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c161-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c161-131">Zeichenfolge, die die IPv4-Adresse des Hosts darstellt.</span><span class="sxs-lookup"><span data-stu-id="2c161-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c161-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c161-132">Requirements</span></span>



| <span data-ttu-id="2c161-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c161-133">Requirement</span></span> | <span data-ttu-id="2c161-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2c161-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c161-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c161-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2c161-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2c161-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2c161-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c161-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2c161-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c161-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c161-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c161-139">Namespace</span></span><br/>                | <span data-ttu-id="2c161-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="2c161-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2c161-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2c161-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c161-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c161-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c161-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c161-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c161-144">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="2c161-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="2c161-145">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aType"**</span><span class="sxs-lookup"><span data-stu-id="2c161-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2c161-146">**Modify-Methode der MicrosoftDNS- \_ atyp-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2c161-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





