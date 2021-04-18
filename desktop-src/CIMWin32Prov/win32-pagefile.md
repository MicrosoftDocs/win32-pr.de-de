---
description: Die Win32- \_ Pagefile-&\# 32; WMI-Klasse stellt die Datei dar, die zum Verarbeiten des Austauschs von virtuellen Speicherdateien in einem Win32-System verwendet wird. Diese Klasse ist veraltet.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345456"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="3ffbd-104">Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ffbd-104">Win32\_PageFile class</span></span>

<span data-ttu-id="3ffbd-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der Win32-Auslagerungs **\_ Datei** stellt die Datei dar, die zum Verarbeiten des Austauschs virtueller Speicherdateien in einem Win32-System verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3ffbd-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="3ffbd-106">Diese Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-106">This class has been deprecated.</span></span>

<span data-ttu-id="3ffbd-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3ffbd-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffbd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ffbd-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="3ffbd-110">Member</span><span class="sxs-lookup"><span data-stu-id="3ffbd-110">Members</span></span>

<span data-ttu-id="3ffbd-111">Die **Win32- \_ Pagefile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3ffbd-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="3ffbd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3ffbd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ffbd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ffbd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ffbd-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3ffbd-114">Methods</span></span>

<span data-ttu-id="3ffbd-115">Die **Win32- \_ Pagefile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="3ffbd-116">Methode</span><span class="sxs-lookup"><span data-stu-id="3ffbd-116">Method</span></span>                                                                                            | <span data-ttu-id="3ffbd-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ffbd-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ffbd-118">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="3ffbd-119">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3ffbd-120">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="3ffbd-121">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3ffbd-122">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3ffbd-123">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3ffbd-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3ffbd-125">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3ffbd-126">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="3ffbd-127">Eine Klassenmethode, die die im Objekt Pfad angegebene logische Datei oder das im Objekt Pfad angegebene Verzeichnis an den Speicherort kopiert, der vom Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="3ffbd-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3ffbd-129">Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den filename-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3ffbd-130">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3ffbd-131">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3ffbd-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3ffbd-133">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3ffbd-134">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="3ffbd-135">Eine Klassenmethode, die bestimmt, ob der Aufrufer über die durch das *Berechtigungs* Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="3ffbd-136">**Benen**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3ffbd-137">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3ffbd-138">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="3ffbd-139">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3ffbd-140">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="3ffbd-141">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3ffbd-142">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3ffbd-143">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="3ffbd-144">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="3ffbd-145">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="3ffbd-146">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ffbd-146">Properties</span></span>

<span data-ttu-id="3ffbd-147">Die **Win32- \_ Pagefile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ffbd-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-151">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-152">Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge in der Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="3ffbd-153">Informationen zu-Werten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="3ffbd-154">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3ffbd-155">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="3ffbd-156">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3ffbd-157">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="3ffbd-158">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="3ffbd-159">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="3ffbd-160">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="3ffbd-161">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="3ffbd-162">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="3ffbd-163">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="3ffbd-164">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="3ffbd-165">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="3ffbd-166">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="3ffbd-167">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="3ffbd-168">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ffbd-169">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-172">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-173">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="3ffbd-174">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-178">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-179">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-179">A short textual description of the object.</span></span>

<span data-ttu-id="3ffbd-180">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-182">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-184">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-185">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="3ffbd-186">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-190">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-191">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3ffbd-192">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3ffbd-193">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3ffbd-194">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="3ffbd-195">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-196">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-199">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-200">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-200">Name of the class.</span></span>

<span data-ttu-id="3ffbd-201">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-203">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-205">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-206">Datum und Uhrzeit der Dateierstellung.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="3ffbd-207">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-211">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-212">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-212">Class of the computer system.</span></span>

<span data-ttu-id="3ffbd-213">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-217">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-218">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-218">Name of the computer system.</span></span>

<span data-ttu-id="3ffbd-219">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-220">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-223">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-224">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-224">A textual description of the object.</span></span>

<span data-ttu-id="3ffbd-225">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-226">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-229">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-230">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="3ffbd-231">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="3ffbd-232">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="3ffbd-232">Example: "c:"</span></span>

<span data-ttu-id="3ffbd-233">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-234">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-237">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-238">Der DOS-kompatible Dateiname.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-238">DOS-compatible file name.</span></span>

