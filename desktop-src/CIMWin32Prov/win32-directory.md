---
description: Das Win32- \_ Verzeichnis&\# 32; WMI-Klasse stellt einen Verzeichniseintrag auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214246"
---
# <a name="win32_directory-class"></a><span data-ttu-id="1c275-103">Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="1c275-103">Win32\_Directory class</span></span>

<span data-ttu-id="1c275-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) des **Win32- \_ Verzeichnisses** stellt einen Verzeichniseintrag auf einem Computersystem mit Windows dar.</span><span class="sxs-lookup"><span data-stu-id="1c275-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="1c275-105">Bei einem Verzeichnis handelt es sich um einen Dateityp, der Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1c275-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="1c275-106">Beispiel: C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="1c275-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="1c275-107">**Win32 \_ Das Verzeichnis** enthält keine Verzeichnisse von Netzwerklaufwerken.</span><span class="sxs-lookup"><span data-stu-id="1c275-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="1c275-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c275-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c275-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1c275-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c275-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c275-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="1c275-111">Member</span><span class="sxs-lookup"><span data-stu-id="1c275-111">Members</span></span>

<span data-ttu-id="1c275-112">Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1c275-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="1c275-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1c275-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c275-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c275-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c275-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="1c275-115">Methods</span></span>

<span data-ttu-id="1c275-116">Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1c275-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="1c275-117">Methode</span><span class="sxs-lookup"><span data-stu-id="1c275-117">Method</span></span>                                                                                             | <span data-ttu-id="1c275-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c275-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c275-119">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="1c275-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="1c275-120">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1c275-121">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="1c275-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="1c275-122">Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1c275-123">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="1c275-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="1c275-124">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1c275-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="1c275-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="1c275-126">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1c275-127">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="1c275-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="1c275-128">Eine Klassenmethode, die die im Objekt Pfad angegebene logische Datei oder das im Objekt Pfad angegebene Verzeichnis an den Speicherort kopiert, der vom Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="1c275-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="1c275-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="1c275-130">Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den *filename* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="1c275-131">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="1c275-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="1c275-132">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="1c275-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1c275-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="1c275-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="1c275-134">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.</span><span class="sxs-lookup"><span data-stu-id="1c275-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1c275-135">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="1c275-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="1c275-136">Eine Klassenmethode, die bestimmt, ob der Aufrufer über die durch das *Berechtigungs* Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).</span><span class="sxs-lookup"><span data-stu-id="1c275-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="1c275-137">**Benen**</span><span class="sxs-lookup"><span data-stu-id="1c275-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="1c275-138">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.</span><span class="sxs-lookup"><span data-stu-id="1c275-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1c275-139">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="1c275-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="1c275-140">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="1c275-141">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="1c275-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="1c275-142">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="1c275-143">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="1c275-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="1c275-144">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="1c275-145">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="1c275-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="1c275-146">Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="1c275-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c275-147">Properties</span></span>

