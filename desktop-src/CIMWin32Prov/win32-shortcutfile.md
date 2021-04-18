---
description: Der Win32- \_ shortcutfile-&\# 32; Die WMI-Klasse stellt Dateien dar, die Verknüpfungen zu anderen Dateien, Verzeichnissen und Befehlen darstellen.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344627"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="60b9b-103">Win32- \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="60b9b-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="60b9b-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ shortcutfile** stellt Dateien dar, die Verknüpfungen zu anderen Dateien, Verzeichnissen und Befehlen darstellen.</span><span class="sxs-lookup"><span data-stu-id="60b9b-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="60b9b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60b9b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="60b9b-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="60b9b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b9b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b9b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
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
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="60b9b-108">Member</span><span class="sxs-lookup"><span data-stu-id="60b9b-108">Members</span></span>

<span data-ttu-id="60b9b-109">Die **Win32- \_ shortcutfile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60b9b-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="60b9b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="60b9b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="60b9b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60b9b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60b9b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="60b9b-112">Methods</span></span>

<span data-ttu-id="60b9b-113">Die **Win32- \_ shortcutfile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60b9b-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="60b9b-114">Methode</span><span class="sxs-lookup"><span data-stu-id="60b9b-114">Method</span></span>                                                                                                | <span data-ttu-id="60b9b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60b9b-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60b9b-116">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="60b9b-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="60b9b-117">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="60b9b-118">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="60b9b-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="60b9b-119">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="60b9b-120">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="60b9b-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="60b9b-121">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="60b9b-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="60b9b-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="60b9b-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="60b9b-123">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="60b9b-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="60b9b-124">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="60b9b-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="60b9b-125">Eine Klassenmethode, die die im Objekt Pfad angegebene logische Datei oder das im Objekt Pfad angegebene Verzeichnis an den Speicherort kopiert, der vom Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="60b9b-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="60b9b-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="60b9b-127">Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="60b9b-128">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="60b9b-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="60b9b-129">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="60b9b-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="60b9b-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="60b9b-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="60b9b-131">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="60b9b-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="60b9b-132">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="60b9b-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="60b9b-133">Eine Klassenmethode, die bestimmt, ob der Aufrufer über die durch das Berechtigungs Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).</span><span class="sxs-lookup"><span data-stu-id="60b9b-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="60b9b-134">**Benen**</span><span class="sxs-lookup"><span data-stu-id="60b9b-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="60b9b-135">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="60b9b-136">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="60b9b-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="60b9b-137">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="60b9b-138">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="60b9b-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="60b9b-139">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="60b9b-140">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="60b9b-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="60b9b-141">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="60b9b-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="60b9b-142">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="60b9b-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="60b9b-143">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="60b9b-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="60b9b-144">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60b9b-144">Properties</span></span>

<span data-ttu-id="60b9b-145">Die **Win32- \_ shortcutfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60b9b-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60b9b-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="60b9b-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b9b-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-149">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="60b9b-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-150">Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge in der Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="60b9b-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="60b9b-151">Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="60b9b-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="60b9b-152">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="60b9b-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="60b9b-153">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="60b9b-154">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="60b9b-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="60b9b-155">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="60b9b-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="60b9b-156">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="60b9b-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="60b9b-157">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="60b9b-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="60b9b-158">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="60b9b-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="60b9b-159">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="60b9b-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="60b9b-160">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="60b9b-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="60b9b-161">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="60b9b-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="60b9b-162">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="60b9b-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="60b9b-163">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="60b9b-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="60b9b-164">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="60b9b-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="60b9b-165">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="60b9b-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="60b9b-166">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="60b9b-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="60b9b-167">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="60b9b-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b9b-168">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="60b9b-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-169">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-171">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="60b9b-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-172">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60b9b-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="60b9b-173">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60b9b-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-177">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="60b9b-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-178">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="60b9b-178">A short textual description of the object.</span></span>

