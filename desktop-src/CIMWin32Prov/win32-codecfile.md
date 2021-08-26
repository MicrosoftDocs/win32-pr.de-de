---
description: Win32 \_ CodecFile&\# 32; Die WMI-Klasse stellt den Audio- oder Videocodec dar, der auf dem Computersystem installiert ist.
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
ms.openlocfilehash: 1d9f41178c69f40513b26de5221af6eb7b5e425acf5c4893f2de87fb18211291
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079910"
---
# <a name="win32_codecfile-class"></a>Win32 \_ CodecFile-Klasse

Die **Win32 CodecFile-WMI-Klasse \_** stellt den Audio- oder Videocodec dar, der auf dem Computersystem installiert ist. [](/windows/desktop/WmiSdk/retrieving-a-class) Codecs konvertieren einen Medienformattyp in einen anderen, in der Regel ein komprimiertes Format in ein nicht komprimiertes Format. Der Name "Codec" wird von einer Kombination aus Komprimierung und Dekomprimierung abgeleitet. Beispielsweise kann ein Codec ein komprimiertes Format wie MS-ADPCM in ein unkomprimiertes Format wie PCM konvertieren, das die meisten Audiohardware direkt wiedergeben kann.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ CodecFile-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ CodecFile-Klasse** verfügt über diese Methoden.



| Methode                                                                                             | Beschreibung                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist.<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist.<br/>                                                                                                                         |
| [**Komprimieren**](compress-method-in-class-win32-codecfile.md)                                       | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                    |
| [**Kopieren**](copy-method-in-class-win32-codecfile.md)                                               | Kopiert die logische Datei oder das Verzeichnis, die bzw. das im Objektpfad angegeben ist, an den speicherort, der durch den Eingabeparameter angegeben wird.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Klassenmethode, die die im Objektpfad angegebene logische Datei oder das im Objektpfad angegebene Verzeichnis an den Speicherort kopiert, der durch den FileName-Parameter angegeben wird.<br/>                                                                    |
| [**Löschen**](delete-method-in-class-win32-codecfile.md)                                           | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Bestimmt, ob der Aufrufer über die vom **Berechtigungsargument** angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Dateiobjekt, sondern auch für die Freigabe, auf der sich die Datei oder das Verzeichnis befindet (sofern es sich auf einer Freigabe befindet).<br/> |
| [**Umbenennen**](rename-method-in-class-win32-codecfile.md)                                           | Klassenmethode, die die im Objektpfad angegebene logische Datei (oder das Verzeichnis) umbenennt.<br/>                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-codecfile.md)                             | Ruft den Besitz der logischen Datei ab, die im Objektpfad angegeben ist.<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | Klassenmethode, die den Besitz der im Objektpfad angegebenen logischen Datei erhält.<br/>                                                                                                                       |
| [**Dekomprimieren**](uncompress-method-in-class-win32-codecfile.md)                                   | Entpackt die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Entpackt die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ CodecFile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitmaske, die die Zugriffsrechte darstellt, die erforderlich sind, um auf die Codecdatei zuzugreifen oder bestimmte Vorgänge auszuführen. Bitwerte finden Sie unter [**Datei- und Verzeichniszugriffsrechtekonstanten.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> Auf FAT-Volumes wird stattdessen der **FULL \_ ACCESS-Wert** zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.

 

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**FILE \_ READ \_ DATA (Datei) oder FILE \_ LIST DIRECTORY \_ (Verzeichnis)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**FILE \_ WRITE \_ DATA (Datei) oder FILE \_ ADD FILE \_ (Verzeichnis)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**FILE \_ APPEND \_ DATA (File) oder FILE \_ ADD \_ SUBDIRECTORY (Directory)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**FILE \_ READ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**FILE \_ \_WRITE EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**FILE \_ EXECUTE (Datei) oder FILE \_ TRAVERSE (Verzeichnis)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**FILE \_ DELETE \_ CHILD (Verzeichnis)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**FILE \_ READ \_ ATTRIBUTES** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE \_ WRITE \_ ATTRIBUTES** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**LESEN \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**WRITE \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**WRITE \_ OWNER** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**SYNCHRONIZE** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archivieren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sollte archiviert werden")
</dt> </dl>

**True** gibt an, dass die Datei archiviert werden soll.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("komprimiert")
</dt> </dl>

**True** gibt an, dass die Datei komprimiert wird.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungsmethode")
</dt> </dl>

Algorithmus oder Tool zum Komprimieren der logischen Datei. Wenn es nicht möglich (oder nicht gewünscht) ist, das Komprimierungsschema zu beschreiben (möglicherweise weil es nicht bekannt ist), verwenden Sie die folgenden Wörter: "Unbekannt", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist oder nicht. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, aber entweder ihr Komprimierungsschema nicht bekannt ist oder nicht offengelegt wird; und "Nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Klassenname")
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht die -Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")
</dt> </dl>

