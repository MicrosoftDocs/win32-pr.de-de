---
description: Verwendet die im Permissions-Parameter festgelegten Werte, um zu bestimmen, ob der Benutzer die angegebenen Berechtigungen in der AccessMask-Eigenschaft des Win32 \_ CodecFile-Objekts festgelegt hat, das die Codecdatei darstellt.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: GetEffectivePermission-Methode der Win32_CodecFile-Klasse (Aclui.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c3740d1c87b5d74968d0bc4eb92ed8246c9a3c2a0a42a3b0c434c74f306a203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878980"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a>GetEffectivePermission-Methode der Win32 \_ CodecFile-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) verwendet die im *Permissions-Parameter* festgelegten Werte, um zu bestimmen, ob der Benutzer die angegebenen Berechtigungen in der **AccessMask-Eigenschaft** des [**Win32 \_ CodecFile-Objekts**](win32-codecfile.md) festgelegt hat, das die Codecdatei darstellt. Die Berechtigungen gelten für die Datei, das Verzeichnis, in dem sich die Datei befindet, und die Freigabe, wenn sich das Verzeichnis oder die Datei in einer Freigabe befinden.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Berechtigungen* \[ In\]
</dt> <dd>

Bitmap der Berechtigungen, die in der **AccessMask-Eigenschaft** des [**Win32 \_ CodecFile-Objekts**](win32-codecfile.md) festgelegt sind.

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE \_ READ \_ DATA (File) FILE \_ LIST DIRECTORY \_ (Directory)** (1 (0x1))


</dt> <dd>

Gewährt das Recht, Daten aus der Datei zu lesen. Für ein Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE \_ WRITE \_ DATA (file) FILE \_ ADD FILE \_ (directory)** (2 (0x2))


</dt> <dd>

Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE \_ APPEND \_ DATA (File) FILE \_ ADD \_ SUBDIRECTORY (directory) (4** (0x4))


</dt> <dd>

Gewährt das Recht, Daten an die Datei anzufügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA** (8 (0x8))


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu lesen.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA** (16 (0x10))


</dt> <dd>

Gewährt das Recht, erweiterte Attribute zu schreiben.

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE \_ EXECUTE (File) FILE \_ TRAVERSE (Directory)** (32 (0x20))


</dt> <dd>

Gewährt das Recht zum Ausführen einer Datei. Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE \_ DELETE \_ CHILD (Verzeichnis)** (64 (0x40))


</dt> <dd>

Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien zu löschen, auch wenn die Dateien schreibgeschützt sind.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE \_ READ \_ ATTRIBUTES** (128 (0x80))


</dt> <dd>

Gewährt das Recht zum Lesen von Dateiattributen.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE \_ WRITE \_ ATTRIBUTES** (256 (0x100))


</dt> <dd>

Gewährt das Recht, Dateiattribute zu ändern.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))


</dt> <dd>

Gewährt Löschzugriff.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**LESEN \_ CONTROL** (131072 (0x20000))


</dt> <dd>

Gewährt Lesezugriff auf den Sicherheitsdeskriptor und den Besitzer.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE \_ DAC** (262144 (0x40000))


</dt> <dd>

Gewährt Schreibzugriff auf die zugriffssteuerungsliste (Discretionary Access Control List, ACL).

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER** (524288 (0x80000))


</dt> <dd>

Weist den Schreibbesitzer zu.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))


</dt> <dd>

Synchronisiert den Zugriff und ermöglicht einem Prozess, auf den Eintritt eines Objekts in den signalisierten Zustand zu warten.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Aufrufer über die angegebenen Berechtigungen verfügt, und **FALSE,** wenn der Aufrufer nicht über die angegebenen Berechtigungen verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Aclui.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

