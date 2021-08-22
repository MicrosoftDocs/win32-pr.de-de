---
description: WMI-Klassen, die Dateien oder Verzeichnisse darstellen, z. B. Win32 CodecFile oder \_ CIM \_ DataFile, enthalten eine AccessMask-Eigenschaft.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Datei- und Verzeichniszugriffsrechte-Konstanten (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8678627b0f7d9ce2ed7f9c8e7e39c49bdcd3b6c3a8313f7d7b3c517c379093d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131382"
---
# <a name="file-and-directory-access-rights-constants"></a>Konstanten für Datei- und Verzeichniszugriffsrechte

WMI-Klassen, die Dateien oder Verzeichnisse darstellen, z. B. [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) oder [**CIM \_ DataFile,**](/windows/desktop/CIMWin32Prov/cim-datafile)enthalten eine **AccessMask-Eigenschaft.** Diese Eigenschaft enthält Biteinstellungen, die die Zugriffsrechte angeben, die ein Benutzer oder eine Gruppe für bestimmte Zugriffe oder Vorgänge für die Datei haben muss. Weitere Informationen finden Sie unter [Dateisicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights) und [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md)

Die Datei- oder Verzeichnisklassen, die eine **AccessMask-Eigenschaft** enthalten, umfassen Folgendes:

-   [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_CIM-Verzeichnis**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Win32-Verzeichnis \_**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Win32-Freigabe \_**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

In der folgenden Liste sind die Werte für Datei- und Verzeichniszugriffsrechte in der **AccessMask-Eigenschaft** aufgeführt. Diese Eigenschaft ist eine Bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_ \_ DATEILESEDATEN**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gewährt das Recht, Daten aus der Datei zu lesen.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_ \_ DATEILISTENVERZEICHNIS**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gewährt das Recht, Daten aus der Datei zu lesen. Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses auflisten zu können.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**DATEI \_ SCHREIBEN VON \_ DATEN**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Gewährt das Recht, Daten in die Datei zu schreiben.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**DATEI \_ HINZUFÜGEN \_ EINER DATEI**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Gewährt das Recht, Daten in die Datei zu schreiben. Für ein Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_DATEIANFÜGEDATEN \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Gewährt das Recht, Daten an die Datei anfügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE \_ ADD \_ SUBDIRECTORY**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Gewährt das Recht, Daten an die Datei anfügen. Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**\_ \_ DATEILESE-EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Gewährt das Recht, erweiterte Attribute zu lesen.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**\_DATEI-SCHREIB-EA \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Gewährt das Recht, erweiterte Attribute zu schreiben.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE \_ EXECUTE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Gewährt das Recht, eine Datei auszuführen.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE \_ TRAVERSE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Gewährt das Recht, eine Datei auszuführen. Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE \_ DELETE \_ CHILD**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Gewährt das Recht, ein Verzeichnis und alle dateien zu löschen, die es enthält (seine unteren Elemente), auch wenn die Dateien schreibgeschützt sind.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_ \_ DATEILESEATTRIBUTE**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Gewährt das Recht, Dateiattribute zu lesen.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_ \_ DATEI-SCHREIBATTRIBUTE**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Gewährt das Recht, Dateiattribute zu ändern.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**Löschen**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Gewährt das Recht, das Objekt zu löschen.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**\_READ-STEUERELEMENT**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Gewährt das Recht, die Informationen im Sicherheitsdeskriptor für das Objekt zu lesen, ohne die Informationen in der SACL einzulesen.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**\_SCHREIB-DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Gewährt das Recht, die DACL in der Objektsicherheitsbeschreibung für das Objekt zu ändern.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Gewährt das Recht, den Besitzer in der Sicherheitsbeschreibung für das Objekt zu ändern.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Gewährt das Recht, das -Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Prozess warten, bis sich das Objekt im signalisierten Zustand befindet. Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Sicherheitskonst constants](wmi-security-constants.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