<span data-ttu-id="1c275-148">Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c275-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c275-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="1c275-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c275-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-152">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="1c275-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-153">Bitmaske, die die für den Zugriff auf bestimmte Vorgänge im Verzeichnis erforderlichen Zugriffsrechte darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c275-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="1c275-154">Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="1c275-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="1c275-155">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="1c275-156">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="1c275-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="1c275-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-158">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1c275-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="1c275-159">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1c275-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="1c275-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="1c275-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-161">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1c275-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="1c275-162">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c275-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="1c275-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Datei \_ Anfügen von \_ Daten (Datei) oder \_ \_ Unterverzeichnis "Datei hinzufügen** " (4)</span><span class="sxs-lookup"><span data-stu-id="1c275-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-164">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="1c275-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="1c275-165">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c275-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="1c275-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="1c275-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-167">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="1c275-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="1c275-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="1c275-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-169">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1c275-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="1c275-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="1c275-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-171">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1c275-171">Grants the right to execute a file.</span></span> <span data-ttu-id="1c275-172">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="1c275-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="1c275-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="1c275-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-174">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="1c275-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="1c275-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="1c275-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-176">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="1c275-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="1c275-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="1c275-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-178">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1c275-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="1c275-179"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="1c275-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-180">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1c275-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="1c275-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="1c275-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-182">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="1c275-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="1c275-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="1c275-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-184">Gewährt Schreibzugriff auf die freigegebene ACL.</span><span class="sxs-lookup"><span data-stu-id="1c275-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="1c275-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="1c275-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-186">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="1c275-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="1c275-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="1c275-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-188">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="1c275-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="1c275-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Zugriff \_ System \_ Sicherheit** (18809343)</span><span class="sxs-lookup"><span data-stu-id="1c275-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="1c275-190">Steuert die Fähigkeit, die SACL in der Sicherheits Beschreibung eines Objekts zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1c275-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c275-191">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="1c275-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-192">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-194">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="1c275-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-195">Gibt an, ob das Archiv Bit im Ordner festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="1c275-196">Das Archiv Bit wird von Sicherungs Programmen verwendet, um zu sichernde Dateien zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1c275-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="1c275-197">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c275-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="1c275-198">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1c275-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-202">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1c275-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-203">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c275-203">A short textual description of the object.</span></span>

<span data-ttu-id="1c275-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="1c275-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-206">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-208">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="1c275-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-209">Gibt an, ob der Ordner komprimiert wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1c275-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="1c275-210">WMI erkennt Ordner, die mithilfe von WMI selbst oder mithilfe der grafischen Benutzeroberfläche komprimiert wurden. Es wird jedoch nicht erkannt. ZIP-Dateien als komprimiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="1c275-211">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="1c275-212">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="1c275-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-216">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="1c275-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-217">Der Algorithmus oder das Tool (in der Regel eine Methode), der zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="1c275-218">Wenn es nicht möglich ist (oder nicht gewünscht), das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, aber entweder ist das Komprimierungs Schema nicht bekannt oder nicht offengelegt. und "nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="1c275-219">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-220">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1c275-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-223">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="1c275-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-224">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1c275-225">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1c275-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1c275-226">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="1c275-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-228">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c275-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-230">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="1c275-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-231">Das Datum, an dem das Dateisystem Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-231">Date that the file system object was created.</span></span> <span data-ttu-id="1c275-232">Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="1c275-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="1c275-233">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1c275-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-237">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="1c275-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-238">Der Name der Erstellungs Klasse des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="1c275-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="1c275-239">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="1c275-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-243">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="1c275-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-244">Der Name des Computers, auf dem das Dateisystem Objekt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="1c275-245">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-246">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c275-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-249">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1c275-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-250">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1c275-250">A textual description of the object.</span></span>

<span data-ttu-id="1c275-251">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-252">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="1c275-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-255">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="1c275-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-256">Laufwerk Buchstabe des Laufwerks (einschließlich Doppelpunkt), in dem das Dateisystem Objekt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="1c275-257">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="1c275-257">Example: "c:"</span></span>

