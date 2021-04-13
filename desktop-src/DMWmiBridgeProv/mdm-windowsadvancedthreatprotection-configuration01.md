---
title: MDM_WindowsAdvancedThreatProtection_Configuration01-Klasse
description: Die MDM \_ windowsadvancedfixprotection \_ Configuration01-Klasse wird verwendet, um die Konfiguration von Windows Defender Advanced Threat Protection-Endpunkten (wdatp) zu bestimmen.
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- MDM_WindowsAdvancedThreatProtection_Configuration01-Klasse
- MDM_WindowsAdvancedThreatProtection_Configuration01-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518425"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="b7603-105">MDM \_ windowsadvancedo Protection \_ Configuration01-Klasse</span><span class="sxs-lookup"><span data-stu-id="b7603-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="b7603-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b7603-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7603-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b7603-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7603-108">Die **MDM \_ windowsadvancedfixprotection \_ Configuration01** -Klasse wird verwendet, um die Konfiguration von Windows Defender Advanced Threat Protection-Endpunkten (wdatp) zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b7603-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="b7603-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b7603-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7603-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7603-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="b7603-111">Member</span><span class="sxs-lookup"><span data-stu-id="b7603-111">Members</span></span>

<span data-ttu-id="b7603-112">Die **MDM \_ windowsadvancedo Protection \_ Configuration01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b7603-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="b7603-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7603-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7603-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7603-114">Properties</span></span>

<span data-ttu-id="b7603-115">Die **MDM \_ windowsadvancedbedrohlich Protection \_ Configuration01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7603-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7603-116">**Gruppen**</span><span class="sxs-lookup"><span data-stu-id="b7603-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7603-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7603-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7603-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b7603-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b7603-119">TBD</span><span class="sxs-lookup"><span data-stu-id="b7603-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="b7603-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7603-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7603-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7603-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7603-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7603-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7603-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7603-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7603-124">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="b7603-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="b7603-125">Für diese Klasse ist die Zeichenfolge "Configuration".</span><span class="sxs-lookup"><span data-stu-id="b7603-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="b7603-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b7603-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7603-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b7603-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7603-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7603-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7603-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7603-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7603-130">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="b7603-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="b7603-131">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="b7603-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="b7603-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="b7603-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7603-133">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7603-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7603-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b7603-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b7603-135">Telemetryreportingfrequency</span><span class="sxs-lookup"><span data-stu-id="b7603-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7603-136">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b7603-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7603-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b7603-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7603-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7603-138">Requirements</span></span>



| <span data-ttu-id="b7603-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7603-139">Requirement</span></span> | <span data-ttu-id="b7603-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b7603-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7603-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7603-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b7603-142">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7603-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b7603-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7603-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b7603-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b7603-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b7603-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7603-145">Namespace</span></span><br/>                | <span data-ttu-id="b7603-146">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b7603-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="b7603-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b7603-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7603-148"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b7603-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="b7603-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b7603-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7603-150"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="b7603-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7603-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7603-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7603-152">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="b7603-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

