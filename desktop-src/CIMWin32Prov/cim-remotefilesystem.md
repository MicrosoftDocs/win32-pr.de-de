---
description: Die CIM- \_ remotefile System-Klasse stellt ein Remote Dateisystem dar, auf das über einen netzwerkbezogenen Dienst zugegriffen wird. In diesem Fall wird der Dateispeicher von einem Computer gehostet, der als Dateiserver fungiert.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: CIM_RemoteFileSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126134"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="dbb7a-104">CIM- \_ remotefile System-Klasse</span><span class="sxs-lookup"><span data-stu-id="dbb7a-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="dbb7a-105">Die **CIM- \_ remotefile** System-Klasse stellt ein Remote Dateisystem dar, auf das über einen netzwerkbezogenen Dienst zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="dbb7a-106">In diesem Fall wird der Dateispeicher von einem Computer gehostet, der als Dateiserver fungiert.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="dbb7a-107">Der Dateispeicher für ein NFS-Dateisystem befindet sich z. b. in der Regel nicht auf den lokal kontrollierten Medien eines Computer Systems, und der Zugriff darauf erfolgt nicht direkt über einen Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="dbb7a-108">Unterklassen von **CIM \_ remotefile** System enthalten Client seitige Konfigurationsinformationen, die sich auf den Zugriff auf das Dateisystem beziehen.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbb7a-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbb7a-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbb7a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbb7a-111">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dbb7a-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb7a-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbb7a-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="dbb7a-114">Member</span><span class="sxs-lookup"><span data-stu-id="dbb7a-114">Members</span></span>

<span data-ttu-id="dbb7a-115">Die **CIM- \_ remotefile System** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbb7a-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="dbb7a-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbb7a-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbb7a-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbb7a-117">Properties</span></span>

<span data-ttu-id="dbb7a-118">Die **CIM- \_ remotefile System** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbb7a-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-120">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-122">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-123">Die Menge des freien Speicherplatzes für das Dateisystem in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="dbb7a-124">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-124">If unknown, enter 0.</span></span>

<span data-ttu-id="dbb7a-125">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dbb7a-126">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbb7a-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-130">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-131">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="dbb7a-132">Wenn unbekannt, oder wenn ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="dbb7a-133">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dbb7a-134">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbb7a-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-138">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-139">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-139">Textual description of the object.</span></span>

<span data-ttu-id="dbb7a-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-141">**Casekonservierte**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbb7a-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-144">Wenn **true**, wird die Groß-/Kleinschreibung von Dateinamen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="dbb7a-145">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbb7a-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-149">**True** gibt an, dass die Dateinamen der Groß-/Kleinschreibung unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="dbb7a-150">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-151">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-152">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dbb7a-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-154">Vom Dateisystem Unterstützte Zeichensätze oder Codierungen.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="dbb7a-155">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbb7a-156">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbb7a-157">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="dbb7a-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="dbb7a-159">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="dbb7a-160">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="dbb7a-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="dbb7a-162">**Erweiterter UNIX-Code** (6)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="dbb7a-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="dbb7a-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbb7a-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-168">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-169">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="dbb7a-170">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="dbb7a-171">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="dbb7a-172">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="dbb7a-173">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-174">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-177">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-178">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dbb7a-179">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dbb7a-180">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-184">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-185">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="dbb7a-186">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-190">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-191">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-191">Scoping computer system's name.</span></span>

<span data-ttu-id="dbb7a-192">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-193">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-196">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-197">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-197">Textual description of the object.</span></span>

<span data-ttu-id="dbb7a-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-199">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-202">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-203">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="dbb7a-204">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="dbb7a-205">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="dbb7a-206">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="dbb7a-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="dbb7a-207">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-208">**File System size**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-209">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-211">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-212">Gesamtgröße des Dateisystems in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="dbb7a-213">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-213">If unknown, enter 0.</span></span>

<span data-ttu-id="dbb7a-214">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dbb7a-215">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dbb7a-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-217">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-219">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-220">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-220">Date and time the object was installed.</span></span> <span data-ttu-id="dbb7a-221">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dbb7a-222">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-223">**Maxdatamelength**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-224">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-226">Maximale Länge eines Datei namens innerhalb des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="dbb7a-227">Der Wert 0 gibt an, dass die Länge des Datei namens unbegrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="dbb7a-228">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-229">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-232">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-233">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-233">Label by which the object is known.</span></span> <span data-ttu-id="dbb7a-234">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dbb7a-235">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-236">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-237">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dbb7a-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-239">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsaccess ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-240">**True** gibt an, dass das Dateisystem schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="dbb7a-241">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-242">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-245">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsmountpoint ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-246">Pfadname oder andere Informationen, die den Stamm des Dateisystems definieren.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="dbb7a-247">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbb7a-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb7a-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbb7a-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbb7a-251">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dbb7a-252">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-252">Current status of the object.</span></span>

<span data-ttu-id="dbb7a-253">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dbb7a-254">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dbb7a-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dbb7a-255">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dbb7a-256">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbb7a-257">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbb7a-258">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dbb7a-259">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dbb7a-260">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dbb7a-261">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dbb7a-262">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dbb7a-263">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dbb7a-264">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dbb7a-265">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dbb7a-266">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="dbb7a-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dbb7a-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dbb7a-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dbb7a-268">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbb7a-268">Remarks</span></span>

<span data-ttu-id="dbb7a-269">Die **CIM- \_ remotefile System** -Klasse wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dbb7a-270">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-270">WMI does not implement this class.</span></span>

<span data-ttu-id="dbb7a-271">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbb7a-272">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dbb7a-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb7a-273">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbb7a-273">Requirements</span></span>



| <span data-ttu-id="dbb7a-274">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbb7a-274">Requirement</span></span> | <span data-ttu-id="dbb7a-275">Wert</span><span class="sxs-lookup"><span data-stu-id="dbb7a-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb7a-276">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-276">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb7a-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbb7a-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbb7a-278">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbb7a-278">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb7a-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbb7a-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbb7a-280">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbb7a-280">Namespace</span></span><br/>                | <span data-ttu-id="dbb7a-281">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbb7a-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbb7a-282">MOF</span><span class="sxs-lookup"><span data-stu-id="dbb7a-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbb7a-283"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dbb7a-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbb7a-284">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb7a-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb7a-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbb7a-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb7a-286">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbb7a-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb7a-287">**CIM- \_ Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="dbb7a-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

