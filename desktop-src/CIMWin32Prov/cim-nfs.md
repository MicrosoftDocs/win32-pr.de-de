---
description: Die CIM- \_ NFS-Klasse stellt ein Remote Dateisystem dar, das mit dem NFS-Protokoll (Network File System) von einem Computersystem bereitgestellt wird.
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: CIM_NFS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748585"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="34426-103">CIM- \_ NFS-Klasse</span><span class="sxs-lookup"><span data-stu-id="34426-103">CIM\_NFS class</span></span>

<span data-ttu-id="34426-104">Die **CIM- \_ NFS** -Klasse stellt ein Remote Dateisystem dar, das mit dem NFS-Protokoll (Network File System) von einem Computersystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="34426-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="34426-105">Die Eigenschaften des NFS-Objekts entsprechen den operativen Aspekten der bereitstellen und stellen die Client seitige Konfiguration für den NFS-Zugriff dar.</span><span class="sxs-lookup"><span data-stu-id="34426-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="34426-106">Der Dateisystemtyp sollte festgelegt werden, um den Typ des Dateisystems anzugeben, der dem Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="34426-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34426-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34426-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34426-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="34426-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="34426-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="34426-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="34426-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34426-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="34426-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
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
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="34426-112">Member</span><span class="sxs-lookup"><span data-stu-id="34426-112">Members</span></span>

<span data-ttu-id="34426-113">Die **CIM- \_ NFS** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="34426-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="34426-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34426-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34426-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34426-115">Properties</span></span>

<span data-ttu-id="34426-116">Die **CIM- \_ NFS** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34426-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34426-117">**Attributecaching**</span><span class="sxs-lookup"><span data-stu-id="34426-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-120">**True** gibt an, dass das Zwischenspeichern von Steuerungs Attributen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34426-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="34426-121">**False** gibt an, dass das Zwischenspeichern von Steuerungs Attributen deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34426-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="34426-122">**Attributecachingfordirectoriesmax**</span><span class="sxs-lookup"><span data-stu-id="34426-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-125">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="34426-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="34426-126">Maximale Anzahl von Sekunden, die zwischengespeicherte Attribute nach der Verzeichnis Aktualisierung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="34426-127">**Attributecachingfordirectoriesmin**</span><span class="sxs-lookup"><span data-stu-id="34426-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-130">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="34426-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="34426-131">Die minimale Anzahl von Sekunden, die zwischengespeicherte Attribute nach der Verzeichnis Aktualisierung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="34426-132">**Attributecachingforregularfilesmax**</span><span class="sxs-lookup"><span data-stu-id="34426-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-135">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="34426-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="34426-136">Maximale Anzahl von Sekunden, die zwischengespeicherte Attribute nach der Datei Änderung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="34426-137">**Attributecachingforregularfilesmin**</span><span class="sxs-lookup"><span data-stu-id="34426-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-140">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="34426-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="34426-141">Die minimale Anzahl von Sekunden, die zwischengespeicherte Attribute nach der Datei Änderung aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="34426-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="34426-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34426-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34426-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="34426-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34426-146">Der Gesamtumfang des freien Speicherplatzes (in Byte) für das Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="34426-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="34426-147">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="34426-147">If unknown, enter 0.</span></span>

<span data-ttu-id="34426-148">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="34426-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34426-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34426-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="34426-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-151">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34426-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34426-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-153">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34426-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34426-154">Dateisysteme können Daten in Blöcken lesen oder schreiben, die unabhängig von den zugrunde liegenden Speicherblöcken definiert sind.</span><span class="sxs-lookup"><span data-stu-id="34426-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="34426-155">Diese Eigenschaft erfasst die Blockgröße des Dateisystems für die Speicherung und den Abruf von Daten.</span><span class="sxs-lookup"><span data-stu-id="34426-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="34426-156">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="34426-157">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34426-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34426-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="34426-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-161">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="34426-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="34426-162">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="34426-162">Short textual description of the object.</span></span>

