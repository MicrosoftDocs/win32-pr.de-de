---
description: Versucht, den referenzierten Dienst in seinen Startzustand zu versetzen.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Start Service-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb530766781de4e23cc86778c1597a5c5c2a1014
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958382"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Start Service-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)

Die **Start Service** -Methode versucht, den Dienst, auf den verwiesen wird, in den Startzustand zu versetzen.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

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

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

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

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

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

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

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

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>

**Jahren**
</dt> <dd>

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**21**
</dt> <dd>

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände anders als der SCM angezeigt. Ein angehaltener Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienst Start Prozedur durchlaufen muss. Ein angehaltene Dienst wird jedoch weiterhin ausgeführt, aber seine funktionstüchtig ist angehalten. Aus diesem Grund muss ein angehaltene Dienst nicht die gesamte Dienst Start Prozedur durchlaufen, sondern erfordert ein anderes Verfahren, um die Funktionsweise fortzusetzen.

Sie müssen die richtige-Methode verwenden, um einen Dienst zu starten, der angehalten wurde, oder um einen Dienst fortzusetzen, der angehalten wurde. Die [**Win32- \_ Dienst**](win32-service.md) Methoden " **StartService** " und " [**ResumeService**](resumeservice-method-in-class-win32-service.md) " sollten in den folgenden Situationen verwendet werden:

-   Wenn ein Dienst aktuell beendet ist, müssen Sie ihn mit der **Start Service** -Methode neu starten. [**ResumeService**](resumeservice-method-in-class-win32-service.md) kann einen Dienst nicht starten, der zurzeit beendet ist.
-   Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](resumeservice-method-in-class-win32-service.md)verwenden. Wenn Sie die **Start Service** -Methode für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "der Dienst wird bereits ausgeführt." Der Dienst bleibt jedoch angehalten, bis der Steuerungs Code zum Fortsetzen des dienstandens an ihn gesendet wird.

Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängt, werden beide Dienste gestartet. Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet. Sie müssen die Association-Klasse [**Win32 \_ dependentservice**](win32-dependentservice.md) und die [assoziatoren von](/windows/desktop/WmiSdk/associators-of-statement) Query verwenden, um die abhängigen Elemente zu suchen und Sie separat zu starten.

## <a name="examples"></a>Beispiele

Das [Remote enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell-Beispiel aktiviert Remote den Remotedesktop-Dienst.

Das PowerShell-Beispiel zum [beenden, starten, aktivieren oder Deaktivieren des Dienstanbieter](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) startet, beendet, aktiviert oder deaktiviert einen Dienst.

Im folgenden vbsscript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ diensdienstanbieter**](win32-service.md)gestartet wird.


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



Im folgenden perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32- \_ Dienstanbieter**](win32-service.md)gestartet wird.


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Das folgende VBScript-Codebeispiel (NetDDE) ist vom NetDDEDSDM-Dienst abhängig. Das Skript findet die Klasse, von der NetDDE abhängt, und startet Sie, wodurch NetDDE nicht automatisch gestartet wird.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Dienst**](win32-service.md)
</dt> <dt>

[WMI-Tasks: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

