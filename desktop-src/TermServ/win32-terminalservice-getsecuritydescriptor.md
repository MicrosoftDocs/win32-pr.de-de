---
title: GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)
description: 'GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste): Gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.'
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- Skripterstellung Windows Verwaltungsinstrumentation , Sicherheit
- Sicherheit Windows Verwaltungsinstrumentation , Skripterstellung
- GetSecurityDescriptor-Remotedesktopdienste
- GetSecurityDescriptor-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , GetSecurityDescriptor-Methode
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13be26eb2f0c68f61cbe97ab61cd9ce2a00ab351f9a797dfe6b1ae92db7a8bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940422"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a>GetSecurityDescriptor-Methode der Win32_Service -Klasse (Remotedesktopdienste)

Die **GetSecurityDescriptor-Methode** gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert. Der Deskriptor wird als Instanz von [**Win32 \_ SecurityDescriptor zurückgegeben.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ out\]
</dt> <dd>

Der dem Dienst zugeordnete Sicherheitsdeskriptor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde akzeptiert.

</dd> <dt>

**1**
</dt> <dd>

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**3**
</dt> <dd>

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**4**
</dt> <dd>

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**5**
</dt> <dd>

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

</dd> <dt>

**6**
</dt> <dd>

Der Dienst wurde nicht gestartet.

</dd> <dt>

**7**
</dt> <dd>

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**10**
</dt> <dd>

Der Dienst wird schon ausgeführt.

</dd> <dt>

**11**
</dt> <dd>

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**12**
</dt> <dd>

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.

</dd> <dt>

**13**
</dt> <dd>

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**14**
</dt> <dd>

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**15**
</dt> <dd>

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**16**
</dt> <dd>

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**17**
</dt> <dd>

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**18**
</dt> <dd>

Der Dienst verfügt beim Start über zirkuläre Abhängigkeiten.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienstname enthält ungültige Zeichen.

</dd> <dt>

**21**
</dt> <dd>

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) und [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Beispiele

Achten Sie beim Abrufen eines Sicherheitsdeskriptors in VBScript darauf, dass Sie "Sicherheit" verwenden und als Administrator ausführen, wie im folgenden Codeausschnitt gezeigt. Andernfalls löst Ihr Code möglicherweise einen Berechtigungsfehler aus.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Ebenso müssen Sie in VB.NET "EnablePrivileges = True" festlegen und die Anwendung als Administrator ausführen.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Dienst \_**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Berechtigungskonst constants**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

