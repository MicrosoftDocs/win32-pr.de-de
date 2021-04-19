---
title: MicrosoftDNS_AAAAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen IPv6-Adresseintrag (AAAA) darstellt. Der AAAA-Datensatz hat häufig den Wert \ 0034; Quad-a Record \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS-MicrosoftDNS_AAAAType Klasse
- DNS-MicrosoftDNS_AAAAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339969"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="47f5f-106">MicrosoftDNS \_ aaaatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="47f5f-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="47f5f-107">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen IPv6-Adresseintrag (AAAA) darstellt.</span><span class="sxs-lookup"><span data-stu-id="47f5f-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="47f5f-108">Der AAAA-Datensatz ist im Allgemeinen als "Quad-a-Datensatz" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="47f5f-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="47f5f-109">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="47f5f-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f5f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f5f-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="47f5f-111">Member</span><span class="sxs-lookup"><span data-stu-id="47f5f-111">Members</span></span>

<span data-ttu-id="47f5f-112">Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47f5f-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="47f5f-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="47f5f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="47f5f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47f5f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47f5f-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="47f5f-115">Methods</span></span>

<span data-ttu-id="47f5f-116">Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="47f5f-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="47f5f-117">Methode</span><span class="sxs-lookup"><span data-stu-id="47f5f-117">Method</span></span>                             | <span data-ttu-id="47f5f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47f5f-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f5f-119">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="47f5f-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="47f5f-120">Instanziiert einen "AAAA"-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer/Hostnamen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und der IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="47f5f-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="47f5f-121">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47f5f-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="47f5f-122">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="47f5f-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="47f5f-123">**Modify**</span><span class="sxs-lookup"><span data-stu-id="47f5f-123">**Modify**</span></span>                         | <span data-ttu-id="47f5f-124">Aktualisiert die TTL-und IPv6-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="47f5f-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="47f5f-125">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="47f5f-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="47f5f-126">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="47f5f-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="47f5f-127">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="47f5f-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="47f5f-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47f5f-128">Properties</span></span>

<span data-ttu-id="47f5f-129">Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47f5f-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47f5f-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="47f5f-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f5f-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="47f5f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f5f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47f5f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47f5f-133">IPv6-Adresse für den Host.</span><span class="sxs-lookup"><span data-stu-id="47f5f-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47f5f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47f5f-134">Requirements</span></span>



| <span data-ttu-id="47f5f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47f5f-135">Requirement</span></span> | <span data-ttu-id="47f5f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="47f5f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f5f-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47f5f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="47f5f-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="47f5f-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47f5f-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47f5f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="47f5f-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47f5f-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47f5f-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="47f5f-141">Namespace</span></span><br/>                | <span data-ttu-id="47f5f-142">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="47f5f-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="47f5f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="47f5f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f5f-144"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="47f5f-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f5f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47f5f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f5f-146">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aaaatype"**</span><span class="sxs-lookup"><span data-stu-id="47f5f-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="47f5f-147">**Modify-Methode der MicrosoftDNS \_ aaaatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="47f5f-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="47f5f-148">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="47f5f-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





