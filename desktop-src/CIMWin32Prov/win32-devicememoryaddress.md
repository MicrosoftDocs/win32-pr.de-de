---
description: Die \_ WMI-Klasse "Win32 devicememoryaddress" stellt eine Gerätespeicher Adresse auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Win32_DeviceMemoryAddress-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958513"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="9dbfe-103">Win32 \_ devicememoryaddress-Klasse</span><span class="sxs-lookup"><span data-stu-id="9dbfe-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="9dbfe-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ devicememoryaddress** " stellt eine Gerätespeicher Adresse auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="9dbfe-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9dbfe-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dbfe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dbfe-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="9dbfe-108">Member</span><span class="sxs-lookup"><span data-stu-id="9dbfe-108">Members</span></span>

<span data-ttu-id="9dbfe-109">Die **Win32 \_ devicememoryaddress** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9dbfe-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="9dbfe-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dbfe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dbfe-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dbfe-111">Properties</span></span>

<span data-ttu-id="9dbfe-112">Die **Win32 \_ devicememoryaddress** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9dbfe-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-117">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9dbfe-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-119">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9dbfe-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-123">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9dbfe-124">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9dbfe-125">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-129">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9dbfe-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-130">Name der System Erstellungs Klasse des Bereichs bezogenen Computers.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="9dbfe-131">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-135">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9dbfe-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-136">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="9dbfe-137">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-141">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-142">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-142">Description of the object.</span></span>

<span data-ttu-id="9dbfe-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-144">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-145">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-148">Endadresse der Speicher Abbild-e/a.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="9dbfe-149">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="9dbfe-150">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9dbfe-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-152">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-155">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-155">Date and time the object was installed.</span></span> <span data-ttu-id="9dbfe-156">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9dbfe-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-158">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-161">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| systemstructures \| cm \_ partielle \_ Ressourcen \_ \| deskriptorflags")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-162">Merkmale der Arbeitsspeicher Ressource auf dem Computersystem, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="9dbfe-163">Die Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9dbfe-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="9dbfe-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**Lesen** ("lesen")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-165">Der Arbeitsspeicher kann gelesen und geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="9dbfe-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>Schreib **geschützt ("** schreibgeschützt")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-167">Der Arbeitsspeicher ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="9dbfe-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**Schreib** geschützt ("schreibgeschützt")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-169">Der Arbeitsspeicher kann nur geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="9dbfe-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("prefetchable")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-171">Ein Speicherblock wird aus dem Hauptspeicher in einen kleinen Puffer kopiert, der vom Speicher-Chipsatz verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="9dbfe-172">Wiederholte Lesevorgänge aus dem gleichen Teil des Arbeitsspeichers sind schneller mit vorab abgesetzbarem Speicher.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="9dbfe-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**Combinedwrite** ("combinedwrite")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-174">TBD</span><span class="sxs-lookup"><span data-stu-id="9dbfe-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="9dbfe-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-176">TBD</span><span class="sxs-lookup"><span data-stu-id="9dbfe-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="9dbfe-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>Zwischen speicherbar **("cachable** ")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-178">TBD</span><span class="sxs-lookup"><span data-stu-id="9dbfe-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="9dbfe-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**Windowdecode** ("windowdecode")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-180">TBD</span><span class="sxs-lookup"><span data-stu-id="9dbfe-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="9dbfe-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Balken** ("Leiste")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="9dbfe-182">TBD</span><span class="sxs-lookup"><span data-stu-id="9dbfe-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9dbfe-183">**Name**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-186">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-187">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-187">Label by which the object is known.</span></span> <span data-ttu-id="9dbfe-188">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9dbfe-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-190">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-191">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-193">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Speicher, zugeordneter e \| /a \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-194">Die Startadresse der Speicher Abbild-e/a.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="9dbfe-195">Die Eigenschaft Hardware Ressourcen Bezeichner sollte auf diesen Wert festgelegt werden, um den zugeordneten e/a-Ressourcen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="9dbfe-196">Diese Eigenschaft wird von [**CIM \_ memorymappedio**](cim-memorymappedio.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="9dbfe-197">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9dbfe-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9dbfe-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbfe-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbfe-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbfe-201">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9dbfe-202">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-202">Current status of the object.</span></span> <span data-ttu-id="9dbfe-203">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9dbfe-204">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="9dbfe-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9dbfe-205">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="9dbfe-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9dbfe-206">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9dbfe-207">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9dbfe-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9dbfe-209">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9dbfe-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9dbfe-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9dbfe-211">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9dbfe-212">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9dbfe-213">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9dbfe-214">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9dbfe-215">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9dbfe-216">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9dbfe-217">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9dbfe-218">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9dbfe-219">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9dbfe-220">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9dbfe-221">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9dbfe-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9dbfe-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9dbfe-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9dbfe-223">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dbfe-223">Remarks</span></span>

<span data-ttu-id="9dbfe-224">Die **Win32 \_ devicememoryaddress** -Klasse wird von [**Win32 \_ systemmemoryresource**](win32-systemmemoryresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9dbfe-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dbfe-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dbfe-225">Requirements</span></span>



| <span data-ttu-id="9dbfe-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dbfe-226">Requirement</span></span> | <span data-ttu-id="9dbfe-227">Wert</span><span class="sxs-lookup"><span data-stu-id="9dbfe-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dbfe-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dbfe-228">Minimum supported client</span></span><br/> | <span data-ttu-id="9dbfe-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dbfe-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9dbfe-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dbfe-230">Minimum supported server</span></span><br/> | <span data-ttu-id="9dbfe-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dbfe-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9dbfe-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="9dbfe-232">Namespace</span></span><br/>                | <span data-ttu-id="9dbfe-233">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9dbfe-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9dbfe-234">MOF</span><span class="sxs-lookup"><span data-stu-id="9dbfe-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dbfe-235"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9dbfe-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dbfe-236">DLL</span><span class="sxs-lookup"><span data-stu-id="9dbfe-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dbfe-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dbfe-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dbfe-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dbfe-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dbfe-239">**Win32 \_ systemmemoryresource**</span><span class="sxs-lookup"><span data-stu-id="9dbfe-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="9dbfe-240">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9dbfe-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

