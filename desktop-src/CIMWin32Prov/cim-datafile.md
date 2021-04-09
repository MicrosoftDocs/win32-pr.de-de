---
description: Die CIM \_ DataFile-Klasse stellt eine benannte Auflistung von Daten oder ausführbarem Code dar. Es werden nur Instanzen von Dateien auf lokalen Festplatten Datenträgern zurückgegeben.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861272"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="ff7b4-104">CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff7b4-104">CIM\_DataFile class</span></span>

<span data-ttu-id="ff7b4-105">Die **CIM \_ DataFile** -Klasse stellt eine benannte Auflistung von Daten oder ausführbarem Code dar.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="ff7b4-106">Es werden nur Instanzen von Dateien auf lokalen Festplatten Datenträgern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff7b4-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff7b4-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff7b4-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ff7b4-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7b4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff7b4-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="ff7b4-112">Member</span><span class="sxs-lookup"><span data-stu-id="ff7b4-112">Members</span></span>

<span data-ttu-id="ff7b4-113">Die **CIM \_ DataFile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ff7b4-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="ff7b4-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ff7b4-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ff7b4-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff7b4-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ff7b4-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="ff7b4-116">Methods</span></span>

<span data-ttu-id="ff7b4-117">Die **CIM \_ DataFile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="ff7b4-118">Methode</span><span class="sxs-lookup"><span data-stu-id="ff7b4-118">Method</span></span>                                                                                          | <span data-ttu-id="ff7b4-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff7b4-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7b4-120">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="ff7b4-121">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ff7b4-122">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ff7b4-123">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="ff7b4-124">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ff7b4-125">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ff7b4-126">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="ff7b4-127">Verwendet die NTFS-Komprimierung, um die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-128">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="ff7b4-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="ff7b4-130">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-131">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="ff7b4-132">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="ff7b4-133">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ff7b4-134">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ff7b4-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="ff7b4-136">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ff7b4-137">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ff7b4-138">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="ff7b4-139">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-140">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ff7b4-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="ff7b4-142">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-143">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ff7b4-144">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="ff7b4-145">Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="ff7b4-146">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="ff7b4-147">**Benen**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="ff7b4-148">Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-149">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ff7b4-150">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="ff7b4-151">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ff7b4-152">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ff7b4-153">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="ff7b4-154">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ff7b4-155">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ff7b4-156">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="ff7b4-157">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-158">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="ff7b4-159">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="ff7b4-160">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ff7b4-161">Wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="ff7b4-162">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff7b4-162">Properties</span></span>

<span data-ttu-id="ff7b4-163">Die **CIM \_ DataFile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff7b4-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-167">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-168">Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge in der Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="ff7b4-169">Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="ff7b4-170">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="ff7b4-171">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ff7b4-172">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ff7b4-173">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ff7b4-174">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ff7b4-175">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ff7b4-176">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ff7b4-177">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ff7b4-178">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ff7b4-179">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ff7b4-180">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ff7b4-181">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ff7b4-182">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ff7b4-183">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ff7b4-184">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ff7b4-185">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ff7b4-186">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-187">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-189">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-190">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="ff7b4-191">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-195">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-196">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-196">A short textual description of the object.</span></span>

<span data-ttu-id="ff7b4-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-199">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-201">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-202">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="ff7b4-203">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-207">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-208">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="ff7b4-209">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="ff7b4-210">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="ff7b4-211">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="ff7b4-212">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-213">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-216">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-217">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-217">Name of the class.</span></span>

<span data-ttu-id="ff7b4-218">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-220">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-222">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-223">Datum und Uhrzeit der Dateierstellung.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="ff7b4-224">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-226">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-228">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-229">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-229">Class of the computer system.</span></span>

<span data-ttu-id="ff7b4-230">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-234">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-235">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-235">Name of the computer system.</span></span>

<span data-ttu-id="ff7b4-236">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-237">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-240">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-241">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-241">A textual description of the object.</span></span>

<span data-ttu-id="ff7b4-242">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-243">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-246">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-247">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="ff7b4-248">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="ff7b4-248">Example: "c:"</span></span>

<span data-ttu-id="ff7b4-249">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-250">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-253">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-254">Der DOS-kompatible Dateiname.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-254">DOS-compatible file name.</span></span>

<span data-ttu-id="ff7b4-255">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="ff7b4-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="ff7b4-256">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-257">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-258">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-260">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-261">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="ff7b4-262">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-263">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-266">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-267">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="ff7b4-268">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="ff7b4-269">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="ff7b4-270">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="ff7b4-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="ff7b4-271">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-272">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-275">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-276">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="ff7b4-277">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="ff7b4-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="ff7b4-278">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-282">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-283">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-283">File name without the file name extension.</span></span> <span data-ttu-id="ff7b4-284">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="ff7b4-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="ff7b4-285">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-286">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-287">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-289">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-290">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="ff7b4-291">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ff7b4-292">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-296">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-297">Deskriptor, der den Dateityp darstellt, der von der **Erweiterungs** Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="ff7b4-298">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-299">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-302">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-303">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-303">Class of the file system.</span></span>

<span data-ttu-id="ff7b4-304">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-308">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-309">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-309">Name of the file system.</span></span>

