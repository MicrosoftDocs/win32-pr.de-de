---
title: MicrosoftDNS_MFType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Weiterleitungs-Agent für einen Domänen Eintrag (MF) darstellt.
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- DNS-MicrosoftDNS_MFType Klasse
- DNS-MicrosoftDNS_MFType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104739"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="f0773-105">MicrosoftDNS- \_ mftype-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0773-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="f0773-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Weiterleitungs-Agent für einen Domänen Eintrag (MF) darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0773-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="f0773-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f0773-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0773-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0773-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="f0773-109">Member</span><span class="sxs-lookup"><span data-stu-id="f0773-109">Members</span></span>

<span data-ttu-id="f0773-110">Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f0773-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="f0773-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f0773-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f0773-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0773-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f0773-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f0773-113">Methods</span></span>

<span data-ttu-id="f0773-114">Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f0773-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="f0773-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f0773-115">Method</span></span>                             | <span data-ttu-id="f0773-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0773-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0773-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="f0773-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f0773-118">Diese Methode instanziiert den MF-Typ RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen der Domäne, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem Host des Mail-Agents.</span><span class="sxs-lookup"><span data-stu-id="f0773-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="f0773-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0773-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f0773-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="f0773-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="f0773-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="f0773-121">**Modify**</span></span>                         | <span data-ttu-id="f0773-122">Diese Methode aktualisiert den TTL-und den MF-Host auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0773-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f0773-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f0773-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f0773-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f0773-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f0773-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="f0773-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="f0773-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0773-126">Properties</span></span>

<span data-ttu-id="f0773-127">Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0773-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0773-128">**MF-Host**</span><span class="sxs-lookup"><span data-stu-id="f0773-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0773-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0773-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0773-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0773-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0773-131">FQDN, der einen Host mit einem e-Mail-Agent angibt, der e-Mail für die Weiterleitung an die angegebene Domäne akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f0773-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0773-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0773-132">Requirements</span></span>



| <span data-ttu-id="f0773-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0773-133">Requirement</span></span> | <span data-ttu-id="f0773-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f0773-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0773-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0773-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f0773-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0773-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f0773-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0773-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f0773-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0773-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f0773-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0773-139">Namespace</span></span><br/>                | <span data-ttu-id="f0773-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f0773-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f0773-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f0773-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0773-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0773-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0773-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0773-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0773-144">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "mftype"**</span><span class="sxs-lookup"><span data-stu-id="f0773-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0773-145">**Modify-Methode der MicrosoftDNS \_ mftype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0773-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="f0773-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f0773-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





