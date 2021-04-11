---
description: Die CIM \_ memorymappedio-Klasse stellt die Computerarchitektur-e/a mit Speicher Abbild dar. Diese Klasse adressiert Arbeitsspeicher-und Port-e/a-Ressourcen.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: CIM_MemoryMappedIO-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041474"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="c3b14-104">CIM \_ memorymappedio-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3b14-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="c3b14-105">Die **CIM \_ memorymappedio** -Klasse stellt die Computerarchitektur-e/a mit Speicher Abbild dar.</span><span class="sxs-lookup"><span data-stu-id="c3b14-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="c3b14-106">Diese Klasse adressiert Arbeitsspeicher-und Port-e/a-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c3b14-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3b14-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c3b14-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c3b14-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c3b14-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c3b14-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c3b14-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c3b14-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c3b14-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b14-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3b14-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="c3b14-112">Member</span><span class="sxs-lookup"><span data-stu-id="c3b14-112">Members</span></span>

<span data-ttu-id="c3b14-113">Die **CIM \_ memorymappedio** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c3b14-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="c3b14-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3b14-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3b14-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3b14-115">Properties</span></span>

<span data-ttu-id="c3b14-116">Die **CIM \_ memorymappedio** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3b14-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3b14-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c3b14-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c3b14-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3b14-121">A short textual description of the object.</span></span>

<span data-ttu-id="c3b14-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c3b14-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-126">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3b14-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3b14-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c3b14-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c3b14-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3b14-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-132">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c3b14-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-133">Die Eigenschaft " **kreationclassname** " des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c3b14-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-137">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3b14-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-138">Die **Name** -Eigenschaft des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3b14-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-142">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c3b14-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-143">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3b14-143">A textual description of the object.</span></span>

<span data-ttu-id="c3b14-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-145">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="c3b14-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-146">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3b14-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c3b14-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-149">Endadresse der zugeordneten e/a-Vorgänge im Speicher.</span><span class="sxs-lookup"><span data-stu-id="c3b14-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="c3b14-150">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c3b14-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3b14-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-152">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3b14-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c3b14-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-155">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3b14-155">Indicates when the object was installed.</span></span> <span data-ttu-id="c3b14-156">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3b14-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c3b14-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="c3b14-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-161">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c3b14-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-162">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c3b14-162">Label by which the object is known.</span></span> <span data-ttu-id="c3b14-163">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c3b14-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c3b14-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="c3b14-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-166">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3b14-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-168">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="c3b14-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-169">Die Startadresse der von einem Speicher abgebildete e/a.</span><span class="sxs-lookup"><span data-stu-id="c3b14-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="c3b14-170">Die Eigenschaft Hardware Ressourcen Bezeichner sollte auf diesen Wert festgelegt werden, um den zugeordneten e/a-Ressourcen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3b14-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="c3b14-171">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c3b14-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c3b14-172">**Status**</span><span class="sxs-lookup"><span data-stu-id="c3b14-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3b14-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3b14-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3b14-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3b14-175">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c3b14-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c3b14-176">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="c3b14-177">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3b14-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c3b14-178">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3b14-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c3b14-179">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c3b14-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c3b14-180">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c3b14-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c3b14-181">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c3b14-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c3b14-182">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c3b14-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c3b14-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3b14-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c3b14-184">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c3b14-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c3b14-185">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c3b14-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c3b14-186">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c3b14-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c3b14-187">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c3b14-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3b14-188">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c3b14-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c3b14-189">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c3b14-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c3b14-190">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c3b14-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c3b14-191">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c3b14-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c3b14-192">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c3b14-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c3b14-193">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c3b14-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c3b14-194">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c3b14-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c3b14-195">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c3b14-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c3b14-196">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c3b14-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c3b14-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c3b14-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c3b14-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3b14-198">Remarks</span></span>

<span data-ttu-id="c3b14-199">Die **CIM-Klasse \_ memorymappedio** wird von [**CIM \_ Systemresource**](cim-systemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c3b14-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="c3b14-200">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c3b14-200">WMI does not implement this class.</span></span> <span data-ttu-id="c3b14-201">Informationen zu Klassen, die von **CIM \_ memorymappedio** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c3b14-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c3b14-202">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c3b14-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c3b14-203">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c3b14-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b14-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3b14-204">Requirements</span></span>



| <span data-ttu-id="c3b14-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3b14-205">Requirement</span></span> | <span data-ttu-id="c3b14-206">Wert</span><span class="sxs-lookup"><span data-stu-id="c3b14-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b14-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3b14-207">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b14-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3b14-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3b14-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3b14-209">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b14-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3b14-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3b14-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3b14-211">Namespace</span></span><br/>                | <span data-ttu-id="c3b14-212">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c3b14-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3b14-213">MOF</span><span class="sxs-lookup"><span data-stu-id="c3b14-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3b14-214"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3b14-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3b14-215">DLL</span><span class="sxs-lookup"><span data-stu-id="c3b14-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3b14-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3b14-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b14-217">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3b14-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b14-218">**CIM- \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="c3b14-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

