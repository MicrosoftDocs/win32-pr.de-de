---
title: MicrosoftDNS_RTType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Route-through-Datensatz (RT) darstellt.
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- DNS-MicrosoftDNS_RTType Klasse
- DNS-MicrosoftDNS_RTType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956619"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="c4138-105">MicrosoftDNS \_ rttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="c4138-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="c4138-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Route-through-Datensatz (RT) darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4138-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="c4138-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c4138-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4138-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4138-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="c4138-109">Member</span><span class="sxs-lookup"><span data-stu-id="c4138-109">Members</span></span>

<span data-ttu-id="c4138-110">Die **MicrosoftDNS \_ rttype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c4138-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="c4138-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4138-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4138-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4138-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4138-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4138-113">Methods</span></span>

<span data-ttu-id="c4138-114">Die **MicrosoftDNS \_ rttype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c4138-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="c4138-115">Methode</span><span class="sxs-lookup"><span data-stu-id="c4138-115">Method</span></span>                             | <span data-ttu-id="c4138-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4138-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4138-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="c4138-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c4138-118">Instanziiert einen RT-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer/Hostnamen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer, der Daten Satz Voreinstellung und dem zwischenhostnamen.</span><span class="sxs-lookup"><span data-stu-id="c4138-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="c4138-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4138-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c4138-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="c4138-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c4138-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="c4138-121">**Modify**</span></span>                         | <span data-ttu-id="c4138-122">Aktualisiert die Gültigkeitsdauer, die Präferenz und den zwischen Host auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4138-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c4138-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c4138-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c4138-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c4138-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c4138-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="c4138-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="c4138-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4138-126">Properties</span></span>

<span data-ttu-id="c4138-127">Die **MicrosoftDNS \_ rttype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4138-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4138-128">**Intermediatehost**</span><span class="sxs-lookup"><span data-stu-id="c4138-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4138-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c4138-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4138-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4138-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4138-131">FQDN, der einen Host angibt, der als zwischengeschalteter Host zum Erreichen des vom Besitzer angegebenen Hosts dienen soll.</span><span class="sxs-lookup"><span data-stu-id="c4138-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="c4138-132">**Bevorzu**</span><span class="sxs-lookup"><span data-stu-id="c4138-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4138-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4138-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4138-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c4138-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4138-135">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c4138-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="c4138-136">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="c4138-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4138-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4138-137">Requirements</span></span>



| <span data-ttu-id="c4138-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4138-138">Requirement</span></span> | <span data-ttu-id="c4138-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c4138-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4138-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4138-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c4138-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c4138-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c4138-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4138-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c4138-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4138-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4138-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4138-144">Namespace</span></span><br/>                | <span data-ttu-id="c4138-145">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c4138-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c4138-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c4138-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4138-147"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4138-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4138-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4138-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4138-149">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ rttype"**</span><span class="sxs-lookup"><span data-stu-id="c4138-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c4138-150">**Modify-Methode der MicrosoftDNS \_ rttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c4138-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="c4138-151">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c4138-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





