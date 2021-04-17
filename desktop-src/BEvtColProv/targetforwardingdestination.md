---
description: Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Targetforwardingdestination-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482795"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="3c3d9-104">Targetforwardingdestination-Klasse</span><span class="sxs-lookup"><span data-stu-id="3c3d9-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="3c3d9-105">Die bekannten Ziele, die die gesammelten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="3c3d9-106">Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="3c3d9-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c3d9-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="3c3d9-109">Member</span><span class="sxs-lookup"><span data-stu-id="3c3d9-109">Members</span></span>

<span data-ttu-id="3c3d9-110">Die Klasse " **targetforwardingdestination** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c3d9-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="3c3d9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c3d9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c3d9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c3d9-112">Properties</span></span>

<span data-ttu-id="3c3d9-113">Die **targetforwardingdestination** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c3d9-114">**Collector Endpoint**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-117">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-118">Der Host: Port Informationen des Endpunkts auf der Collector-Seite.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-119">**Computer**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-122">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-123">Der Name des Ziel Computers, der vom Collector entsprechend seiner Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-124">**Connectedsince**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-125">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-127">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-128">Der Zeitstempel, zu dem die Verbindung hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-129">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-132">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-133">Das Ziel der Daten.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-133">Destination of the data.</span></span> <span data-ttu-id="3c3d9-134">Die Bedeutung hängt vom Weiterleitungs Typen ab.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="3c3d9-135">Kann ein Dateiname oder ein anderer Identifizierungs-ID sein.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-136">**Destinationpattern**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-139">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-140">Muster, das verwendet wird, um das Ziel der Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="3c3d9-141">Die Bedeutung hängt von der Weiterleitungs Art und der Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="3c3d9-142">Für ein festes Ziel wäre das gleiche wie das Ziel selbst.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="3c3d9-143">Für das Ziel mit der Drehung der Dateien würde die Muster Zeichen enthalten, die durch den eigentlichen Index im Ziel ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-144">**Disconnectedsince**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-145">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-147">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-148">Zeitstempel für den Zeitpunkt, zu dem die Verbindung gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-149">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-152">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-153">Fehlermeldung, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-153">Error message if an error was encountered.</span></span> <span data-ttu-id="3c3d9-154">Andernfalls ist es leer.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-155">**Weiterforwardertyp**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-158">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-159">Der Typ der Weiterleitung (z. b. "ETL").</span><span class="sxs-lookup"><span data-stu-id="3c3d9-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-160">**Targetendpoint**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-163">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-164">Die Endpunkt Informationen des Ziel Computers in einem von menschenlesbaren Format.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="3c3d9-165">Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="3c3d9-166">Beispiel: "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="3c3d9-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-167">**Targetguid**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-170">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-171">Die SMBIOS-GUID des Ziel Computers (sofern bekannt).</span><span class="sxs-lookup"><span data-stu-id="3c3d9-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-172">**Targetmac**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-175">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-176">Die Mac-Adresse des Ziel Computers (sofern bekannt).</span><span class="sxs-lookup"><span data-stu-id="3c3d9-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="3c3d9-177">**Wmidatetime**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3d9-178">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c3d9-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c3d9-180">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c3d9-181">Zeitstempel für den Zeitpunkt, zu dem diese Zustandsänderung aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="3c3d9-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c3d9-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c3d9-182">Requirements</span></span>



| <span data-ttu-id="3c3d9-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c3d9-183">Requirement</span></span> | <span data-ttu-id="3c3d9-184">Wert</span><span class="sxs-lookup"><span data-stu-id="3c3d9-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3d9-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-185">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3d9-186">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3c3d9-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3c3d9-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c3d9-187">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3d9-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c3d9-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="3c3d9-189">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c3d9-189">Namespace</span></span><br/>                | <span data-ttu-id="3c3d9-190">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="3c3d9-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="3c3d9-191">MOF</span><span class="sxs-lookup"><span data-stu-id="3c3d9-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c3d9-192"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c3d9-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c3d9-193">DLL</span><span class="sxs-lookup"><span data-stu-id="3c3d9-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c3d9-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c3d9-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

