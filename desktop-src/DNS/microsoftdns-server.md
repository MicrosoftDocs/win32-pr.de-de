---
title: MicrosoftDNS_Server-Klasse
description: Die MicrosoftDNS- \_ Serverklasse beschreibt einen DNS-Server. Jede Instanz dieser Klasse kann mit einer Instanz des MicrosoftDNS \_ -Caches, einer Instanz von MicrosoftDNS \_ -roothints und mehreren Instanzen der MicrosoftDNS-Zone verknüpft werden \_ .
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS-MicrosoftDNS_Server Klasse
- DNS-MicrosoftDNS_Server Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949487"
---
# <a name="microsoftdns_server-class"></a><span data-ttu-id="24c06-106">MicrosoftDNS- \_ Server Klasse</span><span class="sxs-lookup"><span data-stu-id="24c06-106">MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="24c06-107">Die **MicrosoftDNS- \_ Server** Klasse beschreibt einen DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="24c06-107">The **MicrosoftDNS\_Server** class describes a DNS Server.</span></span> <span data-ttu-id="24c06-108">Jede Instanz dieser Klasse kann mit einer Instanz des [**MicrosoftDNS- \_ Caches**](microsoftdns-cache.md), einer Instanz von [**MicrosoftDNS- \_ roothints**](microsoftdns-roothints.md)und mehreren Instanzen der [**MicrosoftDNS- \_ Zone**](microsoftdns-zone.md)verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-108">Every instance of this class may be associated with one instance of [**MicrosoftDNS\_Cache**](microsoftdns-cache.md), one instance of [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md), and multiple instances of [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

<span data-ttu-id="24c06-109">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="24c06-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c06-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="24c06-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a><span data-ttu-id="24c06-111">Member</span><span class="sxs-lookup"><span data-stu-id="24c06-111">Members</span></span>

<span data-ttu-id="24c06-112">Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="24c06-112">The **MicrosoftDNS\_Server** class has these types of members:</span></span>

