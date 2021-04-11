---
description: Aktueller Verlauf der Änderungen an den Weiterleitungs Daten für einen Bereitstellungs Zielcomputer.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Targetforwardinghistory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127772"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="5f73b-103">Targetforwardinghistory-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f73b-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="5f73b-104">Aktueller Verlauf der Änderungen an den Weiterleitungs Daten für einen Bereitstellungs Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="5f73b-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="5f73b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f73b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f73b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f73b-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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

## <a name="members"></a><span data-ttu-id="5f73b-107">Member</span><span class="sxs-lookup"><span data-stu-id="5f73b-107">Members</span></span>

<span data-ttu-id="5f73b-108">Die Klasse " **targetforwardinghistory** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f73b-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="5f73b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f73b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f73b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f73b-110">Properties</span></span>

<span data-ttu-id="5f73b-111">Die **targetforwardinghistory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f73b-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f73b-112">**Collector Endpoint**</span><span class="sxs-lookup"><span data-stu-id="5f73b-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-115">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-116">Die Endpunkt Informationen des Collector-Servers.</span><span class="sxs-lookup"><span data-stu-id="5f73b-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="5f73b-117">Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.</span><span class="sxs-lookup"><span data-stu-id="5f73b-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-118">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5f73b-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-121">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-122">Der Computername des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="5f73b-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-123">**Connectedsince**</span><span class="sxs-lookup"><span data-stu-id="5f73b-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-124">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f73b-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-126">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-127">Der Zeitstempel, der angibt, wann die Verbindung für die Weiterleitungs Daten hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f73b-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-128">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="5f73b-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-131">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-132">Das Ziel der Weiterleitungs Daten, z. b. ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="5f73b-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-133">**Destinationpattern**</span><span class="sxs-lookup"><span data-stu-id="5f73b-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-136">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-137">Das Format, das verwendet wird, um das Ziel der Weiterleitungs Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5f73b-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-138">**Disconnectedsince**</span><span class="sxs-lookup"><span data-stu-id="5f73b-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-139">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f73b-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-141">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-142">Der Zeitstempel, der angibt, wann die Verbindung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f73b-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-143">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="5f73b-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-146">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-147">Eine Fehlermeldung, in der ein aufgetretene Fehler beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f73b-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="5f73b-148">Diese Eigenschaft ist leer, wenn kein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5f73b-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-149">**Weiterforwardertyp**</span><span class="sxs-lookup"><span data-stu-id="5f73b-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-152">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-153">Der Dateityp, der die Weiterleitungs Daten enthält, z. b. ETL.</span><span class="sxs-lookup"><span data-stu-id="5f73b-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-154">**Targetendpoint**</span><span class="sxs-lookup"><span data-stu-id="5f73b-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-157">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-158">Die Endpunkt Informationen des Ziel Computers in einem von menschenlesbaren Format.</span><span class="sxs-lookup"><span data-stu-id="5f73b-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="5f73b-159">Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.</span><span class="sxs-lookup"><span data-stu-id="5f73b-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="5f73b-160">Beispiel: "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="5f73b-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-161">**Targetguid**</span><span class="sxs-lookup"><span data-stu-id="5f73b-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-164">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-165">Die SMBIOS- **GUID** des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="5f73b-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-166">**Targetmac**</span><span class="sxs-lookup"><span data-stu-id="5f73b-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f73b-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-169">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-170">Die Mac-Adresse des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="5f73b-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="5f73b-171">**Wmidatetime**</span><span class="sxs-lookup"><span data-stu-id="5f73b-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73b-172">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f73b-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73b-174">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f73b-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f73b-175">Zeitstempel für den Zeitpunkt, zu dem diese Zustandsänderung aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f73b-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f73b-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f73b-176">Requirements</span></span>



| <span data-ttu-id="5f73b-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f73b-177">Requirement</span></span> | <span data-ttu-id="5f73b-178">Wert</span><span class="sxs-lookup"><span data-stu-id="5f73b-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f73b-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f73b-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5f73b-180">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f73b-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="5f73b-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f73b-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5f73b-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5f73b-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="5f73b-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f73b-183">Namespace</span></span><br/>                | <span data-ttu-id="5f73b-184">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="5f73b-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="5f73b-185">MOF</span><span class="sxs-lookup"><span data-stu-id="5f73b-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f73b-186"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f73b-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f73b-187">DLL</span><span class="sxs-lookup"><span data-stu-id="5f73b-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f73b-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f73b-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5f73b-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f73b-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f73b-190">WMI-Anbieter für Start Ereignis Sammler</span><span class="sxs-lookup"><span data-stu-id="5f73b-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