Erstellungsdatum der Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")
</dt> </dl>

Klasse des Computersystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSName**"), [**\_ CIM-Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computersystemname")
</dt> </dl>

Eine Zeichenfolge, die den Namen des Computersystems darstellt.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ icm \| Description")
</dt> </dl>

Vollständiger Name des Codectreibers. Diese Zeichenfolge soll in großen (beschreibenden) Leerzeichen angezeigt werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Beispiel: "Microsoft PCM Converter"

</dd> <dt>

**Laufwerk**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Laufwerk")
</dt> </dl>

Laufwerkbuchstaben (einschließlich Doppelpunkt) der Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiel: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Acht Punkte drei Dateiname")
</dt> </dl>

DOS-kompatibler Dateiname für diese Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiel: "c: \\ progra~1"

</dd> <dt>

**Verschlüsselt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

True **gibt an,** dass die Datei verschlüsselt ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")
</dt> </dl>

Algorithmus oder Tool zum Verschlüsseln der logischen Datei. Wenn es nicht möglich (oder nicht gewünscht) ist, das Verschlüsselungsschema zu beschreiben (möglicherweise aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "Unbekannt", um zu zeigen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist oder nicht. "Encrypted", um zu zeigen, dass die Datei verschlüsselt ist, aber entweder ihr Verschlüsselungsschema nicht bekannt oder nicht offengelegt ist; und "Not Encrypted", um zu zeigen, dass die logische Datei nicht verschlüsselt ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Erweiterung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")
</dt> </dl>

Dateierweiterung (ohne punkt).

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiele: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Name (ohne Erweiterung) der Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiel: "autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Größe der Datei (in Bytes).

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")
</dt> </dl>

Dateityp (angegeben durch die **Extension-Eigenschaft).**

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")
</dt> </dl>

Klasse des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**Name**"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateisystemname")
</dt> </dl>

Name des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Gruppe**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ drivers.desc")
</dt> </dl>

Codec, der durch diese Klasse dargestellt wird.

Die Werte sind:

<dl> <dd>"Audio"</dd> <dd>"Video"</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Audio** ("Audio")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Video** ("Video")


</dt> <dd></dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

**True** gibt an, dass die Datei ausgeblendet ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Das Objekt wurde installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")
</dt> </dl>

Anzahl der "Datei wird geöffnet", die derzeit für die Datei aktiv sind.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")
</dt> </dl>

Zuletzt wurde auf die Datei zugegriffen.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Lastmodified**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")
</dt> </dl>

Die Datei wurde zuletzt geändert.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")
</dt> </dl>

Herstellerzeichenfolge aus Versionsressource, sofern vorhanden.

Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Geerbter Name, der als Schlüssel einer logischen Dateiinstanz innerhalb eines Dateisystems dient. Vollständige Pfadnamen sollten angegeben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Beispiel: "C: \\ Windows \\ System \\win.ini"

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfad")
</dt> </dl>

Pfad der Datei. Dies schließt führende und nachfolgende umgekehrte Schrägstriche ein.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: " \\ \\ Windows-System \\ "

</dd> <dt>

**Lesbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Lesbar")
</dt> </dl>

Die Datei kann gelesen werden.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Systemdatei")
</dt> </dl>

**True** gibt an, dass die Datei eine Systemdatei ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")
</dt> </dl>

Versionszeichenfolge aus der Versionsressource, sofern vorhanden.

Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.

</dd> <dt>

**Schreibbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schreibbar")
</dt> </dl>

**True** gibt an, dass die Datei geschrieben werden kann.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ CodecFile-Klasse** wird von [**CIM \_ DataFile**](cim-datafile.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

