---
title: Win32_TSDeploymentLicensing-Klasse
description: Lizenzierungs Einstellungen für die Bereitstellung von Remotedesktop Virtualisierung (RDV).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentLicensing-Klasse Remotedesktopdienste
- Win32_TSDeploymentLicensing Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344709"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="52805-105">Win32- \_ Klasse "zdeploymentlicensing"</span><span class="sxs-lookup"><span data-stu-id="52805-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="52805-106">Lizenzierungs Einstellungen für die Bereitstellung von Remotedesktop Virtualisierung (RDV).</span><span class="sxs-lookup"><span data-stu-id="52805-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="52805-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52805-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52805-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="52805-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="52805-109">Member</span><span class="sxs-lookup"><span data-stu-id="52805-109">Members</span></span>

<span data-ttu-id="52805-110">Die Win32-Klasse " **\_ zdeploymentlicensing** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52805-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="52805-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52805-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52805-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52805-112">Properties</span></span>

<span data-ttu-id="52805-113">Die Win32-Klasse " **\_ zdeploymentlicensing** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52805-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52805-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="52805-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52805-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52805-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52805-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52805-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="52805-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="52805-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="52805-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="52805-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52805-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52805-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52805-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52805-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52805-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52805-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52805-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="52805-123">Description of the object.</span></span>

<span data-ttu-id="52805-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52805-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52805-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52805-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="52805-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52805-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52805-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52805-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="52805-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="52805-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="52805-129">The date the object was installed.</span></span> <span data-ttu-id="52805-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52805-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="52805-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52805-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52805-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="52805-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="52805-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="52805-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="52805-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52805-135">Gibt die zu verwendenden Lizenzserver an.</span><span class="sxs-lookup"><span data-stu-id="52805-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="52805-136">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="52805-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52805-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52805-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="52805-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52805-139">Lizenzierungs Modus</span><span class="sxs-lookup"><span data-stu-id="52805-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="52805-140">**Pro Gerät** (2)</span><span class="sxs-lookup"><span data-stu-id="52805-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="52805-141">**Pro Benutzer** (4)</span><span class="sxs-lookup"><span data-stu-id="52805-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="52805-142">**Noch nicht konfiguriert** (5)</span><span class="sxs-lookup"><span data-stu-id="52805-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52805-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="52805-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52805-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52805-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52805-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52805-146">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="52805-146">The name of the object.</span></span>

<span data-ttu-id="52805-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52805-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52805-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="52805-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52805-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52805-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52805-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52805-151">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="52805-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="52805-152">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="52805-152">Current status of the object.</span></span> <span data-ttu-id="52805-153">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="52805-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="52805-154">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="52805-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="52805-155">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="52805-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="52805-156">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="52805-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="52805-157">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="52805-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="52805-158">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52805-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="52805-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="52805-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-160">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="52805-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-161">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="52805-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-162">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="52805-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-163">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="52805-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-164">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="52805-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-165">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="52805-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52805-166">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="52805-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52805-167">**Usecentrallicensingsettings**</span><span class="sxs-lookup"><span data-stu-id="52805-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52805-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52805-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52805-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="52805-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52805-170">Gibt an, ob die Bereitstellungs weiten Lizenzierungs Einstellungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52805-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="52805-171">**True** , wenn diese Einstellungen für alle Server in dieser Bereitstellung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52805-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="52805-172">**false** , um Sie pro Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52805-172">**false** to set them per-server.</span></span> <span data-ttu-id="52805-173">Wenn diese Einstellung auf " **false**" festgelegt ist, werden alle anderen Lizenzierungs Einstellungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="52805-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52805-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52805-174">Requirements</span></span>



| <span data-ttu-id="52805-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52805-175">Requirement</span></span> | <span data-ttu-id="52805-176">Wert</span><span class="sxs-lookup"><span data-stu-id="52805-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52805-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52805-177">Minimum supported client</span></span><br/> | <span data-ttu-id="52805-178">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="52805-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="52805-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52805-179">Minimum supported server</span></span><br/> | <span data-ttu-id="52805-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52805-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="52805-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="52805-181">Namespace</span></span><br/>                | <span data-ttu-id="52805-182">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="52805-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="52805-183">MOF</span><span class="sxs-lookup"><span data-stu-id="52805-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52805-184"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="52805-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="52805-185">DLL</span><span class="sxs-lookup"><span data-stu-id="52805-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52805-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52805-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

