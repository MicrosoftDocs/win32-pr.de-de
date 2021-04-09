---
title: MicrosoftDNS_ResourceRecord-Klasse
description: Die MicrosoftDNS \_ resourcerecord-Klasse stellt die allgemeinen Eigenschaften eines DNS RR dar. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS-MicrosoftDNS_ResourceRecord Klasse
- DNS-MicrosoftDNS_ResourceRecord Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956622"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="4d2b0-105">MicrosoftDNS \_ resourcerecord-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d2b0-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="4d2b0-106">Die **MicrosoftDNS \_ resourcerecord** -Klasse stellt die allgemeinen Eigenschaften eines DNS RR dar.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="4d2b0-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d2b0-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="4d2b0-109">Member</span><span class="sxs-lookup"><span data-stu-id="4d2b0-109">Members</span></span>

<span data-ttu-id="4d2b0-110">Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d2b0-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="4d2b0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d2b0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d2b0-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d2b0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d2b0-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d2b0-113">Methods</span></span>

<span data-ttu-id="4d2b0-114">Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="4d2b0-115">Methode</span><span class="sxs-lookup"><span data-stu-id="4d2b0-115">Method</span></span>                                   | <span data-ttu-id="4d2b0-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d2b0-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2b0-117">**"Kreateingestancefromtextrepresentation"**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="4d2b0-118">Analysiert den RR in der textrepresentation-Zeichenfolge und mit dem eingegebenen DNS-Server und den Container Namen, definiert und instanziiert ein resourcerecord-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="4d2b0-119">Die-Methode gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="4d2b0-120">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="4d2b0-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="4d2b0-121">**Getobjectbytextrepresentation**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="4d2b0-122">Ruft eine vorhandene Instanz der MicrosoftDNS \_ resourcerecord-Unterklasse ab, die von der textrepresentation-Zeichenfolge zusammen mit dem DNS-Server und dem Container Namen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="4d2b0-123">Qualifizierer: keine</span><span class="sxs-lookup"><span data-stu-id="4d2b0-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="4d2b0-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d2b0-124">Properties</span></span>

<span data-ttu-id="4d2b0-125">Die **MicrosoftDNS \_ resourcerecord** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d2b0-126">**Container Name**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-129">Gibt den Namen des Containers für die Zone, den Cache oder die roothints-Instanz an, die das RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-130">**Dnsservername**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-133">Gibt den voll qualifizierten Namen oder die IP-Adresse des DNS-Servers an, der den RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-134">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-137">Stellt den voll qualifizierten Domänen Namen der Domäne dar, die den RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="4d2b0-138">Diese Eigenschaft kann die Zeichen folgen enthalten \\ . Cache \\ oder \\ .. Roothints \\ , wenn der interne Cache oder die roothints den RR-bzw. den RR enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-142">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-143">**Recordclass = 1**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-146">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="4d2b0-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="4d2b0-147">Diese Zeichenfolge stellt die Klasse des Ressourcen Datensatzes dar.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="4d2b0-148">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="4d2b0-148">Valid values include:</span></span>

<span data-ttu-id="4d2b0-149">1: in (Internet)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-149">1: IN (Internet)</span></span>

<span data-ttu-id="4d2b0-150">2: CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-150">2: CS (CSNET)</span></span>

<span data-ttu-id="4d2b0-151">3: ch (Chaos)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="4d2b0-152">4: HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-153">**Recorddata**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-156">Ressourcen Daten Satz Daten.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-157">**Textrepresentation**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-160">Text Darstellung des gesamten RR-Werts.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-161">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-164">Der Zeitpunkt, zu dem die RR zuletzt aktualisiert wurde, ausgedrückt in verstrichenen Stunden seit dem 1. Januar 1601, Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="4d2b0-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="4d2b0-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d2b0-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d2b0-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d2b0-168">Zeit (in Sekunden), die der RR von einem DNS- [*Konflikt Löser*](r-gly.md)zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d2b0-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d2b0-169">Requirements</span></span>



| <span data-ttu-id="4d2b0-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d2b0-170">Requirement</span></span> | <span data-ttu-id="4d2b0-171">Wert</span><span class="sxs-lookup"><span data-stu-id="4d2b0-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2b0-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-172">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2b0-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d2b0-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4d2b0-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-174">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2b0-175">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d2b0-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4d2b0-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d2b0-176">Namespace</span></span><br/>                | <span data-ttu-id="4d2b0-177">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="4d2b0-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4d2b0-178">MOF</span><span class="sxs-lookup"><span data-stu-id="4d2b0-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d2b0-179"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b0-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2b0-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d2b0-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2b0-181">**Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="4d2b0-182">**Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4d2b0-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





