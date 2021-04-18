---
description: Die CIM \_ LogicalFile-Klasse stellt eine benannte Auflistung von Daten dar, bei der es sich um ausführbaren Code handeln kann, der sich in einem Dateisystem in einem Speicherblock befindet.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340106"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="4543d-103">CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="4543d-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="4543d-104">Die **CIM \_ LogicalFile** -Klasse stellt eine benannte Auflistung von Daten dar, bei der es sich um ausführbaren Code handeln kann, der sich in einem Dateisystem in einem Speicherblock befindet.</span><span class="sxs-lookup"><span data-stu-id="4543d-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4543d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4543d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4543d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4543d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4543d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="4543d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4543d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4543d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4543d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4543d-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="4543d-110">Member</span><span class="sxs-lookup"><span data-stu-id="4543d-110">Members</span></span>

<span data-ttu-id="4543d-111">Die **CIM \_ LogicalFile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4543d-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="4543d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4543d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4543d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4543d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4543d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="4543d-114">Methods</span></span>

<span data-ttu-id="4543d-115">Die **CIM \_ LogicalFile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4543d-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="4543d-116">Methode</span><span class="sxs-lookup"><span data-stu-id="4543d-116">Method</span></span>                                                                                             | <span data-ttu-id="4543d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4543d-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4543d-118">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="4543d-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="4543d-119">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="4543d-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="4543d-121">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="4543d-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="4543d-122">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="4543d-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="4543d-124">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="4543d-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="4543d-125">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="4543d-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="4543d-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="4543d-128">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-129">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="4543d-130">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="4543d-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="4543d-131">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="4543d-132">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="4543d-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="4543d-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="4543d-134">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="4543d-135">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="4543d-136">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="4543d-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="4543d-137">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-138">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="4543d-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="4543d-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="4543d-140">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-141">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="4543d-142">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="4543d-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="4543d-143">Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4543d-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="4543d-144">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="4543d-145">**Benen**</span><span class="sxs-lookup"><span data-stu-id="4543d-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="4543d-146">Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-147">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="4543d-148">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="4543d-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="4543d-149">Ruft den Besitz der logischen Datei (oder des Verzeichnisses) ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-150">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="4543d-151">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="4543d-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="4543d-152">Ruft den Besitz der logischen Datei (oder des Verzeichnisses) ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-153">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="4543d-154">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="4543d-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="4543d-155">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-156">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="4543d-157">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="4543d-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="4543d-158">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4543d-159">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="4543d-160">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4543d-160">Properties</span></span>

<span data-ttu-id="4543d-161">Die **CIM \_ LogicalFile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4543d-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4543d-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="4543d-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4543d-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-165">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="4543d-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-166">Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge in der Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4543d-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="4543d-167">Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="4543d-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="4543d-168">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="4543d-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="4543d-169">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="4543d-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="4543d-170">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="4543d-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="4543d-171">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="4543d-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="4543d-172">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="4543d-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="4543d-173">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="4543d-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="4543d-174">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="4543d-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="4543d-175">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="4543d-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="4543d-176">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="4543d-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="4543d-177">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="4543d-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="4543d-178">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="4543d-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="4543d-179">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="4543d-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="4543d-180">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="4543d-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="4543d-181">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="4543d-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="4543d-182">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="4543d-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4543d-183">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="4543d-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-186">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="4543d-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-187">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4543d-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4543d-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-191">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4543d-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-192">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4543d-192">A short textual description of the object.</span></span>

<span data-ttu-id="4543d-193">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4543d-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4543d-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="4543d-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-195">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-197">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="4543d-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-198">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="4543d-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-202">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="4543d-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-203">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="4543d-204">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="4543d-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="4543d-205">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="4543d-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="4543d-206">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="4543d-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="4543d-207">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4543d-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-210">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="4543d-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-211">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="4543d-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="4543d-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-213">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4543d-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-215">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="4543d-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-216">Datum und Uhrzeit der Dateierstellung.</span><span class="sxs-lookup"><span data-stu-id="4543d-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4543d-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-220">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="4543d-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-221">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="4543d-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="4543d-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-225">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="4543d-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-226">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="4543d-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-227">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4543d-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-230">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4543d-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-231">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4543d-231">A textual description of the object.</span></span>

