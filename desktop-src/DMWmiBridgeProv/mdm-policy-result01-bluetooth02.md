---
title: MDM_Policy_Result01_Bluetooth02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Bluetooth02-Klasse stellt die verfügbaren Bluetooth-Verwaltungsrichtlinien dar.
ms.assetid: 629f2323-f6f6-4d4f-8558-9553f4dbe871
keywords:
- MDM_Policy_Result01_Bluetooth02-Klasse
- MDM_Policy_Result01_Bluetooth02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Bluetooth02
- MDM_Policy_Result01_Bluetooth02.InstanceID
- MDM_Policy_Result01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ceb0a3b7a3d2440f9769fde72c01ce4d68c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040976"
---
# <a name="mdm_policy_result01_bluetooth02-class"></a><span data-ttu-id="91ad7-105">MDM- \_ Richtlinie \_ Result01 \_ Bluetooth02-Klasse</span><span class="sxs-lookup"><span data-stu-id="91ad7-105">MDM\_Policy\_Result01\_Bluetooth02 class</span></span>

<span data-ttu-id="91ad7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="91ad7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="91ad7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="91ad7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="91ad7-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Bluetooth02** -Klasse stellt die verfügbaren Bluetooth-Verwaltungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="91ad7-108">The **MDM\_Policy\_Result01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="91ad7-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="91ad7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ad7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ad7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Bluetooth02
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

## <a name="members"></a><span data-ttu-id="91ad7-111">Member</span><span class="sxs-lookup"><span data-stu-id="91ad7-111">Members</span></span>

<span data-ttu-id="91ad7-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Bluetooth02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91ad7-112">The **MDM\_Policy\_Result01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="91ad7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91ad7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91ad7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91ad7-114">Properties</span></span>

<span data-ttu-id="91ad7-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Bluetooth02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91ad7-115">The **MDM\_Policy\_Result01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="91ad7-116">Allowadvertising</span><span class="sxs-lookup"><span data-stu-id="91ad7-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91ad7-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91ad7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91ad7-119">Allowdiscoverablemode</span><span class="sxs-lookup"><span data-stu-id="91ad7-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91ad7-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91ad7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91ad7-122">Allowprekopplung</span><span class="sxs-lookup"><span data-stu-id="91ad7-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91ad7-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91ad7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91ad7-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91ad7-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91ad7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91ad7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91ad7-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91ad7-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="91ad7-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="91ad7-130">Für diese Klasse ist die Zeichenfolge "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="91ad7-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="91ad7-131">Localdevicename</span><span class="sxs-lookup"><span data-stu-id="91ad7-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91ad7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91ad7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91ad7-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="91ad7-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91ad7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91ad7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91ad7-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91ad7-138">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="91ad7-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="91ad7-139">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="91ad7-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="91ad7-140">Serviceszulistliste</span><span class="sxs-lookup"><span data-stu-id="91ad7-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ad7-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91ad7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ad7-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91ad7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91ad7-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91ad7-143">Requirements</span></span>



| <span data-ttu-id="91ad7-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91ad7-144">Requirement</span></span> | <span data-ttu-id="91ad7-145">Wert</span><span class="sxs-lookup"><span data-stu-id="91ad7-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ad7-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91ad7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91ad7-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91ad7-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91ad7-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91ad7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91ad7-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="91ad7-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="91ad7-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="91ad7-150">Namespace</span></span><br/>                | <span data-ttu-id="91ad7-151">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="91ad7-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="91ad7-152">MOF</span><span class="sxs-lookup"><span data-stu-id="91ad7-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91ad7-153"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="91ad7-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="91ad7-154">DLL</span><span class="sxs-lookup"><span data-stu-id="91ad7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ad7-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ad7-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ad7-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91ad7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ad7-157">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="91ad7-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

