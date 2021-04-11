---
title: MDM_Policy_Config01_Power02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Power02-Klasse konfiguriert die Energierichtlinien.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- MDM_Policy_Config01_Power02-Klasse
- MDM_Policy_Config01_Power02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103615"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="ffb14-105">MDM- \_ Richtlinie \_ Config01 \_ Power02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ffb14-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="ffb14-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ffb14-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ffb14-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ffb14-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ffb14-108">Die MDM- \_ Richtlinie \_ Config01 \_ Power02-Klasse konfiguriert die Energierichtlinien.</span><span class="sxs-lookup"><span data-stu-id="ffb14-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="ffb14-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ffb14-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb14-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb14-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
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

## <a name="members"></a><span data-ttu-id="ffb14-111">Member</span><span class="sxs-lookup"><span data-stu-id="ffb14-111">Members</span></span>

<span data-ttu-id="ffb14-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Power02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ffb14-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="ffb14-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffb14-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffb14-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffb14-114">Properties</span></span>

<span data-ttu-id="ffb14-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Power02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ffb14-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ffb14-116">Allowstandbywhensleepingpluggedin</span><span class="sxs-lookup"><span data-stu-id="ffb14-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-119">Display offtimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="ffb14-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-122">Displayofftimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="ffb14-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-125">Hibernatetimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="ffb14-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-128">Hibernatetimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="ffb14-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffb14-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ffb14-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffb14-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffb14-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffb14-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ffb14-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffb14-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-138">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffb14-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-139">Requirements Password-computerwakesonakku</span><span class="sxs-lookup"><span data-stu-id="ffb14-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-142">Requirements Password-computerwakespluggedin</span><span class="sxs-lookup"><span data-stu-id="ffb14-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-145">Standbytimeoutonakku</span><span class="sxs-lookup"><span data-stu-id="ffb14-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffb14-148">Standbytimeoutpluggedin</span><span class="sxs-lookup"><span data-stu-id="ffb14-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb14-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ffb14-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffb14-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ffb14-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffb14-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffb14-151">Requirements</span></span>



| <span data-ttu-id="ffb14-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffb14-152">Requirement</span></span> | <span data-ttu-id="ffb14-153">Wert</span><span class="sxs-lookup"><span data-stu-id="ffb14-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb14-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffb14-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb14-155">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffb14-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffb14-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffb14-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb14-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ffb14-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ffb14-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffb14-158">Namespace</span></span><br/>                | <span data-ttu-id="ffb14-159">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ffb14-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ffb14-160">MOF</span><span class="sxs-lookup"><span data-stu-id="ffb14-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffb14-161"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ffb14-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffb14-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ffb14-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffb14-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffb14-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