<span data-ttu-id="3ffbd-239">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="3ffbd-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="3ffbd-240">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-241">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-242">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-244">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-245">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="3ffbd-246">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-247">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-250">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-251">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="3ffbd-252">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="3ffbd-253">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="3ffbd-254">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="3ffbd-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="3ffbd-255">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-256">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-259">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-260">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="3ffbd-261">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="3ffbd-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="3ffbd-262">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-266">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-267">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-267">File name without the file name extension.</span></span> <span data-ttu-id="3ffbd-268">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="3ffbd-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="3ffbd-269">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-271">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-273">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("size"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-274">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="3ffbd-275">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3ffbd-276">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-280">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-281">Deskriptor, der den Dateityp darstellt, der von der **Erweiterungs** Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="3ffbd-282">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-284">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-286">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-287">Verfügbarer Speicherplatz in der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-287">Space available in the paging file.</span></span> <span data-ttu-id="3ffbd-288">Das Betriebssystem kann die Auslagerungs Datei je nach Bedarf vergrößern, bis die vom Benutzer festgelegten Limits erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="3ffbd-289">Diese Eigenschaft zeigt den Unterschied zwischen der Größe des aktuellen zugegebenen Speichers und der aktuellen Größe der Auslagerungs Datei an. Es wird nicht die größtmögliche Größe der Auslagerungs Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-290">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-293">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-294">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-294">Class of the file system.</span></span>

<span data-ttu-id="3ffbd-295">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-299">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-300">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-300">Name of the file system.</span></span>

<span data-ttu-id="3ffbd-301">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-302">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-303">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-305">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-306">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="3ffbd-307">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-309">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-311">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-312">Anfängliche Größe der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-314">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-316">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-317">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-317">Indicates when the object was installed.</span></span> <span data-ttu-id="3ffbd-318">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3ffbd-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-321">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-323">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-324">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="3ffbd-325">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3ffbd-326">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-327">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-328">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-330">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-331">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="3ffbd-332">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-334">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-336">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-337">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="3ffbd-338">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-339">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-342">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Hersteller")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-343">Die Hersteller Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="3ffbd-344">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-346">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-348">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-349">Maximale Größe der Auslagerungs Datei, die vom Benutzer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="3ffbd-350">Das Betriebssystem lässt nicht zu, dass die Auslagerungs Datei diesen Grenzwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-351">**Name**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-354">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| systempgefileinformation Page \| Name")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-355">Der Name der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-355">Name of the page file.</span></span>

<span data-ttu-id="3ffbd-356">Beispiel: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="3ffbd-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-357">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-360">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-361">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="3ffbd-362">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="3ffbd-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="3ffbd-363">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-364">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-365">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-367">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-368">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="3ffbd-369">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-370">**Status**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-373">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-374">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="3ffbd-375">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3ffbd-376">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3ffbd-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3ffbd-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3ffbd-378">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3ffbd-379">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ffbd-380">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3ffbd-381">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3ffbd-382">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3ffbd-383">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3ffbd-384">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3ffbd-385">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3ffbd-386">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3ffbd-387">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3ffbd-388">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ffbd-389">**System**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-390">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-392">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-393">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="3ffbd-394">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-396">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-398">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-399">Versions Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="3ffbd-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="3ffbd-400">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ffbd-401">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ffbd-402">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3ffbd-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ffbd-404">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="3ffbd-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="3ffbd-405">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="3ffbd-406">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ffbd-407">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ffbd-407">Remarks</span></span>

<span data-ttu-id="3ffbd-408">Die **Win32- \_ Pagefile** -Klasse wird vom [**CIM- \_ Verzeichnis**](cim-directory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3ffbd-409">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ffbd-409">Examples</span></span>

<span data-ttu-id="3ffbd-410">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Statistiken der Auslagerungs Datei aus Instanzen von **Win32 \_ Page File** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="3ffbd-411">Im folgenden perl-Codebeispiel wird veranschaulicht, wie Statistiken der Auslagerungs Datei aus Instanzen von **Win32 \_ Page File** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3ffbd-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3ffbd-412">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ffbd-412">Requirements</span></span>



| <span data-ttu-id="3ffbd-413">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ffbd-413">Requirement</span></span> | <span data-ttu-id="3ffbd-414">Wert</span><span class="sxs-lookup"><span data-stu-id="3ffbd-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffbd-415">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-415">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffbd-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ffbd-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ffbd-417">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ffbd-417">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffbd-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ffbd-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ffbd-419">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ffbd-419">Namespace</span></span><br/>                | <span data-ttu-id="3ffbd-420">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3ffbd-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ffbd-421">MOF</span><span class="sxs-lookup"><span data-stu-id="3ffbd-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ffbd-422"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ffbd-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ffbd-423">DLL</span><span class="sxs-lookup"><span data-stu-id="3ffbd-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ffbd-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ffbd-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ffbd-425">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ffbd-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffbd-426">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="3ffbd-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3ffbd-427">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="3ffbd-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
