---
title: MicrosoftDNS_X25Type-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen X. 25 (x25)-Datensatz darstellt.
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- DNS-MicrosoftDNS_X25Type Klasse
- DNS-MicrosoftDNS_X25Type Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341406"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="c98ba-105">MicrosoftDNS \_ X25Type-Klasse</span><span class="sxs-lookup"><span data-stu-id="c98ba-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="c98ba-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen X. 25 (x25)-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c98ba-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="c98ba-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c98ba-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98ba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c98ba-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="c98ba-109">Member</span><span class="sxs-lookup"><span data-stu-id="c98ba-109">Members</span></span>

<span data-ttu-id="c98ba-110">Die **MicrosoftDNS \_ X25Type** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c98ba-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="c98ba-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c98ba-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c98ba-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c98ba-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c98ba-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="c98ba-113">Methods</span></span>

<span data-ttu-id="c98ba-114">Die **MicrosoftDNS \_ X25Type** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c98ba-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="c98ba-115">Methode</span><span class="sxs-lookup"><span data-stu-id="c98ba-115">Method</span></span>                             | <span data-ttu-id="c98ba-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c98ba-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c98ba-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="c98ba-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c98ba-118">Instanziiert einen "x25"-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und der PSDN-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c98ba-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="c98ba-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c98ba-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c98ba-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="c98ba-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="c98ba-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="c98ba-121">**Modify**</span></span>                         | <span data-ttu-id="c98ba-122">Diese Methode aktualisiert die TTL-und PSDN-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c98ba-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c98ba-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c98ba-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c98ba-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="c98ba-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c98ba-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="c98ba-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c98ba-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c98ba-126">Properties</span></span>

<span data-ttu-id="c98ba-127">Die **MicrosoftDNS \_ X25Type** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c98ba-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c98ba-128">**Psdnaddress**</span><span class="sxs-lookup"><span data-stu-id="c98ba-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ba-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c98ba-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ba-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c98ba-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ba-131">PSDN-Adresse des Besitzers der RR.</span><span class="sxs-lookup"><span data-stu-id="c98ba-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c98ba-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c98ba-132">Requirements</span></span>



| <span data-ttu-id="c98ba-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c98ba-133">Requirement</span></span> | <span data-ttu-id="c98ba-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c98ba-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c98ba-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c98ba-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c98ba-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c98ba-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c98ba-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c98ba-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c98ba-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c98ba-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c98ba-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="c98ba-139">Namespace</span></span><br/>                | <span data-ttu-id="c98ba-140">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c98ba-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c98ba-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c98ba-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c98ba-142"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c98ba-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c98ba-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c98ba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98ba-144">**Die Methode "kreateinzustancefrompropertydata" der X25Type-Klasse von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="c98ba-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c98ba-145">**Modify-Methode der MicrosoftDNS \_ X25Type-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c98ba-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="c98ba-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c98ba-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





