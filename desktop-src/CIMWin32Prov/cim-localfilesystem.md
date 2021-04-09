---
description: Die CIM \_ LocalFile System-Klasse stellt den Dateispeicher dar, der von einem Computersystem über lokale Mittel (z. b. direkten Zugriff auf Gerätetreiber) gesteuert wird.
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: CIM_LocalFileSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861236"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="a240b-103">CIM \_ LocalFile System-Klasse</span><span class="sxs-lookup"><span data-stu-id="a240b-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="a240b-104">Die **CIM \_ LocalFile** System-Klasse stellt den Dateispeicher dar, der von einem Computersystem über lokale Mittel (z. b. direkten Zugriff auf Gerätetreiber) gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="a240b-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="a240b-105">Der Dateispeicher kann direkt vom Computersystem verwaltet werden, ohne dass ein anderer Computer als Dateiserver fungieren muss.</span><span class="sxs-lookup"><span data-stu-id="a240b-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="a240b-106">Bei einem Cluster Dateisystem ist das Dateisystem jedoch lokal und wird daher auf den Cluster abgehandelt.</span><span class="sxs-lookup"><span data-stu-id="a240b-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a240b-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a240b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a240b-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a240b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a240b-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a240b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a240b-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a240b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a240b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a240b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
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

## <a name="members"></a><span data-ttu-id="a240b-112">Member</span><span class="sxs-lookup"><span data-stu-id="a240b-112">Members</span></span>

<span data-ttu-id="a240b-113">Die **CIM \_ LocalFile System** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a240b-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="a240b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a240b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a240b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a240b-115">Properties</span></span>

<span data-ttu-id="a240b-116">Die **CIM \_ LocalFile System** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a240b-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a240b-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="a240b-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-118">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a240b-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-120">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="a240b-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-121">Der freie Speicherplatz (in Bytes) für das Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="a240b-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="a240b-122">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="a240b-122">If unknown, enter 0.</span></span>

<span data-ttu-id="a240b-123">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a240b-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a240b-124">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="a240b-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a240b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-128">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a240b-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-129">Block Größe des Dateisystems für die Speicherung und den Abruf von Daten.</span><span class="sxs-lookup"><span data-stu-id="a240b-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="a240b-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a240b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a240b-131">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-132">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a240b-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-135">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a240b-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-136">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a240b-136">A short textual description of the object.</span></span>

<span data-ttu-id="a240b-137">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-138">**Casekonservierte**</span><span class="sxs-lookup"><span data-stu-id="a240b-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a240b-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a240b-141">Wenn **true**, wird die Groß-/Kleinschreibung von Dateinamen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a240b-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="a240b-142">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="a240b-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a240b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a240b-146">**True** gibt an, dass die Dateinamen der Groß-/Kleinschreibung unterstützt</span><span class="sxs-lookup"><span data-stu-id="a240b-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="a240b-147">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-148">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="a240b-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-149">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a240b-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a240b-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a240b-151">Ein Array, das die vom Dateisystem unterstützten Zeichensätze oder Codierungen definiert.</span><span class="sxs-lookup"><span data-stu-id="a240b-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="a240b-152">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a240b-153">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a240b-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a240b-154">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a240b-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="a240b-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="a240b-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="a240b-156">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="a240b-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="a240b-157">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="a240b-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="a240b-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="a240b-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="a240b-159">**Erweiterter UNIX-Code** (6)</span><span class="sxs-lookup"><span data-stu-id="a240b-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="a240b-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="a240b-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="a240b-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="a240b-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a240b-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="a240b-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-165">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="a240b-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-166">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a240b-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a240b-167">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="a240b-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="a240b-168">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="a240b-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="a240b-169">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="a240b-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="a240b-170">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a240b-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-174">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a240b-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a240b-175">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a240b-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a240b-176">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a240b-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a240b-177">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a240b-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-181">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="a240b-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-182">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="a240b-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="a240b-183">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a240b-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-187">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="a240b-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-188">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a240b-188">Scoping computer system's name.</span></span>

<span data-ttu-id="a240b-189">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-190">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a240b-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-193">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a240b-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-194">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a240b-194">A textual description of the object.</span></span>

