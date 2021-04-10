---
description: Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Getsecuritydescriptor-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
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
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041395"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Getsecuritydescriptor-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)

Die **getsecuritydescriptor** -Methode gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert. Der Deskriptor wird als eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ vorgenommen\]
</dt> <dd>

Die Sicherheits Beschreibung, die dem Dienst zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

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

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>


</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>


</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**Fehlende Berechtigungen**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

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

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>


</dt> <dd>

18

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>


</dt> <dd>

19

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>


</dt> <dd>

20

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>


</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

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

Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL). Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Beispiele

Wenn Sie eine Sicherheits Beschreibung in VBScript abrufen, achten Sie darauf, dass Sie "Sicherheit" ausführen und als Administrator ausführen, wie im folgenden Code Ausschnitt gezeigt. Andernfalls löst der Code möglicherweise einen Berechtigungs Fehler aus.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Legen Sie auf ähnliche Weise in VB.net "enableprivileges = true" fest, und führen Sie die Anwendung als Administrator aus.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



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

[**Win32- \_ Dienst**](win32-service.md)
</dt> <dt>

[**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

