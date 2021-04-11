---
title: MDM_Policy_Config01_Bluetooth02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Bluetooth02-Klasse stellt die verfügbaren Bluetooth-Verwaltungsrichtlinien dar.
ms.assetid: 8544c8df-a57b-4e21-87ee-f819aeddc071
keywords:
- MDM_Policy_Config01_Bluetooth02-Klasse
- MDM_Policy_Config01_Bluetooth02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Bluetooth02
- MDM_Policy_Config01_Bluetooth02.InstanceID
- MDM_Policy_Config01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceeea1cd099fa00d6138a0ff1d37123725f0be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103318"
---
# <a name="mdm_policy_config01_bluetooth02-class"></a><span data-ttu-id="2ce72-105">MDM- \_ Richtlinie \_ Config01 \_ Bluetooth02-Klasse</span><span class="sxs-lookup"><span data-stu-id="2ce72-105">MDM\_Policy\_Config01\_Bluetooth02 class</span></span>

<span data-ttu-id="2ce72-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2ce72-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ce72-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2ce72-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ce72-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Bluetooth02** -Klasse stellt die verfügbaren Bluetooth-Verwaltungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="2ce72-108">The **MDM\_Policy\_Config01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="2ce72-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2ce72-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce72-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ce72-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="2ce72-111">Member</span><span class="sxs-lookup"><span data-stu-id="2ce72-111">Members</span></span>

<span data-ttu-id="2ce72-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Bluetooth02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2ce72-112">The **MDM\_Policy\_Config01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="2ce72-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ce72-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ce72-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ce72-114">Properties</span></span>

<span data-ttu-id="2ce72-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Bluetooth02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ce72-115">The **MDM\_Policy\_Config01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2ce72-116">Allowadvertising</span><span class="sxs-lookup"><span data-stu-id="2ce72-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2ce72-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2ce72-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2ce72-119">Allowdiscoverablemode</span><span class="sxs-lookup"><span data-stu-id="2ce72-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2ce72-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2ce72-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2ce72-122">Allowprekopplung</span><span class="sxs-lookup"><span data-stu-id="2ce72-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2ce72-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2ce72-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ce72-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2ce72-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ce72-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ce72-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ce72-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ce72-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2ce72-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="2ce72-130">Für diese Klasse ist die Zeichenfolge "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="2ce72-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="2ce72-131">Localdevicename</span><span class="sxs-lookup"><span data-stu-id="2ce72-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ce72-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2ce72-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ce72-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2ce72-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ce72-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2ce72-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ce72-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ce72-138">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2ce72-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="2ce72-139">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="2ce72-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="2ce72-140">Serviceszulistliste</span><span class="sxs-lookup"><span data-stu-id="2ce72-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ce72-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2ce72-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ce72-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2ce72-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ce72-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ce72-143">Requirements</span></span>



| <span data-ttu-id="2ce72-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ce72-144">Requirement</span></span> | <span data-ttu-id="2ce72-145">Wert</span><span class="sxs-lookup"><span data-stu-id="2ce72-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce72-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ce72-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce72-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ce72-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ce72-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ce72-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce72-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2ce72-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2ce72-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ce72-150">Namespace</span></span><br/>                | <span data-ttu-id="2ce72-151">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2ce72-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2ce72-152">MOF</span><span class="sxs-lookup"><span data-stu-id="2ce72-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ce72-153"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2ce72-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ce72-154">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce72-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ce72-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce72-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce72-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ce72-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce72-157">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2ce72-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