<span data-ttu-id="a240b-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-196">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="a240b-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-199">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="a240b-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-200">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a240b-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="a240b-201">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="a240b-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="a240b-202">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="a240b-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="a240b-203">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="a240b-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="a240b-204">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-205">**File System size**</span><span class="sxs-lookup"><span data-stu-id="a240b-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-206">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a240b-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-208">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="a240b-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-209">Größe des Dateisystems in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a240b-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="a240b-210">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="a240b-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="a240b-211">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a240b-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a240b-212">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a240b-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-214">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a240b-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-216">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a240b-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-217">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a240b-217">Indicates when the object was installed.</span></span> <span data-ttu-id="a240b-218">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a240b-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a240b-219">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-220">**Maxdatamelength**</span><span class="sxs-lookup"><span data-stu-id="a240b-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-221">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a240b-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a240b-223">Maximale Länge eines Datei namens innerhalb des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="a240b-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="a240b-224">Der Wert 0 (null) gibt an, dass es keine Beschränkung auf die Länge des Datei namens gibt.</span><span class="sxs-lookup"><span data-stu-id="a240b-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="a240b-225">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-226">**Name**</span><span class="sxs-lookup"><span data-stu-id="a240b-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-229">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a240b-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-230">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a240b-230">Label by which the object is known.</span></span> <span data-ttu-id="a240b-231">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a240b-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a240b-232">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-233">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="a240b-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-234">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a240b-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-236">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsaccess ")</span><span class="sxs-lookup"><span data-stu-id="a240b-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-237">**True** gibt an, dass das Dateisystem schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a240b-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="a240b-238">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-239">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="a240b-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-242">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsmountpoint ")</span><span class="sxs-lookup"><span data-stu-id="a240b-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-243">Pfadname oder andere Informationen, die den Stamm des Dateisystems definieren.</span><span class="sxs-lookup"><span data-stu-id="a240b-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="a240b-244">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="a240b-245">**Status**</span><span class="sxs-lookup"><span data-stu-id="a240b-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a240b-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a240b-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a240b-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a240b-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a240b-248">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a240b-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a240b-249">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a240b-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="a240b-250">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a240b-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a240b-251">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a240b-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a240b-252">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="a240b-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a240b-253">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a240b-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a240b-254">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a240b-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a240b-255">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a240b-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a240b-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a240b-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a240b-257">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a240b-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a240b-258">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a240b-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a240b-259">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a240b-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a240b-260">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a240b-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a240b-261">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a240b-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a240b-262">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a240b-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a240b-263">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a240b-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a240b-264">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a240b-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a240b-265">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a240b-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a240b-266">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a240b-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a240b-267">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a240b-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a240b-268">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a240b-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a240b-269">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a240b-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a240b-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a240b-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a240b-271">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a240b-271">Remarks</span></span>

<span data-ttu-id="a240b-272">Die **CIM \_ LocalFile System** -Klasse wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a240b-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="a240b-273">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a240b-273">WMI does not implement this class.</span></span>

<span data-ttu-id="a240b-274">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a240b-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a240b-275">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a240b-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a240b-276">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a240b-276">Requirements</span></span>



| <span data-ttu-id="a240b-277">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a240b-277">Requirement</span></span> | <span data-ttu-id="a240b-278">Wert</span><span class="sxs-lookup"><span data-stu-id="a240b-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a240b-279">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a240b-279">Minimum supported client</span></span><br/> | <span data-ttu-id="a240b-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a240b-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a240b-281">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a240b-281">Minimum supported server</span></span><br/> | <span data-ttu-id="a240b-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a240b-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a240b-283">Namespace</span><span class="sxs-lookup"><span data-stu-id="a240b-283">Namespace</span></span><br/>                | <span data-ttu-id="a240b-284">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a240b-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a240b-285">MOF</span><span class="sxs-lookup"><span data-stu-id="a240b-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a240b-286"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a240b-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a240b-287">DLL</span><span class="sxs-lookup"><span data-stu-id="a240b-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a240b-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a240b-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a240b-289">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a240b-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a240b-290">**CIM- \_ Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="a240b-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