<span data-ttu-id="ff7b4-310">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-311">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-314">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-315">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="ff7b4-316">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-318">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-320">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-321">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-321">Indicates when the object was installed.</span></span> <span data-ttu-id="ff7b4-322">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ff7b4-323">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-325">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-327">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-328">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="ff7b4-329">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ff7b4-330">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-331">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-332">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-334">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-335">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="ff7b4-336">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-338">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-340">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-341">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="ff7b4-342">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-343">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-346">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-347">Die Hersteller Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-348">**Name**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-351">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-352">Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="ff7b4-353">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-353">Full path names should be provided.</span></span>

<span data-ttu-id="ff7b4-354">Beispiel: C: \\ Windows- \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="ff7b4-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="ff7b4-355">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-356">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-357">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-359">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-360">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="ff7b4-361">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="ff7b4-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="ff7b4-362">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-363">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-364">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-366">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-367">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="ff7b4-368">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-369">**Status**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-372">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-373">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="ff7b4-374">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ff7b4-375">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ff7b4-376">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ff7b4-377">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ff7b4-378">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ff7b4-379">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ff7b4-380">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ff7b4-381">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ff7b4-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ff7b4-382">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ff7b4-383">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ff7b4-384">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ff7b4-385">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ff7b4-386">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ff7b4-387">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ff7b4-388">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ff7b4-389">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ff7b4-390">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ff7b4-391">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ff7b4-392">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ff7b4-393">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ff7b4-394">**System**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-395">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-397">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-398">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="ff7b4-399">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-400">**Version**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-403">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-404">Versions Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ff7b4-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="ff7b4-405">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff7b4-406">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ff7b4-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff7b4-408">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="ff7b4-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="ff7b4-409">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="ff7b4-410">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff7b4-411">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff7b4-411">Remarks</span></span>

<span data-ttu-id="ff7b4-412">Die **CIM \_ DataFile** -Klasse wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ff7b4-413">WMI implementiert die **CIM \_ DataFile** -Klasse und alle zugehörigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="ff7b4-414">Die **CIM \_ DataFile** -Klasse ist eine dynamische Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="ff7b4-415">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff7b4-416">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="ff7b4-417">Aus Sicherheitsgründen unterstützt WMI das Aufrufen eines Remote Computers nicht direkt und weist ihn an, Dateien in sich selbst zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="ff7b4-418">Sie können z. b. die relevante Programmiersprache zum Abrufen von FTP oder Robocopy verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="ff7b4-419">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff7b4-419">Examples</span></span>

<span data-ttu-id="ff7b4-420">Im folgenden Skript Center- [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) wird eine **CIM \_ DataFile** -Klasse als Teil einer größeren Anwendung zum Generieren von Exchange-Umgebungs Berichten mithilfe von PowerShell verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="ff7b4-421">Das Beispiel zum Suchen nach [Dateien mit WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) -Code in der TechNet Gallery verwendet eine **CIM- \_ Datendatei** , um eine oder mehrere Dateien auf mehreren Computern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="ff7b4-422">Im folgenden VSB-Codebeispiel wird beschrieben, wie eine standardmäßige Platzhalter Suche für eine DataFile ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="ff7b4-423">Beachten Sie, dass die Trennzeichen für den umgekehrten Schrägstrich mit einem anderen umgekehrten Schrägstrich () versehen werden müssen \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="ff7b4-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="ff7b4-424">Auch, wenn "**CIM \_ DataFile**" verwendet wird.**Der Dateiname**"in der WHERE-Klausel scannt der wmiprvse-Prozess alle Verzeichnisse auf allen verfügbaren Speichergeräten.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="ff7b4-425">Dies kann einige Zeit in Anspruch nehmen, insbesondere, wenn Sie Remote Freigaben zugeordnet haben, und Sie können Virenschutz Warnungen auslöst.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="ff7b4-426">Der folgende Code Ausschnitt schränkt den Suchbereich auf ein bestimmtes Laufwerk, den Pfad und die Dateierweiterung ein.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="ff7b4-427">Im folgenden PowerShell-Codebeispiel wird ein einzelner Attribut Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ff7b4-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="ff7b4-428">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff7b4-428">Requirements</span></span>



| <span data-ttu-id="ff7b4-429">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff7b4-429">Requirement</span></span> | <span data-ttu-id="ff7b4-430">Wert</span><span class="sxs-lookup"><span data-stu-id="ff7b4-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7b4-431">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-431">Minimum supported client</span></span><br/> | <span data-ttu-id="ff7b4-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff7b4-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff7b4-433">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff7b4-433">Minimum supported server</span></span><br/> | <span data-ttu-id="ff7b4-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff7b4-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff7b4-435">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff7b4-435">Namespace</span></span><br/>                | <span data-ttu-id="ff7b4-436">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ff7b4-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff7b4-437">MOF</span><span class="sxs-lookup"><span data-stu-id="ff7b4-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff7b4-438"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ff7b4-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff7b4-439">DLL</span><span class="sxs-lookup"><span data-stu-id="ff7b4-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff7b4-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff7b4-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7b4-441">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff7b4-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7b4-442">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="ff7b4-443">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="ff7b4-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="ff7b4-444">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="ff7b4-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