<span data-ttu-id="4543d-232">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4543d-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4543d-233">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="4543d-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-236">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="4543d-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-237">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="4543d-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="4543d-238">Diese Eigenschaft wird von **CIM \_ LogicalFile** geerbt. Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="4543d-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="4543d-239">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="4543d-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-242">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="4543d-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-243">Der DOS-kompatible Dateiname.</span><span class="sxs-lookup"><span data-stu-id="4543d-243">DOS-compatible file name.</span></span> <span data-ttu-id="4543d-244">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="4543d-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="4543d-245">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="4543d-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-246">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-248">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="4543d-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-249">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-250">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="4543d-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-253">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="4543d-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-254">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="4543d-255">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="4543d-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="4543d-256">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="4543d-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="4543d-257">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="4543d-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="4543d-258">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="4543d-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-261">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="4543d-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-262">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="4543d-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="4543d-263">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="4543d-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="4543d-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="4543d-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-265">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-267">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="4543d-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-268">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="4543d-268">File name without the file name extension.</span></span> <span data-ttu-id="4543d-269">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="4543d-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="4543d-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="4543d-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-271">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4543d-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-273">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="4543d-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-274">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4543d-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="4543d-275">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4543d-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4543d-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="4543d-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-279">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="4543d-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-280">Deskriptor, der den Dateityp darstellt, der von der **Erweiterungs** Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-281">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="4543d-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-284">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="4543d-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-285">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="4543d-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="4543d-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-289">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="4543d-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-290">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="4543d-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-291">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="4543d-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-292">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-294">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="4543d-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-295">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4543d-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-297">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4543d-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-299">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="4543d-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-300">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4543d-300">Indicates when the object was installed.</span></span> <span data-ttu-id="4543d-301">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4543d-302">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4543d-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4543d-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="4543d-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-304">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4543d-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-306">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="4543d-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-307">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="4543d-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="4543d-308">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4543d-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4543d-309">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="4543d-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-310">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4543d-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-312">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="4543d-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-313">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="4543d-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="4543d-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-315">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4543d-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-317">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="4543d-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-318">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="4543d-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="4543d-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-322">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4543d-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4543d-323">Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="4543d-324">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4543d-324">Full path names should be provided.</span></span> <span data-ttu-id="4543d-325">Beispiel: C: \\ Windows- \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="4543d-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="4543d-326">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="4543d-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-329">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="4543d-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-330">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="4543d-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="4543d-331">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="4543d-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="4543d-332">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="4543d-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-333">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-335">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="4543d-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-336">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4543d-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="4543d-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4543d-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-340">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4543d-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-341">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="4543d-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="4543d-342">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4543d-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4543d-343">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4543d-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4543d-344">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="4543d-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4543d-345">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4543d-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4543d-346">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="4543d-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4543d-347">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="4543d-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4543d-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4543d-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4543d-349">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4543d-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4543d-350">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4543d-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4543d-351">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="4543d-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4543d-352">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="4543d-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4543d-353">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4543d-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4543d-354">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4543d-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4543d-355">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="4543d-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4543d-356">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="4543d-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4543d-357">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="4543d-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4543d-358">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="4543d-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4543d-359">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="4543d-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4543d-360">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="4543d-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4543d-361">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="4543d-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4543d-362">**System**</span><span class="sxs-lookup"><span data-stu-id="4543d-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-363">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-365">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="4543d-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-366">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="4543d-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="4543d-367">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="4543d-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4543d-368">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4543d-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4543d-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4543d-370">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="4543d-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="4543d-371">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4543d-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4543d-372">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4543d-372">Remarks</span></span>

<span data-ttu-id="4543d-373">Die **CIM \_ LogicalFile** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4543d-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="4543d-374">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4543d-374">WMI does not implement this class.</span></span> <span data-ttu-id="4543d-375">Informationen zu Klassen, die von **CIM \_ LogicalFile** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4543d-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4543d-376">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4543d-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4543d-377">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4543d-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4543d-378">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4543d-378">Requirements</span></span>



| <span data-ttu-id="4543d-379">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4543d-379">Requirement</span></span> | <span data-ttu-id="4543d-380">Wert</span><span class="sxs-lookup"><span data-stu-id="4543d-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4543d-381">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4543d-381">Minimum supported client</span></span><br/> | <span data-ttu-id="4543d-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4543d-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4543d-383">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4543d-383">Minimum supported server</span></span><br/> | <span data-ttu-id="4543d-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4543d-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4543d-385">Namespace</span><span class="sxs-lookup"><span data-stu-id="4543d-385">Namespace</span></span><br/>                | <span data-ttu-id="4543d-386">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4543d-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4543d-387">MOF</span><span class="sxs-lookup"><span data-stu-id="4543d-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4543d-388"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4543d-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4543d-389">DLL</span><span class="sxs-lookup"><span data-stu-id="4543d-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4543d-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4543d-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4543d-391">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4543d-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4543d-392">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4543d-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

