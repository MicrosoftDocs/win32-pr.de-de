---
description: Versetzt den durch das Win32-Dienstobjekt dargestellten Dienst \_ in den Zustand "Beendet".
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: StopService-Methode der Win32_Service-Klasse (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c8c055c260f4983622010ced5de652cf673391b7ae02a75b40fd28427a78827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751880"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a>StopService-Methode der Win32_Service-Klasse (Sdoias.h)

Die **StopService** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) versetzt den durch das [**Win32-Dienstobjekt \_**](win32-service.md) dargestellten Dienst in den Zustand "Beendet".

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](win32-baseservice.md)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.

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

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**18**
</dt> <dd>

Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienstname weist ungültige Zeichen auf.

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

Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die Dienste mithilfe der Methoden **StopService** und [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) beenden und anhalten. Die Entscheidung, einen Dienst anzuhalten, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:

-   Kann der Dienst angehalten werden? Wenn dies nicht dere ist, ist die einzige Option das Beenden des Diensts.
-   Müssen Sie weiterhin Clientanforderungen für personen verarbeiten, die bereits mit dem Dienst verbunden sind? In diesem Falle ermöglicht das Anhalten eines Diensts in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert wird. Wenn Sie dagegen einen Dienst beenden, werden alle Clients sofort getrennt.
-   Müssen Sie einen Dienst neu konfigurieren und lassen sie sofort wirksam werden? Obwohl Diensteigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten erst wirksam, wenn der Dienst tatsächlich beendet und neu gestartet wurde.

Der Skriptcode, der zum Beenden eines Diensts erforderlich ist, ist fast identisch mit dem Code, der zum Anhalten des Diensts erforderlich ist.

Wenn Sie versuchen, einen Dienst zu beenden, auf dem abhängige Dienste ausgeführt werden, schlägt die **StopService-Methode** mit dem Rückgabewert 3 fehl. Die abhängigen Dienste müssen zuerst beendet werden.

Wenn Sie einen Dienst beenden, überprüfen Sie sofort den [**\_ Win32-Dienst**](win32-service.md).**State-Eigenschaft,** da der -Wert den Dienst möglicherweise weiterhin als ausgeführt zeigt.

## <a name="examples"></a>Beispiele

[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell-Beispiel Legt den Dienststatus für Remotecomputer fest.

Das Beispiel [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript beendet einen Dienst und alle abhängigen Dienste.

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein Dienst heruntergefahren wird.


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



Im folgenden Perl-Codebeispiel wird veranschaulicht, wie ein Dienst heruntergefahren wird.


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Das folgende VBScript-Codebeispiel zeigt, dass Sie den NetDDE-Dienst erst beenden können, wenn die abhängigen Dienste beendet wurden. Stellen Sie zum Ausführen des Skripts sicher, dass der NetDDE-Dienst und die abhängigen Dienste mithilfe des MMC-Snap-Ins Services.msc oder des **Befehls Net Start** ausgeführt werden.

Mit der [**Win32 \_ DependentService-Klasse**](win32-dependentservice.md) können Sie Dienstabhängigkeiten über eine [Associators Of-Abfrage](/windows/desktop/WmiSdk/associators-of-statement) suchen.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Dienst**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

