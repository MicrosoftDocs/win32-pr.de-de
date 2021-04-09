---
description: Ändert die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958440"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a>Changesecurrityberechtigungs-Methode der Win32- \_ Pagefile-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurrityberechtigungs** Änderungen ändern die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist. Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, ist **changesekurityberechtigungen** rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecurityDescriptor* \[ in\]
</dt> <dd>

Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird. Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).

</dd> <dt>

*Option* \[ in\]
</dt> <dd>

Sicherheits Berechtigung, die geändert werden soll. Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (die Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:

`Option = 1 + 4`

Oder

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)


</dt> <dd>

Ändern Sie den Besitzer der logischen Datei.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)


</dt> <dd>

Ändern Sie die Gruppe der logischen Datei.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)


</dt> <dd>

Ändern Sie die DACL der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)


</dt> <dd>

Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.

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

**Nicht spezifizierter Fehler**
</dt> <dd>

8

Ein nicht angegebener Fehler ist aufgetreten.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Der angegebene Name ist ungültig.

</dd> <dt>

**Objekt ist bereits vorhanden.**
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

**Freigabe Verletzung**
</dt> <dd>

15

Eine Freigabe Verletzung ist aufgetreten.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Die angegebene Startdatei ist ungültig.

</dd> <dt>

**Berechtigung nicht aufrechterhalten**
</dt> <dd>

17

Eine für den Vorgang erforderliche Berechtigung fehlt.

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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Pagefile**](win32-pagefile.md)
</dt> </dl>

 

