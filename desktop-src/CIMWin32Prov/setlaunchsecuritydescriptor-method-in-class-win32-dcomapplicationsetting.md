---
description: Aktualisiert den Startsicherheitsdeskriptor der DCOM-Anwendung mit einem neuen Sicherheitsdeskriptor, der von einer Instanz einer Win32 \_ SecurityDescriptor-Klasse definiert wird.
ms.assetid: 72245d22-1a0a-4069-b5d6-9d59e4de4aab
ms.tgt_platform: multiple
title: SetLaunchSecurityDescriptor-Methode der Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e24a58efbb32dcf3d4e3d06b051529560ce745b851b448f2e8eb2acbb9ead95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759710"
---
# <a name="setlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>SetLaunchSecurityDescriptor-Methode der Win32 \_ DCOMApplicationSetting-Klasse

Die **SetLaunchSecurityDescriptor-Methode** aktualisiert den Startsicherheitsdeskriptor der DCOM-Anwendung mit einem neuen Sicherheitsdeskriptor, der von einer Instanz einer [**Win32 \_ SecurityDescriptor-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) definiert wird. Dieser Sicherheitsdeskriptor steuert, wer die Anwendung starten darf. Das Konto, das das Skript oder die Anwendung ausführt, das diese Methode aufruft, muss über die Berechtigungen **SeSecurityPrivilege** und **SeRestorePrivilege** verfügen. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Syntax


```mof
uint32 SetLaunchSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ In\]
</dt> <dd>

Der Sicherheitsdeskriptor, der festgelegt werden soll, der steuert, wer die DCOM-Anwendung starten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie unter [WMI-Rückgabecodes](/windows/desktop/WmiSdk/wmi-return-codes) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolgreicher Abschluss.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**9**
</dt> <dd>

Der Benutzer verfügt nicht über ausreichende Berechtigungen zum Ausführen der -Methode.

</dd> <dt>

**21**
</dt> <dd>

Ein im Methodenaufruf angegebener Parameter ist ungültig.

</dd> <dt>

**Andere**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine SACL [*(System Access Control List).*](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)

Sie können sowohl die DACL als auch die SACL in der [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) aktualisieren, wenn Sie diese Methode aufrufen. Sie können jedoch auch nur die DACL oder nur die SACL aktualisieren.

Die folgenden Werte in [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beide aktualisiert werden.

-   **\_SE DACL \_ PRESENT**

    Gibt an, dass die DACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.

-   **\_SE SACL \_ PRESENT**

    Gibt an, dass die SACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei. Zum Aktualisieren der SACL muss für das Konto die **SeSecurityPrivilege-Berechtigung** aktiviert sein. Für die Skripterstellung lautet der Berechtigungsname **SeSecurityPrivilege.** Weitere Informationen finden Sie unter [**Berechtigungskonstanten.**](/windows/desktop/WmiSdk/privilege-constants)

Wenn die Eigenschaften des Gruppentreuhänders und des Besitzertreuhänders nicht **NULL** sind, werden sie aktualisiert. Andernfalls behält WMI die ursprünglichen Werte bei. Weitere Informationen finden Sie unter [WMI-Sicherheitsdeskriptorobjekte.](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)

Wenn eine neue SACL in einem Aufruf dieser Methode **NULL** ist, bleibt die Sicherheitsbeschreibungs-SACL für das sicherungsfähige Zielobjekt unverändert.

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

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsbeschreibungsobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

