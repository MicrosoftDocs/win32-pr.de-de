---
description: Die CIM \_ Devicefile-Klasse stellt einen logischen Dateityp dar, der ein Gerät darstellt.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958478"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="c151c-103">CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="c151c-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="c151c-104">Die **CIM \_ Devicefile** -Klasse stellt einen logischen Dateityp dar, der ein Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="c151c-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="c151c-105">Diese Konvention eignet sich für Betriebssysteme, die Geräte mit einem Bytestream-e/a-Modell verwalten.</span><span class="sxs-lookup"><span data-stu-id="c151c-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="c151c-106">Das logische Gerät, das dieser Datei zugeordnet ist, wird mithilfe der [**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md) -Beziehung angegeben.</span><span class="sxs-lookup"><span data-stu-id="c151c-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c151c-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c151c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c151c-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c151c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c151c-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c151c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c151c-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c151c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c151c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c151c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="c151c-112">Member</span><span class="sxs-lookup"><span data-stu-id="c151c-112">Members</span></span>

<span data-ttu-id="c151c-113">Die **CIM \_ Devicefile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c151c-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="c151c-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c151c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c151c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c151c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c151c-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="c151c-116">Methods</span></span>

<span data-ttu-id="c151c-117">Die **CIM \_ Devicefile** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c151c-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="c151c-118">Methode</span><span class="sxs-lookup"><span data-stu-id="c151c-118">Method</span></span>                                                                                            | <span data-ttu-id="c151c-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c151c-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c151c-120">**Changesecurrityberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="c151c-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="c151c-121">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c151c-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c151c-123">**Changesecurritypermissionsex**</span><span class="sxs-lookup"><span data-stu-id="c151c-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="c151c-124">Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c151c-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c151c-126">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="c151c-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="c151c-127">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-128">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c151c-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="c151c-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="c151c-130">Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-131">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c151c-132">**Kopieren**</span><span class="sxs-lookup"><span data-stu-id="c151c-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="c151c-133">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c151c-134">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c151c-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="c151c-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="c151c-136">Kopiert die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) an den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c151c-137">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c151c-138">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="c151c-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="c151c-139">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-140">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c151c-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="c151c-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="c151c-142">Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-143">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c151c-144">**Geteffectiveberechtigung**</span><span class="sxs-lookup"><span data-stu-id="c151c-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="c151c-145">Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="c151c-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="c151c-146">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="c151c-147">**Benen**</span><span class="sxs-lookup"><span data-stu-id="c151c-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="c151c-148">Benennt die logische Datei (oder das Verzeichnis) um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-149">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c151c-150">**Take Ownership**</span><span class="sxs-lookup"><span data-stu-id="c151c-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="c151c-151">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c151c-152">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="c151c-153">**Takebesitzshipex**</span><span class="sxs-lookup"><span data-stu-id="c151c-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="c151c-154">Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c151c-155">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="c151c-156">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="c151c-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="c151c-157">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-158">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="c151c-159">**Nicht CompressEx**</span><span class="sxs-lookup"><span data-stu-id="c151c-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="c151c-160">Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c151c-161">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="c151c-162">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c151c-162">Properties</span></span>

<span data-ttu-id="c151c-163">Die **CIM \_ Devicefile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c151c-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c151c-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="c151c-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c151c-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-167">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")</span><span class="sxs-lookup"><span data-stu-id="c151c-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-168">Ein BitArray, das die Zugriffsrechte für die angegebene Datei bzw. das angegebene Verzeichnis für den Benutzer oder die Gruppe darstellt, in dem die Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="c151c-169">Auf FAT-Volumes wird **Vollständiger \_ Zugriff** zurückgegeben, was darauf hinweist, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c151c-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="c151c-170">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c151c-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="c151c-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-172">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="c151c-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="c151c-173">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c151c-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="c151c-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="c151c-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-175">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c151c-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="c151c-176">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c151c-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c151c-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="c151c-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-178">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="c151c-179">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c151c-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="c151c-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="c151c-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-181">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="c151c-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="c151c-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="c151c-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-183">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c151c-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="c151c-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="c151c-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-185">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c151c-185">Grants the right to execute a file.</span></span> <span data-ttu-id="c151c-186">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="c151c-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="c151c-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="c151c-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-188">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="c151c-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="c151c-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="c151c-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-190">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="c151c-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="c151c-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="c151c-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-192">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c151c-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="c151c-193"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="c151c-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-194">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c151c-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="c151c-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="c151c-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-196">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="c151c-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="c151c-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="c151c-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-198">Gewährt Schreibzugriff auf die freigegebene ACL.</span><span class="sxs-lookup"><span data-stu-id="c151c-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="c151c-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="c151c-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-200">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="c151c-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="c151c-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="c151c-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="c151c-202">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="c151c-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c151c-203">**Archivieren**</span><span class="sxs-lookup"><span data-stu-id="c151c-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-204">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-206">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")</span><span class="sxs-lookup"><span data-stu-id="c151c-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-207">**True** gibt an, dass die Datei archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c151c-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="c151c-208">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-209">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c151c-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-212">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c151c-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-213">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c151c-213">Short textual description of the object.</span></span>