<span data-ttu-id="34426-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-164">**Casekonservierte**</span><span class="sxs-lookup"><span data-stu-id="34426-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-165">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-167">Wenn **true**, wird die Groß-/Kleinschreibung von Dateinamen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="34426-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="34426-168">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="34426-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-172">**True** gibt an, dass die Dateinamen der Groß-/Kleinschreibung unterstützt</span><span class="sxs-lookup"><span data-stu-id="34426-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="34426-173">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-174">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="34426-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34426-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34426-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-177">Vom Dateisystem Unterstützte Zeichensätze oder Codierungen.</span><span class="sxs-lookup"><span data-stu-id="34426-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="34426-178">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34426-179">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34426-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34426-180">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="34426-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="34426-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="34426-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="34426-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="34426-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="34426-183">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="34426-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="34426-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="34426-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="34426-185">**Erweiterter UNIX-Code** (6)</span><span class="sxs-lookup"><span data-stu-id="34426-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="34426-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="34426-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="34426-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="34426-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34426-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="34426-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-191">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="34426-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="34426-192">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34426-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="34426-193">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="34426-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="34426-194">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="34426-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="34426-195">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="34426-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="34426-196">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-197">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="34426-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-200">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="34426-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="34426-201">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34426-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="34426-202">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="34426-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="34426-203">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34426-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-207">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="34426-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="34426-208">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="34426-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="34426-209">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="34426-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-213">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="34426-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="34426-214">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34426-214">Scoping computer system's name.</span></span>

<span data-ttu-id="34426-215">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-216">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34426-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-219">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="34426-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="34426-220">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="34426-220">Textual description of the object.</span></span>

<span data-ttu-id="34426-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-222">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="34426-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-225">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Partition \| 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="34426-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="34426-226">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34426-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="34426-227">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="34426-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="34426-228">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="34426-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="34426-229">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="34426-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="34426-230">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-231">**File System size**</span><span class="sxs-lookup"><span data-stu-id="34426-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-232">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34426-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34426-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-234">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34426-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34426-235">Gesamtgröße des Dateisystems in Bytes.</span><span class="sxs-lookup"><span data-stu-id="34426-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="34426-236">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="34426-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="34426-237">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="34426-238">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34426-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34426-239">**Foregroundmount**</span><span class="sxs-lookup"><span data-stu-id="34426-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-240">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-242">**True** gibt an, dass Wiederholungs Versuche im Vordergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34426-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="34426-243">Wenn der Wert **false** ist und der erste einfügversuch fehlschlägt, werden im Hintergrund Wiederholungs Versuche ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34426-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="34426-244">**Hardmount**</span><span class="sxs-lookup"><span data-stu-id="34426-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-247">Wenn **true**, werden NFS-Anforderungen nach der Bereitstellung des Dateisystems wiederholt, bis das Host System antwortet.</span><span class="sxs-lookup"><span data-stu-id="34426-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="34426-248">Wenn **false**, wird nach dem Bereitstellen des Dateisystems ein Fehler zurückgegeben, wenn das Host System nicht antwortet.</span><span class="sxs-lookup"><span data-stu-id="34426-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="34426-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34426-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-250">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="34426-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34426-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-252">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="34426-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="34426-253">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="34426-253">Date and time the object was installed.</span></span> <span data-ttu-id="34426-254">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="34426-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="34426-255">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-256">**Interrupt**</span><span class="sxs-lookup"><span data-stu-id="34426-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-257">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-259">**True** gibt an, dass Interrupts für feste bereit Stellungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34426-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="34426-260">**False** gibt an, dass Interrupts für feste bereit Stellungen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="34426-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="34426-261">**Maxdatamelength**</span><span class="sxs-lookup"><span data-stu-id="34426-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34426-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34426-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-264">Maximale Länge eines Datei namens innerhalb des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="34426-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="34426-265">Der Wert 0 (null) gibt an, dass keine Beschränkung für die Länge des Datei namens vorliegt.</span><span class="sxs-lookup"><span data-stu-id="34426-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="34426-266">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-267">**Mountfailureretries**</span><span class="sxs-lookup"><span data-stu-id="34426-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-268">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-270">Maximale Anzahl von zugelassenen Wiederholungs versuchen.</span><span class="sxs-lookup"><span data-stu-id="34426-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="34426-271">**Name**</span><span class="sxs-lookup"><span data-stu-id="34426-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-274">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="34426-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="34426-275">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="34426-275">Label by which the object is known.</span></span> <span data-ttu-id="34426-276">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="34426-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="34426-277">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-278">**"Read bufferSize"**</span><span class="sxs-lookup"><span data-stu-id="34426-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-279">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34426-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34426-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-281">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34426-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34426-282">Lese Puffergröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="34426-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="34426-283">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34426-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34426-284">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="34426-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-285">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="34426-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34426-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-287">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsaccess ")</span><span class="sxs-lookup"><span data-stu-id="34426-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="34426-288">**True** gibt an, dass das Dateisystem schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="34426-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="34426-289">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-290">**Retransmissionversuche**</span><span class="sxs-lookup"><span data-stu-id="34426-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-291">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34426-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34426-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-293">Maximale Anzahl zulässiger NFS-Neuübertragungen.</span><span class="sxs-lookup"><span data-stu-id="34426-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="34426-294">**Retransmissiontimeout**</span><span class="sxs-lookup"><span data-stu-id="34426-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-295">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34426-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34426-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-297">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zehntel der Sekunden")</span><span class="sxs-lookup"><span data-stu-id="34426-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="34426-298">NFS-Timeout, in Zehntelsekunden.</span><span class="sxs-lookup"><span data-stu-id="34426-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="34426-299">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="34426-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-302">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrfsmountpoint ")</span><span class="sxs-lookup"><span data-stu-id="34426-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="34426-303">Pfadname oder andere Informationen, die den Stamm des Dateisystems definieren.</span><span class="sxs-lookup"><span data-stu-id="34426-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="34426-304">Diese Eigenschaft wird vom [**CIM- \_ Dateisystem**](cim-filesystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="34426-305">**Servercommunicationport**</span><span class="sxs-lookup"><span data-stu-id="34426-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-306">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34426-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34426-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34426-308">UDP-Portnummer des Remote Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="34426-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="34426-309">**Status**</span><span class="sxs-lookup"><span data-stu-id="34426-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="34426-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34426-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-312">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="34426-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="34426-313">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="34426-313">Current status of the object.</span></span>

