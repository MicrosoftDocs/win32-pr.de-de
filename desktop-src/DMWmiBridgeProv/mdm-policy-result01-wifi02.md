---
title: MDM_Policy_Result01_WiFi02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ WiFi02-Klasse stellt die verfügbaren Wi-Fi Richtlinien dar.
ms.assetid: 074C4428-401D-4564-B7AC-45C2221EEC3A
keywords:
- MDM_Policy_Result01_WiFi02-Klasse
- MDM_Policy_Result01_WiFi02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WiFi02
- MDM_Policy_Result01_WiFi02.InstanceID
- MDM_Policy_Result01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff9e0349f7a18da3320fab333d5b5fd36715999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949451"
---
# <a name="mdm_policy_result01_wifi02-class"></a><span data-ttu-id="08e77-105">MDM- \_ Richtlinie \_ Result01 \_ WiFi02-Klasse</span><span class="sxs-lookup"><span data-stu-id="08e77-105">MDM\_Policy\_Result01\_WiFi02 class</span></span>

<span data-ttu-id="08e77-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="08e77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08e77-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="08e77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08e77-108">Die **MDM- \_ Richtlinie \_ Result01 \_ WiFi02** -Klasse stellt die verfügbaren Wi-Fi Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="08e77-108">The **MDM\_Policy\_Result01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="08e77-109">Diese Richtlinien bestimmen Wi-Fi zulässigen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="08e77-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="08e77-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="08e77-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e77-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e77-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WiFi02
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

## <a name="members"></a><span data-ttu-id="08e77-112">Member</span><span class="sxs-lookup"><span data-stu-id="08e77-112">Members</span></span>

<span data-ttu-id="08e77-113">Die **MDM- \_ Richtlinie \_ Result01 \_ WiFi02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08e77-113">The **MDM\_Policy\_Result01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="08e77-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08e77-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08e77-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08e77-115">Properties</span></span>

<span data-ttu-id="08e77-116">Die **MDM- \_ Richtlinie \_ Result01 \_ WiFi02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08e77-116">The **MDM\_Policy\_Result01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08e77-117">Allowautoconnecttowi-Sender-Hotspots</span><span class="sxs-lookup"><span data-stu-id="08e77-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08e77-120">Zuteilungs Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="08e77-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08e77-123">Allowmanualwifconfiguration</span><span class="sxs-lookup"><span data-stu-id="08e77-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08e77-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="08e77-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-127">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08e77-129">Allowwifdirect</span><span class="sxs-lookup"><span data-stu-id="08e77-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08e77-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08e77-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08e77-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08e77-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08e77-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08e77-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08e77-136">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="08e77-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="08e77-137">Für diese Klasse ist die Zeichenfolge "WiFi".</span><span class="sxs-lookup"><span data-stu-id="08e77-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="08e77-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="08e77-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08e77-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08e77-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08e77-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08e77-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08e77-142">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="08e77-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="08e77-143">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="08e77-143">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="08e77-144">Wlanscanmode</span><span class="sxs-lookup"><span data-stu-id="08e77-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e77-145">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e77-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e77-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08e77-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08e77-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08e77-147">Requirements</span></span>



| <span data-ttu-id="08e77-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08e77-148">Requirement</span></span> | <span data-ttu-id="08e77-149">Wert</span><span class="sxs-lookup"><span data-stu-id="08e77-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e77-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08e77-150">Minimum supported client</span></span><br/> | <span data-ttu-id="08e77-151">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08e77-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08e77-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08e77-152">Minimum supported server</span></span><br/> | <span data-ttu-id="08e77-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="08e77-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08e77-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="08e77-154">Namespace</span></span><br/>                | <span data-ttu-id="08e77-155">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="08e77-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="08e77-156">MOF</span><span class="sxs-lookup"><span data-stu-id="08e77-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08e77-157"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08e77-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08e77-158">DLL</span><span class="sxs-lookup"><span data-stu-id="08e77-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08e77-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e77-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e77-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08e77-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e77-161">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="08e77-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

