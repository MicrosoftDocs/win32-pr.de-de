---
title: MDM_Policy_Config01_WirelessDisplay02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02-Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- MDM_Policy_Config01_WirelessDisplay02-Klasse
- MDM_Policy_Config01_WirelessDisplay02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956532"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a><span data-ttu-id="17c87-105">MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02-Klasse</span><span class="sxs-lookup"><span data-stu-id="17c87-105">MDM\_Policy\_Config01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="17c87-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="17c87-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="17c87-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="17c87-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="17c87-108">Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="17c87-108">The **MDM\_Policy\_Config01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="17c87-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="17c87-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c87-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17c87-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
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

## <a name="members"></a><span data-ttu-id="17c87-111">Member</span><span class="sxs-lookup"><span data-stu-id="17c87-111">Members</span></span>

<span data-ttu-id="17c87-112">Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17c87-112">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="17c87-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17c87-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17c87-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17c87-114">Properties</span></span>

<span data-ttu-id="17c87-115">Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17c87-115">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="17c87-116">Allowmdnsankündigung</span><span class="sxs-lookup"><span data-stu-id="17c87-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-119">Allowmdnsdiscovery</span><span class="sxs-lookup"><span data-stu-id="17c87-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-122">Allowprojectionfrompc</span><span class="sxs-lookup"><span data-stu-id="17c87-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-125">Allowprojectionfrompcoverinfrastructure</span><span class="sxs-lookup"><span data-stu-id="17c87-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-128">Allowprojectiontopc</span><span class="sxs-lookup"><span data-stu-id="17c87-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-131">Allowprojectiontopcoverinfrastructure</span><span class="sxs-lookup"><span data-stu-id="17c87-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17c87-134">Zuordnung von "zugeerteninputfromwirelessdisplayreceiver"</span><span class="sxs-lookup"><span data-stu-id="17c87-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17c87-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17c87-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="17c87-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17c87-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17c87-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17c87-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17c87-141">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="17c87-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="17c87-142">Für diese Klasse ist die Zeichenfolge "wirelessdisplay".</span><span class="sxs-lookup"><span data-stu-id="17c87-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="17c87-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="17c87-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="17c87-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17c87-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17c87-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17c87-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17c87-147">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="17c87-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="17c87-148">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="17c87-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="17c87-149">Requirements pinforkopplung</span><span class="sxs-lookup"><span data-stu-id="17c87-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17c87-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17c87-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17c87-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17c87-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17c87-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17c87-152">Requirements</span></span>



| <span data-ttu-id="17c87-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17c87-153">Requirement</span></span> | <span data-ttu-id="17c87-154">Wert</span><span class="sxs-lookup"><span data-stu-id="17c87-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c87-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17c87-155">Minimum supported client</span></span><br/> | <span data-ttu-id="17c87-156">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17c87-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17c87-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17c87-157">Minimum supported server</span></span><br/> | <span data-ttu-id="17c87-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="17c87-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="17c87-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="17c87-159">Namespace</span></span><br/>                | <span data-ttu-id="17c87-160">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="17c87-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="17c87-161">MOF</span><span class="sxs-lookup"><span data-stu-id="17c87-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17c87-162"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="17c87-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="17c87-163">DLL</span><span class="sxs-lookup"><span data-stu-id="17c87-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17c87-164"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="17c87-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

