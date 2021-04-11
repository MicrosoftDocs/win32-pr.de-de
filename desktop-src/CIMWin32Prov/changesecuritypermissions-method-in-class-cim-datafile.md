---
description: Ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127121"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a>Changesecurrityberechtigungs-Methode der CIM \_ DataFile-Klasse

Die **changesecurrityberechtigungs** -Methode ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist. Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert. Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

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

Gibt die Sicherheitsinformationen an.

> [!Note]  
> Eine **Zugriffs** Steuerungs Liste (Access Control List, ACL) in der [**Sicherheits \_ Deskriptor**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) -Struktur gewährt uneingeschränkten Zugriff. Informationen zu den Auswirkungen des unbegrenzten Zugriffs finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

*Option* \[ in\]
</dt> <dd>

Zu ändernde Sicherheits Berechtigung. Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:

`Option = 1 + 4`

oder

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

Ändern Sie die ACL der logischen Datei.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)


</dt> <dd>

Ändern Sie die System-ACL der logischen Datei.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Zugriff verweigert.

</dd> <dt>

**Nicht spezifizierter Fehler**
</dt> <dd>

8

Nicht spezifizierter Fehler.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>

**Objekt ist bereits vorhanden.**
</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>

**Dateisystem nicht NTFS**
</dt> <dd>

11

</dd> <dt>

**Plattform nicht NT/Windows 2000**
</dt> <dd>

12

Plattform nicht Windows NT-basiert.

</dd> <dt>

**Laufwerk nicht identisch**
</dt> <dd>

13

Das Laufwerk ist nicht identisch.

</dd> <dt>

**Verzeichnis nicht leer**
</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>

**Freigabe Verletzung**
</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>

**Berechtigung nicht aufrechterhalten**
</dt> <dd>

17

Die Berechtigung wurde nicht aufrechterhalten.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **changesecurrityberechtigungs** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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

[**CIM- \_ Datendatei**](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM- \_ Datendatei**](cim-datafile.md)
</dt> <dt>

[WMI-Tasks: Dateien und Ordner](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Datei-und Verzeichniszugriffs Rechte-Konstanten**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

