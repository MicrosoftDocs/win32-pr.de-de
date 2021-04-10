---
title: MicrosoftDNS_SOAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Start of Authority (SOA)-Datensatz darstellt.
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- DNS-MicrosoftDNS_SOAType Klasse
- DNS-MicrosoftDNS_SOAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040226"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="cad75-105">MicrosoftDNS- \_ soatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="cad75-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="cad75-106">Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Start of Authority (SOA)-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="cad75-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="cad75-107">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cad75-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad75-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad75-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="cad75-109">Member</span><span class="sxs-lookup"><span data-stu-id="cad75-109">Members</span></span>

<span data-ttu-id="cad75-110">Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cad75-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="cad75-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="cad75-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cad75-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cad75-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cad75-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="cad75-113">Methods</span></span>

<span data-ttu-id="cad75-114">Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cad75-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="cad75-115">Methode</span><span class="sxs-lookup"><span data-stu-id="cad75-115">Method</span></span>     | <span data-ttu-id="cad75-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cad75-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad75-117">**Modify**</span><span class="sxs-lookup"><span data-stu-id="cad75-117">**Modify**</span></span> | <span data-ttu-id="cad75-118">Aktualisiert die TTL, die SOA-Seriennummer, den primären Server, die verantwortliche Partei, das Aktualisierungs Intervall, die Wiederholungs Verzögerung, das Ablauf Limit und die minimale Gültigkeitsdauer (für die Zone) auf die Werte, die als Eingabeparameter dieser Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cad75-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="cad75-119">Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="cad75-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="cad75-120">Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="cad75-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="cad75-121">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="cad75-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cad75-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cad75-122">Properties</span></span>

<span data-ttu-id="cad75-123">Die **MicrosoftDNS- \_ soatype** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cad75-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cad75-124">**Expirelimit**</span><span class="sxs-lookup"><span data-stu-id="cad75-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cad75-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-127">Zeit in Sekunden, bevor eine nicht reagierende Zone nicht mehr autorisierend ist.</span><span class="sxs-lookup"><span data-stu-id="cad75-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-128">**Minimumttl**</span><span class="sxs-lookup"><span data-stu-id="cad75-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cad75-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-131">Niedrigerer Grenzwert für die Zeit (in Sekunden), die ein DNS-Server oder ein cacheresolver einen beliebigen Ressourcen Daten Satz aus der Zone Zwischenspeichern darf, zu der dieser Datensatz gehört.</span><span class="sxs-lookup"><span data-stu-id="cad75-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-132">**PrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="cad75-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cad75-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-135">Autorisierender DNS-Server für die Zone, zu der der Datensatz gehört.</span><span class="sxs-lookup"><span data-stu-id="cad75-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="cad75-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cad75-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-139">Zeit in Sekunden, bevor die Zone, in der dieser Datensatz enthalten ist, aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cad75-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-140">**Verantwortliche Partei**</span><span class="sxs-lookup"><span data-stu-id="cad75-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cad75-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-143">Der Name der verantwortlichen Partei für die Zone, zu der der Datensatz gehört.</span><span class="sxs-lookup"><span data-stu-id="cad75-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="cad75-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cad75-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-147">Zeit (in Sekunden) vor dem erneuten Versuch einer fehlgeschlagenen Aktualisierung der Zone, zu der dieser Datensatz gehört.</span><span class="sxs-lookup"><span data-stu-id="cad75-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cad75-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cad75-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cad75-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cad75-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cad75-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cad75-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cad75-151">Seriennummer des SOA-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="cad75-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cad75-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad75-152">Requirements</span></span>



| <span data-ttu-id="cad75-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cad75-153">Requirement</span></span> | <span data-ttu-id="cad75-154">Wert</span><span class="sxs-lookup"><span data-stu-id="cad75-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad75-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cad75-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cad75-156">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cad75-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cad75-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cad75-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cad75-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cad75-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cad75-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="cad75-159">Namespace</span></span><br/>                | <span data-ttu-id="cad75-160">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="cad75-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cad75-161">MOF</span><span class="sxs-lookup"><span data-stu-id="cad75-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cad75-162"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad75-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cad75-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad75-164">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="cad75-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="cad75-165">**Modify-Methode der MicrosoftDNS- \_ soatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cad75-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





