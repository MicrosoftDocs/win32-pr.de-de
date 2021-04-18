---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Verzeichniseintrags Datei (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der Win32_Directory-Klasse
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
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214129"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a>Changesecurritypermissionsex-Methode der Win32- \_ Verzeichnis Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurritypermissionsex** ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Verzeichniseintrags Datei (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-win32-directory.md) -Methode). Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

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

*SecurityDescriptor* \[ in\]
</dt> <dd>

Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird. Dieser Parameter enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).

</dd> <dt>

*Option* \[ in\]
</dt> <dd>

Sicherheits Berechtigung, die geändert werden soll. Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (-Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:

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

Ändern Sie die DACL-Liste der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)


</dt> <dd>

Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.

</dd> </dl> </dd> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Der Name der Datei oder des Verzeichnisses, in der die **changesecurritypermissionsex** -Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.

</dd> <dt>

*Startdateiname* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **changesecurritypermissionsex** verwendet werden soll. In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen aufgetreten ist Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, das im **ExecMethod** -Befehl angegeben wird. Dieser Parameter ist optional.

Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird. Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert. Dieser Parameter ist optional.

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

Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.

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

[**Win32- \_ Verzeichnis**](win32-directory.md)
</dt> </dl>

 

