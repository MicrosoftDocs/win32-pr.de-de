---
description: Die CIM \_ -Verzeichnis Klasse stellt einen Dateityp dar, der die darin enthaltenen Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346031"
---
# <a name="cim_directory-class"></a><span data-ttu-id="bba2d-103">CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="bba2d-103">CIM\_Directory class</span></span>

<span data-ttu-id="bba2d-104">Die **CIM- \_ Verzeichnis** Klasse stellt einen Dateityp dar, der die darin enthaltenen Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bba2d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bba2d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bba2d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bba2d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bba2d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bba2d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bba2d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bba2d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba2d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba2d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="bba2d-110">Member</span><span class="sxs-lookup"><span data-stu-id="bba2d-110">Members</span></span>

<span data-ttu-id="bba2d-111">Die **CIM- \_ Verzeichnis** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bba2d-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="bba2d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="bba2d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bba2d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bba2d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bba2d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="bba2d-114">Methods</span></span>

<span data-ttu-id="bba2d-115">Die **CIM- \_ Verzeichnis** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bba2d-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="bba2d-116">Methode</span><span class="sxs-lookup"><span data-stu-id="bba2d-116">Method</span></span>                                                                                           | <span data-ttu-id="bba2d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bba2d-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bba2d-118">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="bba2d-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="bba2d-119">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="bba2d-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="bba2d-121">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="bba2d-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="bba2d-122">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="bba2d-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="bba2d-124">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="bba2d-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="bba2d-125">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="bba2d-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="bba2d-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="bba2d-128">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-129">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="bba2d-130">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="bba2d-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="bba2d-131">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bba2d-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="bba2d-132">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="bba2d-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="bba2d-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="bba2d-134">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bba2d-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="bba2d-135">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="bba2d-136">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="bba2d-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="bba2d-137">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-138">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="bba2d-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="bba2d-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="bba2d-140">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-141">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="bba2d-142">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="bba2d-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="bba2d-143">Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="bba2d-144">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="bba2d-145">**Benen**</span><span class="sxs-lookup"><span data-stu-id="bba2d-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="bba2d-146">Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-147">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="bba2d-148">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="bba2d-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="bba2d-149">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="bba2d-150">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="bba2d-151">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="bba2d-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="bba2d-152">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="bba2d-153">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="bba2d-154">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="bba2d-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="bba2d-155">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-156">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="bba2d-157">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="bba2d-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="bba2d-158">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="bba2d-159">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="bba2d-160">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bba2d-160">Properties</span></span>

<span data-ttu-id="bba2d-161">Die **CIM- \_ Verzeichnis** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bba2d-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bba2d-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="bba2d-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bba2d-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-165">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="bba2d-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-166">Bitmaske, die die für den Zugriff auf bestimmte Vorgänge im Verzeichnis erforderlichen Zugriffsrechte darstellt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="bba2d-167">Informationen zu-Werten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="bba2d-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="bba2d-168">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="bba2d-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="bba2d-169">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="bba2d-170">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="bba2d-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="bba2d-171">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="bba2d-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="bba2d-172">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="bba2d-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="bba2d-173">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="bba2d-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="bba2d-174">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="bba2d-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="bba2d-175">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="bba2d-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="bba2d-176">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="bba2d-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="bba2d-177">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="bba2d-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="bba2d-178">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="bba2d-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="bba2d-179">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="bba2d-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="bba2d-180">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="bba2d-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="bba2d-181">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="bba2d-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="bba2d-182">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="bba2d-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="bba2d-183">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="bba2d-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bba2d-184">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="bba2d-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-185">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-187">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="bba2d-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-188">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bba2d-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="bba2d-189">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bba2d-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-193">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bba2d-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-194">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bba2d-194">Short textual description of the object.</span></span>

<span data-ttu-id="bba2d-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="bba2d-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-197">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-199">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="bba2d-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-200">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="bba2d-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="bba2d-201">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="bba2d-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-205">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="bba2d-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-206">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bba2d-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="bba2d-207">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="bba2d-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="bba2d-208">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="bba2d-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="bba2d-209">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="bba2d-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="bba2d-210">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-211">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="bba2d-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-214">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="bba2d-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-215">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="bba2d-215">Name of the class.</span></span>

<span data-ttu-id="bba2d-216">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="bba2d-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-218">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="bba2d-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-220">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="bba2d-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-221">Datum und Uhrzeit, zu der die Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bba2d-221">Date and time that the file was created.</span></span>

<span data-ttu-id="bba2d-222">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bba2d-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-226">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="bba2d-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-227">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="bba2d-227">Class of the computer system.</span></span>

<span data-ttu-id="bba2d-228">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="bba2d-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-232">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="bba2d-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-233">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="bba2d-233">Name of the computer system.</span></span>

<span data-ttu-id="bba2d-234">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-235">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bba2d-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-238">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bba2d-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-239">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="bba2d-239">Textual description of the object.</span></span>

