---
description: Die CIM \_ OperatingSystem-Klasse stellt ein Computerbetriebssystem dar, das aus Software und Firmware besteht, mit denen die Hardware eines Computer Systems verwendbar ist.
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: CIM_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523744"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="8f124-103">CIM- \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f124-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="8f124-104">Die **CIM \_ OperatingSystem** -Klasse stellt ein Computerbetriebssystem dar, das aus Software und Firmware besteht, mit denen die Hardware eines Computer Systems verwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f124-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8f124-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f124-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f124-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f124-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8f124-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f124-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8f124-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f124-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f124-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="8f124-110">Member</span><span class="sxs-lookup"><span data-stu-id="8f124-110">Members</span></span>

<span data-ttu-id="8f124-111">Die **CIM \_ OperatingSystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f124-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="8f124-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f124-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f124-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f124-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f124-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f124-114">Methods</span></span>

<span data-ttu-id="8f124-115">Die **CIM \_ OperatingSystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8f124-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="8f124-116">Methode</span><span class="sxs-lookup"><span data-stu-id="8f124-116">Method</span></span>                                                           | <span data-ttu-id="8f124-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f124-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f124-118">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="8f124-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="8f124-119">Klassenmethode, die das Computersystem herunterfährt und dann neu startet.</span><span class="sxs-lookup"><span data-stu-id="8f124-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="8f124-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f124-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="8f124-121">**Abschlusses**</span><span class="sxs-lookup"><span data-stu-id="8f124-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="8f124-122">Klassenmethode, mit der Programme und DLLs an den Punkt entladen werden, an dem Sie den Computer nicht ausschalten können.</span><span class="sxs-lookup"><span data-stu-id="8f124-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="8f124-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f124-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f124-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f124-124">Properties</span></span>

<span data-ttu-id="8f124-125">Die **CIM \_ OperatingSystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f124-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f124-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f124-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8f124-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-130">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f124-130">Short textual description of the object.</span></span>

<span data-ttu-id="8f124-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f124-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-132">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="8f124-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-135">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f124-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f124-136">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f124-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8f124-137">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8f124-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f124-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-141">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f124-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f124-142">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="8f124-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="8f124-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-146">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f124-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f124-147">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8f124-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="8f124-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-149">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="8f124-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-151">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="8f124-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-152">Die Anzahl der Minuten, für die das Betriebssystem von der Ortszeit (GMT) versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8f124-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="8f124-153">Die Zahl ist positiv, negativ oder 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8f124-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f124-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-157">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8f124-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-158">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f124-158">Textual description of the object.</span></span>