<span data-ttu-id="1c275-258">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-259">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="1c275-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-262">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="1c275-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-263">MS-DOS-kompatibler Name für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="1c275-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="1c275-264">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="1c275-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="1c275-265">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-266">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="1c275-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-267">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-269">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="1c275-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-270">Gibt an, ob der Ordner verschlüsselt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="1c275-271">**True** gibt an, dass der Ordner verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="1c275-272">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-273">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="1c275-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-276">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="1c275-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-277">Der Algorithmus oder das Tool, das zum Verschlüsseln der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="1c275-278">Wenn es nicht möglich ist (oder nicht gewünscht), das Verschlüsselungsschema zu beschreiben (z. & # u. aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist. "Verschlüsselt", um darzustellen, dass die Datei verschlüsselt ist, aber entweder ist das zugehörige Verschlüsselungsschema nicht bekannt oder nicht offengelegt. und "nicht verschlüsselt", um darzustellen, dass die logische Datei nicht verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="1c275-279">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-280">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="1c275-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-283">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="1c275-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-284">Dateinamenerweiterung für das Dateisystem Objekt, ohne den Punkt (.), der die Erweiterung vom Dateinamen trennt.</span><span class="sxs-lookup"><span data-stu-id="1c275-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="1c275-285">Beispiele: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="1c275-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="1c275-286">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1c275-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-290">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="1c275-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-291">Der Dateiname (ohne den Punkt oder die Erweiterung) der Datei.</span><span class="sxs-lookup"><span data-stu-id="1c275-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="1c275-292">Beispiel: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="1c275-292">Example: "autoexec"</span></span>

<span data-ttu-id="1c275-293">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-294">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="1c275-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-295">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c275-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-297">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="1c275-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-298">Größe des Dateisystem Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1c275-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="1c275-299">Obwohl Ordner über eine **FileSize** -Eigenschaft verfügen, wird immer der Wert 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1c275-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="1c275-300">Um die Größe eines Ordners zu bestimmen, verwenden Sie FileSystemObject, oder addieren Sie die Größe aller Dateien, die im Ordner gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1c275-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="1c275-301">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c275-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1c275-302">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="1c275-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-306">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="1c275-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-307">Dateityp (angegeben durch die- **Erweiterungs** Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="1c275-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="1c275-308">Beispielsweise verfügt eine MDB-Datei wahrscheinlich über den Dateityp Microsoft Access-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1c275-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="1c275-309">Eine ASP-Datei hat wahrscheinlich den Dateityp HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="1c275-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="1c275-310">Ordner werden in der Regel einfach als Ordner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c275-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="1c275-311">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-312">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="1c275-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-315">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="1c275-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-316">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="1c275-316">Class of the file system.</span></span>

<span data-ttu-id="1c275-317">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="1c275-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-321">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="1c275-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-322">Typ des Dateisystems (NTFS, FAT, FAT32), das auf dem Laufwerk installiert ist, auf dem sich die Datei oder der Ordner befindet.</span><span class="sxs-lookup"><span data-stu-id="1c275-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="1c275-323">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-324">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="1c275-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-325">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-327">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="1c275-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-328">Gibt an, ob das Dateisystem Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="1c275-329">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="1c275-330">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c275-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-332">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c275-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-334">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="1c275-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-335">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-335">Indicates when the object was installed.</span></span> <span data-ttu-id="1c275-336">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1c275-337">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="1c275-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-339">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c275-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-341">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="1c275-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-342">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="1c275-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="1c275-343">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="1c275-344">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c275-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-345">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="1c275-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-346">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c275-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-348">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="1c275-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-349">Datum, an dem zuletzt auf die Datei zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-349">Date the file was last accessed.</span></span> <span data-ttu-id="1c275-350">Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="1c275-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="1c275-351">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="1c275-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-353">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c275-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-355">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="1c275-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-356">Datum, an dem die Datei zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c275-356">Date the file was last modified.</span></span> <span data-ttu-id="1c275-357">Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="1c275-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="1c275-358">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-359">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c275-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-362">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c275-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c275-363">Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert.</span><span class="sxs-lookup"><span data-stu-id="1c275-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="1c275-364">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c275-364">Full path names should be provided.</span></span> <span data-ttu-id="1c275-365">Beispiel: C: \\ Windows- \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="1c275-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="1c275-366">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-367">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="1c275-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-368">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-370">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="1c275-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-371">Der Pfad für die Datei.</span><span class="sxs-lookup"><span data-stu-id="1c275-371">Path for the file.</span></span> <span data-ttu-id="1c275-372">Der Pfad enthält die führenden und nachfolgenden umgekehrten Schrägstriche, aber nicht den Laufwerk Buchstaben oder den Ordnernamen.</span><span class="sxs-lookup"><span data-stu-id="1c275-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="1c275-373">Für den Ordner c: \\ Windows \\ system32 \\ WBEM lautet der Pfad \\ Windows \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="1c275-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="1c275-374">Für den Ordner c: \\ Scripts lautet der Pfad \\ .</span><span class="sxs-lookup"><span data-stu-id="1c275-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="1c275-375">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-376">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="1c275-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-377">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-379">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="1c275-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-380">Gibt an, ob Sie Elemente im Ordner lesen können.</span><span class="sxs-lookup"><span data-stu-id="1c275-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="1c275-381">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1c275-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="1c275-382">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-383">**Status**</span><span class="sxs-lookup"><span data-stu-id="1c275-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-384">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1c275-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-386">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1c275-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-387">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="1c275-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="1c275-388">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1c275-389">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="1c275-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c275-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1c275-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1c275-391">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1c275-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c275-392">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1c275-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c275-393">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1c275-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1c275-394">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1c275-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1c275-395">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1c275-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1c275-396">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="1c275-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1c275-397">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1c275-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1c275-398">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="1c275-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1c275-399">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="1c275-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1c275-400">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="1c275-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1c275-401">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="1c275-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c275-402">**System**</span><span class="sxs-lookup"><span data-stu-id="1c275-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-403">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-405">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="1c275-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-406">Gibt an, ob das Objekt eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="1c275-407">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="1c275-408">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c275-409">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="1c275-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c275-410">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c275-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1c275-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c275-412">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="1c275-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="1c275-413">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1c275-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="1c275-414">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1c275-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c275-415">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c275-415">Remarks</span></span>

<span data-ttu-id="1c275-416">Die **Win32- \_ Verzeichnis** Klasse wird vom [**CIM- \_ Verzeichnis**](cim-directory.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1c275-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="1c275-417">**Übersicht**</span><span class="sxs-lookup"><span data-stu-id="1c275-417">**Overview**</span></span>

<span data-ttu-id="1c275-418">Ordner sind Dateisystem Objekte, die andere Dateisystem Objekte enthalten sollen.</span><span class="sxs-lookup"><span data-stu-id="1c275-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="1c275-419">Dies bedeutet jedoch nicht, dass alle Ordner gleich sind.</span><span class="sxs-lookup"><span data-stu-id="1c275-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="1c275-420">Stattdessen können sich Ordner erheblich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1c275-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="1c275-421">Einige Ordner sind Betriebssystem Ordner, die in der Regel nicht durch ein Skript geändert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="1c275-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="1c275-422">Einige Ordner sind schreibgeschützt. Dies bedeutet, dass Benutzer auf den Inhalt dieses Ordners zugreifen können, ihn aber nicht hinzufügen, löschen oder ändern können.</span><span class="sxs-lookup"><span data-stu-id="1c275-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="1c275-423">Einige Ordner werden für optimalen Speicher komprimiert, während andere für Benutzer ausgeblendet und nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="1c275-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="1c275-424">WMI verwendet die **Win32- \_ Verzeichnis** Klasse zum Verwalten von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="1c275-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="1c275-425">Die in dieser Klasse verfügbaren Eigenschaften und Methoden sind mit den in der [**CIM \_ DataFile**](cim-datafile.md) -Klasse verfügbaren Eigenschaften und Methoden identisch, der Klasse, die zum Verwalten von Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c275-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="1c275-426">Dies bedeutet, dass Sie, nachdem Sie gelernt haben, wie Sie Ordner mithilfe von WMI verwalten, ohne zusätzliche Arbeit auch wissen, wie Sie Dateien verwalten.</span><span class="sxs-lookup"><span data-stu-id="1c275-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="1c275-427">Die [**Win32- \_ Unterverzeichnis**](win32-subdirectory.md) Zuordnungs Klasse wird auch zum Verwalten von Dateien und Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c275-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="1c275-428">Die **Win32- \_ Unterverzeichnis** Klasse bezieht sich auf einen Ordner und seine unmittelbaren Unterordner.</span><span class="sxs-lookup"><span data-stu-id="1c275-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="1c275-429">Beispielsweise handelt es sich bei Protokollen in der Ordnerstruktur c: \\ Scripts \\ Logs um einen Unterordner von Skripts, und Skripts sind ein Unterordner des Stamm Ordners c: \\ .</span><span class="sxs-lookup"><span data-stu-id="1c275-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="1c275-430">Protokolle werden jedoch nicht als Unterordner von "C:" betrachtet \\ .</span><span class="sxs-lookup"><span data-stu-id="1c275-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="1c275-431">Sie können die Eigenschaften eines beliebigen Ordners im Dateisystem mithilfe der **Win32- \_ Verzeichnis** Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="1c275-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="1c275-432">Die Eigenschaften, die mit dieser Klasse verfügbar sind, werden in Tabelle 11,1 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c275-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="1c275-433">Um die Eigenschaften für einen einzelnen Ordner abzurufen, erstellen Sie eine WQL-Abfrage (Windows Query Language) für die **Win32- \_ Verzeichnis** Klasse, um sicherzustellen, dass Sie den Namen des Ordners einschließen.</span><span class="sxs-lookup"><span data-stu-id="1c275-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="1c275-434">Diese Abfrage bindet z. b. an den Ordner "D: \\ Archive":</span><span class="sxs-lookup"><span data-stu-id="1c275-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="1c275-435">Wenn Sie einen Datei-oder Ordnernamen in einer WQL-Abfrage angeben, stellen Sie sicher, dass Sie Pfad Komponenten mit zwei umgekehrten Schrägstrichen ( \\ \\ ) trennen.</span><span class="sxs-lookup"><span data-stu-id="1c275-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="1c275-436">Wenn Sie das Abrufen von Daten auf ein einzelnes Laufwerk beschränken möchten, geben Sie eine WHERE-Klausel an, in der der Laufwerk Buchstabe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c275-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="1c275-437">Diese Abfrage gibt z. b. eine Liste aller Ordner auf Laufwerk C:</span><span class="sxs-lookup"><span data-stu-id="1c275-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="1c275-438">Wenn Sie alle Ordner auf einem Computer auflisten müssen, beachten Sie, dass diese Abfrage einen längeren Zeitraum in Anspruch nehmen kann.</span><span class="sxs-lookup"><span data-stu-id="1c275-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="1c275-439">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c275-439">Examples</span></span>

<span data-ttu-id="1c275-440">Das folgende VBScript-Beispiel ruft Eigenschaften für den Ordner C: \\ Scripts ab.</span><span class="sxs-lookup"><span data-stu-id="1c275-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="1c275-441">Im folgenden VBScript-Beispiel wird eine Liste aller ausgeblendeten Ordner auf einem Computer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1c275-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="1c275-442">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c275-442">Requirements</span></span>



| <span data-ttu-id="1c275-443">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c275-443">Requirement</span></span> | <span data-ttu-id="1c275-444">Wert</span><span class="sxs-lookup"><span data-stu-id="1c275-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c275-445">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c275-445">Minimum supported client</span></span><br/> | <span data-ttu-id="1c275-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c275-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c275-447">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c275-447">Minimum supported server</span></span><br/> | <span data-ttu-id="1c275-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c275-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c275-449">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c275-449">Namespace</span></span><br/>                | <span data-ttu-id="1c275-450">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c275-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c275-451">MOF</span><span class="sxs-lookup"><span data-stu-id="1c275-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c275-452"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c275-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c275-453">DLL</span><span class="sxs-lookup"><span data-stu-id="1c275-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c275-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c275-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c275-455">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c275-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c275-456">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="1c275-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="1c275-457">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1c275-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

