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
# <a name="win32_directory-class"></a>Win32- \_ Verzeichnis Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) des **Win32- \_ Verzeichnisses** stellt einen Verzeichniseintrag auf einem Computersystem mit Windows dar. Bei einem Verzeichnis handelt es sich um einen Dateityp, der Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt. Beispiel: C: \\ Temp. **Win32 \_ Das Verzeichnis** enthält keine Verzeichnisse von Netzwerklaufwerken.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Methoden.



| Methode                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Changesecurrityberechtigungen**](changesecuritypermissions-method-in-class-win32-directory.md)     | Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.<br/>                                                                                                                        |
| [**Changesecurritypermissionsex**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Klassenmethode, die die Sicherheits Berechtigungen für die logische Datei ändert, die im Objekt Pfad angegeben ist.<br/>                                                                                                                        |
| [**Komprimieren**](compress-method-in-class-win32-directory.md)                                       | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) komprimiert.<br/>                                                                                                                                   |
| [**Kopieren**](copy-method-in-class-win32-directory.md)                                               | Eine Klassenmethode, die die im Objekt Pfad angegebene logische Datei oder das im Objekt Pfad angegebene Verzeichnis an den Speicherort kopiert, der vom Eingabeparameter angegeben wird.<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den *filename* -Parameter angegeben wird.<br/>                                                                                   |
| [**Lösch**](delete-method-in-class-win32-directory.md)                                           | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) löscht.<br/>                                                                                                                                      |
| [**Geteffectiveberechtigung**](geteffectivepermission-method-in-class-win32-directory.md)           | Eine Klassenmethode, die bestimmt, ob der Aufrufer über die durch das *Berechtigungs* Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).<br/> |
| [**Benen**](rename-method-in-class-win32-directory.md)                                           | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.<br/>                                                                                                                                      |
| [**Take Ownership**](takeownership-method-in-class-win32-directory.md)                             | Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.<br/>                                                                                                                                        |
| [**Takebesitzshipex**](takeownershipex-method-in-class-win32-directory.md)                         | Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.<br/>                                                                                                                                        |
| [**Dekomprimieren**](uncompress-method-in-class-win32-directory.md)                                   | Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.<br/>                                                                                                                                 |
| [**Nicht CompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Class-Methode, die die im Objekt Pfad angegebene logische Datei (oder das angegebene Verzeichnis) entkomprimiert.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Verzeichnis** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitmaske, die die für den Zugriff auf bestimmte Vorgänge im Verzeichnis erforderlichen Zugriffsrechte darstellt. Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.

 

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)


</dt> <dd>

Gewährt das Recht, Daten aus der Datei zu lesen. Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)


</dt> <dd>

Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Datei \_ Anfügen von \_ Daten (Datei) oder \_ \_ Unterverzeichnis "Datei hinzufügen** " (4)


</dt> <dd>

Gewährt das Recht zum Anfügen von Daten an die Datei. Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8)


</dt> <dd>

Gewährt das Recht zum Lesen erweiterter Attribute.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16)


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)


</dt> <dd>

Gewährt das Recht, eine Datei auszuführen. Für ein Verzeichnis kann das Verzeichnis durchsucht werden.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)


</dt> <dd>

Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128)


</dt> <dd>

Gewährt das Recht zum Lesen von Dateiattributen.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256)


</dt> <dd>

Erteilt das Recht, Dateiattribute zu ändern.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Löschen** (65536)


</dt> <dd>

Gewährt Lösch Zugriff.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072)


</dt> <dd>

Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144)


</dt> <dd>

Gewährt Schreibzugriff auf die freigegebene ACL.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288)


</dt> <dd>

Weist den Schreib Besitzer zu.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576)


</dt> <dd>

Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Zugriff \_ System \_ Sicherheit** (18809343)


</dt> <dd>

Steuert die Fähigkeit, die SACL in der Sicherheits Beschreibung eines Objekts zu erhalten oder festzulegen.

</dd> </dl>

</dd> <dt>

**Archivieren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")
</dt> </dl>

Gibt an, ob das Archiv Bit im Ordner festgelegt wurde. Das Archiv Bit wird von Sicherungs Programmen verwendet, um zu sichernde Dateien zu identifizieren. **True** gibt an, dass die Datei archiviert werden soll.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")
</dt> </dl>

