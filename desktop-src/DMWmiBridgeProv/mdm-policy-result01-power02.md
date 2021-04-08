---
title: MDM_Policy_Result01_Power02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Power02-Klasse stellt die Energierichtlinien dar.
ms.assetid: 1458228f-f442-4fd4-b402-e0a4c06ecaa5
keywords:
- MDM_Policy_Result01_Power02-Klasse
- MDM_Policy_Result01_Power02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Power02
- MDM_Policy_Result01_Power02.InstanceID
- MDM_Policy_Result01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91635811e876500cb4d3df792067b1eba3d861b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949541"
---
# <a name="mdm_policy_result01_power02-class"></a><span data-ttu-id="6961b-105">MDM- \_ Richtlinie \_ Result01 \_ Power02-Klasse</span><span class="sxs-lookup"><span data-stu-id="6961b-105">MDM\_Policy\_Result01\_Power02 class</span></span>

<span data-ttu-id="6961b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6961b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6961b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6961b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6961b-108">Die MDM- \_ Richtlinie \_ Result01 \_ Power02-Klasse stellt die Energierichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="6961b-108">The MDM\_Policy\_Result01\_Power02 class represents the power policies.</span></span>

<span data-ttu-id="6961b-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6961b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6961b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6961b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="6961b-111">Member</span><span class="sxs-lookup"><span data-stu-id="6961b-111">Members</span></span>

<span data-ttu-id="6961b-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Power02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6961b-112">The **MDM\_Policy\_Result01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="6961b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6961b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6961b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6961b-114">Properties</span></span>

<span data-ttu-id="6961b-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Power02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6961b-115">The **MDM\_Policy\_Result01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6961b-116">Allowstandbywhensleepingpluggedin</span><span class="sxs-lookup"><span data-stu-id="6961b-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-119">Display offtimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="6961b-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-122">Displayofftimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="6961b-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-125">Hibernatetimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="6961b-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-128">Hibernatetimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="6961b-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6961b-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6961b-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6961b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6961b-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6961b-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6961b-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6961b-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6961b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6961b-138">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6961b-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-139">Requirements Password-computerwakesonakku</span><span class="sxs-lookup"><span data-stu-id="6961b-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-142">Requirements Password-computerwakespluggedin</span><span class="sxs-lookup"><span data-stu-id="6961b-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-145">Standbytimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="6961b-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6961b-148">Standbytimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="6961b-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6961b-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6961b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6961b-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6961b-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6961b-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6961b-151">Requirements</span></span>



| <span data-ttu-id="6961b-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6961b-152">Requirement</span></span> | <span data-ttu-id="6961b-153">Wert</span><span class="sxs-lookup"><span data-stu-id="6961b-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6961b-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6961b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6961b-155">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6961b-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6961b-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6961b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6961b-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6961b-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6961b-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="6961b-158">Namespace</span></span><br/>                | <span data-ttu-id="6961b-159">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6961b-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6961b-160">MOF</span><span class="sxs-lookup"><span data-stu-id="6961b-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6961b-161"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6961b-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6961b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6961b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6961b-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6961b-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

