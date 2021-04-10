---
description: Die Win32- \_ codecfile-&\# 32; Die WMI-Klasse stellt den auf dem Computersystem installierten Audio-oder Videocodec dar.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127349"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="8b468-103">Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b468-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="8b468-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) von **Win32 \_ codecfile** stellt den auf dem Computersystem installierten Audiostream oder Videocodec dar.</span><span class="sxs-lookup"><span data-stu-id="8b468-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="8b468-105">Codecs konvertieren einen Medien Formattyp in einen anderen, üblicherweise ein komprimiertes Format in ein unkomprimiertes Format.</span><span class="sxs-lookup"><span data-stu-id="8b468-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="8b468-106">Der Name "Codec" wird von einer Kombination aus "komprimieren" und "decokomprimieren" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8b468-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="8b468-107">Ein Codec kann z. b. ein komprimiertes Format, z. b. ms-ADPCM, in ein nicht komprimiertes Format (z. b. PCM) konvertieren, das die meisten Audiohardware direkt wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="8b468-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="8b468-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b468-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8b468-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8b468-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b468-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b468-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="8b468-111">Member</span><span class="sxs-lookup"><span data-stu-id="8b468-111">Members</span></span>

<span data-ttu-id="8b468-112">Die **Win32 \_ codecfile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b468-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="8b468-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b468-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b468-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b468-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b468-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="8b468-115">Methods</span></span>

<span data-ttu-id="8b468-116">Die **Win32 \_ codecfile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8b468-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="8b468-117">Methode</span><span class="sxs-lookup"><span data-stu-id="8b468-117">Method</span></span>                                                                                             | <span data-ttu-id="8b468-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b468-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b468-119">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="8b468-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="8b468-120">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="8b468-121">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="8b468-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="8b468-122">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="8b468-123">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="8b468-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="8b468-124">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="8b468-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="8b468-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="8b468-126">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="8b468-127">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="8b468-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="8b468-128">Kopiert die im Objekt Pfad angegebene logische Datei oder das Verzeichnis in den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8b468-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="8b468-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="8b468-130">Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den filename-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="8b468-131">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="8b468-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="8b468-132">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="8b468-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="8b468-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="8b468-134">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="8b468-135">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="8b468-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="8b468-136">Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).</span><span class="sxs-lookup"><span data-stu-id="8b468-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="8b468-137">**Benen**</span><span class="sxs-lookup"><span data-stu-id="8b468-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="8b468-138">Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.</span><span class="sxs-lookup"><span data-stu-id="8b468-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="8b468-139">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="8b468-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="8b468-140">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="8b468-141">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="8b468-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="8b468-142">Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="8b468-143">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="8b468-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="8b468-144">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="8b468-145">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="8b468-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="8b468-146">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="8b468-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b468-147">Properties</span></span>

<span data-ttu-id="8b468-148">Die **Win32 \_ codecfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b468-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b468-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="8b468-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b468-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-152">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="8b468-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-153">Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge für die Codec-Datei erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="8b468-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="8b468-154">Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="8b468-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="8b468-155">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b468-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="8b468-156">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="8b468-157">**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="8b468-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="8b468-158">**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="8b468-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="8b468-159">**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="8b468-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="8b468-160">**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="8b468-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="8b468-161">**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="8b468-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="8b468-162">**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="8b468-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="8b468-163">**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="8b468-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="8b468-164">**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="8b468-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="8b468-165">**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="8b468-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="8b468-166">**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="8b468-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="8b468-167">**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="8b468-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="8b468-168">**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="8b468-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="8b468-169">**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="8b468-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="8b468-170">**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="8b468-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b468-171">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="8b468-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-174">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="8b468-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-175">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b468-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="8b468-176">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-177">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8b468-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-180">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8b468-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-181">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b468-181">Short description of the object.</span></span>

<span data-ttu-id="8b468-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="8b468-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-186">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="8b468-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-187">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="8b468-188">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="8b468-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-192">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="8b468-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-193">Der Algorithmus oder das Tool, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="8b468-194">Wenn es nicht möglich ist (oder nicht erwünscht), das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist oder nicht. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, das Komprimierungs Schema jedoch nicht bekannt ist oder nicht offengelegt ist. und "nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="8b468-195">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-196">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="8b468-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-199">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="8b468-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-200">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8b468-201">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8b468-202">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="8b468-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-204">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b468-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-206">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="8b468-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-207">Erstellungsdatum der Datei.</span><span class="sxs-lookup"><span data-stu-id="8b468-207">File creation date.</span></span>