Gibt an, ob der Ordner komprimiert wurde oder nicht. WMI erkennt Ordner, die mithilfe von WMI selbst oder mithilfe der grafischen Benutzeroberfläche komprimiert wurden. Es wird jedoch nicht erkannt. ZIP-Dateien als komprimiert. **True** gibt an, dass die Datei komprimiert wird.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Komprimierungs Methode")
</dt> </dl>

Der Algorithmus oder das Tool (in der Regel eine Methode), der zum Komprimieren der logischen Datei verwendet wird. Wenn es nicht möglich ist (oder nicht gewünscht), das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, aber entweder ist das Komprimierungs Schema nicht bekannt oder nicht offengelegt. und "nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Erstellungsdatum")
</dt> </dl>

Das Datum, an dem das Dateisystem Objekt erstellt wurde. Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**CSCreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System-Klassenname ")
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Computer Systems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Csname**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")
</dt> </dl>

Der Name des Computers, auf dem das Dateisystem Objekt gespeichert wird.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Laufwerk**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Laufwerk Buchstabe des Laufwerks (einschließlich Doppelpunkt), in dem das Dateisystem Objekt gespeichert wird.

Beispiel: "c:"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Eightdotdreidateiname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")
</dt> </dl>

MS-DOS-kompatibler Name für den Ordner.

Beispiel: "c: \\ PROGRA ~ 1"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Verschlüsselt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")
</dt> </dl>

Gibt an, ob der Ordner verschlüsselt wurde. **True** gibt an, dass der Ordner verschlüsselt ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Verschlüsselungsmethode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Verschlüsselungsmethode")
</dt> </dl>

Der Algorithmus oder das Tool, das zum Verschlüsseln der logischen Datei verwendet wird. Wenn es nicht möglich ist (oder nicht gewünscht), das Verschlüsselungsschema zu beschreiben (z. & # u. aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist. "Verschlüsselt", um darzustellen, dass die Datei verschlüsselt ist, aber entweder ist das zugehörige Verschlüsselungsschema nicht bekannt oder nicht offengelegt. und "nicht verschlüsselt", um darzustellen, dass die logische Datei nicht verschlüsselt ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Erweiterung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateierweiterung")
</dt> </dl>

Dateinamenerweiterung für das Dateisystem Objekt, ohne den Punkt (.), der die Erweiterung vom Dateinamen trennt.

Beispiele: "txt", "MOF", "MDB"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Der Dateiname (ohne den Punkt oder die Erweiterung) der Datei.

Beispiel: "Autoexec"

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Größe des Dateisystem Objekts in Bytes. Obwohl Ordner über eine **FileSize** -Eigenschaft verfügen, wird immer der Wert 0 zurückgegeben. Um die Größe eines Ordners zu bestimmen, verwenden Sie FileSystemObject, oder addieren Sie die Größe aller Dateien, die im Ordner gespeichert sind.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateityp")
</dt> </dl>

Dateityp (angegeben durch die- **Erweiterungs** Eigenschaft).

Beispielsweise verfügt eine MDB-Datei wahrscheinlich über den Dateityp Microsoft Access-Anwendung. Eine ASP-Datei hat wahrscheinlich den Dateityp HTML-Dokument. Ordner werden in der Regel einfach als Ordner angezeigt.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**"F"-Klassenname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Datei System-Klassenname")
</dt> </dl>

Klasse des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ File System**](cim-filesystem.md).**Name**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Datei System Name ")
</dt> </dl>

Typ des Dateisystems (NTFS, FAT, FAT32), das auf dem Laufwerk installiert ist, auf dem sich die Datei oder der Ordner befindet.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Gibt an, ob das Dateisystem Objekt ausgeblendet ist. **True** gibt an, dass die Datei ausgeblendet ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("aktuelle Datei öffnende Anzahl")
</dt> </dl>

Anzahl von "Datei öffnen", die zurzeit für die Datei aktiv sind.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Letzter Zugriff**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Letzter Zugriff")
</dt> </dl>

Datum, an dem zuletzt auf die Datei zugegriffen wurde. Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last modified")
</dt> </dl>

Datum, an dem die Datei zuletzt geändert wurde. Weitere Informationen zum Arbeiten mit Datums-und Uhrzeit Formaten in WMI finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Name-Eigenschaft ist eine Zeichenfolge, die den geerbten Namen darstellt, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert. Vollständige Pfadnamen müssen angegeben werden. Beispiel: C: \\ Windows- \\ System \\win.ini

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Pfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Der Pfad für die Datei. Der Pfad enthält die führenden und nachfolgenden umgekehrten Schrägstriche, aber nicht den Laufwerk Buchstaben oder den Ordnernamen.

