---
description: 'GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter): Gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert.'
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096988"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>GetSecurityDescriptor-Methode der Win32_Service-Klasse (CIMWin32-WMI-Anbieter)

Die **GetSecurityDescriptor-Methode** gibt den Sicherheitsdeskriptor zurück, der den Zugriff auf den Dienst steuert. Der Deskriptor wird als Instanz von [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.

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

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>


</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>


</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>


</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>


</dt> <dd>

5

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](win32-baseservice.md)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.

</dd> <dt>


</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>


</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**Berechtigung fehlt**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>


</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>


</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>


</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>


</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>


</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>


</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>


</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>


</dt> <dd>

17

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>


</dt> <dd>

18

Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.

</dd> <dt>


</dt> <dd>

19

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>


</dt> <dd>

20

Der Dienstname enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>


</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>


</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>


</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**Win32 \_ SecurityDescriptor-Instanz**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) stellt einen [**SECURITY \_ DESCRIPTOR \_ CONTROL-Datentyp**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine DACL (Discretionary [*Access Control List)*](/windows/desktop/SecGloss/d-gly) und eine Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) Weitere Informationen finden Sie unter [Access Control Listen.](/windows/desktop/SecAuthZ/access-control-lists)

Wenn **seSecurityPrivilege** beim Abrufen eines Sicherheitsdeskriptors nicht gewährt oder aktiviert wird, wird nur die DACL in der zurückgegebenen Sicherheitsbeschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) und [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Beispiele

Achten Sie beim Abrufen eines Sicherheitsdeskriptors in VBScript darauf, dass Sie "Sicherheit" verwenden und als Administrator ausführen, wie im folgenden Codeausschnitt gezeigt. Andernfalls löst Ihr Code möglicherweise einen Berechtigungsfehler aus.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Ebenso müssen Sie in VB.NET sicherstellen, dass Sie "EnablePrivileges = True" festlegen und die Anwendung als Administrator ausführen.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32-Dienst \_**](win32-service.md)
</dt> <dt>

[**Berechtigungskonst constants**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

