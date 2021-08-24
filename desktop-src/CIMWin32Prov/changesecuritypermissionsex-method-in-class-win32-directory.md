---
description: Ändert die Sicherheitsberechtigungen für die Verzeichniseintragsdatei, die im Objektpfad angegeben ist (diese Methode ist eine erweiterte Version der ChangeSecurityPermissions-Methode).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: ChangeSecurityPermissionsEx-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d90a6a76067421c3b23c0ec5124fa5da85e029e81d0307a2b4b66d01231fe56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323030"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a>ChangeSecurityPermissionsEx-Methode der Win32 \_ Directory-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** ändert die Sicherheitsberechtigungen für die Verzeichniseintragsdatei, die im Objektpfad angegeben ist (diese Methode ist eine erweiterte Version der [**ChangeSecurityPermissions-Methode).**](changesecuritypermissions-method-in-class-win32-directory.md) Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheitsberechtigungen aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Ausdruck, der in eine Instanz von [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird. Dieser Parameter enthält neue Sicherheitsberechtigungen für die Instanz von [**Win32 \_ PageFile**](win32-pagefile.md).

</dd> <dt>

*Option* \[ In\]
</dt> <dd>

Zu ändernde Sicherheitsberechtigungen. Verwenden Sie beispielsweise Folgendes, um die Sicherheit der Besitzer- und der Dacl-Zugriffssteuerungsliste (Discretionary Access Control List, DACL) zu ändern:

`Option = 1 + 4`

Oder

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

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE \_ \_DACL-SICHERHEITSINFORMATIONEN \_** (4)


</dt> <dd>

Ändern Sie die DACL-Liste der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE \_ \_SACL-SICHERHEITSINFORMATIONEN \_** (8)


</dt> <dd>

Ändern Sie die Systemzugriffssteuerungsliste (SACL) der logischen Datei.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Name der Datei oder des Verzeichnisses, in der die **ChangeSecurityPermissionsEx-Methode** fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das Verzeichnis, die bzw. das als Ausgangspunkt für **ChangeSecurityPermissionsEx** verwendet werden soll. In der Regel ist der *StartFileName-Parameter* der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, in der ein Fehler aus dem vorherigen Methodenaufruf aufgetreten ist. Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im **ExecMethod-Aufruf** angegeben ist. Dieser Parameter ist optional.

Wenn *StartFileName* verwendet wird, muss *Recursive* auch auf TRUE festgelegt werden.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

True gibt an, dass die Besitzänderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile-Instanz**](cim-logicalfile.md) angegeben wird. Bei Dateiinstanzen wird der *Rekursive* Eingabeparameter ignoriert. Dieser Parameter ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung ist erfolgreich.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Zugriff verweigert.“

</dd> <dt>

**Nicht angegebener Fehler**
</dt> <dd>

8

Es ist ein nicht angegebener Fehler aufgetreten.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Der angegebene Name ist ungültig.

</dd> <dt>

**Objekt ist bereits vorhanden**
</dt> <dd>

10

Das Objekt "" ist bereits vorhanden.

</dd> <dt>

**Dateisystem nicht NTFS**
</dt> <dd>

11

Das Dateisystem ist kein NTFS-Dateisystem.

</dd> <dt>

**Plattform nicht NT/Windows 2000**
</dt> <dd>

12

Die Plattform ist nicht Windows.

</dd> <dt>

**Laufwerk nicht identisch**
</dt> <dd>

13

Das Laufwerk ist nicht identisch.

</dd> <dt>

**Verzeichnis nicht leer**
</dt> <dd>

14

Das Verzeichnis ist nicht leer.

</dd> <dt>

**Verletzung der Freigabe**
</dt> <dd>

15

Es liegt ein Freigabeverstoß vor.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Die angegebene Startdatei ist ungültig.

</dd> <dt>

**Berechtigung nicht gehalten**
</dt> <dd>

17

Für den Vorgang ist keine Berechtigung erforderlich.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ein angegebener Parameter ist ungültig.

</dd> </dl>

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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Verzeichnis**](win32-directory.md)
</dt> </dl>

 