Für den Ordner c: \\ Windows \\ system32 \\ WBEM lautet der Pfad \\ Windows \\ system32 \\ . Für den Ordner c: \\ Scripts lautet der Pfad \\ .

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Lesbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")
</dt> </dl>

Gibt an, ob Sie Elemente im Ordner lesen können. **True** gibt an, dass die Datei gelesen werden kann.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.

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

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Datei")
</dt> </dl>

Gibt an, ob das Objekt eine Systemdatei ist. **True** gibt an, dass die Datei eine Systemdatei ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Schreibbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("beschreibbar")
</dt> </dl>

**True** gibt an, dass die Datei geschrieben werden kann.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Verzeichnis** Klasse wird vom [**CIM- \_ Verzeichnis**](cim-directory.md)abgeleitet.

**Übersicht**

Ordner sind Dateisystem Objekte, die andere Dateisystem Objekte enthalten sollen. Dies bedeutet jedoch nicht, dass alle Ordner gleich sind. Stattdessen können sich Ordner erheblich unterscheiden. Einige Ordner sind Betriebssystem Ordner, die in der Regel nicht durch ein Skript geändert werden sollten. Einige Ordner sind schreibgeschützt. Dies bedeutet, dass Benutzer auf den Inhalt dieses Ordners zugreifen können, ihn aber nicht hinzufügen, löschen oder ändern können. Einige Ordner werden für optimalen Speicher komprimiert, während andere für Benutzer ausgeblendet und nicht sichtbar sind.

WMI verwendet die **Win32- \_ Verzeichnis** Klasse zum Verwalten von Ordnern. Die in dieser Klasse verfügbaren Eigenschaften und Methoden sind mit den in der [**CIM \_ DataFile**](cim-datafile.md) -Klasse verfügbaren Eigenschaften und Methoden identisch, der Klasse, die zum Verwalten von Dateien verwendet wird. Dies bedeutet, dass Sie, nachdem Sie gelernt haben, wie Sie Ordner mithilfe von WMI verwalten, ohne zusätzliche Arbeit auch wissen, wie Sie Dateien verwalten.

Die [**Win32- \_ Unterverzeichnis**](win32-subdirectory.md) Zuordnungs Klasse wird auch zum Verwalten von Dateien und Ordnern verwendet. Die **Win32- \_ Unterverzeichnis** Klasse bezieht sich auf einen Ordner und seine unmittelbaren Unterordner. Beispielsweise handelt es sich bei Protokollen in der Ordnerstruktur c: \\ Scripts \\ Logs um einen Unterordner von Skripts, und Skripts sind ein Unterordner des Stamm Ordners c: \\ . Protokolle werden jedoch nicht als Unterordner von "C:" betrachtet \\ .

Sie können die Eigenschaften eines beliebigen Ordners im Dateisystem mithilfe der **Win32- \_ Verzeichnis** Klasse abrufen. Die Eigenschaften, die mit dieser Klasse verfügbar sind, werden in Tabelle 11,1 angezeigt. Um die Eigenschaften für einen einzelnen Ordner abzurufen, erstellen Sie eine WQL-Abfrage (Windows Query Language) für die **Win32- \_ Verzeichnis** Klasse, um sicherzustellen, dass Sie den Namen des Ordners einschließen. Diese Abfrage bindet z. b. an den Ordner "D: \\ Archive":

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

Wenn Sie einen Datei-oder Ordnernamen in einer WQL-Abfrage angeben, stellen Sie sicher, dass Sie Pfad Komponenten mit zwei umgekehrten Schrägstrichen ( \\ \\ ) trennen.

Wenn Sie das Abrufen von Daten auf ein einzelnes Laufwerk beschränken möchten, geben Sie eine WHERE-Klausel an, in der der Laufwerk Buchstabe angegeben ist. Diese Abfrage gibt z. b. eine Liste aller Ordner auf Laufwerk C:

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Wenn Sie alle Ordner auf einem Computer auflisten müssen, beachten Sie, dass diese Abfrage einen längeren Zeitraum in Anspruch nehmen kann.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel ruft Eigenschaften für den Ordner C: \\ Scripts ab.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Verzeichnis**](cim-directory.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