<span data-ttu-id="c151c-214">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="c151c-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-218">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span><span class="sxs-lookup"><span data-stu-id="c151c-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-219">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="c151c-220">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="c151c-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-224">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")</span><span class="sxs-lookup"><span data-stu-id="c151c-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-225">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="c151c-226">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="c151c-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="c151c-227">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="c151c-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="c151c-228">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="c151c-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="c151c-229">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-230">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c151c-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-233">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="c151c-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-234">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="c151c-234">Name of the class.</span></span>

<span data-ttu-id="c151c-235">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="c151c-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-237">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c151c-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-239">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")</span><span class="sxs-lookup"><span data-stu-id="c151c-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-240">Das Erstellungsdatum der Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-240">File's creation date.</span></span>

<span data-ttu-id="c151c-241">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c151c-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-245">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")</span><span class="sxs-lookup"><span data-stu-id="c151c-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-246">Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="c151c-246">Class of the computer system.</span></span>

<span data-ttu-id="c151c-247">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c151c-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-251">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="c151c-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-252">Der Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="c151c-252">Name of the computer system.</span></span>

<span data-ttu-id="c151c-253">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-254">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c151c-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-257">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c151c-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-258">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c151c-258">Textual description of the object.</span></span>

<span data-ttu-id="c151c-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-260">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="c151c-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-263">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="c151c-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-264">Laufwerk Buchstabe (einschließlich des Doppelpunkts, der auf den Laufwerk Buchstaben folgt) der Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="c151c-265">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-266">Beispiel: "c:"</span><span class="sxs-lookup"><span data-stu-id="c151c-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-267">**Eightdotdreidateiname**</span><span class="sxs-lookup"><span data-stu-id="c151c-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-270">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")</span><span class="sxs-lookup"><span data-stu-id="c151c-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-271">Der DOS-kompatible Dateiname für die Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="c151c-272">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-273">Beispiel: "c: \\ PROGRA ~ 1"</span><span class="sxs-lookup"><span data-stu-id="c151c-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-274">**Verschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="c151c-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-275">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-277">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")</span><span class="sxs-lookup"><span data-stu-id="c151c-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-278">**True** gibt an, dass die Datei verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="c151c-279">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-280">**Verschlüsselungsmethode**</span><span class="sxs-lookup"><span data-stu-id="c151c-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-283">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")</span><span class="sxs-lookup"><span data-stu-id="c151c-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-284">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool identifiziert, das zum Verschlüsseln einer logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="c151c-285">Wenn das Verschlüsselungsschema nicht verwendet wird (z. b. aus Sicherheitsgründen), verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="c151c-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="c151c-286">Wenn die Datei verschlüsselt ist, das Verschlüsselungsschema jedoch unbekannt ist oder nicht offengelegt ist, verwenden Sie "verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="c151c-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="c151c-287">Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "nicht verschlüsselt".</span><span class="sxs-lookup"><span data-stu-id="c151c-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="c151c-288">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-289">**Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="c151c-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-292">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")</span><span class="sxs-lookup"><span data-stu-id="c151c-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-293">Dateinamenerweiterung ohne den vorangehenden Punkt (Punkt).</span><span class="sxs-lookup"><span data-stu-id="c151c-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="c151c-294">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-295">Beispiel: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="c151c-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c151c-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-299">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")</span><span class="sxs-lookup"><span data-stu-id="c151c-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-300">Dateiname ohne Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="c151c-300">File name without the file name extension.</span></span>

<span data-ttu-id="c151c-301">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-302">Beispiel: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="c151c-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-303">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="c151c-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-304">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c151c-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-306">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c151c-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-307">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c151c-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="c151c-308">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-309">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c151c-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="c151c-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-313">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")</span><span class="sxs-lookup"><span data-stu-id="c151c-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-314">Deskriptor, der den Dateityp darstellt (angegeben durch die- **Erweiterungs** Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="c151c-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="c151c-315">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-316">**"F"-Klassenname**</span><span class="sxs-lookup"><span data-stu-id="c151c-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-319">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="c151c-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-320">Klasse des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="c151c-320">Class of the file system.</span></span>

<span data-ttu-id="c151c-321">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="c151c-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-325">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")</span><span class="sxs-lookup"><span data-stu-id="c151c-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-326">Der Name des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="c151c-326">Name of the file system.</span></span>

