---
description: Stellt die identifizierenden Informationen zu einem Videomonitor dar, z. b. Herstellername, Jahr der Fertigung oder Seriennummer.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Wmimonitorid-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106367508"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="6424d-103">Wmimonitorid-Klasse</span><span class="sxs-lookup"><span data-stu-id="6424d-103">WmiMonitorID class</span></span>

<span data-ttu-id="6424d-104">Die **wmimonitorid-** WMI-Klasse stellt die identifizierenden Informationen zu einem Videomonitor dar, z. b. Herstellername, Jahr der Fertigung oder Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="6424d-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="6424d-105">Die Daten in dieser Klasse entsprechen den Daten im Anbieter-/Produktions-Identifikations-Block der Videoeingabe Definition des standardmäßigen Enhanced Display Identification Data (E-EDID)-Standards von Video Electronics Standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="6424d-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6424d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6424d-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="6424d-107">Member</span><span class="sxs-lookup"><span data-stu-id="6424d-107">Members</span></span>

<span data-ttu-id="6424d-108">Die **wmimonitorid-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6424d-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="6424d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6424d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6424d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6424d-110">Properties</span></span>

<span data-ttu-id="6424d-111">Die **wmimonitorid-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6424d-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6424d-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="6424d-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6424d-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="6424d-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="6424d-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6424d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6424d-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6424d-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6424d-120">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="6424d-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="6424d-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-122">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6424d-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6424d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-124">Name des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="6424d-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-125">**Manufacturernamelength**</span><span class="sxs-lookup"><span data-stu-id="6424d-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6424d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-128">Die Länge des Hersteller namens in der **ManufacturerName** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6424d-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-129">**Productcodeid**</span><span class="sxs-lookup"><span data-stu-id="6424d-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-130">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6424d-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6424d-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-132">Vom Hersteller zugewiesene Produktcode-ID.</span><span class="sxs-lookup"><span data-stu-id="6424d-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-133">**Serialzahlkennung**</span><span class="sxs-lookup"><span data-stu-id="6424d-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6424d-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6424d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-136">Seriennummer.</span><span class="sxs-lookup"><span data-stu-id="6424d-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6424d-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6424d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6424d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-140">Der Anzeige Name des Monitors.</span><span class="sxs-lookup"><span data-stu-id="6424d-140">The friendly name of the monitor.</span></span> <span data-ttu-id="6424d-141">Die Größe des Namens entspricht der Länge, die von der userfriendlynamelength-Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6424d-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-142">Userfriendlynamelength</span><span class="sxs-lookup"><span data-stu-id="6424d-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6424d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-145">Anzahl der Zeichen im Namen in der userfriendlyname-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6424d-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-146">**Weekof-Hersteller**</span><span class="sxs-lookup"><span data-stu-id="6424d-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-147">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6424d-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-149">Woche der Fertigung nach Wochen Nummer.</span><span class="sxs-lookup"><span data-stu-id="6424d-149">Week of manufacture by week number.</span></span> <span data-ttu-id="6424d-150">Der Bereich liegt zwischen 1 und 53.</span><span class="sxs-lookup"><span data-stu-id="6424d-150">The range is from 1 through 53.</span></span> <span data-ttu-id="6424d-151">NULL (0) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6424d-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="6424d-152">**Yearomamanufacturing**</span><span class="sxs-lookup"><span data-stu-id="6424d-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6424d-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6424d-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6424d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6424d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6424d-155">Jahr der Fertigung.</span><span class="sxs-lookup"><span data-stu-id="6424d-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6424d-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6424d-156">Remarks</span></span>

<span data-ttu-id="6424d-157">Eine Erläuterung dazu, wie die Arrays übersetzt werden, in denen die Seriennummern-IDs gespeichert sind, finden Sie im Artikel [Bericht über Monitor Informationen mit Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) .</span><span class="sxs-lookup"><span data-stu-id="6424d-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="6424d-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6424d-158">Examples</span></span>

<span data-ttu-id="6424d-159">Das folgende PowerShell-Beispiel ruft die Seriennummer mehrerer Monitore ab.</span><span class="sxs-lookup"><span data-stu-id="6424d-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="6424d-160">Der folgende VBScript-Code ruft außerdem Monitor-ID-Informationen von einem System ab.</span><span class="sxs-lookup"><span data-stu-id="6424d-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="6424d-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6424d-161">Requirements</span></span>



| <span data-ttu-id="6424d-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6424d-162">Requirement</span></span> | <span data-ttu-id="6424d-163">Wert</span><span class="sxs-lookup"><span data-stu-id="6424d-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6424d-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6424d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="6424d-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6424d-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6424d-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6424d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="6424d-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6424d-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6424d-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="6424d-168">Namespace</span></span><br/>                | <span data-ttu-id="6424d-169">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="6424d-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6424d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="6424d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6424d-171"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6424d-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6424d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="6424d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6424d-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6424d-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6424d-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6424d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6424d-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6424d-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