-   [<span data-ttu-id="24c06-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="24c06-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="24c06-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24c06-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24c06-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="24c06-115">Methods</span></span>

<span data-ttu-id="24c06-116">Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="24c06-116">The **MicrosoftDNS\_Server** class has these methods.</span></span>



| <span data-ttu-id="24c06-117">Methode</span><span class="sxs-lookup"><span data-stu-id="24c06-117">Method</span></span>                   | <span data-ttu-id="24c06-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24c06-118">Description</span></span>                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="24c06-119">**Getchilshedname**</span><span class="sxs-lookup"><span data-stu-id="24c06-119">**GetDistinguishedName**</span></span> | <span data-ttu-id="24c06-120">Ruft den DNS-Distinguished Name für die Zone ab.</span><span class="sxs-lookup"><span data-stu-id="24c06-120">Retrieves DNS distinguished name for the zone.</span></span><br/>                        |
| <span data-ttu-id="24c06-121">**Startscavenging**</span><span class="sxs-lookup"><span data-stu-id="24c06-121">**StartScavenging**</span></span>      | <span data-ttu-id="24c06-122">Startet das Bereinigung veralteter Datensätze in den Zonen, die für das Löschen von Daten stehen.</span><span class="sxs-lookup"><span data-stu-id="24c06-122">Starts scavenging stale records in the zones subjected to scavenging.</span></span><br/> |
| <span data-ttu-id="24c06-123">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="24c06-123">**StartService**</span></span>         | <span data-ttu-id="24c06-124">Hiermit wird der DNS-Server gestartet.</span><span class="sxs-lookup"><span data-stu-id="24c06-124">Starts the DNS Server.</span></span><br/>                                                |
| <span data-ttu-id="24c06-125">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="24c06-125">**StopService**</span></span>          | <span data-ttu-id="24c06-126">Beendet den DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="24c06-126">Stops the DNS Server.</span></span><br/>                                                 |



 

### <a name="properties"></a><span data-ttu-id="24c06-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24c06-127">Properties</span></span>

<span data-ttu-id="24c06-128">Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24c06-128">The **MicrosoftDNS\_Server** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24c06-129">**Addressbeantworungslimit**</span><span class="sxs-lookup"><span data-stu-id="24c06-129">**AddressAnswerLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-132">Maximale Anzahl von Host Datensätzen, die als Reaktion auf eine Adress Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-132">Maximum number of host records returned in response to an address request.</span></span> <span data-ttu-id="24c06-133">Werte zwischen 5 und 28 sind gültig.</span><span class="sxs-lookup"><span data-stu-id="24c06-133">Values between 5 and 28 are valid.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-134">**AllowUpdate**</span><span class="sxs-lookup"><span data-stu-id="24c06-134">**AllowUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-137">Gibt an, ob der DNS-Server dynamische Update Anforderungen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="24c06-137">Specifies whether the DNS Server accepts dynamic update requests.</span></span> <span data-ttu-id="24c06-138">Gültige Werte sind wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="24c06-138">Valid values are as shown in the following table.</span></span>



| <span data-ttu-id="24c06-139">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-139">Value</span></span>                                                                                                | <span data-ttu-id="24c06-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-140">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-141"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-141"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-142">Keine Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="24c06-142">No Restrictions.</span></span><br/>                                                                           |
| <span id="1"></span><dl> <span data-ttu-id="24c06-143"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-143"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-144">Lässt keine dynamische Aktualisierung von SOA-Datensätzen zu.</span><span class="sxs-lookup"><span data-stu-id="24c06-144">Does not allow dynamic updates of SOA records.</span></span><br/>                                             |
| <span id="2"></span><dl> <span data-ttu-id="24c06-145"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-145"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-146">Lässt keine dynamischen Updates von NS-Datensätzen am Zonen Stamm zu.</span><span class="sxs-lookup"><span data-stu-id="24c06-146">Does not allow dynamic updates of NS records at the zone root.</span></span><br/>                             |
| <span id="4"></span><dl> <span data-ttu-id="24c06-147"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-147"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24c06-148">Lässt keine dynamischen Updates von NS-Einträgen zu, die sich nicht im Zonen Stamm befinden (Delegierung von NS-Einträgen).</span><span class="sxs-lookup"><span data-stu-id="24c06-148">Does not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span><br/> |



 

<span data-ttu-id="24c06-149">Addieren Sie diese Werte, um den Einstellungs Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="24c06-149">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-150">**Autocacheupdate**</span><span class="sxs-lookup"><span data-stu-id="24c06-150">**AutoCacheUpdate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-151">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-153">Gibt an, ob der DNS-Server versucht, seine Cache Einträge mithilfe von Daten von Stamm Servern zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="24c06-153">Indicates whether the DNS Server attempts to update its cache entries using data from root servers.</span></span> <span data-ttu-id="24c06-154">Wenn ein DNS-Server gestartet wird, benötigt er eine Liste der "Hinweise" des Stamm Servers und eine Einträge für die Server, die in der Vergangenheit als Cachedatei bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="24c06-154">When a DNS Server boots, it needs a list of root server 'hints' NS and A records for the servers historically called the cache file.</span></span> <span data-ttu-id="24c06-155">Microsoft DNS-Server verfügen über eine Funktion, mit der Sie versuchen können, eine neue Cachedatei auf der Grundlage der Antworten von Stamm Servern zurückzuschreiben.</span><span class="sxs-lookup"><span data-stu-id="24c06-155">Microsoft DNS Servers have a feature that enables them to attempt to write back a new cache file based on the responses from root servers.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-156">**Autoconfigfilezones**</span><span class="sxs-lookup"><span data-stu-id="24c06-156">**AutoConfigFileZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-159">Gibt an, welche standardmäßigen primären Zonen, die für den Namen des DNS-Servers autorisierend sind, aktualisiert werden müssen, wenn der Namen Server geändert wird.</span><span class="sxs-lookup"><span data-stu-id="24c06-159">Indicates which standard primary zones that are authoritative for the name of the DNS Server must be updated when the name server changes.</span></span> <span data-ttu-id="24c06-160">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24c06-160">Valid values are as follows:</span></span>



| <span data-ttu-id="24c06-161">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-161">Value</span></span>                                                                                                | <span data-ttu-id="24c06-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-162">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-163"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-163"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-164">Keine.</span><span class="sxs-lookup"><span data-stu-id="24c06-164">None.</span></span><br/>                                           |
| <span id="1"></span><dl> <span data-ttu-id="24c06-165"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-165"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-166">Nur Server, die dynamische Updates zulassen.</span><span class="sxs-lookup"><span data-stu-id="24c06-166">Only servers that allow dynamic updates.</span></span><br/>        |
| <span id="2"></span><dl> <span data-ttu-id="24c06-167"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-167"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-168">Nur Server, die keine dynamischen Updates zulassen.</span><span class="sxs-lookup"><span data-stu-id="24c06-168">Only servers that do not allow dynamic updates.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="24c06-169"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-169"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24c06-170">Alle Server.</span><span class="sxs-lookup"><span data-stu-id="24c06-170">All servers.</span></span><br/>                                    |



 

<span data-ttu-id="24c06-171">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="24c06-171">The default value is 1.</span></span>

<span data-ttu-id="24c06-172">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="24c06-172">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="24c06-173">Die Zahl 3 stellt alle Server dar.</span><span class="sxs-lookup"><span data-stu-id="24c06-173">The number 3 represents All servers.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-174">**Bindsecon-Datenbanken**</span><span class="sxs-lookup"><span data-stu-id="24c06-174">**BindSecondaries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-175">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-176">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-177">Bestimmt das AXFR-Nachrichtenformat beim Senden an sekundäre DNS-Server-Objekte, die nicht von Microsoft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-177">Determines the AXFR message format when sending to non-Microsoft DNS Server secondaries.</span></span> <span data-ttu-id="24c06-178">Wenn diese Einstellung auf "true" festgelegt ist, sendet der DNS-Server Übertragungen an sekundäre DNS-Server-Replikate im nicht komprimierten Format.</span><span class="sxs-lookup"><span data-stu-id="24c06-178">When set to TRUE, the DNS Server sends transfers to non-Microsoft DNS Server secondaries in the uncompressed format.</span></span> <span data-ttu-id="24c06-179">Bei "false" werden alle Übertragungen im schnellen Format gesendet.</span><span class="sxs-lookup"><span data-stu-id="24c06-179">When FALSE, all transfers are sent in the fast format.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-180">**Bootmethod**</span><span class="sxs-lookup"><span data-stu-id="24c06-180">**BootMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-183">Initialisierungs Methode für den DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="24c06-183">Initialization method for the DNS Server.</span></span> <span data-ttu-id="24c06-184">Gültige Werte werden in der folgenden Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24c06-184">Valid values are shown in the following table.</span></span>



| <span data-ttu-id="24c06-185">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-185">Value</span></span>                                                                                                | <span data-ttu-id="24c06-186">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-186">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-187"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-187"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-188">Nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="24c06-188">Uninitialized.</span></span><br/>                    |
| <span id="1"></span><dl> <span data-ttu-id="24c06-189"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-189"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-190">Starten von einer Datei aus.</span><span class="sxs-lookup"><span data-stu-id="24c06-190">Boot from file.</span></span><br/>                   |
| <span id="2"></span><dl> <span data-ttu-id="24c06-191"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-191"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-192">Starten von der Registrierung aus.</span><span class="sxs-lookup"><span data-stu-id="24c06-192">Boot from registry.</span></span><br/>               |
| <span id="3"></span><dl> <span data-ttu-id="24c06-193"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-193"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="24c06-194">Starten von Verzeichnis und Registrierung.</span><span class="sxs-lookup"><span data-stu-id="24c06-194">Boot from directory and registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="24c06-195">**DefaultAgingState**</span><span class="sxs-lookup"><span data-stu-id="24c06-195">**DefaultAgingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-198">Der Standardwert für **ScavengingInterval** ist für alle Active Directory integrierten Zonen festgelegt, die auf diesem DNS-Server erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c06-198">Default **ScavengingInterval** value set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="24c06-199">Der Standardwert ist 0 (null), was bedeutet, dass das Bereinigung deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="24c06-199">The default value is zero, indicating scavenging is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-200">**DefaultNoRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="24c06-200">**DefaultNoRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-202">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-203">Kein Aktualisierungs Intervall (in Stunden) für alle Active Directory integrierten Zonen, die auf diesem DNS-Server erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c06-203">No-refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="24c06-204">Der Standardwert ist 168 Stunden (sieben Tage).</span><span class="sxs-lookup"><span data-stu-id="24c06-204">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="24c06-205">**DefaultRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="24c06-205">**DefaultRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-206">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-207">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-207">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-208">Aktualisierungs Intervall (in Stunden), das für alle Active Directory integrierten Zonen festgelegt wird, die auf diesem DNS-Server erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c06-208">Refresh interval, in hours, set for all Active Directory-integrated zones created on this DNS Server.</span></span> <span data-ttu-id="24c06-209">Der Standardwert ist 168 Stunden (sieben Tage).</span><span class="sxs-lookup"><span data-stu-id="24c06-209">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="24c06-210">**Disableautoreverversionen**</span><span class="sxs-lookup"><span data-stu-id="24c06-210">**DisableAutoReverseZones**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-211">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-212">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-213">Gibt an, ob der DNS-Server automatisch standardmäßige Reverse-Lookupzonen erstellt.</span><span class="sxs-lookup"><span data-stu-id="24c06-213">Indicates whether the DNS Server automatically creates standard reverse look up zones.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-214">**Disjoinnetze**</span><span class="sxs-lookup"><span data-stu-id="24c06-214">**DisjointNets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-215">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-216">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-217">Gibt an, ob die Standard Port Bindung für einen Socket, der zum Senden von Abfragen an DNS-Remote Server verwendet wird, überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="24c06-217">Indicates whether the default port binding for a socket used to send queries to remote DNS Servers can be overridden.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-218">**Dsavailable**</span><span class="sxs-lookup"><span data-stu-id="24c06-218">**DsAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-221">Gibt an, ob auf dem DNS-Server ein verfügbarer DS vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-221">Indicates whether there is an available DS on the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-222">**Dspollinginterval**</span><span class="sxs-lookup"><span data-stu-id="24c06-222">**DsPollingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-223">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-224">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-224">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-225">Intervall (in Sekunden) zum Abfragen der in DS integrierten Zonen.</span><span class="sxs-lookup"><span data-stu-id="24c06-225">Interval, in seconds, to poll the DS-integrated zones.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-226">**Dstombstoneinterval**</span><span class="sxs-lookup"><span data-stu-id="24c06-226">**DsTombstoneInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-227">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-228">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-229">Lebensdauer von Datensätzen mit tombstoning in den in einem Verzeichnisdienst integrierten Zonen, ausgedrückt in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="24c06-229">Lifetime of tombstoned records in Directory Service integrated zones, expressed in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-230">**EDNSCacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="24c06-230">**EDnsCacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-231">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-231">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-233">Lebensdauer (in Sekunden) der zwischengespeicherten Informationen, die die von anderen DNS-Servern unterstützte EDNS-Version beschreiben.</span><span class="sxs-lookup"><span data-stu-id="24c06-233">Lifetime, in seconds, of the cached information describing the EDNS version supported by other DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-234">**Enabledirectoriypartitions**</span><span class="sxs-lookup"><span data-stu-id="24c06-234">**EnableDirectoryPartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-235">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-236">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-237">Gibt an, ob die Unterstützung für Anwendungsverzeichnis Partitionen auf dem DNS-Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-237">Specifies whether support for application directory partitions is enabled on the DNS Server.</span></span>

<span data-ttu-id="24c06-238">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="24c06-238">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="24c06-239">Diese Methode heißt enabledirectorypartitionsupport.</span><span class="sxs-lookup"><span data-stu-id="24c06-239">This method is named EnableDirectoryPartitionSupport.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-240">**EnableDnsSec**</span><span class="sxs-lookup"><span data-stu-id="24c06-240">**EnableDnsSec**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-241">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-242">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-243">Gibt an, ob der DNS-Server DNSSEC-spezifische RRS, Key, SIG und NXT in einer Antwort enthält, die in der folgenden Tabelle aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="24c06-243">Specifies whether the DNS Server includes DNSSEC-specific RRs, KEY, SIG, and NXT in a response, per the following table:</span></span>



| <span data-ttu-id="24c06-244">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-244">Value</span></span>                                                                                                | <span data-ttu-id="24c06-245">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-245">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-246"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-246"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-247">In der Antwort sind keine DNSSEC-Einträge enthalten, es sei denn, die Abfrage hat einen Ressourcen Eintrags Satz des DNSSEC-Daten Satz Typs angefordert.</span><span class="sxs-lookup"><span data-stu-id="24c06-247">No DNSSEC records are included in the response unless the query requested a resource record set of the DNSSEC record type.</span></span><br/>          |
| <span id="1"></span><dl> <span data-ttu-id="24c06-248"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-248"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-249">DNSSEC-Datensätze sind in der Antwort gemäß RFC 2535 enthalten.</span><span class="sxs-lookup"><span data-stu-id="24c06-249">DNSSEC records are included in the response according to RFC 2535.</span></span><br/>                                                                  |
| <span id="2"></span><dl> <span data-ttu-id="24c06-250"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-250"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-251">DNSSEC-Datensätze sind nur in einer Antwort enthalten, wenn die ursprüngliche Client Abfrage den Opt-Ressourcen Daten Satz gemäß RFC 2671 enthielt.</span><span class="sxs-lookup"><span data-stu-id="24c06-251">DNSSEC records are included in a response only if the original client query contained the OPT resource record according to RFC 2671</span></span><br/> |



 

<span data-ttu-id="24c06-252">Wenn eine Abfrage einen Ressourcen Eintrags Satz des DNSSEC-Typs anfordert, antwortet der DNS-Server immer mit solchen Datensätzen, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24c06-252">If a query requests a resource record set of the DNSSEC type, the DNS Server always responds with such records, if available.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-253">**EnableEDnsProbes**</span><span class="sxs-lookup"><span data-stu-id="24c06-253">**EnableEDnsProbes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-254">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-254">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-255">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-255">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-256">Gibt das Verhalten des DNS-Servers an.</span><span class="sxs-lookup"><span data-stu-id="24c06-256">Specifies the behavior of the DNS Server.</span></span> <span data-ttu-id="24c06-257">TRUE gibt an, dass der DNS-Server nach RFC 2671 immer mit opt-Ressourcen Einträgen antwortet, es sei denn, der Remote Server hat angegeben, dass EDNS in einem früheren Exchange nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-257">When TRUE, the DNS Server always responds with OPT resource records according to RFC 2671, unless the remote server has indicated it does not support EDNS in a prior exchange.</span></span> <span data-ttu-id="24c06-258">FALSE gibt an, dass der DNS-Server nur dann auf Abfragen mit OPTS antwortet, wenn opts in der ursprünglichen Abfrage gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-258">If FALSE, the DNS Server responds to queries with OPTs only if OPTs are sent in the original query.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-259">**EventLogLevel**</span><span class="sxs-lookup"><span data-stu-id="24c06-259">**EventLogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-260">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-260">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-261">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-261">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-262">Gibt an, welche Ereignisse der DNS-Server im Ereignisanzeige System Protokoll aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="24c06-262">Indicates which events the DNS Server records in the Event Viewer system log.</span></span> <span data-ttu-id="24c06-263">Die folgenden Werte werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c06-263">The following values are used.</span></span>



| <span data-ttu-id="24c06-264">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-264">Value</span></span>                                                                                                | <span data-ttu-id="24c06-265">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-265">Meaning</span></span>                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-266"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-266"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-267">Keine.</span><span class="sxs-lookup"><span data-stu-id="24c06-267">None.</span></span><br/>                         |
| <span id="1"></span><dl> <span data-ttu-id="24c06-268"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-268"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-269">Nur Fehler protokollieren.</span><span class="sxs-lookup"><span data-stu-id="24c06-269">Log only errors.</span></span><br/>              |
| <span id="2"></span><dl> <span data-ttu-id="24c06-270"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-270"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-271">Protokolliert nur Warnungen und Fehler.</span><span class="sxs-lookup"><span data-stu-id="24c06-271">Log only warnings and errors.</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="24c06-272"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-272"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24c06-273">Alle Ereignisse protokollieren.</span><span class="sxs-lookup"><span data-stu-id="24c06-273">Log all events.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="24c06-274">**Weiterleitungen**</span><span class="sxs-lookup"><span data-stu-id="24c06-274">**ForwardDelegations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-275">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-276">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-276">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-277">Gibt an, ob Abfragen an Delegierte Subzonen weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-277">Specifies whether queries to delegated sub-zones are forwarded.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-278">**Weiterleitungen**</span><span class="sxs-lookup"><span data-stu-id="24c06-278">**Forwarders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-279">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="24c06-279">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24c06-280">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-280">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-281">Listet die IP-Adressen der Weiterleitungen auf, an die der DNS-Server Abfragen weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="24c06-281">Enumerates the list of IP addresses of Forwarders to which the DNS Server forwards queries.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-282">**"Forwardingtimeout"**</span><span class="sxs-lookup"><span data-stu-id="24c06-282">**ForwardingTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-284">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-284">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-285">Die Zeit (in Sekunden), die ein DNS-Server, der eine Abfrage weiterleitet, auf Auflösung von der Weiterleitung wartet [*, bevor versucht*](f-gly.md) wird, die Abfrage selbst aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="24c06-285">Time, in seconds, a DNS Server forwarding a query will wait for resolution from the [*forwarder*](f-gly.md) before attempting to resolve the query itself.</span></span>

<span data-ttu-id="24c06-286">Dieser Wert ist bedeutungslos, wenn der Weiterleitungsserver nicht für die Verwendung der Rekursion festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-286">This value is meaningless if the forwarding server is not set to use recursion.</span></span> <span data-ttu-id="24c06-287">Um dies zu ermitteln, überprüfen Sie die Eigenschaft ' isslave ' Boolean.</span><span class="sxs-lookup"><span data-stu-id="24c06-287">To determine this, check the IsSlave Boolean property.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-288">**Isslave**</span><span class="sxs-lookup"><span data-stu-id="24c06-288">**IsSlave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-291">**True** , wenn der DNS-Server keine Rekursion verwendet, wenn die Namensauflösung durch Weiterleitungen fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="24c06-291">**TRUE** if the DNS server does not use recursion when name-resolution through forwarders fails.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-292">**Listenadressen**</span><span class="sxs-lookup"><span data-stu-id="24c06-292">**ListenAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-293">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="24c06-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24c06-294">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-294">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-295">Listet die IP-Adressen auf, auf denen der DNS-Server Abfragen empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="24c06-295">Enumerates the list of IP addresses on which the DNS Server can receive queries.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-296">**Localnetpriority**</span><span class="sxs-lookup"><span data-stu-id="24c06-296">**LocalNetPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-298">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-298">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-299">Gibt an, ob der DNS-Server bei der Rückgabe von Datensätzen Priorität für die lokale Netzwerkadresse erhält.</span><span class="sxs-lookup"><span data-stu-id="24c06-299">Indicates whether the DNS Server gives priority to the local net address when returning A records.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-300">**LogFileMaxSize**</span><span class="sxs-lookup"><span data-stu-id="24c06-300">**LogFileMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-301">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-302">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-302">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-303">Größe des DNS-Server-Debugprotokolls in Bytes.</span><span class="sxs-lookup"><span data-stu-id="24c06-303">Size of the DNS Server debug log, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-304">**LogFilePath**</span><span class="sxs-lookup"><span data-stu-id="24c06-304">**LogFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c06-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-306">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-306">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-307">Dateiname und Pfad für das DNS-Server-Debugprotokoll.</span><span class="sxs-lookup"><span data-stu-id="24c06-307">File name and path for the DNS Server debug log.</span></span> <span data-ttu-id="24c06-308">Der Standardwert ist% System32% \\ DNS \\ DNS. log.</span><span class="sxs-lookup"><span data-stu-id="24c06-308">Default is %system32%\\dns\\dns.log.</span></span> <span data-ttu-id="24c06-309">Relative Pfade sind relativ zu% systemroot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="24c06-309">Relative paths are relative to %Systemroot%\\System32.</span></span> <span data-ttu-id="24c06-310">Absolute Pfade können verwendet werden, UNC-Pfade werden jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24c06-310">Absolute paths may be used, but UNC paths are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-311">**Logipfilterlist**</span><span class="sxs-lookup"><span data-stu-id="24c06-311">**LogIPFilterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-312">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="24c06-312">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24c06-313">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-313">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-314">Liste der IP-Adressen, die zum Filtern von in das Debugprotokoll geschriebenen DNS-Ereignissen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-314">List of IP addresses used to filter DNS events written to the debug log.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-315">**LogLevel**</span><span class="sxs-lookup"><span data-stu-id="24c06-315">**LogLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-316">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-317">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-317">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-318">Gibt an, welche Richtlinien im Ereignisanzeige System Protokoll aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-318">Indicates which policies are activated in the Event Viewer system log.</span></span>

<span data-ttu-id="24c06-319">Sollte auf Grundlage des folgenden Algorithmus auf bestimmte Werte festgelegt werden: für jede Richtlinie (die im Ereignisanzeige System Protokoll aktiviert werden soll) wird ein bestimmter Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="24c06-319">Should be set to specific values based on the following algorithm: Every policy (to be activated in the Event Viewer system log) is assigned a specific value.</span></span>



| <span data-ttu-id="24c06-320">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-320">Value</span></span>                                                                                                                  | <span data-ttu-id="24c06-321">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-321">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="24c06-322"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-322"><dt>**1**</dt></span></span> </dl>                   | <span data-ttu-id="24c06-323">Such.</span><span class="sxs-lookup"><span data-stu-id="24c06-323">Query.</span></span><br/>                                   |
| <span id="16"></span><dl> <span data-ttu-id="24c06-324"><dt>**Uhr**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-324"><dt>**16**</dt></span></span> </dl>                 | <span data-ttu-id="24c06-325">Informiert.</span><span class="sxs-lookup"><span data-stu-id="24c06-325">Notify.</span></span><br/>                                  |
| <span id="32"></span><dl> <span data-ttu-id="24c06-326"><dt>**32**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-326"><dt>**32**</dt></span></span> </dl>                 | <span data-ttu-id="24c06-327">Alisierungs.</span><span class="sxs-lookup"><span data-stu-id="24c06-327">Update.</span></span><br/>                                  |
| <span id="254"></span><dl> <span data-ttu-id="24c06-328"><dt>**254**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-328"><dt>**254**</dt></span></span> </dl>               | <span data-ttu-id="24c06-329">Nicht abgefragt Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="24c06-329">Nonquery transactions.</span></span><br/>                   |
| <span id="256"></span><dl> <span data-ttu-id="24c06-330"><dt>**256**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-330"><dt>**256**</dt></span></span> </dl>               | <span data-ttu-id="24c06-331">Fragen.</span><span class="sxs-lookup"><span data-stu-id="24c06-331">Questions.</span></span><br/>                               |
| <span id="512"></span><dl> <span data-ttu-id="24c06-332"><dt>**512**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-332"><dt>**512**</dt></span></span> </dl>               | <span data-ttu-id="24c06-333">Beantwortet.</span><span class="sxs-lookup"><span data-stu-id="24c06-333">Answers.</span></span><br/>                                 |
| <span id="4096"></span><dl> <span data-ttu-id="24c06-334"><dt>**4096**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-334"><dt>**4096**</dt></span></span> </dl>             | <span data-ttu-id="24c06-335">Send.</span><span class="sxs-lookup"><span data-stu-id="24c06-335">Send.</span></span><br/>                                    |
| <span id="8192"></span><dl> <span data-ttu-id="24c06-336"><dt>**8192**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-336"><dt>**8192**</dt></span></span> </dl>             | <span data-ttu-id="24c06-337">Medizinisch.</span><span class="sxs-lookup"><span data-stu-id="24c06-337">Receive.</span></span><br/>                                 |
| <span id="16384"></span><dl> <span data-ttu-id="24c06-338"><dt>**16384**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-338"><dt>**16384**</dt></span></span> </dl>           | <span data-ttu-id="24c06-339">UDP.</span><span class="sxs-lookup"><span data-stu-id="24c06-339">UDP.</span></span><br/>                                     |
| <span id="32768"></span><dl> <span data-ttu-id="24c06-340"><dt>**32768**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-340"><dt>**32768**</dt></span></span> </dl>           | <span data-ttu-id="24c06-341">TCP.</span><span class="sxs-lookup"><span data-stu-id="24c06-341">TCP.</span></span><br/>                                     |
| <span id="65535"></span><dl> <span data-ttu-id="24c06-342"><dt>**65535**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-342"><dt>**65535**</dt></span></span> </dl>           | <span data-ttu-id="24c06-343">Alle Pakete.</span><span class="sxs-lookup"><span data-stu-id="24c06-343">All packets.</span></span><br/>                             |
| <span id="65536"></span><dl> <span data-ttu-id="24c06-344"><dt>**65536**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-344"><dt>**65536**</dt></span></span> </dl>           | <span data-ttu-id="24c06-345">NT-Verzeichnisdienst-Schreib Transaktion.</span><span class="sxs-lookup"><span data-stu-id="24c06-345">NT Directory Service write transaction.</span></span><br/>  |
| <span id="131072"></span><dl> <span data-ttu-id="24c06-346"><dt>**131072**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-346"><dt>**131072**</dt></span></span> </dl>         | <span data-ttu-id="24c06-347">NT-Verzeichnisdienst-Aktualisierungs Transaktion.</span><span class="sxs-lookup"><span data-stu-id="24c06-347">NT Directory Service update transaction.</span></span><br/> |
| <span id="16777216"></span><dl> <span data-ttu-id="24c06-348"><dt>**16777216**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-348"><dt>**16777216**</dt></span></span> </dl>     | <span data-ttu-id="24c06-349">Vollständige Pakete.</span><span class="sxs-lookup"><span data-stu-id="24c06-349">Full packets.</span></span><br/>                            |
| <span id="2147483648"></span><dl> <span data-ttu-id="24c06-350"><dt>**2147483648**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-350"><dt>**2147483648**</dt></span></span> </dl> | <span data-ttu-id="24c06-351">Schreiben Sie.</span><span class="sxs-lookup"><span data-stu-id="24c06-351">Write through.</span></span><br/>                           |



 

<span data-ttu-id="24c06-352">Die Summe der Werte, die allen zu aktivierenden Richtlinien entsprechen, wird in dieser Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="24c06-352">The sum of the values corresponding to all the policies to be activated is indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-353">**Looseemwildcarding**</span><span class="sxs-lookup"><span data-stu-id="24c06-353">**LooseWildcarding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-354">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-355">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-355">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-356">Gibt an, ob der DNS-Server lose Platzhalter Vorgänge ausführt.</span><span class="sxs-lookup"><span data-stu-id="24c06-356">Indicates whether the DNS Server performs loose wildcarding.</span></span> <span data-ttu-id="24c06-357">Wenn nicht definiert oder 0 (null), folgt der Server dem in der DNS-RFC angegebenen Platzhalter Verhalten.</span><span class="sxs-lookup"><span data-stu-id="24c06-357">If undefined or zero, the server follows the wildcarding behavior specified in the DNS RFC.</span></span> <span data-ttu-id="24c06-358">In diesem Fall wird empfohlen, MX-Einträge für alle Hosts aufzunehmen, die keine e-Mail empfangen können.</span><span class="sxs-lookup"><span data-stu-id="24c06-358">In this case, an administrator is advised to include MX records for all hosts incapable of receiving mail.</span></span> <span data-ttu-id="24c06-359">Wenn der Wert ungleich NULL ist, wird vom Server der nächste Platzhalter Knoten gesucht. in diesem Fall sollte ein Administrator MX-Einträge am Zonen Stamm und in einem Platzhalter Knoten (" \* ") direkt unterhalb des Zonen Stamms ablegen.</span><span class="sxs-lookup"><span data-stu-id="24c06-359">If nonzero, the server seeks the closest wildcard node; in this case, an administrator should put MX records at the zone root and in a wildcard node ('\*') directly below the zone root.</span></span> <span data-ttu-id="24c06-360">Administratoren sollten außerdem selbst verweisende MX-Einträge auf Hosts platzieren, die ihre eigene e-Mail erhalten.</span><span class="sxs-lookup"><span data-stu-id="24c06-360">Also, administrators should put self-referencing MX records on hosts that receive their own mail.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-361">**Maxcachettl**</span><span class="sxs-lookup"><span data-stu-id="24c06-361">**MaxCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-362">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-363">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-363">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-364">Maximale Zeit in Sekunden, während der der Datensatz einer rekursiven Namensabfrage im DNS-Server Cache verbleiben kann.</span><span class="sxs-lookup"><span data-stu-id="24c06-364">Maximum time, in seconds, the record of a recursive name query may remain in the DNS Server cache.</span></span> <span data-ttu-id="24c06-365">Der DNS-Server löscht Datensätze aus dem Cache, wenn der Wert dieses Eintrags abläuft, auch wenn der Wert des TTL-Felds im Datensatz größer ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-365">The DNS Server deletes records from the cache when the value of this entry expires, even if the value of the TTL field in the record is greater.</span></span>

<span data-ttu-id="24c06-366">Der Standardwert dieser Eigenschaft ist 86.400 Sekunden (1 Tag).</span><span class="sxs-lookup"><span data-stu-id="24c06-366">The default value of this property is 86,400 seconds (1 day).</span></span>

</dd> <dt>

<span data-ttu-id="24c06-367">**Maxnegativecachettl**</span><span class="sxs-lookup"><span data-stu-id="24c06-367">**MaxNegativeCacheTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-368">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-369">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-369">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-370">Die maximale Zeit in Sekunden, die ein Namensfehler Ergebnis einer rekursiven Abfrage im DNS-Server Cache verbleiben kann.</span><span class="sxs-lookup"><span data-stu-id="24c06-370">Maximum time, in seconds, a name error result from a recursive query may remain in the DNS Server cache.</span></span> <span data-ttu-id="24c06-371">DNS löscht Datensätze aus dem Cache, wenn dieser Timer abläuft, auch wenn das TTL-Feld größer ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-371">DNS deletes records from the cache when this timer expires, even if the TTL field is greater.</span></span> <span data-ttu-id="24c06-372">Der Standardwert ist 86.400 (ein Tag).</span><span class="sxs-lookup"><span data-stu-id="24c06-372">Default value is 86,400 (one day).</span></span>

</dd> <dt>

<span data-ttu-id="24c06-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="24c06-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c06-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c06-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24c06-376">Der voll qualifizierte Domänen Name (FQDN) oder die IP-Adresse des DNS-Servers.</span><span class="sxs-lookup"><span data-stu-id="24c06-376">Fully qualified domain name (FQDN) or IP address of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-377">**Namecheckflag**</span><span class="sxs-lookup"><span data-stu-id="24c06-377">**NameCheckFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-378">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-379">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-379">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-380">Gibt den Satz berechtigter Zeichen an, die in DNS-Namen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24c06-380">Indicates the set of eligible characters to be used in DNS names.</span></span> <span data-ttu-id="24c06-381">Die folgenden Werte werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c06-381">The following values are used.</span></span>



| <span data-ttu-id="24c06-382">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-382">Value</span></span>                                                                                                | <span data-ttu-id="24c06-383">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-383">Meaning</span></span>                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-384"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-384"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-385">Strict RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24c06-385">Strict RFC (ANSI)</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="24c06-386"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-386"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-387">Nicht-RFC (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24c06-387">Non RFC (ANSI)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="24c06-388"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-388"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="24c06-389">Multibyte (UTF8)</span><span class="sxs-lookup"><span data-stu-id="24c06-389">Multibyte (UTF8)</span></span><br/>  |



 

<span data-ttu-id="24c06-390">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="24c06-390">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="24c06-391">Der Wert "2" gibt "Any" an.</span><span class="sxs-lookup"><span data-stu-id="24c06-391">A value of "2" indicates "Any."</span></span>

</dd> <dt>

<span data-ttu-id="24c06-392">**NoRecursion**</span><span class="sxs-lookup"><span data-stu-id="24c06-392">**NoRecursion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-393">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-393">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-394">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-394">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-395">Gibt an, ob der DNS-Server rekursive Suche ausführt.</span><span class="sxs-lookup"><span data-stu-id="24c06-395">Indicates whether the DNS Server performs recursive look ups.</span></span> <span data-ttu-id="24c06-396">TRUE gibt an, dass rekursive Suchen nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-396">TRUE indicates recursive look ups are not performed.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-397">**Rekursionretry**</span><span class="sxs-lookup"><span data-stu-id="24c06-397">**RecursionRetry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-398">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-399">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-399">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-400">Verstrichene Sekunden vor Wiederholungsversuch für eine rekursive Suche.</span><span class="sxs-lookup"><span data-stu-id="24c06-400">Elapsed seconds before retrying a recursive look up.</span></span> <span data-ttu-id="24c06-401">Wenn die Eigenschaft nicht definiert oder NULL ist, werden nach drei Sekunden Wiederholungs Versuche durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="24c06-401">If the property is undefined or zero, retries are made after three seconds.</span></span> <span data-ttu-id="24c06-402">Benutzer werden davon abgeraten, diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="24c06-402">Users are discouraged from altering this property.</span></span> <span data-ttu-id="24c06-403">Es gibt bestimmte Situationen, in denen die Eigenschaft geändert werden soll. ein Beispiel hierfür ist, wenn der DNS-Server über eine langsame Verbindung mit Remote Servern kontaktiert und der DNS-Server wiederholt wird, bevor die Antwort vom Remote-DNS empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="24c06-403">There are certain situations when the property should be changed; one example is when the DNS Server contacts remote servers over a slow link, and the DNS Server is retrying before receiving response from the remote DNS.</span></span> <span data-ttu-id="24c06-404">In diesem Fall wäre es sinnvoll, den Timeout zu erhöhen, wenn die beobachtete Antwortzeit des Remote-DNS etwas länger ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-404">In this case, raising the time out to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-405">**Recursiontimeout**</span><span class="sxs-lookup"><span data-stu-id="24c06-405">**RecursionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-406">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-406">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-407">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-407">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-408">Verstrichene Sekunden, bevor der DNS-Server eine rekursive Abfrage ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="24c06-408">Elapsed seconds before the DNS Server gives up recursive query.</span></span> <span data-ttu-id="24c06-409">Wenn die Eigenschaft nicht definiert oder NULL ist, gibt der DNS-Server nach 15 Sekunden einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="24c06-409">If the property is undefined or zero, the DNS Server gives up after 15 seconds.</span></span> <span data-ttu-id="24c06-410">Im Allgemeinen ist das 15-Sekunden-Timeout ausreichend, damit alle ausstehenden Antworten an den DNS-Server zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="24c06-410">In general, the 15-second time out is sufficient to allow any outstanding response to get back to the DNS Server.</span></span>

<span data-ttu-id="24c06-411">Benutzer werden davon abgeraten, diese Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="24c06-411">Users are discouraged from altering this property.</span></span> <span data-ttu-id="24c06-412">Ein Szenario, in dem die Eigenschaft geändert werden sollte, ist, wenn der DNS-Server über eine langsame Verbindung mit Remote Servern kontaktiert wird und der DNS-Server beobachtet wird, dass Abfragen (mit Server \_ Fehlern) abgelehnt werden, bevor Antworten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-412">One scenario where the property should be changed is when the DNS Server contacts remote servers over a slow link, and the DNS Server is observed rejecting queries (with SERVER\_FAILURE) before responses are received.</span></span>

<span data-ttu-id="24c06-413">Clientresolver wiederholen auch Abfragen, daher ist eine sorgfältige Untersuchung erforderlich, um zu bestimmen, ob Remote Antworten tatsächlich der Abfrage zugeordnet sind, für die ein Timeout aufgetreten ist. In diesem Fall wäre es sinnvoll, den Timeout Wert so zu erhöhen, dass er etwas länger als die beobachtete Antwortzeit des Remote-DNS ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-413">Client resolvers also retry queries, so careful investigation is required to determine whether remote responses are actually associated with the query that timed out. In this case, raising the time out value to be slightly longer than the observed response time from the remote DNS would be reasonable.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-414">**Roundrobin**</span><span class="sxs-lookup"><span data-stu-id="24c06-414">**RoundRobin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-415">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-416">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-416">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-417">Gibt an, ob der DNS-Server mehrere A-Einträge aufrundet.</span><span class="sxs-lookup"><span data-stu-id="24c06-417">Indicates whether the DNS Server round robins multiple A records.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-418">**RpcProtocol**</span><span class="sxs-lookup"><span data-stu-id="24c06-418">**RpcProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-419">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24c06-419">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-420">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-420">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-421">RPC-Protokoll oder-Protokolle, über die administrative RPC ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-421">RPC protocol or protocols over which administrative RPC runs.</span></span> <span data-ttu-id="24c06-422">Der folgende Algorithmus wird verwendet, um einen bestimmten Wert zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="24c06-422">The following algorithm is used to assign a specific value:</span></span>



| <span data-ttu-id="24c06-423">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-423">Value</span></span>                                                                                                | <span data-ttu-id="24c06-424">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24c06-424">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="24c06-425"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-425"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="24c06-426">Keine</span><span class="sxs-lookup"><span data-stu-id="24c06-426">None</span></span><br/>        |
| <span id="1"></span><dl> <span data-ttu-id="24c06-427"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-427"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24c06-428">TCP</span><span class="sxs-lookup"><span data-stu-id="24c06-428">TCP</span></span><br/>         |
| <span id="2"></span><dl> <span data-ttu-id="24c06-429"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-429"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24c06-430">Named Pipes</span><span class="sxs-lookup"><span data-stu-id="24c06-430">Named Pipes</span></span><br/> |
| <span id="4"></span><dl> <span data-ttu-id="24c06-431"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-431"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24c06-432">LPC</span><span class="sxs-lookup"><span data-stu-id="24c06-432">LPC</span></span><br/>         |



 

<span data-ttu-id="24c06-433">Die Summe der Werte gibt die verwendeten Protokolle an.</span><span class="sxs-lookup"><span data-stu-id="24c06-433">The sum of the values indicates the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-434">**ScavengingInterval**</span><span class="sxs-lookup"><span data-stu-id="24c06-434">**ScavengingInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-435">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-435">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-436">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-436">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-437">Intervall (in Stunden) zwischen zwei aufeinander folgenden Bereinigung-Vorgängen, die vom DNS-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-437">Interval, in hours, between two consecutive scavenging operations performed by the DNS Server.</span></span> <span data-ttu-id="24c06-438">NULL gibt an, dass das Bereinigung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-438">Zero indicates scavenging is disabled.</span></span> <span data-ttu-id="24c06-439">Der Standardwert ist 168 Stunden (sieben Tage).</span><span class="sxs-lookup"><span data-stu-id="24c06-439">The default value is 168 hours (seven days).</span></span>

</dd> <dt>

<span data-ttu-id="24c06-440">**Secureresponses**</span><span class="sxs-lookup"><span data-stu-id="24c06-440">**SecureResponses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-441">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-441">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-442">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-442">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-443">Gibt an, ob der DNS-Server exklusiv Datensätze in derselben Unterstruktur speichert wie der Server, von dem Sie bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c06-443">Indicates whether the DNS Server exclusively saves records of names in the same subtree as the server that provided them.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-444">**SendPort**</span><span class="sxs-lookup"><span data-stu-id="24c06-444">**SendPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-445">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-446">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-446">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-447">Port, an den der DNS-Server UDP-Abfragen an andere Server sendet.</span><span class="sxs-lookup"><span data-stu-id="24c06-447">Port on which the DNS Server sends UDP queries to other servers.</span></span> <span data-ttu-id="24c06-448">Standardmäßig sendet der DNS-Server Abfragen an einen Socket, der an den DNS-Port gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="24c06-448">By default, the DNS Server sends queries on a socket bound to the DNS port.</span></span>

<span data-ttu-id="24c06-449">In bestimmten Situationen ist dies nicht die beste Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="24c06-449">Under certain situations, this is not the best configuration.</span></span> <span data-ttu-id="24c06-450">Ein offensichtlicher Fall ist, wenn ein Administrator den DNS-Port mit einer Firewall blockiert, um den externen Zugriff auf den DNS-Server zu verhindern, der Server jedoch weiterhin in der Lage sein soll, eine Verbindung mit den Internet-DNS-Servern aufzunehmen, um die Namensauflösung für interne Clients</span><span class="sxs-lookup"><span data-stu-id="24c06-450">One obvious case is when an administrator blocks the DNS port with a firewall to prevent outside access to the DNS Server, but still wants the server to be able to contact Internet DNS Servers to provide name resolution for internal clients.</span></span> <span data-ttu-id="24c06-451">Ein weiterer Fall ist, wenn der DNS-Server nicht zusammenhängende Netze unterstützt (die Eigenschaft **disjointnets** , die auf true festgelegt ist, identifiziert dieses Szenario).</span><span class="sxs-lookup"><span data-stu-id="24c06-451">Another case is when the DNS Server is supporting disjoint nets (the property **DisjointNets** set to TRUE identifies this scenario).</span></span> <span data-ttu-id="24c06-452">In diesen Fällen weist das Festlegen der **sendonnondnsport** -Eigenschaft auf einen Wert ungleich NULL den DNS-Server an, an einen beliebigen Port für das Senden an Remote-DNS-Server zu binden.</span><span class="sxs-lookup"><span data-stu-id="24c06-452">In these cases, setting the **SendOnNonDnsPort** property to a nonzero value directs the DNS Server to bind to an arbitrary port for sending to remote DNS Servers.</span></span>

<span data-ttu-id="24c06-453">Wenn der **sendonnondnsport** -Wert größer als 1024 ist, bindet der DNS-Server explizit an den angegebenen Portwert.</span><span class="sxs-lookup"><span data-stu-id="24c06-453">If the **SendOnNonDnsPort** value is greater than 1024, the DNS Server binds explicitly to the port value given.</span></span> <span data-ttu-id="24c06-454">Diese Konfigurationsoption ist nützlich, wenn ein Administrator den DNS-abfrageport zu firewallzwecken korrigieren muss.</span><span class="sxs-lookup"><span data-stu-id="24c06-454">This configuration option is useful when an administrator needs to fix the DNS query port for firewall purposes.</span></span>

<span data-ttu-id="24c06-455">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="24c06-455">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="24c06-456">Das Festlegen der sendport-Eigenschaft auf einen Wert ungleich 0 (null) bewirkt, dass der DNS-Server an einen beliebigen Port zum Senden an Remote-DNS-Server gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="24c06-456">Setting the SendPort property to a non-zero value causes the DNS server to bind to an arbitrary port for sending to remote DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-457">**Serveradressen**</span><span class="sxs-lookup"><span data-stu-id="24c06-457">**ServerAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-458">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="24c06-458">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24c06-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c06-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24c06-460">Listet die IP-Adressen für den DNS-Server auf.</span><span class="sxs-lookup"><span data-stu-id="24c06-460">Enumerates the list of IP addresses for the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-461">**Strictfile-paramesing**</span><span class="sxs-lookup"><span data-stu-id="24c06-461">**StrictFileParsing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-462">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-462">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-463">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-463">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-464">Gibt an, ob [*Zonendateien*](z-gly.md) vom DNS-Server strikt analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="24c06-464">Indicates whether the DNS Server parses [*zone files*](z-gly.md) strictly.</span></span> <span data-ttu-id="24c06-465">Wenn Sie nicht definiert oder NULL ist, protokolliert der Server ungültige Daten in der Zonendatei und ignoriert diese, und die Daten werden weiterhin geladen.</span><span class="sxs-lookup"><span data-stu-id="24c06-465">If undefined or zero, the server will log and ignore bad data in the zone file and continue to load.</span></span> <span data-ttu-id="24c06-466">Wenn der Wert ungleich NULL ist, protokolliert der Server Fehler bei Zonendateien und schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="24c06-466">If nonzero, the server will log and fail on zone file errors.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-467">**Update Options**</span><span class="sxs-lookup"><span data-stu-id="24c06-467">**UpdateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-468">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c06-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24c06-470">Schränkt den Typ der Datensätze ein, die auf dem Server dynamisch aktualisiert werden können, und wird zusätzlich zu den **AllowUpdate** -Einstellungen auf Server-und Zonen Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c06-470">Restricts the type of records that can be dynamically updated on the server, used in addition to the **AllowUpdate** settings on Server and Zone objects.</span></span>

<span data-ttu-id="24c06-471">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="24c06-471">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="24c06-472">0: keine Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="24c06-472">0: No restrictions.</span></span>

<span data-ttu-id="24c06-473">1: dynamische Updates von SOA-Datensätzen nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="24c06-473">1: Do not allow dynamic updates of SOA records.</span></span>

<span data-ttu-id="24c06-474">2: lassen Sie keine dynamischen Updates von NS-Datensätzen am Zonen Stamm zu.</span><span class="sxs-lookup"><span data-stu-id="24c06-474">2: Do not allow dynamic updates of NS records at the zone root.</span></span>

<span data-ttu-id="24c06-475">4: lassen Sie keine dynamischen Updates von NS-Einträgen zu, die sich nicht im Zonen Stamm befinden (Delegierung NS-Einträge).</span><span class="sxs-lookup"><span data-stu-id="24c06-475">4: Do not allow dynamic updates of NS records not at the zone root (delegation NS records).</span></span>

<span data-ttu-id="24c06-476">Addieren Sie diese Werte, um den Einstellungs Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="24c06-476">Sum these values to determine the setting value.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-477">**Version**</span><span class="sxs-lookup"><span data-stu-id="24c06-477">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-478">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c06-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24c06-480">Version des DNS-Servers.</span><span class="sxs-lookup"><span data-stu-id="24c06-480">Version of the DNS Server.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-481">**Schreib Autorität**</span><span class="sxs-lookup"><span data-stu-id="24c06-481">**WriteAuthorityNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-482">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-483">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-483">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-484">Gibt an, ob der DNS-Server bei erfolgreicher Antwort NS-und SOA-Einträge in den Autorisierungs Abschnitt schreibt.</span><span class="sxs-lookup"><span data-stu-id="24c06-484">Specifies whether the DNS Server writes NS and SOA records to the authority section on successful response.</span></span>

</dd> <dt>

<span data-ttu-id="24c06-485">**Xfrconnecttimeout**</span><span class="sxs-lookup"><span data-stu-id="24c06-485">**XfrConnectTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c06-486">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24c06-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24c06-487">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c06-487">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24c06-488">Die Zeit in Sekunden, während der der DNS-Server auf eine erfolgreiche TCP-Verbindung mit einem Remote Server wartet, wenn eine Zonen Übertragung versucht wird.</span><span class="sxs-lookup"><span data-stu-id="24c06-488">Time, in seconds, the DNS Server waits for a successful TCP connection to a remote server when attempting a zone transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24c06-489">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24c06-489">Requirements</span></span>



| <span data-ttu-id="24c06-490">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24c06-490">Requirement</span></span> | <span data-ttu-id="24c06-491">Wert</span><span class="sxs-lookup"><span data-stu-id="24c06-491">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24c06-492">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24c06-492">Minimum supported client</span></span><br/> | <span data-ttu-id="24c06-493">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24c06-493">None supported</span></span><br/>                                                              |
| <span data-ttu-id="24c06-494">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24c06-494">Minimum supported server</span></span><br/> | <span data-ttu-id="24c06-495">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24c06-495">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24c06-496">Namespace</span><span class="sxs-lookup"><span data-stu-id="24c06-496">Namespace</span></span><br/>                | <span data-ttu-id="24c06-497">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="24c06-497">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="24c06-498">MOF</span><span class="sxs-lookup"><span data-stu-id="24c06-498">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24c06-499"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24c06-499"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c06-500">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24c06-500">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c06-501">**Start Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="24c06-501">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="24c06-502">**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="24c06-502">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="24c06-503">**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="24c06-503">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="24c06-504">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**</span><span class="sxs-lookup"><span data-stu-id="24c06-504">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