<span data-ttu-id="8f124-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f124-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-160">**Distri**</span><span class="sxs-lookup"><span data-stu-id="8f124-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-161">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f124-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f124-163">**True** gibt an, dass das Betriebssystem auf mehrere Computersystem Knoten verteilt ist, die als Cluster gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f124-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="8f124-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-165">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-167">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-168">Die Anzahl der derzeit nicht verwendeten und verfügbaren physischen Speicher in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="8f124-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="8f124-169">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-170">**Freespaceinpagingfiles**</span><span class="sxs-lookup"><span data-stu-id="8f124-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-171">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-173">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="8f124-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-174">Anzahl von Kilobyte, die in den Auslagerungs Dateien des Betriebssystems zugeordnet werden können, ohne dass andere Seiten ausgetauscht werden müssen. Der Wert 0 gibt an, dass keine Auslagerungs Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8f124-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="8f124-175">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-176">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="8f124-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-177">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-179">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-180">Anzahl von Kilobyte des virtuellen Speichers, der derzeit nicht verwendet wird und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="8f124-181">Dies kann z. b. durch Hinzufügen der Menge an freiem RAM zum Umfang des freien Speicherplatzes berechnet werden (d. h. durch das Hinzufügen der Eigenschaften **FreePhysicalMemory** und **freespaceinpagingfiles** ).</span><span class="sxs-lookup"><span data-stu-id="8f124-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="8f124-182">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f124-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-184">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f124-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-186">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8f124-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-187">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f124-187">Date and time the object was installed.</span></span> <span data-ttu-id="8f124-188">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8f124-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f124-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="8f124-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-191">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f124-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f124-193">Uhrzeit, zu der das Betriebssystem zuletzt gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f124-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="8f124-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-195">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f124-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-197">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrsystemdate "," MIF. Allgemeine Informationen zu DMTF \| \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="8f124-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-198">Das Betriebssystem Konzept für das lokale Datum und die Uhrzeit des Tages.</span><span class="sxs-lookup"><span data-stu-id="8f124-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-199">**Maxnumofprocesses**</span><span class="sxs-lookup"><span data-stu-id="8f124-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-200">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f124-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-202">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrsystemmaxprocesses ")</span><span class="sxs-lookup"><span data-stu-id="8f124-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-203">Maximale Anzahl von Prozess Kontexten, die vom Betriebssystem unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="8f124-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="8f124-204">Wenn kein festes Maximum vorhanden ist, sollte der Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8f124-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="8f124-205">Auf Systemen mit einem maximalen Höchstwert kann dieses Objekt bei der Diagnose von Fehlern helfen, die auftreten, wenn der Höchstwert erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="8f124-206">Wenn unbekannt, geben Sie-1 ein.</span><span class="sxs-lookup"><span data-stu-id="8f124-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="8f124-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-208">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-210">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-211">Maximale Anzahl von KB Arbeitsspeicher, die einem Prozess zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="8f124-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="8f124-212">Bei Betriebssystemen ohne virtuellen Arbeitsspeicher entspricht dieser Wert in der Regel der Gesamtmenge an physischem Arbeitsspeicher (abzüglich des vom BIOS und dem Betriebssystem genutzten Speichers).</span><span class="sxs-lookup"><span data-stu-id="8f124-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="8f124-213">Bei einigen Betriebssystemen kann dieser Wert unendlich sein. in diesem Fall sollte 0 eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f124-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="8f124-214">In anderen Fällen kann dieser Wert eine Konstante sein, z. b. 2 GB oder 4 GB.</span><span class="sxs-lookup"><span data-stu-id="8f124-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="8f124-215">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-216">**Name**</span><span class="sxs-lookup"><span data-stu-id="8f124-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-219">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name")</span><span class="sxs-lookup"><span data-stu-id="8f124-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-220">Der Schlüssel einer Betriebssystem Instanz innerhalb eines Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="8f124-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="8f124-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f124-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-222">**"Numoflicensedusers"**</span><span class="sxs-lookup"><span data-stu-id="8f124-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-223">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f124-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f124-225">Anzahl der Benutzerlizenzen für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="8f124-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="8f124-226">Wenn unbegrenzt, geben Sie 0 (falls unbekannt) ein, geben Sie-1 ein.</span><span class="sxs-lookup"><span data-stu-id="8f124-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-227">**Anzahlungsprozesse**</span><span class="sxs-lookup"><span data-stu-id="8f124-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-228">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f124-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-230">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrsystemprocesses ")</span><span class="sxs-lookup"><span data-stu-id="8f124-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-231">Anzahl von Prozess Kontexten, die derzeit auf dem Betriebssystem geladen oder ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8f124-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-232">**Numofusers**</span><span class="sxs-lookup"><span data-stu-id="8f124-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-233">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f124-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-235">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrsystemnumusers ")</span><span class="sxs-lookup"><span data-stu-id="8f124-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-236">Anzahl der Benutzersitzungen, für die das Betriebssystem derzeit Zustandsinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="8f124-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="8f124-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="8f124-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f124-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-240">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**".**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="8f124-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-241">Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="8f124-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f124-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="8f124-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f124-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="8f124-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="8f124-244"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="8f124-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="8f124-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="8f124-246"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="8f124-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-247">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="8f124-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="8f124-248"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="8f124-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="8f124-249"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="8f124-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="8f124-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="8f124-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="8f124-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="8f124-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-252">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="8f124-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="8f124-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="8f124-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="8f124-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="8f124-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="8f124-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="8f124-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="8f124-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="8f124-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="8f124-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="8f124-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="8f124-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="8f124-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="8f124-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-260">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="8f124-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="8f124-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="8f124-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="8f124-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="8f124-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="8f124-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="8f124-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="8f124-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="8f124-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="8f124-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="8f124-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8f124-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="8f124-268"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="8f124-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="8f124-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="8f124-270"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="8f124-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="8f124-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="8f124-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="8f124-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="8f124-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="8f124-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="8f124-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="8f124-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="8f124-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="8f124-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="8f124-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="8f124-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="8f124-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="8f124-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="8f124-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="8f124-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="8f124-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="8f124-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="8f124-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="8f124-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="8f124-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="8f124-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="8f124-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="8f124-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="8f124-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="8f124-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="8f124-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="8f124-285"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="8f124-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-286">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="8f124-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="8f124-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="8f124-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-288">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="8f124-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="8f124-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="8f124-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-290">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="8f124-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="8f124-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="8f124-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="8f124-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="8f124-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="8f124-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="8f124-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="8f124-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="8f124-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="8f124-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="8f124-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="8f124-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="8f124-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="8f124-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="8f124-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="8f124-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-299">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="8f124-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="8f124-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="8f124-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="8f124-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="8f124-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="8f124-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="8f124-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="8f124-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="8f124-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="8f124-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="8f124-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="8f124-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="8f124-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="8f124-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="8f124-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="8f124-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="8f124-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="8f124-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="8f124-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="8f124-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="8f124-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="8f124-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="8f124-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="8f124-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="8f124-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="8f124-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="8f124-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="8f124-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="8f124-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="8f124-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="8f124-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="8f124-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="8f124-316">Palm OS</span><span class="sxs-lookup"><span data-stu-id="8f124-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="8f124-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="8f124-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="8f124-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="8f124-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="8f124-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="8f124-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="8f124-320"><span id="OS_390"></span><span id="os_390"></span>**Betriebssystem/390** (60)</span><span class="sxs-lookup"><span data-stu-id="8f124-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="8f124-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="8f124-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="8f124-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="8f124-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f124-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="8f124-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-326">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="8f124-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-327">Beschreibt den Hersteller und den Betriebs Systemtyp, wenn die Eigenschaft " **OSType** " auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="8f124-328">Das Format der Zeichenfolge, die in **OtherTypeDescription** eingefügt wurde, sollte ähnlich wie die für **OSType** definierten **Werte** Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="8f124-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="8f124-329">Diese Eigenschaft sollte auf NULL festgelegt werden, wenn **OSType** ein anderer Wert als 1 (eins) ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-330">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="8f124-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-331">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-333">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="8f124-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-334">Die Anzahl der Kilobyte, die in den Auslagerungs Dateien des Betriebssystems gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="8f124-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="8f124-335">Diese Zahl stellt nicht die tatsächliche physische Größe der Auslagerungs Datei auf dem Datenträger dar.</span><span class="sxs-lookup"><span data-stu-id="8f124-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="8f124-336">Der Wert 0 (null) gibt an, dass keine Auslagerungs Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8f124-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="8f124-337">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-338">**Status**</span><span class="sxs-lookup"><span data-stu-id="8f124-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-341">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8f124-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-342">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f124-342">Current status of the object.</span></span>

