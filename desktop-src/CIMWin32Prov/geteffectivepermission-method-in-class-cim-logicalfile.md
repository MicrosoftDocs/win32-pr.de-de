---
description: Bestimmt, ob der Aufrufer über die aggregierten Berechtigungen für das CIM LogicalFile-Objekt und die Freigabe verfügt, auf der sich die Datei oder das Verzeichnis befindet, wie durch das \_ Permissions-Argument angegeben.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: GetEffectivePermission-Methode der CIM_LogicalFile -Klasse (Aclui.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fcafa33d9761d813b075b0f6bb56e5d940c73346bea4d4147366b5569679b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675824"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a>GetEffectivePermission-Methode der CIM \_ LogicalFile-Klasse

Die **GetEffectivePermission-Methode** bestimmt, ob der Aufrufer über die aggregierten Berechtigungen für das [**CIM \_ LogicalFile-Objekt**](cim-logicalfile.md) und die Freigabe verfügt, auf der sich die Datei oder das Verzeichnis befindet, wie durch das *Permissions-Argument* angegeben.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Liste der Berechtigungen, die der Benutzer abfragen kann.

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

Gewährt das Recht, ein Verzeichnis und alle dateien zu löschen, die es enthält, auch wenn die Dateien schreibgeschützt sind.

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

Gewährt Schreibzugriff auf die abhängige ACL.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER** (524288)


</dt> <dd>

Weist den Schreibbesitzer zu.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)


</dt> <dd>

Synchronisiert den Zugriff und ermöglicht es einem Prozess, darauf zu warten, dass ein Objekt in den signalisierten Zustand übertritt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Aufruf über die erforderliche Berechtigung verfügt. andernfalls wird false **zurückgegeben.**

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Aclui.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ LogicalFile**](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

