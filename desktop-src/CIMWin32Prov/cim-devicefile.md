---
description: Die CIM \_ DeviceFile-Klasse stellt einen Typ einer logischen Datei dar, die ein Gerät darstellt.
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
ms.openlocfilehash: 71eefcc6a0c33f1981c6b83a03a2d4fe59acf9d438c6710e2381f887be76b5e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924520"
---
# <a name="cim_devicefile-class"></a>\_CIM-Klasse "DeviceFile"

Die **CIM \_ DeviceFile-Klasse** stellt einen Typ einer logischen Datei dar, die ein Gerät darstellt. Diese Konvention ist nützlich für Betriebssysteme, die Geräte mithilfe eines Bytestream-E/A-Modells verwalten. Das logische Gerät, das dieser Datei zugeordnet ist, wird mithilfe der [**\_ CIM-Beziehung DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) angegeben.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **CIM \_ DeviceFile-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ DeviceFile-Klasse** verfügt über diese Methoden.



| Methode                                                                                            | BESCHREIBUNG                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md)     | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | Ändert die Sicherheitsberechtigungen für die logische Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                   |
| [**Komprimieren**](compress-method-in-class-cim-devicefile.md)                                       | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-devicefile.md)                                   | Komprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                              |
| [**Kopieren**](copy-method-in-class-cim-devicefile.md)                                               | Kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort. Nicht von WMI implementiert.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-devicefile.md)                                           | Kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort. Nicht von WMI implementiert.<br/> |
| [**Löschen**](delete-method-in-class-cim-devicefile.md)                                           | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-devicefile.md)                                       | Löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-devicefile.md)           | Bestimmt, ob der Aufrufer über die durch das Permission-Argument angegebenen **aggregierten Berechtigungen** verfügt. Nicht von WMI implementiert.<br/>                |
| [**Umbenennen**](rename-method-in-class-cim-devicefile.md)                                           | Benennt die logische Datei (oder das Verzeichnis) um, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md)                             | Erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-devicefile.md)                         | Erhält den Besitz der logischen Datei, die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                                   |
| [**Dekomprimieren**](uncompress-method-in-class-cim-devicefile.md)                                   | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-devicefile.md)                               | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. Nicht von WMI implementiert.<br/>                                            |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ DeviceFile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitarray, das die Zugriffsrechte für die bestimmte Datei oder das Verzeichnis darstellt, die bzw. das vom Benutzer oder der Gruppe gehalten wird, in dessen Namen die Instanz zurückgegeben wird. Auf FAT-Volumes **wird FULL \_ ACCESS** zurückgegeben, was darauf hinweist, dass keine Sicherheit für das Objekt festgelegt wurde.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE \_ READ \_ DATA (Datei) oder FILE \_ LIST DIRECTORY \_ (Verzeichnis)** (1)


</dt> <dd>

Gewährt das Recht, Daten aus der Datei zu lesen. Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses auflisten zu können.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE \_ WRITE \_ DATA (Datei) oder FILE \_ ADD FILE \_ (Verzeichnis)** (2)


</dt> <dd>

Gewährt das Recht, Daten in die Datei zu schreiben. Für ein Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE \_ APPEND \_ DATA (Datei) oder FILE \_ ADD \_ SUBDIRECTORY (Verzeichnis)** (4)


</dt> <dd>

Gewährt das Recht, Daten an die Datei anfügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA** (8)


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu lesen.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA** (16)


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE \_ EXECUTE (File) oder FILE \_ TRAVERSE (Verzeichnis)** (32)


</dt> <dd>

Gewährt das Recht, eine Datei auszuführen. Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE \_ DELETE \_ CHILD (Verzeichnis)** (64)


</dt> <dd>

Gewährt das Recht, ein Verzeichnis und alle dateien zu löschen, die es enthält (seine unteren Elemente), auch wenn die Dateien schreibgeschützt sind.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE \_ LESEN \_ VON ATTRIBUTEN** (128)


</dt> <dd>

Gewährt das Recht, Dateiattribute zu lesen.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE \_ WRITE \_ ATTRIBUTES** (256)