<span data-ttu-id="34426-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34426-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="34426-315">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="34426-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="34426-316">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="34426-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="34426-317">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="34426-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34426-318">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="34426-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34426-319">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="34426-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="34426-320">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="34426-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="34426-321">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="34426-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="34426-322">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="34426-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="34426-323">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="34426-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="34426-324">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="34426-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="34426-325">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="34426-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="34426-326">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="34426-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="34426-327">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="34426-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34426-328">**"Write-bufferSize"**</span><span class="sxs-lookup"><span data-stu-id="34426-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34426-329">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34426-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34426-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34426-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34426-331">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="34426-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34426-332">Schreibpuffer Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="34426-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="34426-333">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34426-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34426-334">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34426-334">Remarks</span></span>

<span data-ttu-id="34426-335">Die **CIM- \_ NFS** -Klasse wird von [**CIM \_ remotefile System**](cim-remotefilesystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="34426-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="34426-336">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="34426-336">WMI does not implement this class.</span></span>

<span data-ttu-id="34426-337">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="34426-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34426-338">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="34426-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34426-339">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34426-339">Requirements</span></span>



| <span data-ttu-id="34426-340">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34426-340">Requirement</span></span> | <span data-ttu-id="34426-341">Wert</span><span class="sxs-lookup"><span data-stu-id="34426-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34426-342">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34426-342">Minimum supported client</span></span><br/> | <span data-ttu-id="34426-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34426-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34426-344">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34426-344">Minimum supported server</span></span><br/> | <span data-ttu-id="34426-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34426-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34426-346">Namespace</span><span class="sxs-lookup"><span data-stu-id="34426-346">Namespace</span></span><br/>                | <span data-ttu-id="34426-347">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="34426-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34426-348">MOF</span><span class="sxs-lookup"><span data-stu-id="34426-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34426-349"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34426-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34426-350">DLL</span><span class="sxs-lookup"><span data-stu-id="34426-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34426-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34426-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34426-352">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34426-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34426-353">**CIM- \_ remotefile System**</span><span class="sxs-lookup"><span data-stu-id="34426-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

