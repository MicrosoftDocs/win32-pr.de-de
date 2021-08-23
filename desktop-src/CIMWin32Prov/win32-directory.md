---
description: Win32 \_ Directory&\# 32; Die WMI-Klasse stellt einen Verzeichniseintrag auf einem Computersystem dar, auf dem Windows ausgeführt wird.
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
ms.openlocfilehash: 1247a965f5d447ab2e6e86737feff96b205a6a74e3cab5e3e94cade9a2f8394c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699850"
---
# <a name="win32_directory-class"></a>Win32 \_ Directory-Klasse

Die **Win32 \_ Directory WMI-Klasse** stellt einen Verzeichniseintrag auf einem Computersystem dar, auf dem Windows ausgeführt wird. [](/windows/desktop/WmiSdk/retrieving-a-class) Ein Verzeichnis ist ein Dateityp, der Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt. Beispiel: C: \\ TEMP. **Win32 \_ Das Verzeichnis** enthält keine Verzeichnisse von Netzwerklaufwerken.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ Directory-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ Directory-Klasse** verfügt über diese Methoden.



| Methode                                                                                             | Beschreibung                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)     | Klassenmethode, die die Sicherheitsberechtigungen für die im Objektpfad angegebene logische Datei ändert.<br/>                                                                                                                        |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Klassenmethode, die die Sicherheitsberechtigungen für die im Objektpfad angegebene logische Datei ändert.<br/>                                                                                                                        |
| [**Komprimieren**](compress-method-in-class-win32-directory.md)                                       | Klassenmethode, die die logische Datei (oder das Verzeichnis) komprimiert, die im Objektpfad angegeben ist.<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | Klassenmethode, die die logische Datei (oder das Verzeichnis) komprimiert, die im Objektpfad angegeben ist.<br/>                                                                                                                                   |
| [**Kopieren**](copy-method-in-class-win32-directory.md)                                               | Klassenmethode, die die im Objektpfad angegebene logische Datei oder das im Objektpfad angegebene Verzeichnis an den speicherort kopiert, der durch den Eingabeparameter angegeben wird.<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | Klassenmethode, die die im Objektpfad angegebene logische Datei oder das im Objektpfad angegebene Verzeichnis an den Speicherort kopiert, der durch den *FileName-Parameter* angegeben wird.<br/>                                                                                   |
| [**Löschen**](delete-method-in-class-win32-directory.md)                                           | Klassenmethode, die die logische Datei (oder das Verzeichnis) löscht, die im Objektpfad angegeben ist.<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | Klassenmethode, die die logische Datei (oder das Verzeichnis) löscht, die im Objektpfad angegeben ist.<br/>                                                                                                                                      |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-directory.md)           | Klassenmethode, die bestimmt, ob der Aufrufer über die vom *Permissions-Argument* angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Dateiobjekt, sondern auch für die Freigabe, auf der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).<br/> |
| [**Umbenennen**](rename-method-in-class-win32-directory.md)                                           | Klassenmethode, die die im Objektpfad angegebene logische Datei (oder das Verzeichnis) umbenennt.<br/>                                                                                                                                      |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md)                             | Klassenmethode, die den Besitz der im Objektpfad angegebenen logischen Datei erhält.<br/>                                                                                                                                        |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-directory.md)                         | Klassenmethode, die den Besitz der im Objektpfad angegebenen logischen Datei erhält.<br/>                                                                                                                                        |
| [**Dekomprimieren**](uncompress-method-in-class-win32-directory.md)                                   | Klassenmethode, mit der die im Objektpfad angegebene logische Datei (oder das Verzeichnis) nicht mehr komprimiert wird.<br/>                                                                                                                                 |
| [**UncompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Klassenmethode, mit der die im Objektpfad angegebene logische Datei (oder das Verzeichnis) nicht mehr komprimiert wird.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Directory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitmaske, die die Zugriffsrechte darstellt, die erforderlich sind, um auf das Verzeichnis zuzugreifen oder bestimmte Vorgänge auszuführen. Bitwerte finden Sie unter [**Datei- und Verzeichniszugriffsrechtekonstanten.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> Auf FAT-Volumes wird stattdessen der **FULL \_ ACCESS-Wert** zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.

 

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE \_ READ \_ DATA (Datei) oder FILE \_ LIST DIRECTORY \_ (Verzeichnis)** (1)


</dt> <dd>

Gewährt das Recht, Daten aus der Datei zu lesen. Für ein Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE \_ WRITE \_ DATA (Datei) oder FILE \_ ADD FILE \_ (Verzeichnis)** (2)


</dt> <dd>

Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE \_ APPEND \_ DATA (File) oder FILE \_ ADD \_ SUBDIRECTORY** (4)


</dt> <dd>

Gewährt das Recht, Daten an die Datei anzufügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA** (8)


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu lesen.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ \_WRITE EA** (16)


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE \_ EXECUTE (Datei) oder FILE \_ TRAVERSE (Verzeichnis)** (32)


</dt> <dd>

Gewährt das Recht zum Ausführen einer Datei. Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE \_ DELETE \_ CHILD (Verzeichnis)** (64)


</dt> <dd>

Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Dateien) zu löschen, auch wenn die Dateien schreibgeschützt sind.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE \_ READ \_ ATTRIBUTES** (128)


</dt> <dd>

Gewährt das Recht zum Lesen von Dateiattributen.

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

<span id="READ_CONTROL"></span><span id="read_control"></span>**LESEN \_ CONTROL** (131072)


</dt> <dd>

Gewährt Lesezugriff auf den Sicherheitsdeskriptor und den Besitzer.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE \_ DAC** (262144)


</dt> <dd>

Gewährt Schreibzugriff auf die bedingte Zugriffssteuerungsliste.

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

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS \_ \_SYSTEMSICHERHEIT** (18809343)


</dt> <dd>

Steuert die Möglichkeit, die SACL in der Sicherheitsbeschreibung eines Objekts abzurufen oder festzulegen.

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

Gibt an, ob das Archivbit im Ordner festgelegt wurde. Das Archivbit wird von Sicherungsprogrammen verwendet, um Dateien zu identifizieren, die gesichert werden sollen. **True** gibt an, dass die Datei archiviert werden soll.

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

Eine kurze Textbeschreibung des Objekts.

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

Gibt an, ob der Ordner komprimiert wurde. WMI erkennt Ordner, die mithilfe von WMI selbst oder über die grafische Benutzeroberfläche komprimiert wurden. .ZIP Dateien werden jedoch nicht als komprimiert erkannt. **True** gibt an, dass die Datei komprimiert wird.

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

Algorithmus oder Tool (in der Regel eine Methode), der zum Komprimieren der logischen Datei verwendet wird. Wenn es nicht möglich (oder nicht gewünscht) ist, das Komprimierungsschema zu beschreiben (möglicherweise weil es nicht bekannt ist), verwenden Sie die folgenden Wörter: "Unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, aber entweder ihr Komprimierungsschema nicht bekannt ist oder nicht offengelegt wird; und "Nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.

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

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen dieser Klasse und ihrer Unterklassen.

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

Datum, an dem das Dateisystemobjekt erstellt wurde. Weitere Informationen zum Arbeiten mit WMI-Datums- und -Uhrzeitformaten finden Sie unter [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Erstellungsklassenname des Bereichscomputersystems.

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

Name des Computers, auf dem das Dateisystemobjekt gespeichert ist.

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

Eine Textbeschreibung des Objekts.

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

Laufwerkbuchstabe des Laufwerks (einschließlich Doppelpunkt), auf dem das Dateisystemobjekt gespeichert wird.

Beispiel: "c:"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Acht Punkte drei Dateiname")
</dt> </dl>

MS-DOS - kompatibler Name für den Ordner.

Beispiel: "c: \\ progra~1"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Verschlüsselt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselt")
</dt> </dl>

Gibt an, ob der Ordner verschlüsselt wurde. **True** gibt an, dass der Ordner verschlüsselt ist.

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

Algorithmus oder Tool zum Verschlüsseln der logischen Datei. Wenn es nicht möglich (oder nicht gewünscht) ist, das Verschlüsselungsschema zu beschreiben (möglicherweise aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "Unbekannt", um darzustellen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist. "Verschlüsselt", um darzustellen, dass die Datei verschlüsselt ist, aber entweder das Verschlüsselungsschema nicht bekannt ist oder nicht offengelegt wird; und "Nicht verschlüsselt", um darzustellen, dass die logische Datei nicht verschlüsselt ist.

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

Dateierweiterung für das Dateisystemobjekt, ohne den Punkt (.), der die Erweiterung vom Dateinamen trennt.

Beispiele: "txt", "mof", "mdb"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Dateiname (ohne Punkt oder Erweiterung) der Datei.

Beispiel: "autoexec"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Größe"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Größe des Dateisystemobjekts in Bytes. Obwohl Ordner eine **FileSize-Eigenschaft** besitzen, wird immer der Wert 0 zurückgegeben. Um die Größe eines Ordners zu bestimmen, verwenden Sie das FileSystemObject, oder fügen Sie die Größe aller im Ordner gespeicherten Dateien hinzu.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

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

Beispielsweise hat eine MDB-Datei wahrscheinlich den Dateityp Microsoft Access Application. Eine ASP-Datei weist wahrscheinlich den Dateityp HTML-Dokument auf. Ordner werden in der Regel einfach als Ordner gemeldet.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CreationClassName**"), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateisystemklassenname")
</dt> </dl>

Klasse des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**Name**), [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateisystemname")
</dt> </dl>

Typ des Dateisystems (NTFS, FAT, FAT32), das auf dem Laufwerk installiert ist, auf dem sich die Datei oder der Ordner befindet.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Gibt an, ob das Dateisystemobjekt ausgeblendet ist. **True** gibt an, dass die Datei ausgeblendet ist.

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

Datum, an dem zuletzt auf die Datei zugegriffen wurde. Weitere Informationen zum Arbeiten mit WMI-Datums- und -Uhrzeitformaten finden Sie unter [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Datum, an dem die Datei zuletzt geändert wurde. Weitere Informationen zum Arbeiten mit WMI-Datums- und -Uhrzeitformaten finden Sie unter [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Dateiinstanz in einem Dateisystem dient. Vollständige Pfadnamen sollten angegeben werden. Beispiel: C: \\ Windows \\ System \\win.ini

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfad")
</dt> </dl>

Pfad für die Datei. Der Pfad enthält die führenden und nachgestellten umgekehrten Schrägstriche, aber nicht den Laufwerkbuchstaben oder den Ordnernamen.

Für den Ordner c: \\ windows \\ system32 \\ wbem lautet der Pfad \\ windows \\ system32 \\ . Für den Ordner c: \\ scripts lautet der Pfad \\ .

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Lesbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Lesbar")
</dt> </dl>

Gibt an, ob Sie Elemente im Ordner lesen können. **True** gibt an, dass die Datei gelesen werden kann.

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

Zeichenfolge, die den aktuellen Status des Objekts angibt.

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

Gibt an, ob das Objekt eine Systemdatei ist. **True** gibt an, dass die Datei eine Systemdatei ist.

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

Die **Win32 \_ Directory-Klasse** wird von [**CIM \_ Directory**](cim-directory.md)abgeleitet.

**Übersicht**

Ordner sind Dateisystemobjekte, die andere Dateisystemobjekte enthalten sollen. Dies bedeutet jedoch nicht, dass alle Ordner gleich sind. Stattdessen können Ordner erheblich variieren. Einige Ordner sind Betriebssystemordner, die in der Regel nicht durch ein Skript geändert werden sollten. Einige Ordner sind schreibgeschützt. Das bedeutet, dass Benutzer auf den Inhalt dieses Ordners zugreifen können, diese Inhalte jedoch nicht hinzufügen, löschen oder ändern können. Einige Ordner werden für optimale Speicherung komprimiert, während andere ausgeblendet und für Benutzer nicht sichtbar sind.

WMI verwendet die **Win32 \_ Directory-Klasse** zum Verwalten von Ordnern. Die in dieser Klasse verfügbaren Eigenschaften und Methoden sind mit den Eigenschaften und Methoden identisch, die in der [**CIM \_ DataFile-Klasse,**](cim-datafile.md) der Klasse zum Verwalten von Dateien, verfügbar sind. Dies bedeutet, dass Sie, nachdem Sie gelernt haben, wie Ordner mithilfe von WMI verwaltet werden, auch ohne zusätzlichen Aufwand wissen, wie Sie Dateien verwalten.

Die [**\_ Win32-Unterverzeichniszuordnungsklasse**](win32-subdirectory.md) wird auch zum Verwalten von Dateien und Ordnern verwendet. Die **\_ Win32-Unterverzeichnisklasse** verknüpft einen Ordner und seine unmittelbaren Unterordner. Beispielsweise ist in der Ordnerstruktur C: \\ \\ Skriptprotokolle, Protokolle ein Unterordner von Skripts und Skripts ein Unterordner des Stammordners C: \\ . Protokolle gelten jedoch nicht als Unterordner von C: \\ .

Sie können die Eigenschaften eines beliebigen Ordners im Dateisystem mithilfe der **Win32 \_ Directory-Klasse** abrufen. Die mit dieser Klasse verfügbaren Eigenschaften werden in Tabelle 11.1 angezeigt. Um die Eigenschaften für einen einzelnen Ordner abzurufen, erstellen Sie eine WQL-Abfrage (Windows Query Language) für die **Win32 \_ Directory-Klasse,** und stellen Sie sicher, dass Sie den Namen des Ordners einschließen. Diese Abfrage wird beispielsweise an den Ordner D: \\ Archiv gebunden:

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

Achten Sie beim Angeben eines Datei- oder Ordnernamens in einer WQL-Abfrage darauf, dass Sie zwei umgekehrte Schrägstriche \\ \\ () verwenden, um Pfadkomponenten zu trennen.

Wenn Sie den Datenabruf auf ein einzelnes Laufwerk beschränken möchten, fügen Sie eine Where-Klausel ein, die den Laufwerkbuchstaben angibt. Diese Abfrage gibt beispielsweise eine Liste aller Ordner auf Laufwerk C zurück:

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Wenn Sie alle Ordner auf einem Computer aufzählen müssen, beachten Sie, dass diese Abfrage eine längere Zeit in Anspruch nehmen kann.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel werden Eigenschaften für den Ordner C: \\ Skripts abgerufen.


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



Im folgenden VBScript-Beispiel wird eine Liste aller ausgeblendeten Ordner auf einem Computer zurückgegeben.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



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

[**\_CIM-Verzeichnis**](cim-directory.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

