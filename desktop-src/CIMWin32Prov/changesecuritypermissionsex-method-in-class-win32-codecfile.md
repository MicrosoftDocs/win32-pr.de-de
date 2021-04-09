---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Codec-Datei (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861039"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a>Changesecurritypermissionsex-Methode der Win32- \_ codecfile-Klasse

Die **changesecurritypermissionsex** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Codec-Datei (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-win32-directory.md) -Methode). Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.

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

Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird. Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ codecfile**](win32-codecfile.md).

</dd> <dt>

*Option* \[ in\]
</dt> <dd>

Die tatsächliche Sicherheits Berechtigung, die geändert werden soll. Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (-Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:

`Option = 1 + 4`

Oder

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1 (0x1))


</dt> <dd>

Ändern Sie den Besitzer der logischen Datei.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2 (0x2))


</dt> <dd>

Ändern Sie die Gruppe der logischen Datei.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4 (0x4))


</dt> <dd>

Ändern Sie die freigegebene Zugriffs Steuerungs Liste (DACL) der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8 (0x8))


</dt> <dd>

Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.

</dd> </dl> </dd> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Der Name der Datei oder des Verzeichnisses, in der die **changesecurritypermissionsex** -Methode fehlgeschlagen ist. Dieser Parameter ist NULL, wenn die Methode erfolgreich ausgeführt wird.

</dd> <dt>

*Startdateiname* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **changesecurritypermissionsex** verwendet werden soll. In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen aufgetreten ist Wenn dieser Parameter NULL ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die Eigentumsänderungen rekursiv auf Dateien und Verzeichnisse in dem Verzeichnis angewendet werden, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird. Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.

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

Die Plattform ist nicht Windows NT oder Windows 2000.

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

[**Win32- \_ codecfile**](win32-codecfile.md)
</dt> </dl>

 

