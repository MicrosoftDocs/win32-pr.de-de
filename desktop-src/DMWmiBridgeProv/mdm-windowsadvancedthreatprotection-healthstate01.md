---
title: MDM_WindowsAdvancedThreatProtection_HealthState01-Klasse
description: Die MDM \_ windowsadvancedfixprotection \_ HealthState01-Klasse wird verwendet, um den Integritäts Status von Windows Defender Advanced Threat Protection (wdatp)-Endpunkten zu ermitteln.
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- MDM_WindowsAdvancedThreatProtection_HealthState01-Klasse
- MDM_WindowsAdvancedThreatProtection_HealthState01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956857"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="ae79d-105">MDM \_ windowsadvancedo Protection \_ HealthState01-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae79d-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="ae79d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ae79d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ae79d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ae79d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ae79d-108">Die **MDM \_ windowsadvancedfixprotection \_ HealthState01** -Klasse wird verwendet, um den Integritäts Status von Windows Defender Advanced Threat Protection (wdatp)-Endpunkten zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ae79d-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="ae79d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ae79d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae79d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae79d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="ae79d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ae79d-111">Members</span></span>

<span data-ttu-id="ae79d-112">Die **MDM \_ windowsadvancedo Protection \_ HealthState01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ae79d-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="ae79d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae79d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae79d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae79d-114">Properties</span></span>

<span data-ttu-id="ae79d-115">Die **MDM \_ windowsadvancedbedrohlich Protection \_ HealthState01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae79d-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae79d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae79d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae79d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae79d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae79d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae79d-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ae79d-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="ae79d-121">Für diese Klasse ist die Zeichenfolge "healthstate".</span><span class="sxs-lookup"><span data-stu-id="ae79d-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="ae79d-122">Last verbunden</span><span class="sxs-lookup"><span data-stu-id="ae79d-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-123">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae79d-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae79d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ae79d-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="ae79d-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae79d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae79d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ae79d-128">Organisations</span><span class="sxs-lookup"><span data-stu-id="ae79d-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae79d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae79d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae79d-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ae79d-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae79d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae79d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae79d-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae79d-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ae79d-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="ae79d-136">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="ae79d-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="ae79d-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="ae79d-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae79d-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae79d-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae79d-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae79d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae79d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae79d-140">Requirements</span></span>



| <span data-ttu-id="ae79d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae79d-141">Requirement</span></span> | <span data-ttu-id="ae79d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ae79d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae79d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae79d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ae79d-144">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae79d-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae79d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae79d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ae79d-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ae79d-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ae79d-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae79d-147">Namespace</span></span><br/>                | <span data-ttu-id="ae79d-148">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ae79d-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ae79d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ae79d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae79d-150"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae79d-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ae79d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ae79d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae79d-152"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="ae79d-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae79d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae79d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae79d-154">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ae79d-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

