---
description: Die KLASSE CIM LogicalFile stellt eine benannte Sammlung von Daten dar, bei der es sich um ausführbaren Code handelt, der sich in einem Dateisystem \_ in einem Speicher extent befindet.
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
ms.openlocfilehash: 457bf0e094e4196c2ff60b05581daf5dc6a51349530d3563119962e01c94c40d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548270"
---
# <a name="cim_logicalfile-class"></a>CIM \_ LogicalFile-Klasse

Die **KLASSE CIM \_ LogicalFile** stellt eine benannte Sammlung von Daten dar, bei der es sich um ausführbaren Code handelt, der sich in einem Dateisystem in einem Speicher extent befindet.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **KLASSE CIM \_ LogicalFile** verfügt über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **KLASSE CIM \_ LogicalFile** verfügt über diese Methoden.



| Methode                                                                                             | Beschreibung                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                   |
| [**Komprimieren**](compress-method-in-class-cim-logicalfile.md)                                       | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-logicalfile.md)                                   | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                              |
| [**Kopieren**](copy-method-in-class-cim-logicalfile.md)                                               | Kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort. Nicht von WMI implementiert.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-logicalfile.md)                                           | Kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort. Nicht von WMI implementiert.<br/> |
| [**Löschen**](delete-method-in-class-cim-logicalfile.md)                                           | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-logicalfile.md)                                       | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-logicalfile.md)           | Bestimmt, ob der Aufrufer über die durch das Permission-Argument angegebenen **aggregierten Berechtigungen** verfügt. Nicht von WMI implementiert.<br/>                |
| [**Umbenennen**](rename-method-in-class-cim-logicalfile.md)                                           | Benennt die logische Datei (oder das Verzeichnis) um, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md)                             | Erhält den Besitz der logischen Datei (oder des Verzeichnisses), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                    |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-logicalfile.md)                         | Erhält den Besitz der logischen Datei (oder des Verzeichnisses), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                    |
| [**Dekomprimieren**](uncompress-method-in-class-cim-logicalfile.md)                                   | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-logicalfile.md)                               | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                            |



 

### <a name="properties"></a>Eigenschaften

Die **KLASSE CIM \_ LogicalFile** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitmaske, die die Zugriffsrechte darstellt, die erforderlich sind, um auf die Datei zu zugreifen oder bestimmte Vorgänge für die Datei durchzuführen. Bitwerte finden Sie unter [**Konstanten für Datei- und Verzeichniszugriffsrechte.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> Auf FAT-Volumes wird stattdessen **der FULL \_ ACCESS-Wert** zurückgegeben, der angibt, dass keine Sicherheit für das Objekt festgelegt wurde.

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**FILE \_ READ \_ DATA (Datei) oder FILE \_ LIST DIRECTORY \_ (Verzeichnis)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**FILE \_ WRITE \_ DATA (Datei) oder FILE \_ ADD FILE \_ (Verzeichnis)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**FILE \_ APPEND \_ DATA (Datei) oder FILE \_ ADD \_ SUBDIRECTORY (Verzeichnis)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**FILE \_ READ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**FILE \_ WRITE \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**FILE \_ EXECUTE (File) oder FILE \_ TRAVERSE (Verzeichnis)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**FILE \_ DELETE \_ CHILD (Verzeichnis)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**FILE \_ LESEN \_ VON ATTRIBUTEN** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE \_ WRITE \_ ATTRIBUTES** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**READ \_ CONTROL** (131072)


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

True **gibt an,** dass die Datei archiviert werden soll.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")
</dt> </dl>

True **gibt an,** dass die Datei komprimiert wird.

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")
</dt> </dl>

Freiformzeichenfolge, die den Algorithmus oder das Tool zum Komprimieren der logischen Datei angibt. Wenn das Komprimierungsschema unbekannt oder nicht beschrieben ist, verwenden Sie "Unknown". Wenn die logische Datei komprimiert ist, das Komprimierungsschema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "Compressed". Wenn die logische Datei nicht komprimiert ist, verwenden Sie "Nicht komprimiert".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Klassenname")
</dt> </dl>

Name der Klasse.

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")
</dt> </dl>

Datum und Uhrzeit der Dateierstellung.

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

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSName**"), [**\_ CIM-Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computersystemname")
</dt> </dl>

Name des Computersystems.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Laufwerk**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Laufwerk")
</dt> </dl>

Laufwerkbuchstaben (einschließlich des Doppelpunkts, der dem Laufwerkbuchstaben folgt) der Datei. Diese Eigenschaft wird von **CIM \_ LogicalFile geerbt.** Beispiel: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Acht Punkte drei Dateiname")
</dt> </dl>

DOS-kompatibler Dateiname. Beispiel: "c: \\ progra~1"

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

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")
</dt> </dl>

Freiformzeichenfolge, die den Algorithmus oder das Tool zum Verschlüsseln einer logischen Datei identifiziert. Wenn das Verschlüsselungsschema nicht verschlüsselt ist (z. B. aus Sicherheitsgründen), verwenden Sie "Unknown". Wenn die Datei verschlüsselt ist, ihr Verschlüsselungsschema jedoch unbekannt oder nicht offengelegt ist, verwenden Sie "Encrypted". Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "Nicht verschlüsselt".

</dd> <dt>

**Erweiterung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")
</dt> </dl>

Dateierweiterung ohne vorherigen Punkt (Punkt). Beispiel: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Dateiname ohne Dateierweiterung. Beispiel: "MyDataFile"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Größe der Datei in Bytes.

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

Deskriptor, der den durch die Extension-Eigenschaft **angegebenen Dateityp** darstellt.

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

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

True **gibt an,** dass die Datei ausgeblendet ist.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

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

Datum und Uhrzeit des letzten Zugriffs auf die Datei.

</dd> <dt>

**Lastmodified**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")
</dt> </dl>

Datum und Uhrzeit der letzten Änderung der Datei.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Dateiinstanz in einem Dateisystem dient. Vollständige Pfadnamen sollten angegeben werden. Beispiel: C: \\ Windows \\ System \\win.ini

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfad")
</dt> </dl>

Pfad der Datei, einschließlich der führenden und nachgestellten umgekehrten Schrägstriche. Beispiel: " \\ \\ Windows-System \\ "

</dd> <dt>

**Lesbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Lesbar")
</dt> </dl>

**True** gibt an, dass die Datei gelesen werden kann.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebsbereite Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Fehler" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. ein SMART-fähiges Festplattenlaufwerk).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Datenträgerspiegelung, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Administrativen Arbeiten angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ LogicalFile-Klasse** wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

WMI implementiert diese Klasse nicht. Informationen zu Klassen, die von **CIM \_ LogicalFile** abgeleitet werden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

