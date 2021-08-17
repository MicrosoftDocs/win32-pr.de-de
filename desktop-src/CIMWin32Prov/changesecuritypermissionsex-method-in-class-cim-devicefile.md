---
description: Ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene Gerätedatei (diese Methode ist eine erweiterte Version der ChangeSecurityPermissions-Methode).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: ChangeSecurityPermissionsEx-Methode der CIM_DeviceFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6d70c11077873154040e30cabfb460546f79b1088ff124884e35f3698aaf78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959139"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>ChangeSecurityPermissionsEx-Methode der CIM \_ DeviceFile-Klasse

Die **ChangeSecurityPermissionsEx-Methode** ändert die Sicherheitsberechtigungen für die Gerätedatei, die im Objektpfad angegeben ist (diese Methode ist eine erweiterte Version der [**ChangeSecurityPermissions-Methode).**](changesecuritypermissions-method-in-class-cim-devicefile.md) Wenn die logische Datei ein Verzeichnis ist, verhält sich diese Methode rekursiv und ändert die Sicherheitsberechtigungen für alle Dateien und Unterverzeichnisse, die das Verzeichnis enthält. Diese Methode wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecurityDescriptor* \[ In\]
</dt> <dd>

Gibt die Sicherheitsinformationen an.

> [!Caution]  
> Eine  NULL-ACL in der [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt unbegrenzten Zugriff.

 

</dd> <dt>

*Option* \[ In\]
</dt> <dd>

Zu ändernde Sicherheitsberechtigung. Verwenden Sie beispielsweise , um die Besitzer- und DACL-Sicherheit zu ändern.

`Option = 1 + 4`

oder

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE \_ \_ \_ BESITZERSICHERHEITSINFORMATIONEN** (1)


</dt> <dd>

Ändern Sie den Besitzer der logischen Datei.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE \_ \_ \_ GRUPPENSICHERHEITSINFORMATIONEN** (2)


</dt> <dd>

Ändern Sie die Gruppe der logischen Datei.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE \_ \_ \_ DACL-SICHERHEITSINFORMATIONEN** (4)


</dt> <dd>

Ändern Sie die ACL der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE \_ \_ \_ SACL-SICHERHEITSINFORMATIONEN** (8)


</dt> <dd>

Ändern Sie die System-ACL der logischen Datei.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der bzw. dem die Methode fehlgeschlagen ist. Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Untergeordnete Datei (oder Verzeichnis), die als Ausgangspunkt für diese Methode verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der bzw. dem beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL ist,** wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod-Aufruf angegeben**](/windows/desktop/WmiSdk/swbemservices-execmethod) ist.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

True **gibt** an, dass die -Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ DeviceFile-Instanz angegeben**](cim-devicefile.md) wird. Bei Dateiinstanzen wird dieser Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

<dl> <dt>


</dt> <dd>

0

Erfolg.

</dd> <dt>


</dt> <dd>

2

Zugriff verweigert:

</dd> <dt>


</dt> <dd>

8

Nicht angegebener Fehler.

</dd> <dt>


</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>


</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>


</dt> <dd>

11

Dateisystem, nicht NTFS.

</dd> <dt>


</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>


</dt> <dd>

13

Laufwerk nicht identisch.

</dd> <dt>


</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>


</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>


</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>


</dt> <dd>

17

Die Berechtigung wurde nicht gehalten.

</dd> <dt>


</dt> <dd>

21

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ DeviceFile](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

