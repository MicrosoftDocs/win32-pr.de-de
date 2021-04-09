---
description: Die \_ WMI-Klasse "Win32 systemmemoryresource abstract" stellt eine Systemspeicher Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Win32_SystemMemoryResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861663"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="452d3-103">Win32- \_ systemmemoryresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="452d3-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="452d3-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemmemoryresource** abstract" stellt eine Systemspeicher Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="452d3-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="452d3-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="452d3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="452d3-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="452d3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="452d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="452d3-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="452d3-108">Member</span><span class="sxs-lookup"><span data-stu-id="452d3-108">Members</span></span>

<span data-ttu-id="452d3-109">Die **Win32- \_ systemmemoryresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="452d3-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="452d3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="452d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="452d3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="452d3-111">Properties</span></span>

<span data-ttu-id="452d3-112">Die **Win32- \_ systemmemoryresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="452d3-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="452d3-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="452d3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="452d3-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="452d3-117">A short textual description of the object.</span></span>

<span data-ttu-id="452d3-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-119">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="452d3-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-122">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="452d3-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="452d3-123">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="452d3-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="452d3-124">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="452d3-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="452d3-125">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="452d3-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-129">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="452d3-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="452d3-130">Die Eigenschaft " **kreationclassname** " des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="452d3-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="452d3-131">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="452d3-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-135">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="452d3-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="452d3-136">Die **Name** -Eigenschaft des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="452d3-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="452d3-137">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="452d3-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-141">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="452d3-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-142">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="452d3-142">A textual description of the object.</span></span>

<span data-ttu-id="452d3-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-144">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="452d3-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-145">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="452d3-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-147">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="452d3-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-148">Endadresse der zugeordneten e/a-Vorgänge im Speicher.</span><span class="sxs-lookup"><span data-stu-id="452d3-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="452d3-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="452d3-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="452d3-150">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="452d3-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-152">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="452d3-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-154">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="452d3-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-155">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="452d3-155">Indicates when the object was installed.</span></span> <span data-ttu-id="452d3-156">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="452d3-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="452d3-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="452d3-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-161">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="452d3-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-162">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="452d3-162">Label by which the object is known.</span></span> <span data-ttu-id="452d3-163">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="452d3-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="452d3-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="452d3-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-166">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="452d3-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-168">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="452d3-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-169">Die Startadresse der von einem Speicher abgebildete e/a.</span><span class="sxs-lookup"><span data-stu-id="452d3-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="452d3-170">Die Eigenschaft Hardware Ressourcen Bezeichner sollte auf diesen Wert festgelegt werden, um den zugeordneten e/a-Ressourcen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="452d3-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="452d3-171">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="452d3-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="452d3-172">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="452d3-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="452d3-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="452d3-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="452d3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="452d3-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="452d3-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="452d3-176">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="452d3-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="452d3-177">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="452d3-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="452d3-178">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="452d3-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="452d3-179">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="452d3-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="452d3-180">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="452d3-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="452d3-181">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="452d3-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="452d3-182">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="452d3-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="452d3-183">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="452d3-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="452d3-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="452d3-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="452d3-185">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="452d3-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="452d3-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="452d3-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="452d3-187">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="452d3-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="452d3-188">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="452d3-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="452d3-189">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="452d3-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="452d3-190">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="452d3-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="452d3-191">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="452d3-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="452d3-192">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="452d3-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="452d3-193">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="452d3-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="452d3-194">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="452d3-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="452d3-195">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="452d3-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="452d3-196">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="452d3-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="452d3-197">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="452d3-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="452d3-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="452d3-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="452d3-199">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="452d3-199">Remarks</span></span>

<span data-ttu-id="452d3-200">Die Win32-Klasse " **\_ systemmemoryresource** " wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="452d3-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="452d3-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="452d3-201">Requirements</span></span>



| <span data-ttu-id="452d3-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="452d3-202">Requirement</span></span> | <span data-ttu-id="452d3-203">Wert</span><span class="sxs-lookup"><span data-stu-id="452d3-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="452d3-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="452d3-204">Minimum supported client</span></span><br/> | <span data-ttu-id="452d3-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="452d3-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="452d3-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="452d3-206">Minimum supported server</span></span><br/> | <span data-ttu-id="452d3-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="452d3-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="452d3-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="452d3-208">Namespace</span></span><br/>                | <span data-ttu-id="452d3-209">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="452d3-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="452d3-210">MOF</span><span class="sxs-lookup"><span data-stu-id="452d3-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="452d3-211"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="452d3-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="452d3-212">DLL</span><span class="sxs-lookup"><span data-stu-id="452d3-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="452d3-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="452d3-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452d3-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="452d3-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452d3-215">**CIM \_ memorymappedio**</span><span class="sxs-lookup"><span data-stu-id="452d3-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="452d3-216">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="452d3-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
