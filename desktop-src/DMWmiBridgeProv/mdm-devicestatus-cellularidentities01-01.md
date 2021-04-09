---
title: MDM_DeviceStatus_CellularIdentities01_01-Klasse
description: Mithilfe der Klasse "MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01" können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- MDM_DeviceStatus_CellularIdentities01_01-Klasse
- MDM_DeviceStatus_CellularIdentities01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859090"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="2896f-105">MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="2896f-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="2896f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2896f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2896f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2896f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2896f-108">Mithilfe der Klasse " **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** " können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.</span><span class="sxs-lookup"><span data-stu-id="2896f-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="2896f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2896f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2896f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2896f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="2896f-111">Member</span><span class="sxs-lookup"><span data-stu-id="2896f-111">Members</span></span>

<span data-ttu-id="2896f-112">Die **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2896f-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2896f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2896f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2896f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2896f-114">Properties</span></span>

<span data-ttu-id="2896f-115">Die **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2896f-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2896f-116">Commercializationoperator</span><span class="sxs-lookup"><span data-stu-id="2896f-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2896f-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="2896f-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2896f-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="2896f-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2896f-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2896f-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2896f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2896f-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2896f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2896f-129">Knoten für Abfragen auf SIM-Karten.</span><span class="sxs-lookup"><span data-stu-id="2896f-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="2896f-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2896f-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2896f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2896f-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2896f-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2896f-134">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2896f-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="2896f-135">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="2896f-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="2896f-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2896f-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2896f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2896f-139">Roamingcompliance</span><span class="sxs-lookup"><span data-stu-id="2896f-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2896f-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2896f-142">Roamingstatus</span><span class="sxs-lookup"><span data-stu-id="2896f-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2896f-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2896f-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2896f-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2896f-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2896f-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2896f-145">Requirements</span></span>



| <span data-ttu-id="2896f-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2896f-146">Requirement</span></span> | <span data-ttu-id="2896f-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2896f-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2896f-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2896f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2896f-149">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2896f-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2896f-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2896f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2896f-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2896f-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2896f-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="2896f-152">Namespace</span></span><br/>                | <span data-ttu-id="2896f-153">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2896f-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2896f-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2896f-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2896f-155"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2896f-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2896f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="2896f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2896f-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2896f-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2896f-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2896f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2896f-159">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2896f-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

