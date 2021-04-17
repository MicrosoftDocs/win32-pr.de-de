---
description: Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Targetforwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522907"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="446f9-103">Targetforwarding-Klasse</span><span class="sxs-lookup"><span data-stu-id="446f9-103">TargetForwarding class</span></span>

<span data-ttu-id="446f9-104">Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="446f9-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="446f9-105">Auf einem Bereitstellungs Zielcomputer können mehrere Weiterleitungen konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="446f9-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="446f9-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="446f9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="446f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="446f9-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a><span data-ttu-id="446f9-108">Member</span><span class="sxs-lookup"><span data-stu-id="446f9-108">Members</span></span>

<span data-ttu-id="446f9-109">Die **targetforwarding** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="446f9-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="446f9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="446f9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="446f9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="446f9-111">Properties</span></span>

<span data-ttu-id="446f9-112">Die **targetforwarding** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="446f9-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="446f9-113">**Collector Endpoint**</span><span class="sxs-lookup"><span data-stu-id="446f9-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-116">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-117">Die Endpunkt Informationen des Collector-Servers.</span><span class="sxs-lookup"><span data-stu-id="446f9-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="446f9-118">Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.</span><span class="sxs-lookup"><span data-stu-id="446f9-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-119">**Computer**</span><span class="sxs-lookup"><span data-stu-id="446f9-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-122">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-123">Der Computername des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="446f9-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-124">**Connectedsince**</span><span class="sxs-lookup"><span data-stu-id="446f9-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-125">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="446f9-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-127">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-128">Der Zeitstempel, der angibt, wann die Verbindung für die Weiterleitungs Daten hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="446f9-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-129">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="446f9-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-132">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-133">Das Ziel der Weiterleitungs Daten, z. b. ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="446f9-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-134">**Destinationpattern**</span><span class="sxs-lookup"><span data-stu-id="446f9-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-137">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-138">Das Format, das verwendet wird, um das Ziel der Weiterleitungs Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="446f9-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-139">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="446f9-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-142">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-143">Eine Fehlermeldung, in der ein aufgetretene Fehler beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="446f9-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="446f9-144">Diese Eigenschaft ist leer, wenn kein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="446f9-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-145">**Weiterforwardertyp**</span><span class="sxs-lookup"><span data-stu-id="446f9-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-148">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-149">Der Dateityp, der die Weiterleitungs Daten enthält, z. b. ETL.</span><span class="sxs-lookup"><span data-stu-id="446f9-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-150">**Targetendpoint**</span><span class="sxs-lookup"><span data-stu-id="446f9-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-153">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-154">Die Endpunkt Informationen des Ziel Computers in einem von menschenlesbaren Format.</span><span class="sxs-lookup"><span data-stu-id="446f9-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="446f9-155">Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.</span><span class="sxs-lookup"><span data-stu-id="446f9-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="446f9-156">Beispiel: "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="446f9-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="446f9-157">**Targetguid**</span><span class="sxs-lookup"><span data-stu-id="446f9-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-160">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-161">Die SMBIOS- **GUID** des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="446f9-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="446f9-162">**Targetmac**</span><span class="sxs-lookup"><span data-stu-id="446f9-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446f9-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="446f9-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446f9-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="446f9-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446f9-165">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="446f9-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="446f9-166">Die Mac-Adresse des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="446f9-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="446f9-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="446f9-167">Requirements</span></span>



| <span data-ttu-id="446f9-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="446f9-168">Requirement</span></span> | <span data-ttu-id="446f9-169">Wert</span><span class="sxs-lookup"><span data-stu-id="446f9-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="446f9-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="446f9-170">Minimum supported client</span></span><br/> | <span data-ttu-id="446f9-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="446f9-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="446f9-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="446f9-172">Minimum supported server</span></span><br/> | <span data-ttu-id="446f9-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="446f9-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="446f9-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="446f9-174">Namespace</span></span><br/>                | <span data-ttu-id="446f9-175">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="446f9-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="446f9-176">MOF</span><span class="sxs-lookup"><span data-stu-id="446f9-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="446f9-177"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="446f9-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="446f9-178">DLL</span><span class="sxs-lookup"><span data-stu-id="446f9-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="446f9-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="446f9-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="446f9-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="446f9-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446f9-181">WMI-Anbieter für Start Ereignis Sammler</span><span class="sxs-lookup"><span data-stu-id="446f9-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