<span data-ttu-id="c151c-327">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-328">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="c151c-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-329">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-331">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="c151c-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-332">**True** gibt an, dass die Datei ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="c151c-333">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c151c-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-335">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c151c-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c151c-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-338">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c151c-338">Date and time when the object was installed.</span></span> <span data-ttu-id="c151c-339">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c151c-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="c151c-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c151c-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-344">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")</span><span class="sxs-lookup"><span data-stu-id="c151c-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-345">Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="c151c-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="c151c-346">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-347">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c151c-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-348">**Letzter Zugriff**</span><span class="sxs-lookup"><span data-stu-id="c151c-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-349">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c151c-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-351">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")</span><span class="sxs-lookup"><span data-stu-id="c151c-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-352">Datum und Uhrzeit des letzten Zugriffs auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="c151c-353">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="c151c-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-355">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c151c-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-357">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")</span><span class="sxs-lookup"><span data-stu-id="c151c-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-358">Datum und Uhrzeit der letzten Änderung der Datei.</span><span class="sxs-lookup"><span data-stu-id="c151c-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="c151c-359">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="c151c-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-363">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c151c-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c151c-364">Geerbter Name, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems dient (Bereitstellen vollständiger Pfadnamen).</span><span class="sxs-lookup"><span data-stu-id="c151c-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="c151c-365">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c151c-366">Beispiel: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="c151c-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-367">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="c151c-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-368">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-370">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="c151c-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-371">Der Pfad der Datei, einschließlich der führenden und nachfolgenden umgekehrten Schrägstriche.</span><span class="sxs-lookup"><span data-stu-id="c151c-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="c151c-372">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-373">Beispiel: " \\ Windows \\ System \\ "</span><span class="sxs-lookup"><span data-stu-id="c151c-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="c151c-374">**Lesbare**</span><span class="sxs-lookup"><span data-stu-id="c151c-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-375">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-377">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")</span><span class="sxs-lookup"><span data-stu-id="c151c-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-378">**True** gibt an, dass die Datei gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c151c-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="c151c-379">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="c151c-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c151c-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-383">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c151c-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-384">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c151c-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="c151c-385">Der Betriebs-und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c151c-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="c151c-386">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c151c-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c151c-387">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c151c-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c151c-388">Der Status "nicht betriebsbereit" kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c151c-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c151c-389">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c151c-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c151c-390">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c151c-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c151c-391">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c151c-392">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c151c-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c151c-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c151c-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c151c-394">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c151c-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c151c-395">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c151c-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c151c-396">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c151c-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c151c-397">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c151c-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c151c-398">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c151c-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c151c-399">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c151c-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c151c-400">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c151c-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c151c-401">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c151c-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c151c-402">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c151c-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c151c-403">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c151c-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c151c-404">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c151c-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c151c-405">**System**</span><span class="sxs-lookup"><span data-stu-id="c151c-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-406">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-408">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")</span><span class="sxs-lookup"><span data-stu-id="c151c-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-409">**True** gibt an, dass die Datei eine Systemdatei ist.</span><span class="sxs-lookup"><span data-stu-id="c151c-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="c151c-410">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c151c-411">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="c151c-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c151c-412">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c151c-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c151c-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c151c-414">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")</span><span class="sxs-lookup"><span data-stu-id="c151c-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="c151c-415">**True** gibt an, dass die Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c151c-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="c151c-416">Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c151c-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c151c-417">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c151c-417">Remarks</span></span>

<span data-ttu-id="c151c-418">Die **CIM \_ Devicefile** -Klasse wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c151c-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c151c-419">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c151c-419">WMI does not implement this class.</span></span>

<span data-ttu-id="c151c-420">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c151c-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c151c-421">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c151c-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c151c-422">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c151c-422">Requirements</span></span>



| <span data-ttu-id="c151c-423">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c151c-423">Requirement</span></span> | <span data-ttu-id="c151c-424">Wert</span><span class="sxs-lookup"><span data-stu-id="c151c-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c151c-425">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c151c-425">Minimum supported client</span></span><br/> | <span data-ttu-id="c151c-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c151c-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c151c-427">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c151c-427">Minimum supported server</span></span><br/> | <span data-ttu-id="c151c-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c151c-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c151c-429">Namespace</span><span class="sxs-lookup"><span data-stu-id="c151c-429">Namespace</span></span><br/>                | <span data-ttu-id="c151c-430">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c151c-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c151c-431">MOF</span><span class="sxs-lookup"><span data-stu-id="c151c-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c151c-432"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c151c-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c151c-433">DLL</span><span class="sxs-lookup"><span data-stu-id="c151c-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c151c-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c151c-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c151c-435">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c151c-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c151c-436">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="c151c-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

