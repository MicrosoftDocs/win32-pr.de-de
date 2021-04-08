---
title: Win32_TSVmMetadataItem-Klasse
description: Stellt ein Metadatenelement für einen Remotedesktop virtuellen Computer dar.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataItem-Klasse Remotedesktopdienste
- Win32_TSVmMetadataItem Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949475"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="aa37a-105">Win32- \_ TSVmMetadataItem-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa37a-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="aa37a-106">Stellt ein Metadatenelement für einen Remotedesktop virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="aa37a-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="aa37a-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa37a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa37a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa37a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="aa37a-109">Member</span><span class="sxs-lookup"><span data-stu-id="aa37a-109">Members</span></span>

<span data-ttu-id="aa37a-110">Die **Win32- \_ TSVmMetadataItem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa37a-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="aa37a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa37a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa37a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa37a-112">Properties</span></span>

<span data-ttu-id="aa37a-113">Die **Win32- \_ TSVmMetadataItem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa37a-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa37a-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aa37a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="aa37a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa37a-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="aa37a-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa37a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa37a-123">Description of the object.</span></span>

<span data-ttu-id="aa37a-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa37a-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa37a-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="aa37a-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa37a-129">The date the object was installed.</span></span> <span data-ttu-id="aa37a-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa37a-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="aa37a-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa37a-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa37a-135">The name of the object.</span></span>

<span data-ttu-id="aa37a-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-137">**SectionID**</span><span class="sxs-lookup"><span data-stu-id="aa37a-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="aa37a-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa37a-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-141">Gibt den Abschnitt innerhalb der Metadaten an, in denen sich dieses Element befindet.</span><span class="sxs-lookup"><span data-stu-id="aa37a-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="aa37a-142">0</span><span class="sxs-lookup"><span data-stu-id="aa37a-142">0</span></span>
</dt> <dd>

<span data-ttu-id="aa37a-143">Konfigurations Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-144">1</span><span class="sxs-lookup"><span data-stu-id="aa37a-144">1</span></span>
</dt> <dd>

<span data-ttu-id="aa37a-145">Bereich "Aufklärungs Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="aa37a-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa37a-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="aa37a-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-149">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="aa37a-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-150">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa37a-150">Current status of the object.</span></span> <span data-ttu-id="aa37a-151">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa37a-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aa37a-152">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="aa37a-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aa37a-153">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="aa37a-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aa37a-154">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa37a-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aa37a-155">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="aa37a-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aa37a-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="aa37a-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="aa37a-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="aa37a-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-158">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="aa37a-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-159">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="aa37a-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-160">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="aa37a-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="aa37a-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-162">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="aa37a-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-163">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="aa37a-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aa37a-164">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="aa37a-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa37a-165">**Wert**</span><span class="sxs-lookup"><span data-stu-id="aa37a-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aa37a-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-168">Der Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aa37a-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="aa37a-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="aa37a-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa37a-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa37a-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa37a-172">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa37a-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa37a-173">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="aa37a-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa37a-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa37a-174">Requirements</span></span>



| <span data-ttu-id="aa37a-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa37a-175">Requirement</span></span> | <span data-ttu-id="aa37a-176">Wert</span><span class="sxs-lookup"><span data-stu-id="aa37a-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa37a-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa37a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="aa37a-178">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa37a-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="aa37a-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa37a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="aa37a-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa37a-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="aa37a-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa37a-181">Namespace</span></span><br/>                | <span data-ttu-id="aa37a-182">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aa37a-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="aa37a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="aa37a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa37a-184"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="aa37a-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="aa37a-185">DLL</span><span class="sxs-lookup"><span data-stu-id="aa37a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa37a-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa37a-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

