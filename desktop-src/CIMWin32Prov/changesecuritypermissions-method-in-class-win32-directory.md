---
description: 'ChangeSecurityPermissions-Methode der Win32_Directory Klasse: Ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene Logische Verzeichniseintragsdatei.'
ms.assetid: de2b3269-61e0-484c-8bea-00578422491f
ms.tgt_platform: multiple
title: ChangeSecurityPermissions-Methode der Win32_Directory Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0eb6c8e86d21894bcf8abcf921706e46b78f45844d4bd7f66c8d6cfcfc019d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323180"
---
# <a name="changesecuritypermissions-method-of-the-win32_directory-class"></a>ChangeSecurityPermissions-Methode der Win32 \_ Directory-Klasse

Die **WMI-Klassenmethode ChangeSecurityPermissions** ändert die Sicherheitsberechtigungen für die logische Verzeichniseintragsdatei, die im Objektpfad angegeben ist. Wenn die logische Datei ein Verzeichnis ist, ist **ChangeSecurityPermissions** rekursiv und ändert die Sicherheitsberechtigungen aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält. Die **ChangeSecurityPermissions-Klasse** gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecurityDescriptor* \[ In\]
</dt> <dd>

Ausdruck, der in eine Instanz von [**Win32 \_ SecurityDescriptor auflöset.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Dieser Deskriptor enthält neue Sicherheitsberechtigungen für die Instanz von [**Win32 \_ PageFile.**](win32-pagefile.md)

</dd> <dt>

*Option* \[ In\]
</dt> <dd>

Sicherheitsprivileg, das geändert werden soll. Verwenden Sie beispielsweise Folgendes, um die Sicherheit für Besitzer und dacläre Zugriffssteuerungsliste (Discretionary Access Control List, DACL) zu ändern:

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

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE \_ \_ \_ DACL-SICHERHEITSINFORMATIONEN** (4)


</dt> <dd>

Ändern Sie die daCL der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE \_ \_ \_ SACL-SICHERHEITSINFORMATIONEN** (8)


</dt> <dd>

Ändern Sie die Systemzugriffssteuerungsliste (SACL) der logischen Datei.

</dd> </dl> </dd> </dl>

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

**Das Objekt ist bereits vorhanden.**
</dt> <dd>

10

Das Objekt "" ist bereits vorhanden.

</dd> <dt>

**Dateisystem, nicht NTFS**
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

**Freigabeverletzung**
</dt> <dd>

15

Es liegt ein Freigabeverstoß vor.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Die angegebene Startdatei ist ungültig.

</dd> <dt>

**Nicht gehaltene Rechte**
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

[**Win32-Verzeichnis \_**](win32-directory.md)
</dt> </dl>

 

