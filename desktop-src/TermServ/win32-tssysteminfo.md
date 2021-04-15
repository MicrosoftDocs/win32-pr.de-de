---
title: Win32_TSSystemInfo-Klasse
description: Stellt den zentralisierten Veröffentlichungs Server-Informationsdienst dar.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Win32_TSSystemInfo-Klasse Remotedesktopdienste
- Win32_TSSystemInfo Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476194"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="18731-105">Win32- \_ tssysteminfo-Klasse</span><span class="sxs-lookup"><span data-stu-id="18731-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="18731-106">Stellt den zentralisierten Veröffentlichungs Server-Informationsdienst dar.</span><span class="sxs-lookup"><span data-stu-id="18731-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="18731-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18731-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18731-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="18731-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="18731-109">Member</span><span class="sxs-lookup"><span data-stu-id="18731-109">Members</span></span>

<span data-ttu-id="18731-110">Die Win32-Klasse " **\_ tssysteminfo** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18731-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="18731-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18731-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18731-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18731-112">Properties</span></span>

<span data-ttu-id="18731-113">Die **Win32 \_ tssysteminfo** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18731-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18731-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18731-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18731-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18731-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18731-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="18731-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18731-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="18731-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="18731-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18731-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18731-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18731-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18731-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18731-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18731-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18731-123">Description of the object.</span></span>

<span data-ttu-id="18731-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18731-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18731-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18731-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="18731-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18731-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18731-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="18731-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="18731-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18731-129">The date the object was installed.</span></span> <span data-ttu-id="18731-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="18731-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="18731-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18731-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18731-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="18731-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18731-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18731-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18731-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18731-135">The name of the object.</span></span>

<span data-ttu-id="18731-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18731-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18731-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="18731-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18731-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18731-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18731-140">Die Versionsnummer dieses WMI-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="18731-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="18731-141">**Rdugroup**</span><span class="sxs-lookup"><span data-stu-id="18731-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18731-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18731-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18731-144">Die Gruppe Remotedesktop Benutzer im SDDL-Format (Security Deskriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="18731-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="18731-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="18731-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18731-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18731-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18731-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18731-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18731-148">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="18731-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="18731-149">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="18731-149">Current status of the object.</span></span> <span data-ttu-id="18731-150">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="18731-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18731-151">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="18731-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18731-152">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="18731-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18731-153">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="18731-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18731-154">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="18731-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18731-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="18731-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="18731-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="18731-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-157">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="18731-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-158">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="18731-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-159">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="18731-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-160">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="18731-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-161">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="18731-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-162">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="18731-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18731-163">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="18731-163">("Service")</span></span>


<span data-ttu-id="18731-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="18731-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="18731-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18731-165">Requirements</span></span>



| <span data-ttu-id="18731-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18731-166">Requirement</span></span> | <span data-ttu-id="18731-167">Wert</span><span class="sxs-lookup"><span data-stu-id="18731-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18731-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18731-168">Minimum supported client</span></span><br/> | <span data-ttu-id="18731-169">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="18731-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="18731-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18731-170">Minimum supported server</span></span><br/> | <span data-ttu-id="18731-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18731-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="18731-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="18731-172">Namespace</span></span><br/>                | <span data-ttu-id="18731-173">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="18731-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="18731-174">MOF</span><span class="sxs-lookup"><span data-stu-id="18731-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18731-175"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18731-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="18731-176">DLL</span><span class="sxs-lookup"><span data-stu-id="18731-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18731-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18731-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

