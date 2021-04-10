---
title: MicrosoftDNS_Zone-Klasse
description: Die MicrosoftDNS- \_ Zonen Klasse beschreibt eine DNS-Zone. Jede Instanz der MicrosoftDNS- \_ Zonen Klasse muss genau einem DNS-Server zugewiesen werden. Zonen können mehreren Instanzen der MicrosoftDNS- \_ Domäne oder der MicrosoftDNS- \_ resourcerecord-Klassen zugeordnet werden.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS-MicrosoftDNS_Zone Klasse
- DNS-MicrosoftDNS_Zone Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041106"
---
# <a name="microsoftdns_zone-class"></a><span data-ttu-id="41431-107">MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="41431-107">MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="41431-108">Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="41431-108">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="41431-109">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="41431-109">When the term is removed from the software, we’ll remove it from this article.</span></span>

> [!NOTE]
> <span data-ttu-id="41431-110">Dieser Artikel enthält Verweise auf den Begriff Master Server, einen Begriff, den Microsoft nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="41431-110">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="41431-111">Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.</span><span class="sxs-lookup"><span data-stu-id="41431-111">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="41431-112">Die **MicrosoftDNS- \_ Zonen** Klasse beschreibt eine DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="41431-112">The **MicrosoftDNS\_Zone** class describes a DNS Zone.</span></span> <span data-ttu-id="41431-113">Jede Instanz der **MicrosoftDNS- \_ Zonen** Klasse muss genau einem DNS-Server zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="41431-113">Every instance of the **MicrosoftDNS\_Zone** class must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="41431-114">Zonen können mehreren Instanzen der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) oder der [**MicrosoftDNS- \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klassen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="41431-114">Zones may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="41431-115">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="41431-115">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41431-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="41431-116">Syntax</span></span>

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a><span data-ttu-id="41431-117">Member</span><span class="sxs-lookup"><span data-stu-id="41431-117">Members</span></span>

<span data-ttu-id="41431-118">Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41431-118">The **MicrosoftDNS\_Zone** class has these types of members:</span></span>

-   [<span data-ttu-id="41431-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="41431-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="41431-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41431-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41431-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="41431-121">Methods</span></span>

<span data-ttu-id="41431-122">Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="41431-122">The **MicrosoftDNS\_Zone** class has these methods.</span></span>



| <span data-ttu-id="41431-123">Methode</span><span class="sxs-lookup"><span data-stu-id="41431-123">Method</span></span>                   | <span data-ttu-id="41431-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41431-124">Description</span></span>                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41431-125">**AgeAllRecords**</span><span class="sxs-lookup"><span data-stu-id="41431-125">**AgeAllRecords**</span></span>        | <span data-ttu-id="41431-126">Ermöglicht die Alterung für einige oder alle nicht-NS-und nicht-SOA-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="41431-126">Enables aging for some or all non-NS and non-SOA records.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="41431-127">**Changezonetype**</span><span class="sxs-lookup"><span data-stu-id="41431-127">**ChangeZoneType**</span></span>       | <span data-ttu-id="41431-128">Ändert Zonen Typen.</span><span class="sxs-lookup"><span data-stu-id="41431-128">Changes zone types.</span></span> <br/> <span data-ttu-id="41431-129">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-129">Qualifiers: Implemented</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="41431-130">**"Kreatezone"**</span><span class="sxs-lookup"><span data-stu-id="41431-130">**CreateZone**</span></span>           | <span data-ttu-id="41431-131">Erstellt eine neue Zone.</span><span class="sxs-lookup"><span data-stu-id="41431-131">Creates a new zone.</span></span> <br/> <span data-ttu-id="41431-132">Qualifizierer: keine.</span><span class="sxs-lookup"><span data-stu-id="41431-132">Qualifiers: None.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="41431-133">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="41431-133">**ForceRefresh**</span></span>         | <span data-ttu-id="41431-134">Erzwingt ein Update der sekundären Datenbank vom DNS-Master Server.</span><span class="sxs-lookup"><span data-stu-id="41431-134">Forces an update of the secondary from the Master DNS Server.</span></span> <br/> <span data-ttu-id="41431-135">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-135">Qualifiers: Implemented</span></span><br/>                                                                                               |
| <span data-ttu-id="41431-136">**Getchilshedname**</span><span class="sxs-lookup"><span data-stu-id="41431-136">**GetDistinguishedName**</span></span> | <span data-ttu-id="41431-137">Ruft den Distinguished Name DS für die Zone ab.</span><span class="sxs-lookup"><span data-stu-id="41431-137">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="41431-138">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-138">Qualifiers: Implemented</span></span><br/>                                                                                                                 |
| <span data-ttu-id="41431-139">**Pausegzone**</span><span class="sxs-lookup"><span data-stu-id="41431-139">**PauseZone**</span></span>            | <span data-ttu-id="41431-140">Hält die Zone an.</span><span class="sxs-lookup"><span data-stu-id="41431-140">Pauses the Zone.</span></span> <br/> <span data-ttu-id="41431-141">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-141">Qualifiers: Implemented</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="41431-142">**Reloadzone**</span><span class="sxs-lookup"><span data-stu-id="41431-142">**ReloadZone**</span></span>           | <span data-ttu-id="41431-143">Lädt die Zone erneut.</span><span class="sxs-lookup"><span data-stu-id="41431-143">Reloads the Zone.</span></span> <br/> <span data-ttu-id="41431-144">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-144">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="41431-145">**Resetsecon-Replikate**</span><span class="sxs-lookup"><span data-stu-id="41431-145">**ResetSecondaries**</span></span>     | <span data-ttu-id="41431-146">Setzt das Array der sekundären IP-Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="41431-146">Resets the secondary ip address array.</span></span> <br/> <span data-ttu-id="41431-147">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-147">Qualifiers: Implemented</span></span><br/>                                                                                                                      |
| <span data-ttu-id="41431-148">**Resumezone**</span><span class="sxs-lookup"><span data-stu-id="41431-148">**ResumeZone**</span></span>           | <span data-ttu-id="41431-149">Nimmt die Zone wieder auf.</span><span class="sxs-lookup"><span data-stu-id="41431-149">Resumes the Zone.</span></span> <br/> <span data-ttu-id="41431-150">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-150">Qualifiers: Implemented</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="41431-151">**Updatefromds**</span><span class="sxs-lookup"><span data-stu-id="41431-151">**UpdateFromDS**</span></span>         | <span data-ttu-id="41431-152">Erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS).</span><span class="sxs-lookup"><span data-stu-id="41431-152">Forces an update of the Zone from the Directory Service (DS).</span></span> <span data-ttu-id="41431-153">Damit diese Methode gültig ist, muss zonetype gleich 0 sein. die Zone muss tatsächlich in DS gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="41431-153">For this method to be valid, the ZoneType must be 0 the Zone must indeed be stored in the DS.</span></span> <br/> <span data-ttu-id="41431-154">Qualifizierer: Implementiert</span><span class="sxs-lookup"><span data-stu-id="41431-154">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="41431-155">**"Write Backzone"**</span><span class="sxs-lookup"><span data-stu-id="41431-155">**WriteBackZone**</span></span>        | <span data-ttu-id="41431-156">Speichert Zonendaten in der zugehörigen Zonendatei.</span><span class="sxs-lookup"><span data-stu-id="41431-156">Saves Zone data to its zone file.</span></span> <br/> <span data-ttu-id="41431-157">Qualifizierer: implementiert, statisch</span><span class="sxs-lookup"><span data-stu-id="41431-157">Qualifiers: Implemented, static</span></span><br/>                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="41431-158">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41431-158">Properties</span></span>

<span data-ttu-id="41431-159">Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41431-159">The **MicrosoftDNS\_Zone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41431-160">**Zunehmendem**</span><span class="sxs-lookup"><span data-stu-id="41431-160">**Aging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-161">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-163">Gibt das Verhalten für die Alterung und das Verhalten der Zone an.</span><span class="sxs-lookup"><span data-stu-id="41431-163">Specifies the aging and scavenging behavior of the zone.</span></span> <span data-ttu-id="41431-164">NULL gibt an, dass das Bereinigung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="41431-164">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="41431-165">Wenn das Bereinigung deaktiviert ist, werden die Zeitstempel der Datensätze in der Zone nicht aktualisiert, und die Datensätze unterliegen nicht dem scräging.</span><span class="sxs-lookup"><span data-stu-id="41431-165">When scavenging is disabled, the timestamps of records in the zone are not refreshed, and the records are not subjected to scavenging.</span></span> <span data-ttu-id="41431-166">Wenn diese Einstellung auf 1 festgelegt ist, werden die Datensätze gelöscht, und ihre Zeitstempel werden aktualisiert, wenn der Server die Anforderung für das dynamische Update für die Datensätze empfängt.</span><span class="sxs-lookup"><span data-stu-id="41431-166">When set to one, records are subjected to scavenging and their timestamps are refreshed when the server receives the dynamic update request for the records.</span></span> <span data-ttu-id="41431-167">Für Active Directory integrierte Zonen wird dieser Wert auf die *DefaultAgingState* -Eigenschaft des DNS-Servers festgelegt, auf dem die Zone erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41431-167">For Active Directory-integrated zones, this value is set to the *DefaultAgingState* property of the DNS Server where the zone is created.</span></span> <span data-ttu-id="41431-168">Für Standard primäre Zonen ist der Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="41431-168">For standard primary zones, the default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="41431-169">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="41431-169">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-172">Gibt an, ob die Zone dynamische Update Anforderungen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="41431-172">Indicates whether the Zone accepts dynamic update requests.</span></span>

</dd> <dt>

<span data-ttu-id="41431-173">**Automatisch**</span><span class="sxs-lookup"><span data-stu-id="41431-173">**AutoCreated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-176">Gibt an, ob die Zone automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41431-176">Indicates whether the Zone is autocreated.</span></span>

</dd> <dt>

<span data-ttu-id="41431-177">**Availforscavengetime**</span><span class="sxs-lookup"><span data-stu-id="41431-177">**AvailForScavengeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-178">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-180">Gibt die Zeit an, zu der der Server versuchen kann, die Zone zu löschen.</span><span class="sxs-lookup"><span data-stu-id="41431-180">Specifies the time when the server may attempt scavenging the zone.</span></span> <span data-ttu-id="41431-181">Auch wenn die Zone so konfiguriert ist, dass die Weiterbildung aktiviert ist, versucht der DNS-Server erst nach diesem Moment, diese Zone zu löschen.</span><span class="sxs-lookup"><span data-stu-id="41431-181">Even if the zone is configured to enable scavenging the DNS server will not attempt scavenging this zone until after this moment.</span></span> <span data-ttu-id="41431-182">Dieser Wert wird auf die aktuelle Uhrzeit zuzüglich des Aktualisierungs Intervalls der Zone festgelegt, wenn die Zone geladen wird.</span><span class="sxs-lookup"><span data-stu-id="41431-182">This value is set to the current time plus the Refresh Interval of the zone whenever the zone is loaded.</span></span> <span data-ttu-id="41431-183">Dieser Parameter wird lokal gespeichert und nicht in andere Kopien der Zone repliziert.</span><span class="sxs-lookup"><span data-stu-id="41431-183">This parameter is stored locally, and is not replicated to other copies of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="41431-184">**Datendatei**</span><span class="sxs-lookup"><span data-stu-id="41431-184">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41431-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41431-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-187">Gibt den Namen der Zonendatei an.</span><span class="sxs-lookup"><span data-stu-id="41431-187">Indicates the name of the zone file.</span></span>

</dd> <dt>

<span data-ttu-id="41431-188">**Disablewinsrecordreplizierung**</span><span class="sxs-lookup"><span data-stu-id="41431-188">**DisableWINSRecordReplication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-189">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-191">Gibt an, ob der WINS-Datensatz repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="41431-191">Indicates whether the WINS record is replicated.</span></span> <span data-ttu-id="41431-192">Wenn true festgelegt ist, ist die WINS-Daten Satz Replikation deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="41431-192">If set to TRUE, WINS record replication is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="41431-193">**Dsintegriert**</span><span class="sxs-lookup"><span data-stu-id="41431-193">**DsIntegrated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-194">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-196">Gibt an, ob die Zone DS-integriert ist.</span><span class="sxs-lookup"><span data-stu-id="41431-196">Specifies whether the zone is DS integrated.</span></span>

</dd> <dt>

<span data-ttu-id="41431-197">**Forwarderslave**</span><span class="sxs-lookup"><span data-stu-id="41431-197">**ForwarderSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-198">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-200">Gibt an, ob das DNS Rekursion verwendet, wenn die Namen für die angegebene vorwärts Zone aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="41431-200">Indicates whether the DNS uses recursion when resolving the names for the specified forward zone.</span></span> <span data-ttu-id="41431-201">Gilt nur für bedingte Weiterleitungs Zonen.</span><span class="sxs-lookup"><span data-stu-id="41431-201">Applicable to Conditional Forwarding zones only.</span></span>

</dd> <dt>

<span data-ttu-id="41431-202">**Weiterforwardertimeout**</span><span class="sxs-lookup"><span data-stu-id="41431-202">**ForwarderTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-205">Gibt die Zeit in Sekunden an, die ein DNS-Server, der eine Abfrage für den Namen in der Forward-Zone weiterleitet, auf eine Auflösung von der Weiterleitung wartet, bevor versucht wird, die Abfrage selbst aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="41431-205">Indicates the time, in seconds, a DNS server forwarding a query for the name under the forward zone waits for resolution from the forwarder before attempting to resolve the query itself.</span></span> <span data-ttu-id="41431-206">Dieser Parameter gilt nur für die vorwärts Zonen.</span><span class="sxs-lookup"><span data-stu-id="41431-206">This parameter is applicable to the Forward zones only.</span></span>

</dd> <dt>

<span data-ttu-id="41431-207">**Lasterfolgreichen fulsoacheck**</span><span class="sxs-lookup"><span data-stu-id="41431-207">**LastSuccessfulSoaCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-210">Die Anzahl der Sekunden seit dem 1. Januar 1970 GMT, seit die SOA-Seriennummer für die Zone zuletzt aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="41431-210">Number of seconds since the beginning of January 1, 1970 GMT, since the SOA serial number for the zone was last checked.</span></span>

</dd> <dt>

<span data-ttu-id="41431-211">**Lasterfolgreiches XFR**</span><span class="sxs-lookup"><span data-stu-id="41431-211">**LastSuccessfulXfr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-212">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-214">Die Anzahl der Sekunden seit dem 1. Januar 1970 GMT, seit die Zone zuletzt von einem Master Server übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="41431-214">Number of seconds since the beginning of January 1, 1970 GMT, since the zone was last transferred from a master server.</span></span>

</dd> <dt>

<span data-ttu-id="41431-215">**Localmasterservers**</span><span class="sxs-lookup"><span data-stu-id="41431-215">**LocalMasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-216">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41431-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41431-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-218">Lokale IP-Adressen der Master-DNS-Server für diese Zone.</span><span class="sxs-lookup"><span data-stu-id="41431-218">Local IP addresses of the master DNS servers for this zone.</span></span> <span data-ttu-id="41431-219">Wenn festgelegt, werden diese Master Server in Active Directory überlaufen.</span><span class="sxs-lookup"><span data-stu-id="41431-219">If set, these masters over-ride the MasterServers found in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="41431-220">**Master Server**</span><span class="sxs-lookup"><span data-stu-id="41431-220">**MasterServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-221">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41431-221">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41431-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-223">IP-Adressen der Master-DNS-Server für diese Zone.</span><span class="sxs-lookup"><span data-stu-id="41431-223">IP addresses of the master DNS servers for this zone.</span></span>

</dd> <dt>

<span data-ttu-id="41431-224">**NoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="41431-224">**NoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-227">Gibt das Zeitintervall zwischen der letzten Aktualisierung des Zeitstempels eines Datensatzes und dem frühesten Zeitpunkt an, zu dem der Zeitstempel aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="41431-227">Specifies the time interval between the last update of a record's timestamp and the earliest moment when the timestamp can be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="41431-228">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="41431-228">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-229">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-231">Gibt an, ob die Master Zone die sekundären Replikate über Änderungen in der RRS-Datenbank benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="41431-231">Indicates whether the master Zone notifies secondaries of any changes in its RRs database.</span></span> <span data-ttu-id="41431-232">Legen Sie auf 1 fest, um sekundäre Datenbanken zu Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="41431-232">Set to 1 to notify secondaries.</span></span>

</dd> <dt>

<span data-ttu-id="41431-233">**Notifyservers**</span><span class="sxs-lookup"><span data-stu-id="41431-233">**NotifyServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-234">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41431-234">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41431-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-236">Array von Zeichen folgen, das IP-Adressen von DNS-Servern auflistet, die über Änderungen in dieser Zone benachrichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41431-236">Array of strings enumerating IP addresses of DNS servers to be notified of changes in this zone.</span></span>

</dd> <dt>

<span data-ttu-id="41431-237">**Angehalten**</span><span class="sxs-lookup"><span data-stu-id="41431-237">**Paused**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-238">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-238">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-240">Gibt an, ob die Zone angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="41431-240">Indicates whether the Zone is paused.</span></span>

</dd> <dt>

<span data-ttu-id="41431-241">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="41431-241">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-242">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-244">Gibt das Aktualisierungs Intervall an, in dem die Datensätze mit einem Zeitstempel ungleich NULL aktualisiert werden, damit Sie in der Zone verbleiben.</span><span class="sxs-lookup"><span data-stu-id="41431-244">Specifies the refresh interval, during which the records with nonzero timestamp are expected to be refreshed to remain in the zone.</span></span> <span data-ttu-id="41431-245">Datensätze, die nach Ablauf des Aktualisierungs Intervalls nicht aktualisiert wurden, können durch das nächste von einem Server ausgeführte Bereinigung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="41431-245">Records that have not been refreshed by expiration of the Refresh interval could be removed by the next scavenging performed by a server.</span></span> <span data-ttu-id="41431-246">Dieser Wert sollte nie kleiner als der längste Aktualisierungs Zeitraum der in der Zone registrierten Datensätze sein.</span><span class="sxs-lookup"><span data-stu-id="41431-246">This value should never be less than the longest refresh period of the records registered in the zone.</span></span> <span data-ttu-id="41431-247">Werte, die zu klein sind, können dazu führen, dass gültige DNS-Einträge entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="41431-247">Values that are too small may lead to removal of valid DNS records.</span></span> <span data-ttu-id="41431-248">Werte, die zu groß sind, verlängern die Lebensdauer veralteter Datensätze.</span><span class="sxs-lookup"><span data-stu-id="41431-248">values that are too large prolong the lifetime of stale records.</span></span> <span data-ttu-id="41431-249">Dieser Wert wird auf die *DefaultRefreshInterval* -Eigenschaft des DNS-Servers festgelegt, auf dem die Zone erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41431-249">This value is set to the *DefaultRefreshInterval* property of the DNS server where the zone is created.</span></span>

</dd> <dt>

<span data-ttu-id="41431-250">**Umgekehr**</span><span class="sxs-lookup"><span data-stu-id="41431-250">**Reverse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-253">Gibt an, ob die Zone umgekehrt (true) oder vorwärts (false) ist.</span><span class="sxs-lookup"><span data-stu-id="41431-253">Indicates whether the Zone is reverse (TRUE) or forward (FALSE).</span></span>

</dd> <dt>

<span data-ttu-id="41431-254">**Scavengeservers**</span><span class="sxs-lookup"><span data-stu-id="41431-254">**ScavengeServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-255">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41431-255">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41431-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-257">Ein Array von Zeichen folgen, das die Liste der IP-Adressen von DNS-Servern auflistet, die für die Ausführung veralteter Datensätze dieser Zone berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="41431-257">Array of strings that enumerates the list of IP addresses of DNS servers that are allowed to perform scavenging of stale records of this zone.</span></span> <span data-ttu-id="41431-258">Wenn die Liste nicht angegeben wird, darf jeder primäre DNS-Server, der für die Zone autorisierend ist, die Zone durchlaufen, wenn andere Voraussetzungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="41431-258">If the list is not specified, any primary DNS server authoritative for the zone is allowed to scavenge the zone when other prerequisites are met.</span></span>

</dd> <dt>

<span data-ttu-id="41431-259">**Secondaryservers**</span><span class="sxs-lookup"><span data-stu-id="41431-259">**SecondaryServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-260">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41431-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41431-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-262">Array von Zeichen folgen, das IP-Adressen von DNS-Servern auflistet, die diese Zone durch Zonen Replikation empfangen dürfen.</span><span class="sxs-lookup"><span data-stu-id="41431-262">Array of strings enumerating IP addresses of DNS servers allowed to receive this zone through zone replication.</span></span>

</dd> <dt>

<span data-ttu-id="41431-263">**Securesecon-Replikate**</span><span class="sxs-lookup"><span data-stu-id="41431-263">**SecureSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-266">Gibt an, ob die Zonen Übertragung nur für bestimmte sekundäre Replikate zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="41431-266">Indicates whether zone transfer is allowed to designated secondaries only.</span></span> <span data-ttu-id="41431-267">Die vorgesehenen sekundären Replikate sind DNS-Server, deren IP-Adressen in secondariesipaddressesarray aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="41431-267">Designated secondaries are DNS Servers whose IP addresses are listed in SecondariesIPAddressesArray.</span></span>

</dd> <dt>

<span data-ttu-id="41431-268">**Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="41431-268">**Shutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-269">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-271">Gibt an, ob die Kopie der Zone abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="41431-271">Indicates whether the copy of the Zone is expired.</span></span> <span data-ttu-id="41431-272">TRUE gibt an, dass die Zone abgelaufen ist oder heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="41431-272">If TRUE, the Zone is expired, or shut down.</span></span>

</dd> <dt>

<span data-ttu-id="41431-273">**Usenbstat**</span><span class="sxs-lookup"><span data-stu-id="41431-273">**UseNBStat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-274">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-276">Dieser boolesche Wert gibt an, ob die Zone NBSTAT Reverse Lookup verwendet.</span><span class="sxs-lookup"><span data-stu-id="41431-276">This Boolean indicates whether the Zone uses NBStat reverse lookup.</span></span>

</dd> <dt>

<span data-ttu-id="41431-277">**Usewins**</span><span class="sxs-lookup"><span data-stu-id="41431-277">**UseWins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-278">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41431-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41431-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-280">Gibt an, ob die Zone WINS-Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="41431-280">Indicates whether the Zone uses WINS look up.</span></span>

</dd> <dt>

<span data-ttu-id="41431-281">**Zonetype**</span><span class="sxs-lookup"><span data-stu-id="41431-281">**ZoneType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41431-282">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41431-282">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41431-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41431-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41431-284">Gibt den Typ der Zone an.</span><span class="sxs-lookup"><span data-stu-id="41431-284">Indicates the type of the Zone.</span></span> <span data-ttu-id="41431-285">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="41431-285">Valid values are:</span></span>

-   <span data-ttu-id="41431-286">DS integriert</span><span class="sxs-lookup"><span data-stu-id="41431-286">DS integrated</span></span>
-   <span data-ttu-id="41431-287">Primär</span><span class="sxs-lookup"><span data-stu-id="41431-287">Primary</span></span>
-   <span data-ttu-id="41431-288">Secondary</span><span class="sxs-lookup"><span data-stu-id="41431-288">Secondary</span></span>

<span data-ttu-id="41431-289">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="41431-289">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="41431-290">Weitere Werte:</span><span class="sxs-lookup"><span data-stu-id="41431-290">Additional values:</span></span>

-   <span data-ttu-id="41431-291">Cache</span><span class="sxs-lookup"><span data-stu-id="41431-291">Cache</span></span>
-   <span data-ttu-id="41431-292">Stub</span><span class="sxs-lookup"><span data-stu-id="41431-292">Stub</span></span>
-   <span data-ttu-id="41431-293">Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="41431-293">Forwarder</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41431-294">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41431-294">Requirements</span></span>



| <span data-ttu-id="41431-295">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41431-295">Requirement</span></span> | <span data-ttu-id="41431-296">Wert</span><span class="sxs-lookup"><span data-stu-id="41431-296">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41431-297">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41431-297">Minimum supported client</span></span><br/> | <span data-ttu-id="41431-298">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41431-298">None supported</span></span><br/>                                                              |
| <span data-ttu-id="41431-299">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41431-299">Minimum supported server</span></span><br/> | <span data-ttu-id="41431-300">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41431-300">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="41431-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="41431-301">Namespace</span></span><br/>                | <span data-ttu-id="41431-302">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="41431-302">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="41431-303">MOF</span><span class="sxs-lookup"><span data-stu-id="41431-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41431-304"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41431-304"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41431-305">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41431-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41431-306">**MicrosoftDNS- \_ Domäne**</span><span class="sxs-lookup"><span data-stu-id="41431-306">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="41431-307">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-307">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="41431-308">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-308">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="41431-309">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-309">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="41431-310">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-310">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="41431-311">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-311">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="41431-312">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-312">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="41431-313">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-313">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="41431-314">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-314">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="41431-315">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-315">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="41431-316">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-316">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="41431-317">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="41431-317">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