<span data-ttu-id="60b9b-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="60b9b-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-181">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-183">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="60b9b-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-184">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="60b9b-185">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="60b9b-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-189">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="60b9b-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-190">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="60b9b-191">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="60b9b-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="60b9b-192">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="60b9b-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="60b9b-193">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="60b9b-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="60b9b-194">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-195">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="60b9b-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-198">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="60b9b-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-199">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="60b9b-199">Name of the class.</span></span>

<span data-ttu-id="60b9b-200">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="60b9b-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-202">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60b9b-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-204">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="60b9b-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-205">Datum und Uhrzeit der Dateierstellung.</span><span class="sxs-lookup"><span data-stu-id="60b9b-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="60b9b-206">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60b9b-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-210">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="60b9b-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-211">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="60b9b-211">Class of the computer system.</span></span>

<span data-ttu-id="60b9b-212">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="60b9b-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-216">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="60b9b-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-217">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="60b9b-217">Name of the computer system.</span></span>

<span data-ttu-id="60b9b-218">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-219">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60b9b-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-222">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="60b9b-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-223">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="60b9b-223">A textual description of the object.</span></span>

<span data-ttu-id="60b9b-224">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-225">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="60b9b-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-226">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-228">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="60b9b-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-229">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="60b9b-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="60b9b-230">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="60b9b-230">Example: "c:"</span></span>

<span data-ttu-id="60b9b-231">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-232">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="60b9b-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-235">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="60b9b-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-236">Der Dateiname im 8,3-Format.</span><span class="sxs-lookup"><span data-stu-id="60b9b-236">File name in 8.3 format.</span></span>

<span data-ttu-id="60b9b-237">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="60b9b-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="60b9b-238">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-239">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="60b9b-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-240">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-242">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="60b9b-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-243">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="60b9b-244">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-245">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="60b9b-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-248">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="60b9b-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-249">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="60b9b-250">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="60b9b-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="60b9b-251">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="60b9b-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="60b9b-252">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="60b9b-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="60b9b-253">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-254">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="60b9b-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-257">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="60b9b-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-258">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="60b9b-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="60b9b-259">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="60b9b-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="60b9b-260">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="60b9b-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-264">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="60b9b-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-265">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="60b9b-265">File name without the file name extension.</span></span>

