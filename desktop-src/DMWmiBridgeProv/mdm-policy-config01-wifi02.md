---
title: MDM_Policy_Config01_WiFi02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ WiFi02-Klasse stellt die verfügbaren Wi-Fi Richtlinien dar.
ms.assetid: 68CFBB5E-F365-4D1A-8EF1-CC070E9A7982
keywords:
- MDM_Policy_Config01_WiFi02-Klasse
- MDM_Policy_Config01_WiFi02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02.InstanceID
- MDM_Policy_Config01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00848613f1f0e9fd4ab6db9dc4afdabe54ce538c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858930"
---
# <a name="mdm_policy_config01_wifi02-class"></a><span data-ttu-id="c1f19-105">MDM- \_ Richtlinie \_ Config01 \_ WiFi02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c1f19-105">MDM\_Policy\_Config01\_WiFi02 class</span></span>

<span data-ttu-id="c1f19-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c1f19-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c1f19-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c1f19-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c1f19-108">Die **MDM- \_ Richtlinie \_ Config01 \_ WiFi02** -Klasse stellt die verfügbaren Wi-Fi Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c1f19-108">The **MDM\_Policy\_Config01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="c1f19-109">Diese Richtlinien bestimmen Wi-Fi zulässigen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c1f19-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="c1f19-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c1f19-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f19-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1f19-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="c1f19-112">Member</span><span class="sxs-lookup"><span data-stu-id="c1f19-112">Members</span></span>

<span data-ttu-id="c1f19-113">Die **MDM- \_ Richtlinie \_ Config01 \_ WiFi02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c1f19-113">The **MDM\_Policy\_Config01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="c1f19-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1f19-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1f19-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1f19-115">Properties</span></span>

<span data-ttu-id="c1f19-116">Die **MDM- \_ Richtlinie \_ Config01 \_ WiFi02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1f19-116">The **MDM\_Policy\_Config01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c1f19-117">Allowautoconnecttowi-Sender-Hotspots</span><span class="sxs-lookup"><span data-stu-id="c1f19-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f19-120">Zuteilungs Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="c1f19-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f19-123">Allowmanualwifconfiguration</span><span class="sxs-lookup"><span data-stu-id="c1f19-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f19-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="c1f19-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-127">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1f19-129">Allowwifdirect</span><span class="sxs-lookup"><span data-stu-id="c1f19-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1f19-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1f19-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c1f19-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f19-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1f19-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c1f19-136">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c1f19-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="c1f19-137">Für diese Klasse ist die Zeichenfolge "WiFi".</span><span class="sxs-lookup"><span data-stu-id="c1f19-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="c1f19-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c1f19-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c1f19-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c1f19-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1f19-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c1f19-142">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c1f19-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="c1f19-143">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="c1f19-143">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="c1f19-144">Wlanscanmode</span><span class="sxs-lookup"><span data-stu-id="c1f19-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1f19-145">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1f19-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1f19-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c1f19-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1f19-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1f19-147">Requirements</span></span>



| <span data-ttu-id="c1f19-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1f19-148">Requirement</span></span> | <span data-ttu-id="c1f19-149">Wert</span><span class="sxs-lookup"><span data-stu-id="c1f19-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f19-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1f19-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f19-151">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1f19-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1f19-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1f19-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f19-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1f19-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c1f19-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1f19-154">Namespace</span></span><br/>                | <span data-ttu-id="c1f19-155">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c1f19-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c1f19-156">MOF</span><span class="sxs-lookup"><span data-stu-id="c1f19-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1f19-157"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c1f19-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1f19-158">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f19-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1f19-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f19-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1f19-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1f19-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f19-161">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c1f19-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

