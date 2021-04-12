---
title: MicrosoftDNS_PTRType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Zeiger (PTR)-Datensatz darstellt.
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS-MicrosoftDNS_PTRType Klasse
- DNS-MicrosoftDNS_PTRType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517951"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="51ffe-105">MicrosoftDNS \_ ptrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="51ffe-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="51ffe-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Zeiger (PTR)-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="51ffe-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="51ffe-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="51ffe-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ffe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51ffe-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="51ffe-109">Member</span><span class="sxs-lookup"><span data-stu-id="51ffe-109">Members</span></span>

<span data-ttu-id="51ffe-110">Die **MicrosoftDNS \_ ptrtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51ffe-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="51ffe-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="51ffe-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="51ffe-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51ffe-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51ffe-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="51ffe-113">Methods</span></span>

<span data-ttu-id="51ffe-114">Die **MicrosoftDNS \_ ptrtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="51ffe-115">Methode</span><span class="sxs-lookup"><span data-stu-id="51ffe-115">Method</span></span>                             | <span data-ttu-id="51ffe-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51ffe-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ffe-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="51ffe-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="51ffe-118">Instanziiert einen DNS-PTR-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem FQDN des PTR-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="51ffe-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="51ffe-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51ffe-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="51ffe-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="51ffe-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="51ffe-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="51ffe-121">**Modify**</span></span>                         | <span data-ttu-id="51ffe-122">Aktualisiert den TTL-und den PTR-Domänen Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ffe-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="51ffe-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="51ffe-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="51ffe-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="51ffe-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="51ffe-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="51ffe-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="51ffe-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51ffe-126">Properties</span></span>

<span data-ttu-id="51ffe-127">Die **MicrosoftDNS \_ ptrtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51ffe-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51ffe-128">**Ptrdomainname**</span><span class="sxs-lookup"><span data-stu-id="51ffe-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51ffe-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51ffe-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51ffe-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51ffe-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51ffe-131">Der voll qualifizierte Namen der PTR-Daten Satz Daten.</span><span class="sxs-lookup"><span data-stu-id="51ffe-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51ffe-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51ffe-132">Requirements</span></span>



| <span data-ttu-id="51ffe-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51ffe-133">Requirement</span></span> | <span data-ttu-id="51ffe-134">Wert</span><span class="sxs-lookup"><span data-stu-id="51ffe-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51ffe-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51ffe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51ffe-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="51ffe-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51ffe-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51ffe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51ffe-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51ffe-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51ffe-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="51ffe-139">Namespace</span></span><br/>                | <span data-ttu-id="51ffe-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="51ffe-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="51ffe-141">MOF</span><span class="sxs-lookup"><span data-stu-id="51ffe-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51ffe-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51ffe-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ffe-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51ffe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ffe-144">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ ptrtype"**</span><span class="sxs-lookup"><span data-stu-id="51ffe-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="51ffe-145">**Modify-Methode der MicrosoftDNS \_ ptrtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="51ffe-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="51ffe-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="51ffe-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





