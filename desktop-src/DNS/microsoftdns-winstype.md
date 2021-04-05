---
title: MicrosoftDNS_WINSType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen WINS-Datensatz (Windows Internet Name Service) darstellt.
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS-MicrosoftDNS_WINSType Klasse
- DNS-MicrosoftDNS_WINSType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859040"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="ea8a2-105">MicrosoftDNS- \_ winstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="ea8a2-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="ea8a2-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen WINS-Datensatz (Windows Internet Name Service) darstellt.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="ea8a2-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea8a2-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="ea8a2-109">Member</span><span class="sxs-lookup"><span data-stu-id="ea8a2-109">Members</span></span>

<span data-ttu-id="ea8a2-110">Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ea8a2-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="ea8a2-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ea8a2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea8a2-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea8a2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea8a2-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="ea8a2-113">Methods</span></span>

<span data-ttu-id="ea8a2-114">Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="ea8a2-115">Methode</span><span class="sxs-lookup"><span data-stu-id="ea8a2-115">Method</span></span>                             | <span data-ttu-id="ea8a2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea8a2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8a2-117">**"Kreateinzustancefrompropertydata"**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ea8a2-118">Instanziiert einen WINS-Typ von RR basierend auf den Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer und dem WINS-ZuordnungsFlag, dem Such Timeout, dem Cache Timeout und der Liste der IP-Adressen für die Suche.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="ea8a2-119">Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ea8a2-120">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="ea8a2-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ea8a2-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-121">**Modify**</span></span>                         | <span data-ttu-id="ea8a2-122">Aktualisiert die Gültigkeitsdauer, das ZuordnungsFlag, das Nachschlage Timeout, den Cache Timeout und die WINS-Server auf die Werte, die als Eingabeparameter dieser Methode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ea8a2-123">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ea8a2-124">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ea8a2-125">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="ea8a2-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="ea8a2-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea8a2-126">Properties</span></span>

<span data-ttu-id="ea8a2-127">Die **MicrosoftDNS- \_ winstype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea8a2-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8a2-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea8a2-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8a2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8a2-131">Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="ea8a2-132">**Lookuptimeout**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8a2-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea8a2-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8a2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8a2-135">Zeit (in Sekunden), die ein DNS-Server versucht, mithilfe von WINS eine Auflösung durchsuchen zu können.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="ea8a2-136">**Mappingflag**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8a2-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea8a2-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8a2-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8a2-139">WINS-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="ea8a2-140">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="ea8a2-141">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-141">The following values are valid.</span></span>



| <span data-ttu-id="ea8a2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8a2-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="ea8a2-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ea8a2-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="ea8a2-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8a2-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="ea8a2-145">Replikationsflag</span><span class="sxs-lookup"><span data-stu-id="ea8a2-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="ea8a2-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8a2-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="ea8a2-147">Flag "keine Replikation (lokaler Datensatz)"</span><span class="sxs-lookup"><span data-stu-id="ea8a2-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ea8a2-148">**Windows Server**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8a2-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8a2-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea8a2-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8a2-151">Liste mit durch Trennzeichen getrennten IP-Adressen von WINS-Servern, die in WINS-suchen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea8a2-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea8a2-152">Requirements</span></span>



| <span data-ttu-id="ea8a2-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea8a2-153">Requirement</span></span> | <span data-ttu-id="ea8a2-154">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8a2-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8a2-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea8a2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8a2-156">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea8a2-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea8a2-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea8a2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8a2-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea8a2-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea8a2-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea8a2-159">Namespace</span></span><br/>                | <span data-ttu-id="ea8a2-160">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ea8a2-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ea8a2-161">MOF</span><span class="sxs-lookup"><span data-stu-id="ea8a2-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea8a2-162"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea8a2-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8a2-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea8a2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8a2-164">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ winstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ea8a2-165">**Modify-Methode der MicrosoftDNS- \_ winstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="ea8a2-166">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="ea8a2-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





