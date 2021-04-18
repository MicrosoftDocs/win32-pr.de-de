---
title: MDM_WindowsAdvancedThreatProtection-Klasse
description: Die MDM \_ windowsadvancedfixprotection-Klasse wird zum integrieren und offboarding von Endpunkten für Windows Defender Advanced Threat Protection (wdatp) verwendet.
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- MDM_WindowsAdvancedThreatProtection-Klasse
- MDM_WindowsAdvancedThreatProtection-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339354"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="48be2-105">MDM \_ windowsadvancedo Protection-Klasse</span><span class="sxs-lookup"><span data-stu-id="48be2-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="48be2-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="48be2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="48be2-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="48be2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="48be2-108">Die **MDM \_ windowsadvancedfixprotection** -Klasse wird zum integrieren und offboarding von Endpunkten für Windows Defender Advanced Threat Protection (wdatp) verwendet.</span><span class="sxs-lookup"><span data-stu-id="48be2-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="48be2-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="48be2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48be2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="48be2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="48be2-111">Member</span><span class="sxs-lookup"><span data-stu-id="48be2-111">Members</span></span>

<span data-ttu-id="48be2-112">Die **MDM \_ windowsadvancedo Protection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48be2-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="48be2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48be2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48be2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48be2-114">Properties</span></span>

<span data-ttu-id="48be2-115">Die **MDM \_ windowsadvancedo Protection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48be2-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48be2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="48be2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48be2-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48be2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48be2-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48be2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48be2-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48be2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48be2-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="48be2-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="48be2-121">Für diese Klasse lautet die Zeichenfolge "windowsadvanced-Protection".</span><span class="sxs-lookup"><span data-stu-id="48be2-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="48be2-122">Offboarding</span><span class="sxs-lookup"><span data-stu-id="48be2-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48be2-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48be2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48be2-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="48be2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="48be2-125">Onboarding</span><span class="sxs-lookup"><span data-stu-id="48be2-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48be2-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48be2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48be2-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="48be2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48be2-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="48be2-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48be2-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="48be2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48be2-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48be2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48be2-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48be2-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48be2-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="48be2-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="48be2-133">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="48be2-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48be2-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48be2-134">Requirements</span></span>



| <span data-ttu-id="48be2-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48be2-135">Requirement</span></span> | <span data-ttu-id="48be2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="48be2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48be2-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48be2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="48be2-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48be2-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48be2-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48be2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="48be2-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="48be2-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="48be2-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="48be2-141">Namespace</span></span><br/>                | <span data-ttu-id="48be2-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="48be2-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="48be2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="48be2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48be2-144"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48be2-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="48be2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="48be2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48be2-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="48be2-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48be2-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48be2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48be2-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="48be2-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

