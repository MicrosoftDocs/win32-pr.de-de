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
# <a name="win32_codecfile-class"></a>Win32- \_ codecfile-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) von **Win32 \_ codecfile** stellt den auf dem Computersystem installierten Audiostream oder Videocodec dar. Codecs konvertieren einen Medien Formattyp in einen anderen, üblicherweise ein komprimiertes Format in ein unkomprimiertes Format. Der Name "Codec" wird von einer Kombination aus "komprimieren" und "decokomprimieren" abgeleitet. Ein Codec kann z. b. ein komprimiertes Format, z. b. ms-ADPCM, in ein nicht komprimiertes Format (z. b. PCM) konvertieren, das die meisten Audiohardware direkt wiedergeben kann.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32 \_ codecfile** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ codecfile** -Klasse verfügt über diese Methoden.



| Methode                                                                                             | BESCHREIBUNG                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Changesecurrityberechtigungen**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.<br/>                                                                                                                         |
| [**Changesecurritypermissionsex**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.<br/>                                                                                                                         |
| [**Komprimieren**](compress-method-in-class-win32-codecfile.md)                                       | Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Komprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                    |
| [**Kopieren**](copy-method-in-class-win32-codecfile.md)                                               | Kopiert die im Objekt Pfad angegebene logische Datei oder das Verzeichnis in den Speicherort, der durch den Eingabeparameter angegeben wird.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Class-Methode, die die im Objekt Pfad angegebene logische Datei oder das Verzeichnis an den Speicherort kopiert, der durch den filename-Parameter angegeben wird.<br/>                                                                    |
| [**Lösch**](delete-method-in-class-win32-codecfile.md)                                           | Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                       |
| [**Geteffectiveberechtigung**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Bestimmt, ob der Aufrufer über die durch das **Berechtigungs** Argument angegebenen aggregierten Berechtigungen verfügt, nicht nur für das Datei Objekt, sondern auf der Freigabe, in der sich die Datei oder das Verzeichnis befindet (wenn es sich auf einer Freigabe befindet).<br/> |
| [**Benen**](rename-method-in-class-win32-codecfile.md)                                           | Klassenmethode, die die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) umbenennt.<br/>                                                                                                                     |
| [**Take Ownership**](takeownership-method-in-class-win32-codecfile.md)                             | Ruft den Besitz der logischen Datei ab, die im Objekt Pfad angegeben ist.<br/>                                                                                                                                         |
| [**Takebesitzshipex**](takeownershipex-method-in-class-win32-codecfile.md)                         | Klassenmethode, die den Besitz der logischen Datei erhält, die im Objekt Pfad angegeben ist.<br/>                                                                                                                       |
| [**Dekomprimieren**](uncompress-method-in-class-win32-codecfile.md)                                   | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                  |
| [**Nicht CompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Dekomprimiert die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ codecfile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zugriffsrechte")
</dt> </dl>

Bitmaske, die die Zugriffsrechte darstellt, die für den Zugriff auf oder das Ausführen bestimmter Vorgänge für die Codec-Datei erforderlich sind Informationen zu Bitwerten finden Sie unter [**Datei-und Verzeichniszugriffs Rechte Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.

 

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**Datei \_ Lesen von \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**Datei \_ Schreiben von \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**Datei \_ Lese \_ Attribute** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**Datei \_ \_Attribute schreiben** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Löschen** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Lesen Sie \_ Steuer** Element (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Schreiben \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Schreiben \_ Besitzer** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Synchronisieren** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archivieren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("sollte archiviert werden")
</dt> </dl>

**True** gibt an, dass die Datei archiviert werden soll.

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

Kurze Beschreibung des Objekts.

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

**True** gibt an, dass die Datei komprimiert wird.

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

Der Algorithmus oder das Tool, das zum Komprimieren der logischen Datei verwendet wird. Wenn es nicht möglich ist (oder nicht erwünscht), das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei komprimiert ist oder nicht. "Komprimiert", um darzustellen, dass die Datei komprimiert ist, das Komprimierungs Schema jedoch nicht bekannt ist oder nicht offengelegt ist. und "nicht komprimiert", um darzustellen, dass die logische Datei nicht komprimiert ist.

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

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

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

Erstellungsdatum der Datei.

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

Klasse des Computer Systems.

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

Zeichenfolge, die den Namen des Computer Systems darstellt.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ mediaresources \\ \\ ICM \| Description")
</dt> </dl>

Der vollständige Name des Codec-Treibers. Diese Zeichenfolge soll in großen (beschreibenden) Leerzeichen angezeigt werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Beispiel: "Microsoft PCM Converter"

</dd> <dt>

**Laufwerk**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Laufwerk Buchstabe (einschließlich Doppelpunkt) der Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: "c:"

</dd> <dt>

**Eightdotdreidateiname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Punkt 3 Dateiname")
</dt> </dl>

DOS-kompatibler Dateiname für diese Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: "c: \\ PROGRA ~ 1"

</dd> <dt>

**Verschlüsselt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verschlüsselt")
</dt> </dl>

**True** gibt an, dass die Datei verschlüsselt ist.

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

Der Algorithmus oder das Tool, das zum Verschlüsseln der logischen Datei verwendet wird. Wenn es nicht möglich ist (oder nicht gewünscht), das Verschlüsselungsschema zu beschreiben (möglicherweise aus Sicherheitsgründen), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass nicht bekannt ist, ob die logische Datei verschlüsselt ist oder nicht. "Verschlüsselt", um darzustellen, dass die Datei verschlüsselt ist, das zugehörige Verschlüsselungsschema jedoch nicht bekannt ist oder nicht offengelegt ist. und "nicht verschlüsselt", um darzustellen, dass die logische Datei nicht verschlüsselt ist.

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

Dateinamenerweiterung (ohne den Punkt).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiele: "txt", "MOF", "MDB"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateiname")
</dt> </dl>

Der Name (ohne Erweiterung) der Datei.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: "Autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Größe der Datei (in Bytes).

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Der Name des Dateisystems.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Gruppieren**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")
</dt> </dl>

Der Codec, der durch diese Klasse dargestellt wird.

Die Werte sind:

<dl> <dd>Audio</dd> <dd>Video</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Audiodatei** ("Audiodatei")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Video** ("Video")


</dt> <dd></dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

**True** gibt an, dass die Datei ausgeblendet ist.

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

Das Objekt wurde installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

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

Es wurde zuletzt auf die Datei zugegriffen.

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

Die Datei wurde zuletzt geändert.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller")
</dt> </dl>

Die Hersteller Zeichenfolge aus der Versions Ressource, sofern vorhanden.

Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der geerbte Name, der als Schlüssel einer logischen Datei Instanz innerhalb eines Dateisystems fungiert. Vollständige Pfadnamen müssen angegeben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Beispiel: "C: \\ Windows \\ System \\win.ini"

</dd> <dt>

**Pfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Der Pfad der Datei. Dies umfasst führende und nachfolgende umgekehrte Schrägstriche.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

Beispiel: " \\ Windows \\ System \\ "

</dd> <dt>

**Lesbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("lesbar")
</dt> </dl>

Die Datei kann gelesen werden.

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

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**True** gibt an, dass die Datei eine Systemdatei ist.

Diese Eigenschaft wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) (Win32), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")
</dt> </dl>

Versions Zeichenfolge aus der Versions Ressource, sofern vorhanden.

Diese Eigenschaft wird von [**CIM \_ DataFile**](cim-datafile.md)geerbt.

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

Die **Win32- \_ codecfile** -Klasse wird von [**CIM \_ DataFile**](cim-datafile.md)abgeleitet.

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

[**CIM- \_ Datendatei**](cim-datafile.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

