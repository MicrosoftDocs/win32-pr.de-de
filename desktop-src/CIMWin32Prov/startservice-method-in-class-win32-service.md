---
description: 'StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, den Referenzdienst in seinen Startzustand zu stellen.'
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
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
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086158"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>StartService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)

Die **StartService-Methode** versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.

In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

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

## <a name="remarks"></a>Bemerkungen

Es scheint zwar keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst zu geben, aber die beiden Zustände unterscheiden sich vom SCM. Ein beendeter Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienststartprozedur durchlaufen muss. Ein angehaltener Dienst wird jedoch weiterhin ausgeführt, aber seine Funktion wurde angehalten. Aus diesem Grund muss ein angehaltener Dienst nicht die gesamte Dienststartprozedur durchlaufen, sondern eine andere Prozedur, um die Funktionsweise fortzusetzen.

Sie müssen die richtige Methode verwenden, um einen angehaltenen Dienst zu starten oder einen angehaltenen Dienst fortzusetzen. Die [**Win32-Dienstmethoden \_**](win32-service.md) **StartService** und [**ResumeService**](resumeservice-method-in-class-win32-service.md) sollten in den folgenden Situationen verwendet werden:

-   Wenn ein Dienst derzeit beendet wird, müssen Sie ihn mithilfe der **StartService-Methode** neu starten. [**ResumeService**](resumeservice-method-in-class-win32-service.md) kann einen Dienst, der derzeit beendet ist, nicht starten.
-   Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](resumeservice-method-in-class-win32-service.md)verwenden. Wenn Sie die **StartService-Methode** für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "Der Dienst wird bereits ausgeführt." Der Dienst bleibt jedoch angehalten, bis der Dienststeuerungscode zum Fortsetzen an ihn gesendet wird.

Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängig ist, werden beide Dienste gestartet. Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet. Sie müssen die Zuordnungsklasse [**Win32 \_ DependentService**](win32-dependentservice.md) und die [Associators Of-Abfrage](/windows/desktop/WmiSdk/associators-of-statement) verwenden, um die Abhängigen zu suchen und separat zu starten.

## <a name="examples"></a>Beispiele

Das [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell-Beispiel aktiviert remote den Remotedesktop Dienst.

Das PowerShell-Beispiel ["Dienst beenden", "Starten", "Aktivieren" oder "Deaktivieren"](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) startet, beendet, aktiviert oder deaktiviert einen Dienst.

Im folgenden VBSScript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts gestartet \_ wird.**](win32-service.md)


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



Im folgenden Perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts gestartet \_ wird.**](win32-service.md)


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



Das folgende VBScript-Codebeispiel, NetDDE, ist vom NetDDEDSDM-Dienst abhängig. Das Skript sucht die Klasse, von der NetDDE abhängt, und startet sie, wodurch NetDDE nicht automatisch gestartet wird.


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



| Anforderungen | Wert |
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

[**Win32-Dienst \_**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

