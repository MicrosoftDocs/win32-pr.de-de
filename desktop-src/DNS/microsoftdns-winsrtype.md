---
title: MicrosoftDNS_WINSRType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen WINS-Reverse-Nachschlage Eintrag (WINSR) darstellt.
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- DNS-MicrosoftDNS_WINSRType Klasse
- DNS-MicrosoftDNS_WINSRType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392184"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="eec7b-105">MicrosoftDNS \_ winsrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="eec7b-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="eec7b-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen WINS-Reverse-Nachschlage Eintrag (WINSR) darstellt.</span><span class="sxs-lookup"><span data-stu-id="eec7b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="eec7b-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="eec7b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec7b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eec7b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="eec7b-109">Member</span><span class="sxs-lookup"><span data-stu-id="eec7b-109">Members</span></span>

<span data-ttu-id="eec7b-110">Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eec7b-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="eec7b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="eec7b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="eec7b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eec7b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eec7b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eec7b-113">Methods</span></span>

<span data-ttu-id="eec7b-114">Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eec7b-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="eec7b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="eec7b-115">Method</span></span>                             | <span data-ttu-id="eec7b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eec7b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec7b-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="eec7b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="eec7b-118">Instanziiert einen WINSR-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem WINS-ZuordnungsFlag, dem Reverse-Nachschlage Timeout, dem WINS-Cache Timeout und dem anzufügende Domänen Namen</span><span class="sxs-lookup"><span data-stu-id="eec7b-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="eec7b-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eec7b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="eec7b-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="eec7b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="eec7b-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="eec7b-121">**Modify**</span></span>                         | <span data-ttu-id="eec7b-122">Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die Ergebnis Domäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eec7b-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="eec7b-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="eec7b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="eec7b-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="eec7b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="eec7b-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="eec7b-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="eec7b-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eec7b-126">Properties</span></span>

<span data-ttu-id="eec7b-127">Die **MicrosoftDNS \_ winsrtype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eec7b-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eec7b-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="eec7b-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec7b-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eec7b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec7b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eec7b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eec7b-131">Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="eec7b-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="eec7b-132">**Lookuptimeout**</span><span class="sxs-lookup"><span data-stu-id="eec7b-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec7b-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eec7b-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec7b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eec7b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eec7b-135">Timeout (in Sekunden) für einen DNS-Server mit umgekehrter WINS-Suche.</span><span class="sxs-lookup"><span data-stu-id="eec7b-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="eec7b-136">**Mappingflag**</span><span class="sxs-lookup"><span data-stu-id="eec7b-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec7b-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eec7b-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec7b-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eec7b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eec7b-139">Das WINSR-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="eec7b-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="eec7b-140">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="eec7b-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="eec7b-141">**Resultdomain**</span><span class="sxs-lookup"><span data-stu-id="eec7b-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec7b-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eec7b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eec7b-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eec7b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eec7b-144">Domänen Name, der an zurückgegebene NetBIOS-Namen angehängt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eec7b-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eec7b-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eec7b-145">Requirements</span></span>



| <span data-ttu-id="eec7b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eec7b-146">Requirement</span></span> | <span data-ttu-id="eec7b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="eec7b-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec7b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eec7b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="eec7b-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eec7b-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eec7b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eec7b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="eec7b-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eec7b-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eec7b-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="eec7b-152">Namespace</span></span><br/>                | <span data-ttu-id="eec7b-153">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="eec7b-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eec7b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="eec7b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eec7b-155"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eec7b-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec7b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eec7b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec7b-157">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Klasse "winsrtype"**</span><span class="sxs-lookup"><span data-stu-id="eec7b-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="eec7b-158">**Modify-Methode der MicrosoftDNS \_ winsrtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eec7b-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="eec7b-159">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="eec7b-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





