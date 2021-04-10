---
title: MDM_SharedPC-Klasse
description: Die MDM \_ sharedpc-Klasse wird verwendet, um Einstellungen für die Verwendung von freigegebenen PCs zu konfigurieren.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- MDM_SharedPC-Klasse
- MDM_SharedPC-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040138"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="1b652-105">MDM \_ sharedpc-Klasse</span><span class="sxs-lookup"><span data-stu-id="1b652-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="1b652-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b652-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1b652-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1b652-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1b652-108">Die MDM \_ sharedpc-Klasse wird verwendet, um Einstellungen für die Verwendung von freigegebenen PCs zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1b652-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="1b652-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1b652-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b652-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b652-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="1b652-111">Member</span><span class="sxs-lookup"><span data-stu-id="1b652-111">Members</span></span>

<span data-ttu-id="1b652-112">Die **MDM \_ sharedpc** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1b652-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="1b652-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b652-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b652-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1b652-114">Properties</span></span>

<span data-ttu-id="1b652-115">Die **MDM \_ sharedpc** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1b652-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1b652-116">Accountmodel</span><span class="sxs-lookup"><span data-stu-id="1b652-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-119">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b652-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-123">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-124">Disklevelcaching</span><span class="sxs-lookup"><span data-stu-id="1b652-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-125">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-127">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-128">Disklevellösch</span><span class="sxs-lookup"><span data-stu-id="1b652-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-131">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-132">Enableaccountmanager</span><span class="sxs-lookup"><span data-stu-id="1b652-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-135">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="1b652-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-139">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-140">Inactivethreshold</span><span class="sxs-lookup"><span data-stu-id="1b652-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-143">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="1b652-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1b652-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b652-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1b652-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b652-147">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b652-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b652-148">Kioskmodeaumid</span><span class="sxs-lookup"><span data-stu-id="1b652-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b652-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-151">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-152">Kioskmudeusertiledisplaytext</span><span class="sxs-lookup"><span data-stu-id="1b652-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b652-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-155">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="1b652-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-157">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-159">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-160">Maxpagefilesizemb</span><span class="sxs-lookup"><span data-stu-id="1b652-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-161">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-163">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="1b652-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1b652-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b652-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1b652-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b652-167">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b652-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1b652-168">Restrictlocalstorage</span><span class="sxs-lookup"><span data-stu-id="1b652-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-169">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-171">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-172">""-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1b652-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-173">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-175">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-176">Setpowerpolicies</span><span class="sxs-lookup"><span data-stu-id="1b652-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-177">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-179">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-180">Signinonresume</span><span class="sxs-lookup"><span data-stu-id="1b652-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-181">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-183">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1b652-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="1b652-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b652-185">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1b652-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b652-186">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1b652-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b652-187">Weitere Informationen finden Sie unter [sharedpc CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="1b652-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b652-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b652-188">Requirements</span></span>



| <span data-ttu-id="1b652-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b652-189">Requirement</span></span> | <span data-ttu-id="1b652-190">Wert</span><span class="sxs-lookup"><span data-stu-id="1b652-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b652-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b652-191">Minimum supported client</span></span><br/> | <span data-ttu-id="1b652-192">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b652-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b652-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b652-193">Minimum supported server</span></span><br/> | <span data-ttu-id="1b652-194">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b652-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1b652-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b652-195">Namespace</span></span><br/>                | <span data-ttu-id="1b652-196">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1b652-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="1b652-197">MOF</span><span class="sxs-lookup"><span data-stu-id="1b652-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b652-198"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b652-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b652-199">DLL</span><span class="sxs-lookup"><span data-stu-id="1b652-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b652-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b652-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

