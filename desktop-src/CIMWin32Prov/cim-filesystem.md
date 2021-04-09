---
description: Die CIM- \_ Dateisystem Klasse stellt eine Datei oder ein DataSet dar, die sich lokal auf einem Computersystem befinden oder von einem Dateiserver Remote eingebunden werden.
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: CIM_FileSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861255"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="84709-103">CIM- \_ Dateisystem Klasse</span><span class="sxs-lookup"><span data-stu-id="84709-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="84709-104">Die **CIM- \_ Dateisystem** Klasse stellt eine Datei oder ein DataSet dar, die sich lokal auf einem Computersystem befinden oder von einem Dateiserver Remote eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="84709-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84709-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="84709-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84709-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84709-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84709-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="84709-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="84709-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="84709-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84709-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="84709-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="84709-110">Member</span><span class="sxs-lookup"><span data-stu-id="84709-110">Members</span></span>

<span data-ttu-id="84709-111">Die **CIM- \_ Dateisystem** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="84709-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="84709-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84709-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84709-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84709-113">Properties</span></span>

<span data-ttu-id="84709-114">Die **CIM- \_ Dateisystem** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="84709-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84709-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="84709-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-116">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84709-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84709-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="84709-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="84709-119">Der freie Speicherplatz (in Bytes) für das Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="84709-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="84709-120">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="84709-120">If unknown, enter 0.</span></span>

<span data-ttu-id="84709-121">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="84709-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="84709-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="84709-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84709-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84709-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-125">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="84709-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="84709-126">Block Größe des Dateisystems für die Speicherung und den Abruf von Daten.</span><span class="sxs-lookup"><span data-stu-id="84709-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="84709-127">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="84709-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="84709-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="84709-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-131">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="84709-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84709-132">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="84709-132">A short textual description of the object.</span></span>

<span data-ttu-id="84709-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="84709-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84709-134">**Casekonservierte**</span><span class="sxs-lookup"><span data-stu-id="84709-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="84709-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84709-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84709-137">Wenn **true**, wird die Groß-/Kleinschreibung von Dateinamen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="84709-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="84709-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="84709-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="84709-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84709-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84709-141">**True** gibt an, dass die Dateinamen der Groß-/Kleinschreibung unterstützt</span><span class="sxs-lookup"><span data-stu-id="84709-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="84709-142">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="84709-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-143">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="84709-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84709-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84709-145">Ein Array, das die vom Dateisystem unterstützten Zeichensätze oder Codierungen definiert.</span><span class="sxs-lookup"><span data-stu-id="84709-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84709-146">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="84709-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84709-147">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="84709-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="84709-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="84709-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="84709-149">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="84709-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="84709-150">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="84709-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="84709-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="84709-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="84709-152">**Erweiterter UNIX-Code** (6)</span><span class="sxs-lookup"><span data-stu-id="84709-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="84709-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="84709-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="84709-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="84709-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84709-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="84709-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-158">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="84709-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="84709-159">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84709-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="84709-160">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="84709-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="84709-161">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="84709-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="84709-162">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="84709-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="84709-163">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="84709-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-166">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="84709-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="84709-167">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84709-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="84709-168">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="84709-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="84709-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84709-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-172">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="84709-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="84709-173">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="84709-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="84709-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="84709-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-177">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="84709-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="84709-178">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="84709-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="84709-179">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84709-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-182">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="84709-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84709-183">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="84709-183">A textual description of the object.</span></span>

<span data-ttu-id="84709-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="84709-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84709-185">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="84709-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-188">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="84709-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="84709-189">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84709-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="84709-190">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="84709-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="84709-191">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="84709-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="84709-192">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="84709-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="84709-193">**File System size**</span><span class="sxs-lookup"><span data-stu-id="84709-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-194">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84709-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84709-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-196">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="84709-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="84709-197">Größe des Dateisystems in Bytes.</span><span class="sxs-lookup"><span data-stu-id="84709-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="84709-198">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="84709-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="84709-199">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="84709-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="84709-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84709-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-201">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="84709-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84709-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-203">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="84709-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84709-204">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="84709-204">Indicates when the object was installed.</span></span> <span data-ttu-id="84709-205">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="84709-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="84709-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="84709-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84709-207">**Maxdatamelength**</span><span class="sxs-lookup"><span data-stu-id="84709-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84709-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84709-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84709-210">Maximale Länge eines Datei namens innerhalb des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="84709-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="84709-211">Der Wert 0 (null) gibt an, dass es keine Beschränkung auf die Länge des Datei namens gibt.</span><span class="sxs-lookup"><span data-stu-id="84709-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="84709-212">**Name**</span><span class="sxs-lookup"><span data-stu-id="84709-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-215">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="84709-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="84709-216">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="84709-216">Label by which the object is known.</span></span> <span data-ttu-id="84709-217">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="84709-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="84709-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="84709-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84709-219">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="84709-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-220">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="84709-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84709-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-222">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsaccess ")</span><span class="sxs-lookup"><span data-stu-id="84709-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="84709-223">**True** gibt an, dass das Dateisystem schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="84709-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="84709-224">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="84709-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-227">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsmountpoint ")</span><span class="sxs-lookup"><span data-stu-id="84709-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="84709-228">Pfadname oder andere Informationen, die den Stamm des Dateisystems definieren.</span><span class="sxs-lookup"><span data-stu-id="84709-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="84709-229">**Status**</span><span class="sxs-lookup"><span data-stu-id="84709-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84709-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="84709-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84709-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="84709-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84709-232">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="84709-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84709-233">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="84709-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="84709-234">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="84709-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="84709-235">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="84709-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="84709-236">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="84709-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="84709-237">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="84709-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="84709-238">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="84709-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="84709-239">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="84709-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="84709-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="84709-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84709-241">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="84709-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84709-242">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="84709-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84709-243">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="84709-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84709-244">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="84709-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84709-245">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="84709-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84709-246">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="84709-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84709-247">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="84709-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84709-248">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="84709-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84709-249">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="84709-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84709-250">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="84709-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84709-251">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="84709-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84709-252">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="84709-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84709-253">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="84709-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="84709-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84709-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="84709-255">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84709-255">Remarks</span></span>

<span data-ttu-id="84709-256">Die **CIM-Klasse \_ File System** wird [**von \_ CIM LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="84709-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="84709-257">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="84709-257">WMI does not implement this class.</span></span>

<span data-ttu-id="84709-258">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="84709-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84709-259">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="84709-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84709-260">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84709-260">Requirements</span></span>



| <span data-ttu-id="84709-261">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84709-261">Requirement</span></span> | <span data-ttu-id="84709-262">Wert</span><span class="sxs-lookup"><span data-stu-id="84709-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84709-263">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84709-263">Minimum supported client</span></span><br/> | <span data-ttu-id="84709-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84709-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84709-265">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84709-265">Minimum supported server</span></span><br/> | <span data-ttu-id="84709-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84709-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84709-267">Namespace</span><span class="sxs-lookup"><span data-stu-id="84709-267">Namespace</span></span><br/>                | <span data-ttu-id="84709-268">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84709-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84709-269">MOF</span><span class="sxs-lookup"><span data-stu-id="84709-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84709-270"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84709-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84709-271">DLL</span><span class="sxs-lookup"><span data-stu-id="84709-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84709-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84709-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84709-273">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84709-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84709-274">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="84709-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

