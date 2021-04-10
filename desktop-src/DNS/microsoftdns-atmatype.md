---
title: MicrosoftDNS_ATMAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die den Atma-Datensatz (ATM Address to Name) darstellt.
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS-MicrosoftDNS_ATMAType Klasse
- DNS-MicrosoftDNS_ATMAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956474"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="133ea-105">MicrosoftDNS \_ atmatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="133ea-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="133ea-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die den Atma-Datensatz (ATM Address to Name) darstellt.</span><span class="sxs-lookup"><span data-stu-id="133ea-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="133ea-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="133ea-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="133ea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="133ea-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="133ea-109">Member</span><span class="sxs-lookup"><span data-stu-id="133ea-109">Members</span></span>

<span data-ttu-id="133ea-110">Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="133ea-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="133ea-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="133ea-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="133ea-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="133ea-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="133ea-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="133ea-113">Methods</span></span>

<span data-ttu-id="133ea-114">Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="133ea-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="133ea-115">Methode</span><span class="sxs-lookup"><span data-stu-id="133ea-115">Method</span></span>                             | <span data-ttu-id="133ea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="133ea-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="133ea-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="133ea-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="133ea-118">Instanziiert einen Atma-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer/Knoten Namen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer und dem ATM-Format und der Adresse.</span><span class="sxs-lookup"><span data-stu-id="133ea-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="133ea-119">Gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="133ea-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="133ea-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="133ea-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="133ea-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="133ea-121">**Modify**</span></span>                         | <span data-ttu-id="133ea-122">Aktualisiert die TTL, das Format und die Atma-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="133ea-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="133ea-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="133ea-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="133ea-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="133ea-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="133ea-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="133ea-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="133ea-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="133ea-126">Properties</span></span>

<span data-ttu-id="133ea-127">Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="133ea-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="133ea-128">**Atmaddress**</span><span class="sxs-lookup"><span data-stu-id="133ea-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ea-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="133ea-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="133ea-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ea-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ea-131">Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht.</span><span class="sxs-lookup"><span data-stu-id="133ea-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="133ea-132">Die ersten 4 Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="133ea-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="133ea-133">Das signifikanteste Byte wird in Byte 0 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="133ea-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="133ea-134">**Format**</span><span class="sxs-lookup"><span data-stu-id="133ea-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ea-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ea-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ea-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ea-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ea-137">ATM-Adressformat.</span><span class="sxs-lookup"><span data-stu-id="133ea-137">ATM address format.</span></span> <span data-ttu-id="133ea-138">Gültige Werte sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.</span><span class="sxs-lookup"><span data-stu-id="133ea-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="133ea-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="133ea-139">Requirements</span></span>



| <span data-ttu-id="133ea-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="133ea-140">Requirement</span></span> | <span data-ttu-id="133ea-141">Wert</span><span class="sxs-lookup"><span data-stu-id="133ea-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="133ea-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="133ea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="133ea-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="133ea-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="133ea-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="133ea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="133ea-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="133ea-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="133ea-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="133ea-146">Namespace</span></span><br/>                | <span data-ttu-id="133ea-147">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="133ea-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="133ea-148">MOF</span><span class="sxs-lookup"><span data-stu-id="133ea-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="133ea-149"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="133ea-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="133ea-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="133ea-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133ea-151">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="133ea-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="133ea-152">**Modify-Methode der MicrosoftDNS \_ atmatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="133ea-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="133ea-153">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="133ea-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





