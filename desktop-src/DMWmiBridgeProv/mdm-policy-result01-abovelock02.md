---
title: MDM_Policy_Result01_AboveLock02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ AboveLock02-Klasse stellt Richtlinien dar, die Aktionen bestimmen, die über dem Geräte Sperrbildschirm zulässig sind.
ms.assetid: 0b6d4083-2484-450b-9261-5ef339db4707
keywords:
- MDM_Policy_Result01_AboveLock02-Klasse
- MDM_Policy_Result01_AboveLock02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02.InstanceID
- MDM_Policy_Result01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530ed3c4afd3b6e888ee77d0963881c2b4d5ef93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956530"
---
# <a name="mdm_policy_result01_abovelock02-class"></a><span data-ttu-id="dd2ec-105">MDM- \_ Richtlinie \_ Result01 \_ AboveLock02-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd2ec-105">MDM\_Policy\_Result01\_AboveLock02 class</span></span>

<span data-ttu-id="dd2ec-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd2ec-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dd2ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd2ec-108">Die **MDM- \_ Richtlinie \_ Result01 \_ AboveLock02** -Klasse stellt Richtlinien dar, die Aktionen bestimmen, die über dem Geräte Sperrbildschirm zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-108">The **MDM\_Policy\_Result01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="dd2ec-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2ec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2ec-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="dd2ec-111">Member</span><span class="sxs-lookup"><span data-stu-id="dd2ec-111">Members</span></span>

<span data-ttu-id="dd2ec-112">Die **MDM- \_ Richtlinie \_ Result01 \_ AboveLock02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd2ec-112">The **MDM\_Policy\_Result01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="dd2ec-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd2ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd2ec-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd2ec-114">Properties</span></span>

<span data-ttu-id="dd2ec-115">Die **MDM- \_ Richtlinie \_ Result01 \_ AboveLock02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-115">The **MDM\_Policy\_Result01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd2ec-116">Allowcortanaabovelock</span><span class="sxs-lookup"><span data-stu-id="dd2ec-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2ec-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd2ec-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd2ec-119">Allow-UPS</span><span class="sxs-lookup"><span data-stu-id="dd2ec-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2ec-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd2ec-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd2ec-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2ec-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd2ec-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2ec-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd2ec-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="dd2ec-127">Für diese Klasse ist die Zeichenfolge "abovelock".</span><span class="sxs-lookup"><span data-stu-id="dd2ec-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="dd2ec-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2ec-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd2ec-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2ec-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2ec-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd2ec-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="dd2ec-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="dd2ec-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="dd2ec-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2ec-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd2ec-134">Requirements</span></span>



| <span data-ttu-id="dd2ec-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd2ec-135">Requirement</span></span> | <span data-ttu-id="dd2ec-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dd2ec-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2ec-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd2ec-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2ec-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2ec-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd2ec-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd2ec-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2ec-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd2ec-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd2ec-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd2ec-141">Namespace</span></span><br/>                | <span data-ttu-id="dd2ec-142">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dd2ec-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="dd2ec-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dd2ec-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd2ec-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd2ec-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd2ec-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2ec-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2ec-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2ec-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2ec-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd2ec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2ec-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="dd2ec-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

