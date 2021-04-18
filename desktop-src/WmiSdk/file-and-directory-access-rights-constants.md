---
description: WMI-Klassen, die Dateien oder Verzeichnisse darstellen, wie z. b. Win32 \_ codecfile oder CIM \_ DataFile, enthalten eine AccessMask-Eigenschaft.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Datei-und Verzeichniszugriffs Rechte-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365927"
---
# <a name="file-and-directory-access-rights-constants"></a>Datei-und Verzeichniszugriffs Rechte-Konstanten

WMI-Klassen, die Dateien oder Verzeichnisse darstellen, wie z. b. [**Win32 \_ codecfile**](/windows/desktop/CIMWin32Prov/win32-codecfile) oder [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), enthalten eine **AccessMask** -Eigenschaft. Diese Eigenschaft enthält Biteinstellungen, mit denen die Zugriffsrechte angegeben werden, die ein Benutzer oder eine Gruppe für den Zugriff auf die Datei haben muss. Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

Die Datei-oder Verzeichnis Klassen, die eine **AccessMask** -Eigenschaft enthalten, umfassen Folgendes:

-   [**CIM- \_ Datendatei**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**CIM- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Win32- \_ codecfile**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Win32- \_ Verzeichnis**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32- \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Win32- \_ Freigabe**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32- \_ shortcutfile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

In der folgenden Liste sind die Werte für Datei-und Verzeichnis Zugriffsrechte in der **AccessMask** -Eigenschaft aufgelistet. Diese Eigenschaft ist eine Bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**Datei \_ Lese \_ Daten**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gewährt das Recht, Daten aus der Datei zu lesen.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**Datei \_ Listen \_ Verzeichnis**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gewährt das Recht, Daten aus der Datei zu lesen. Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**Datei \_ Schreib \_ Daten**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Gewährt das Recht, Daten in die Datei zu schreiben.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**Datei \_ Hinzufügen \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Gewährt das Recht, Daten in die Datei zu schreiben. Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**Datei \_ Anfügen \_ Daten**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Gewährt das Recht zum Anfügen von Daten an die Datei. Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**\_Unterverzeichnis "Datei hinzufügen" \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Gewährt das Recht zum Anfügen von Daten an die Datei. Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lese- \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Gewährt das Recht zum Lesen erweiterter Attribute.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreib- \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Gewährt das Recht, erweiterte Attribute zu schreiben.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**Datei \_ Ausführung**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Gewährt das Recht, eine Datei auszuführen.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**Datei \_ Durchlauf**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Gewährt das Recht, eine Datei auszuführen. Für ein Verzeichnis kann das Verzeichnis durchsucht werden.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**Datei \_ Delete \_ Child**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Gewährt das Recht zum Lesen von Dateiattributen.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ Schreib \_ Attribute**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Erteilt das Recht, Dateiattribute zu ändern.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**Lösch**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Gewährt das Recht, das Objekt zu löschen.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lese \_ Steuerelement**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Erteilt das Recht, die Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**\_DAC schreiben**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Erteilt das Recht, die DACL in der Objekt Sicherheits Beschreibung für das-Objekt zu ändern.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**\_Besitzer schreiben**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Erteilt das Recht, den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisiert**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Gewährt das Recht, das-Objekt für die Synchronisierung zu verwenden. Dies ermöglicht einem Prozess, zu warten, bis sich das Objekt im signalisierten Zustand befindet. Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