<span data-ttu-id="bba2d-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-241">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="bba2d-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-244">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="bba2d-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-245">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="bba2d-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="bba2d-246">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-247">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="bba2d-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-248">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="bba2d-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-251">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="bba2d-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-252">Der DOS-kompatible Dateiname.</span><span class="sxs-lookup"><span data-stu-id="bba2d-252">DOS-compatible file name.</span></span> <span data-ttu-id="bba2d-253">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-254">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="bba2d-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-255">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="bba2d-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-256">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-258">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="bba2d-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-259">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="bba2d-260">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-261">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="bba2d-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-264">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="bba2d-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-265">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bba2d-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="bba2d-266">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="bba2d-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="bba2d-267">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="bba2d-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="bba2d-268">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="bba2d-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="bba2d-269">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-270">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="bba2d-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-273">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="bba2d-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-274">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="bba2d-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="bba2d-275">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-276">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="bba2d-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="bba2d-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-280">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="bba2d-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-281">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="bba2d-281">File name without the file name extension.</span></span>

<span data-ttu-id="bba2d-282">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-283">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="bba2d-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-284">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="bba2d-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-285">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bba2d-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-287">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="bba2d-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-288">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bba2d-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="bba2d-289">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-290">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bba2d-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="bba2d-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-294">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="bba2d-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-295">Deskriptor, der den Dateityp darstellt (angegeben durch die- **Erweiterungs** Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="bba2d-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="bba2d-296">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-297">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="bba2d-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-300">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="bba2d-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-301">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="bba2d-301">Class of the file system.</span></span>

<span data-ttu-id="bba2d-302">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="bba2d-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-306">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="bba2d-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-307">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="bba2d-307">Name of the file system.</span></span>

<span data-ttu-id="bba2d-308">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-309">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="bba2d-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-310">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-312">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="bba2d-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-313">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="bba2d-314">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bba2d-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-316">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="bba2d-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-318">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="bba2d-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-319">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bba2d-319">Date and time when the object was installed.</span></span> <span data-ttu-id="bba2d-320">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bba2d-321">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="bba2d-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-323">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bba2d-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-325">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="bba2d-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-326">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="bba2d-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="bba2d-327">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-328">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bba2d-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-329">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="bba2d-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-330">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="bba2d-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-332">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="bba2d-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-333">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="bba2d-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="bba2d-334">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="bba2d-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-336">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="bba2d-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-338">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="bba2d-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-339">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="bba2d-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="bba2d-340">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-341">**Name**</span><span class="sxs-lookup"><span data-stu-id="bba2d-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-344">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bba2d-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-345">Geerbter Name, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems dient (Bereitstellen vollständiger Pfadnamen).</span><span class="sxs-lookup"><span data-stu-id="bba2d-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="bba2d-346">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bba2d-347">Beispiel: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="bba2d-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-348">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="bba2d-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-351">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="bba2d-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-352">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="bba2d-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="bba2d-353">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-354">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="bba2d-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-355">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="bba2d-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-356">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-358">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="bba2d-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-359">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="bba2d-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="bba2d-360">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="bba2d-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bba2d-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-364">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="bba2d-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-365">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="bba2d-366">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bba2d-367">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="bba2d-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bba2d-368">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bba2d-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bba2d-369">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="bba2d-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bba2d-370">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="bba2d-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bba2d-371">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="bba2d-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bba2d-372">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="bba2d-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bba2d-373">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="bba2d-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bba2d-374">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="bba2d-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bba2d-375">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="bba2d-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bba2d-376">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="bba2d-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bba2d-377">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="bba2d-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bba2d-378">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="bba2d-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bba2d-379">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="bba2d-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bba2d-380">**System**</span><span class="sxs-lookup"><span data-stu-id="bba2d-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-381">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-383">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="bba2d-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-384">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="bba2d-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="bba2d-385">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba2d-386">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="bba2d-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba2d-387">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bba2d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba2d-389">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="bba2d-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="bba2d-390">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="bba2d-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="bba2d-391">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bba2d-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bba2d-392">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bba2d-392">Remarks</span></span>

<span data-ttu-id="bba2d-393">Die **CIM- \_ Verzeichnis** Klasse wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bba2d-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="bba2d-394">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bba2d-394">WMI does not implement this class.</span></span> <span data-ttu-id="bba2d-395">Weitere Informationen zu Klassen, die vom **CIM- \_ Verzeichnis** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bba2d-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bba2d-396">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bba2d-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bba2d-397">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bba2d-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba2d-398">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bba2d-398">Requirements</span></span>



| <span data-ttu-id="bba2d-399">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bba2d-399">Requirement</span></span> | <span data-ttu-id="bba2d-400">Wert</span><span class="sxs-lookup"><span data-stu-id="bba2d-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba2d-401">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bba2d-401">Minimum supported client</span></span><br/> | <span data-ttu-id="bba2d-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bba2d-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bba2d-403">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bba2d-403">Minimum supported server</span></span><br/> | <span data-ttu-id="bba2d-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bba2d-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bba2d-405">Namespace</span><span class="sxs-lookup"><span data-stu-id="bba2d-405">Namespace</span></span><br/>                | <span data-ttu-id="bba2d-406">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bba2d-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bba2d-407">MOF</span><span class="sxs-lookup"><span data-stu-id="bba2d-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba2d-408"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bba2d-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba2d-409">DLL</span><span class="sxs-lookup"><span data-stu-id="bba2d-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba2d-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba2d-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba2d-411">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bba2d-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba2d-412">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="bba2d-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