<span data-ttu-id="8b468-208">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b468-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-212">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="8b468-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-213">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="8b468-213">Class of the computer system.</span></span>

<span data-ttu-id="8b468-214">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="8b468-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-218">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="8b468-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-219">Zeichenfolge, die den Namen des Computer Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b468-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="8b468-220">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-221">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b468-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-224">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ mediaresources \\ \\ ICM \| Description")</span><span class="sxs-lookup"><span data-stu-id="8b468-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-225">Der vollständige Name des Codec-Treibers.</span><span class="sxs-lookup"><span data-stu-id="8b468-225">Full name of the codec driver.</span></span> <span data-ttu-id="8b468-226">Diese Zeichenfolge soll in großen (beschreibenden) Leerzeichen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="8b468-227">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8b468-228">Beispiel: "Microsoft PCM Converter"</span><span class="sxs-lookup"><span data-stu-id="8b468-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-229">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="8b468-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-232">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="8b468-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-233">Laufwerk Buchstabe (einschließlich Doppelpunkt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="8b468-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="8b468-234">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-235">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="8b468-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-236">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="8b468-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-239">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="8b468-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-240">DOS-kompatibler Dateiname für diese Datei.</span><span class="sxs-lookup"><span data-stu-id="8b468-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="8b468-241">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-242">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="8b468-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-243">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="8b468-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-244">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-246">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="8b468-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-247">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="8b468-248">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-249">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="8b468-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-252">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="8b468-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-253">Der Algorithmus oder das Tool, das zum Verschlüsseln der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="8b468-254">Wenn es nicht möglich ist (oder nicht gewünscht), das Verschlüsselungsschema zu beschreiben (möglicherweise aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist oder nicht. "Verschlüsselt", um darzustellen, dass die Datei verschlüsselt ist, das zugehörige Verschlüsselungsschema jedoch nicht bekannt ist oder nicht offengelegt ist. und "nicht verschlüsselt", um darzustellen, dass die logische Datei nicht verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="8b468-255">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-256">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="8b468-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-259">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="8b468-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-260">Dateinamenerweiterung (ohne den Punkt).</span><span class="sxs-lookup"><span data-stu-id="8b468-260">File name extension (without the dot).</span></span>

<span data-ttu-id="8b468-261">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-262">Beispiele: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="8b468-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8b468-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-266">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="8b468-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-267">Der Name (ohne Erweiterung) der Datei.</span><span class="sxs-lookup"><span data-stu-id="8b468-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="8b468-268">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-269">Beispiel: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="8b468-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="8b468-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-271">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b468-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-273">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="8b468-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-274">Größe der Datei (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8b468-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="8b468-275">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-276">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8b468-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="8b468-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-280">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="8b468-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-281">Dateityp (angegeben durch die- **Erweiterungs** Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="8b468-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="8b468-282">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-283">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="8b468-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-286">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="8b468-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-287">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="8b468-287">Class of the file system.</span></span>

<span data-ttu-id="8b468-288">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="8b468-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-292">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="8b468-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-293">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="8b468-293">Name of the file system.</span></span>

<span data-ttu-id="8b468-294">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-295">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="8b468-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-298">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")</span><span class="sxs-lookup"><span data-stu-id="8b468-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-299">Der Codec, der durch diese Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b468-299">Codec represented by this class.</span></span>

<span data-ttu-id="8b468-300">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8b468-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="8b468-301">Audio</span><span class="sxs-lookup"><span data-stu-id="8b468-301">"Audio"</span></span></dd> <dd><span data-ttu-id="8b468-302">Video</span><span class="sxs-lookup"><span data-stu-id="8b468-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="8b468-303">**Audiodatei** ("Audiodatei")</span><span class="sxs-lookup"><span data-stu-id="8b468-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="8b468-304">**Video** ("Video")</span><span class="sxs-lookup"><span data-stu-id="8b468-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b468-305">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="8b468-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-306">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-308">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="8b468-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-309">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="8b468-310">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8b468-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-312">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b468-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-314">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8b468-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-315">Das Objekt wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="8b468-315">Object was installed.</span></span> <span data-ttu-id="8b468-316">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8b468-317">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="8b468-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-319">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b468-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-321">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="8b468-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-322">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="8b468-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="8b468-323">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-324">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8b468-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-325">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="8b468-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-326">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b468-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-328">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="8b468-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-329">Es wurde zuletzt auf die Datei zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="8b468-329">File was last accessed.</span></span>

<span data-ttu-id="8b468-330">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="8b468-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-332">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b468-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-334">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="8b468-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-335">Die Datei wurde zuletzt geändert.</span><span class="sxs-lookup"><span data-stu-id="8b468-335">File was last modified.</span></span>

<span data-ttu-id="8b468-336">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-337">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="8b468-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-340">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller")</span><span class="sxs-lookup"><span data-stu-id="8b468-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-341">Die Hersteller Zeichenfolge aus der Versions Ressource, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b468-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="8b468-342">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-343">**Name**</span><span class="sxs-lookup"><span data-stu-id="8b468-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-346">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b468-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b468-347">Der geerbte Name, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert.</span><span class="sxs-lookup"><span data-stu-id="8b468-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="8b468-348">Vollständige Pfadnamen müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-348">Full path names should be provided.</span></span>

<span data-ttu-id="8b468-349">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8b468-350">Beispiel: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="8b468-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-351">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="8b468-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-354">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="8b468-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-355">Der Pfad der Datei.</span><span class="sxs-lookup"><span data-stu-id="8b468-355">Path of the file.</span></span> <span data-ttu-id="8b468-356">Dies umfasst führende und nachfolgende umgekehrte Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="8b468-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="8b468-357">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8b468-358">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="8b468-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="8b468-359">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="8b468-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-360">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-362">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="8b468-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-363">Die Datei kann gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-363">File can be read.</span></span>

<span data-ttu-id="8b468-364">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="8b468-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-366">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-368">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8b468-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-369">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b468-369">Current status of the object.</span></span> <span data-ttu-id="8b468-370">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8b468-371">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="8b468-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8b468-372">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="8b468-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8b468-373">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b468-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8b468-374">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8b468-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8b468-375">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8b468-376">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8b468-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8b468-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8b468-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8b468-378">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8b468-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8b468-379">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8b468-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b468-380">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8b468-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8b468-381">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8b468-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8b468-382">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8b468-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8b468-383">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8b468-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8b468-384">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8b468-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8b468-385">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8b468-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8b468-386">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8b468-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8b468-387">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8b468-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8b468-388">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8b468-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b468-389">**System**</span><span class="sxs-lookup"><span data-stu-id="8b468-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-390">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-392">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="8b468-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-393">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="8b468-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="8b468-394">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="8b468-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-396">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b468-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-398">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="8b468-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-399">Versions Zeichenfolge aus der Versions Ressource, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b468-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="8b468-400">Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b468-401">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="8b468-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b468-402">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b468-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b468-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b468-404">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="8b468-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="8b468-405">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b468-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="8b468-406">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8b468-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b468-407">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b468-407">Remarks</span></span>

<span data-ttu-id="8b468-408">Die **Win32- \_ codecfile** -Klasse wird von [**CIM \_ DataFile**](cim-datafile.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8b468-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b468-409">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b468-409">Requirements</span></span>



| <span data-ttu-id="8b468-410">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b468-410">Requirement</span></span> | <span data-ttu-id="8b468-411">Wert</span><span class="sxs-lookup"><span data-stu-id="8b468-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b468-412">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b468-412">Minimum supported client</span></span><br/> | <span data-ttu-id="8b468-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b468-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b468-414">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b468-414">Minimum supported server</span></span><br/> | <span data-ttu-id="8b468-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b468-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b468-416">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b468-416">Namespace</span></span><br/>                | <span data-ttu-id="8b468-417">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b468-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b468-418">MOF</span><span class="sxs-lookup"><span data-stu-id="8b468-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b468-419"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b468-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b468-420">DLL</span><span class="sxs-lookup"><span data-stu-id="8b468-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b468-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b468-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b468-422">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b468-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b468-423">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="8b468-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="8b468-424">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b468-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