<span data-ttu-id="60b9b-266">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="60b9b-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="60b9b-267">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-268">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="60b9b-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60b9b-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-271">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("size"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="60b9b-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-272">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="60b9b-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="60b9b-273">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60b9b-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="60b9b-274">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="60b9b-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-278">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="60b9b-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-279">Deskriptor, der den Dateityp darstellt, der von der **Erweiterungs** Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="60b9b-280">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-281">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="60b9b-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-284">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="60b9b-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-285">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="60b9b-285">Class of the file system.</span></span>

<span data-ttu-id="60b9b-286">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="60b9b-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-290">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="60b9b-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-291">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="60b9b-291">Name of the file system.</span></span>

<span data-ttu-id="60b9b-292">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-293">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="60b9b-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-294">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-296">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="60b9b-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-297">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="60b9b-298">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60b9b-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-300">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60b9b-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-302">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="60b9b-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-303">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="60b9b-303">Indicates when the object was installed.</span></span> <span data-ttu-id="60b9b-304">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="60b9b-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="60b9b-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-307">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60b9b-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-309">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="60b9b-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-310">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="60b9b-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="60b9b-311">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="60b9b-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="60b9b-312">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-313">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="60b9b-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-314">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60b9b-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-316">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="60b9b-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-317">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="60b9b-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="60b9b-318">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="60b9b-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-320">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60b9b-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-322">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="60b9b-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-323">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="60b9b-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="60b9b-324">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-325">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="60b9b-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-328">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Hersteller")</span><span class="sxs-lookup"><span data-stu-id="60b9b-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-329">Die Hersteller Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="60b9b-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="60b9b-330">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-331">**Name**</span><span class="sxs-lookup"><span data-stu-id="60b9b-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-334">Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="60b9b-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-335">Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert.</span><span class="sxs-lookup"><span data-stu-id="60b9b-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="60b9b-336">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60b9b-336">Full path names should be provided.</span></span>

<span data-ttu-id="60b9b-337">Beispiel: C: \\ Windows- \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="60b9b-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="60b9b-338">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-339">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="60b9b-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-342">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="60b9b-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-343">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="60b9b-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="60b9b-344">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="60b9b-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="60b9b-345">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-346">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="60b9b-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-347">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-349">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="60b9b-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-350">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="60b9b-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="60b9b-351">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="60b9b-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-355">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="60b9b-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-356">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="60b9b-357">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="60b9b-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="60b9b-358">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="60b9b-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="60b9b-359">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="60b9b-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="60b9b-360">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="60b9b-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="60b9b-361">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="60b9b-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="60b9b-362">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="60b9b-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="60b9b-363">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="60b9b-364">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="60b9b-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="60b9b-365">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="60b9b-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="60b9b-366">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="60b9b-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="60b9b-367">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="60b9b-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60b9b-368">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="60b9b-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="60b9b-369">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="60b9b-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="60b9b-370">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="60b9b-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="60b9b-371">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="60b9b-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="60b9b-372">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="60b9b-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="60b9b-373">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="60b9b-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="60b9b-374">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="60b9b-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="60b9b-375">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="60b9b-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="60b9b-376">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="60b9b-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60b9b-377">**System**</span><span class="sxs-lookup"><span data-stu-id="60b9b-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-378">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-380">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="60b9b-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-381">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="60b9b-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="60b9b-382">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-383">**Target**</span><span class="sxs-lookup"><span data-stu-id="60b9b-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-384">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-386">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ beginthreadex")</span><span class="sxs-lookup"><span data-stu-id="60b9b-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-387">Der Name des Objekts, zu dem diese Verknüpfung gehört.</span><span class="sxs-lookup"><span data-stu-id="60b9b-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-388">**Version**</span><span class="sxs-lookup"><span data-stu-id="60b9b-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-389">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60b9b-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-391">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) (Win32), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="60b9b-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-392">Versions Zeichenfolge aus der Versions Ressource (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="60b9b-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="60b9b-393">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b9b-394">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="60b9b-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b9b-395">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60b9b-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b9b-397">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="60b9b-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="60b9b-398">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="60b9b-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="60b9b-399">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60b9b-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b9b-400">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60b9b-400">Remarks</span></span>

<span data-ttu-id="60b9b-401">Die **Win32-Klasse \_ shortcutfile** wird von [**CIM \_ DataFile**](cim-datafile.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="60b9b-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60b9b-402">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b9b-402">Requirements</span></span>



| <span data-ttu-id="60b9b-403">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b9b-403">Requirement</span></span> | <span data-ttu-id="60b9b-404">Wert</span><span class="sxs-lookup"><span data-stu-id="60b9b-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b9b-405">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60b9b-405">Minimum supported client</span></span><br/> | <span data-ttu-id="60b9b-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60b9b-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60b9b-407">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60b9b-407">Minimum supported server</span></span><br/> | <span data-ttu-id="60b9b-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60b9b-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60b9b-409">Namespace</span><span class="sxs-lookup"><span data-stu-id="60b9b-409">Namespace</span></span><br/>                | <span data-ttu-id="60b9b-410">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60b9b-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60b9b-411">MOF</span><span class="sxs-lookup"><span data-stu-id="60b9b-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b9b-412"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60b9b-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b9b-413">DLL</span><span class="sxs-lookup"><span data-stu-id="60b9b-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b9b-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b9b-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b9b-415">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b9b-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b9b-416">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="60b9b-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="60b9b-417">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="60b9b-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
