---
title: MDM_Policy_Result01_WirelessDisplay02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ WirelessDisplay02-Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.
ms.assetid: fbdfa785-8747-47b4-9802-da1c245ca222
keywords:
- MDM_Policy_Result01_WirelessDisplay02-Klasse
- MDM_Policy_Result01_WirelessDisplay02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02.InstanceID
- MDM_Policy_Result01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f4e309d1c54f12d99dfbeaa0b80807249e61fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040149"
---
# <a name="mdm_policy_result01_wirelessdisplay02-class"></a><span data-ttu-id="d5a26-105">MDM- \_ Richtlinie \_ Result01 \_ WirelessDisplay02-Klasse</span><span class="sxs-lookup"><span data-stu-id="d5a26-105">MDM\_Policy\_Result01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="d5a26-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d5a26-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d5a26-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d5a26-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d5a26-108">Die **MDM- \_ Richtlinie \_ Result01 \_ WirelessDisplay02** -Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="d5a26-108">The **MDM\_Policy\_Result01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="d5a26-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d5a26-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a26-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5a26-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="d5a26-111">Member</span><span class="sxs-lookup"><span data-stu-id="d5a26-111">Members</span></span>

<span data-ttu-id="d5a26-112">Die **MDM- \_ Richtlinie \_ Result01 \_ WirelessDisplay02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d5a26-112">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="d5a26-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5a26-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5a26-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5a26-114">Properties</span></span>

<span data-ttu-id="d5a26-115">Die **MDM- \_ Richtlinie \_ Result01 \_ WirelessDisplay02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5a26-115">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d5a26-116">Allowmdnsankündigung</span><span class="sxs-lookup"><span data-stu-id="d5a26-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-119">Allowmdnsdiscovery</span><span class="sxs-lookup"><span data-stu-id="d5a26-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-122">Allowprojectionfrompc</span><span class="sxs-lookup"><span data-stu-id="d5a26-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-125">Allowprojectionfrompcoverinfrastructure</span><span class="sxs-lookup"><span data-stu-id="d5a26-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-128">Allowprojectiontopc</span><span class="sxs-lookup"><span data-stu-id="d5a26-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-131">Allowprojectiontopcoverinfrastructure</span><span class="sxs-lookup"><span data-stu-id="d5a26-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d5a26-134">Zuordnung von "zugeerteninputfromwirelessdisplayreceiver"</span><span class="sxs-lookup"><span data-stu-id="d5a26-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d5a26-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d5a26-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d5a26-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5a26-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5a26-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5a26-141">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="d5a26-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="d5a26-142">Für diese Klasse ist die Zeichenfolge "wirelessdisplay".</span><span class="sxs-lookup"><span data-stu-id="d5a26-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="d5a26-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d5a26-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d5a26-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5a26-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5a26-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5a26-147">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d5a26-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="d5a26-148">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="d5a26-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="d5a26-149">Requirements pinforkopplung</span><span class="sxs-lookup"><span data-stu-id="d5a26-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a26-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5a26-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a26-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5a26-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5a26-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5a26-152">Requirements</span></span>



| <span data-ttu-id="d5a26-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5a26-153">Requirement</span></span> | <span data-ttu-id="d5a26-154">Wert</span><span class="sxs-lookup"><span data-stu-id="d5a26-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a26-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5a26-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a26-156">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5a26-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d5a26-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5a26-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a26-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5a26-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d5a26-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5a26-159">Namespace</span></span><br/>                | <span data-ttu-id="d5a26-160">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d5a26-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d5a26-161">MOF</span><span class="sxs-lookup"><span data-stu-id="d5a26-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5a26-162"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d5a26-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="d5a26-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a26-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a26-164"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="d5a26-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