</dt> <dd>

Gewährt das Recht, Dateiattribute zu ändern.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)


</dt> <dd>

Gewährt Löschzugriff.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**READ \_ CONTROL** (131072)


</dt> <dd>

Gewährt Lesezugriff auf den Sicherheitsdeskriptor und Besitzer.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE \_ DAC** (262144)


</dt> <dd>

Gewährt Schreibzugriff auf die abhängige Zugriffssteuerungsliste.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER** (524288)


</dt> <dd>

Weist den Schreibbesitzer zu.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)


</dt> <dd>

Synchronisiert den Zugriff und ermöglicht einem Prozess, auf den Eintritt eines Objekts in den signalisierten Zustand zu warten.

</dd> </dl>

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

Kurze Textbeschreibung des Objekts.

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

Freiformzeichenfolge, die den Algorithmus oder das Tool zum Komprimieren der logischen Datei angibt. Wenn das Komprimierungsschema unbekannt oder nicht beschrieben ist, verwenden Sie "Unknown". Wenn die logische Datei komprimiert ist, das Komprimierungsschema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "Compressed". Wenn die logische Datei nicht komprimiert ist, verwenden Sie "Nicht komprimiert".

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

Name der Klasse.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

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

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSCreationClassName**), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computersystemklassenname")
</dt> </dl>

Klasse des Computersystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSName**"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computersystemname")
</dt> </dl>

Name des Computersystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beschreibung")
</dt> </dl>

Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Laufwerk**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Laufwerk")
</dt> </dl>

Laufwerkbuchstabe (einschließlich des Doppelpunkts, der auf den Laufwerkbuchstaben folgt) der Datei. Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

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

DOS-kompatibler Dateiname für die Datei. Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: "c: \\ progra~1"

</dd> <dt>

**Verschlüsselt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselt")
</dt> </dl>

**True** gibt an, dass die Datei verschlüsselt ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")
</dt> </dl>

Freiformzeichenfolge, die den Algorithmus oder das Tool zum Verschlüsseln einer logischen Datei identifiziert. Wenn das Verschlüsselungsschema nicht geschützt ist (z. B. aus Sicherheitsgründen), verwenden Sie "Unknown". Wenn die Datei verschlüsselt ist, aber entweder ihr Verschlüsselungsschema unbekannt ist oder nicht offengelegt wird, verwenden Sie "Encrypted". Wenn die logische Datei nicht verschlüsselt ist, verwenden Sie "Not Encrypted".

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Erweiterung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")
</dt> </dl>

Dateinamenerweiterung ohne den vorherigen Punkt (Punkt).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Dateiname ohne Dateierweiterung.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiel: "MyDataFile"

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

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")
</dt> </dl>

Deskriptor, der den Dateityp darstellt (angegeben durch die **Extension-Eigenschaft).**

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**Name**"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateisystemname")
</dt> </dl>

Name des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

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

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Aktuelle Anzahl geöffneter Dateien")
</dt> </dl>

Anzahl der "Datei wird geöffnet", die derzeit für die Datei aktiv sind.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

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

Datum und Uhrzeit des letzten Datei-Zugriffes.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

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

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Geerbter Name, der als Schlüssel einer logischen Dateiinstanz innerhalb eines Dateisystems dient (geben Sie vollständige Pfadnamen an).

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Beispiel: "C: \\ Windows \\ System \\win.ini"

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Pfad der Datei, einschließlich vor- und nachher folgende schräge Schrägstriche. Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

Beispiel: " \\ windows \\ system \\ "

</dd> <dt>

**Lesbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")
</dt> </dl>

True **gibt an,** dass die Datei gelesen werden kann.

Diese Eigenschaft wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Betriebsstatus und nicht betriebsbereiter Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. eine SMART-fähige Festplatte).

Der nicht operative Status kann "Error", "Starting", "Stopping" und "Service" enthalten. "Dienst" kann während der Spiegelung des Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

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

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


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

Die **CIM \_ DeviceFile-Klasse** wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)abgeleitet.

WMI implementiert diese Klasse nicht.

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

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