<span data-ttu-id="8f124-343">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f124-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8f124-344">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8f124-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f124-345">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8f124-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8f124-346">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8f124-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f124-347">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8f124-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f124-348">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8f124-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8f124-349">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8f124-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8f124-350">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8f124-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8f124-351">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8f124-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8f124-352">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8f124-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8f124-353">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8f124-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8f124-354">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8f124-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8f124-355">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8f124-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8f124-356">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8f124-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f124-357">**Totaltauapspacesize**</span><span class="sxs-lookup"><span data-stu-id="8f124-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-358">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-360">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-361">Gesamter Auslagerungs Bereich in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="8f124-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="8f124-362">Dieser Wert kann NULL (nicht angegeben) sein, wenn der Auslagerungs Bereich nicht von den Auslagerungs Dateien unterschieden wird.</span><span class="sxs-lookup"><span data-stu-id="8f124-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="8f124-363">Allerdings unterscheiden einige Betriebssysteme diese Konzepte.</span><span class="sxs-lookup"><span data-stu-id="8f124-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="8f124-364">Beispielsweise können gesamte Prozesse in UNIX "ausgetauscht" werden, wenn die freie Seitenliste sinkt und unter dem angegebenen Betrag liegt.</span><span class="sxs-lookup"><span data-stu-id="8f124-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="8f124-365">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-366">**Totalvirtualmemorysize**</span><span class="sxs-lookup"><span data-stu-id="8f124-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-367">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-369">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-370">Anzahl der Kilobyte des virtuellen Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="8f124-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="8f124-371">Berechnen Sie diese z. b., indem Sie die Menge an Gesamt RAM der Größe des Auslagerungs Raums hinzufügen (d. h. die Menge an Arbeitsspeicher in der **SizeStoredInPagingFiles** -Eigenschaft hinzufügen oder durch das Computersystem aggregiert).</span><span class="sxs-lookup"><span data-stu-id="8f124-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="8f124-372">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="8f124-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-374">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f124-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-376">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="8f124-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-377">Gesamtmenge an physischem Arbeitsspeicher (in Kilobyte), die für das Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8f124-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="8f124-378">Dieser Wert gibt nicht notwendigerweise die tatsächliche Menge an physischem Speicher an, sondern dem Betriebssystem als verfügbar gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="8f124-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="8f124-379">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f124-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8f124-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="8f124-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f124-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f124-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f124-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f124-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f124-383">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Betriebs System \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="8f124-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="8f124-384">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f124-384">Version of the operation.</span></span>

<span data-ttu-id="8f124-385">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="8f124-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="8f124-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="8f124-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="8f124-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="8f124-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f124-388">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f124-388">Remarks</span></span>

<span data-ttu-id="8f124-389">Die **CIM- \_ OperatingSystem** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f124-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="8f124-390">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f124-390">WMI does not implement this class.</span></span> <span data-ttu-id="8f124-391">Informationen zu WMI-Klassen, die vom **CIM- \_ OperatingSystem** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f124-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8f124-392">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f124-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f124-393">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f124-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f124-394">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f124-394">Requirements</span></span>



| <span data-ttu-id="8f124-395">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f124-395">Requirement</span></span> | <span data-ttu-id="8f124-396">Wert</span><span class="sxs-lookup"><span data-stu-id="8f124-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f124-397">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f124-397">Minimum supported client</span></span><br/> | <span data-ttu-id="8f124-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f124-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f124-399">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f124-399">Minimum supported server</span></span><br/> | <span data-ttu-id="8f124-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f124-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f124-401">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f124-401">Namespace</span></span><br/>                | <span data-ttu-id="8f124-402">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f124-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f124-403">MOF</span><span class="sxs-lookup"><span data-stu-id="8f124-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f124-404"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f124-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f124-405">DLL</span><span class="sxs-lookup"><span data-stu-id="8f124-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f124-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f124-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f124-407">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f124-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f124-408">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8f124-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

