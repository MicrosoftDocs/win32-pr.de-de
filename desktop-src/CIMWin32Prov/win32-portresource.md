---
description: Die \_ WMI-Klasse von Win32 portresource stellt einen I/O-Port auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Win32_PortResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958227"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="a1555-103">Win32 \_ portresource-Klasse</span><span class="sxs-lookup"><span data-stu-id="a1555-103">Win32\_PortResource class</span></span>

<span data-ttu-id="a1555-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ portresource** stellt einen I/O-Port auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1555-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="a1555-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1555-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a1555-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a1555-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1555-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1555-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a1555-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1555-108">Members</span></span>

<span data-ttu-id="a1555-109">Die **Win32 \_ portresource** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1555-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="a1555-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1555-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1555-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1555-111">Properties</span></span>

<span data-ttu-id="a1555-112">Die **Win32 \_ portresource** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1555-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1555-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="a1555-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a1555-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Configuration Manager Structures \| IO \_ Info")</span><span class="sxs-lookup"><span data-stu-id="a1555-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-117">**True** gibt an, dass diese Instanz einen der Bereiche mit einem Alias darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1555-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="a1555-118">**False** gibt an, dass die Instanz eine Basis Portadresse darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1555-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="a1555-119">Eine Basis Portadresse ist eine vorgegebene Portadresse für einen bestimmten Dienst oder ein bestimmtes Gerät.</span><span class="sxs-lookup"><span data-stu-id="a1555-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="a1555-120">Eine Port-Alias Adresse ist eine Adresse, auf die ein Gerät antwortet, als ob es sich um die tatsächliche Adresse eines e/a-Ports handelt.</span><span class="sxs-lookup"><span data-stu-id="a1555-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="a1555-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a1555-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-124">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a1555-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-125">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1555-125">Short description of the object.</span></span>

<span data-ttu-id="a1555-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-127">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a1555-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-130">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a1555-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a1555-131">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1555-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a1555-132">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a1555-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a1555-133">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1555-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-137">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a1555-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a1555-138">Der Name der Erstellungs Klasse des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="a1555-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="a1555-139">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a1555-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-143">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a1555-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a1555-144">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="a1555-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="a1555-145">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1555-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-149">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a1555-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-150">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1555-150">Description of the object.</span></span>

<span data-ttu-id="a1555-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-152">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="a1555-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-153">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1555-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-155">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a1555-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-156">Endadresse der zugeordneten e/a-Vorgänge im Speicher.</span><span class="sxs-lookup"><span data-stu-id="a1555-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="a1555-157">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="a1555-158">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a1555-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1555-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-160">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1555-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-162">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a1555-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-163">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1555-163">Date and time the object was installed.</span></span> <span data-ttu-id="a1555-164">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a1555-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a1555-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1555-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-169">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a1555-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-170">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a1555-170">Label by which the object is known.</span></span> <span data-ttu-id="a1555-171">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a1555-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a1555-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-173">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="a1555-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-174">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1555-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-176">Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a1555-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-177">Die Startadresse der von einem Speicher abgebildete e/a.</span><span class="sxs-lookup"><span data-stu-id="a1555-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="a1555-178">Die Eigenschaft Hardware Ressourcen Bezeichner sollte auf diesen Wert festgelegt werden, um den zugeordneten e/a-Ressourcen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1555-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="a1555-179">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="a1555-180">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a1555-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1555-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="a1555-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1555-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1555-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1555-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1555-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1555-184">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a1555-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a1555-185">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1555-185">Current status of the object.</span></span> <span data-ttu-id="a1555-186">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1555-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a1555-187">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="a1555-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a1555-188">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="a1555-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a1555-189">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1555-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a1555-190">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a1555-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a1555-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1555-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a1555-192">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a1555-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a1555-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a1555-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a1555-194">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a1555-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a1555-195">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a1555-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1555-196">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a1555-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a1555-197">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a1555-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a1555-198">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a1555-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a1555-199">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a1555-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a1555-200">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a1555-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a1555-201">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a1555-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a1555-202">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a1555-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a1555-203">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a1555-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a1555-204">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a1555-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a1555-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a1555-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a1555-206">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1555-206">Remarks</span></span>

<span data-ttu-id="a1555-207">Die **Win32 \_ portresource** -Klasse wird von [**Win32 \_ systemmemoryresource**](win32-systemmemoryresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a1555-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1555-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1555-208">Requirements</span></span>



| <span data-ttu-id="a1555-209">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1555-209">Requirement</span></span> | <span data-ttu-id="a1555-210">Wert</span><span class="sxs-lookup"><span data-stu-id="a1555-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1555-211">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1555-211">Minimum supported client</span></span><br/> | <span data-ttu-id="a1555-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1555-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1555-213">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1555-213">Minimum supported server</span></span><br/> | <span data-ttu-id="a1555-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1555-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1555-215">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1555-215">Namespace</span></span><br/>                | <span data-ttu-id="a1555-216">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a1555-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1555-217">MOF</span><span class="sxs-lookup"><span data-stu-id="a1555-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1555-218"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a1555-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1555-219">DLL</span><span class="sxs-lookup"><span data-stu-id="a1555-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1555-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1555-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1555-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1555-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1555-222">**Win32 \_ systemmemoryresource**</span><span class="sxs-lookup"><span data-stu-id="a1555-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="a1555-223">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a1555-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
