---
description: 'PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, den Dienst im angehaltenen Zustand zu platzieren.'
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d5546ef4c67a6c9fa23f723f45725b19999770e11771608e197d6b759ca61de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504540"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>PauseService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** versucht, den Dienst im angehaltenen Zustand zu platzieren.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 PauseService();
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

Der Dienst verfügt beim Starten über zirkuläre Abhängigkeiten.

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

Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die [**Methoden StopService**](stopservice-method-in-class-win32-service.md) und [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) verwenden, um Dienste zu beenden und anzuhalten. Die Entscheidung, einen Dienst zu beenden, anstatt ihn anzuhalten (oder umgekehrt), hängt von mehreren Faktoren ab, z. B.:

-   Kann der Dienst angehalten werden? Wenn nicht, ist die einzige Option das Beenden des Diensts.
-   Müssen Sie weiterhin Clientanforderungen für alle Personen behandeln, die bereits mit dem Dienst verbunden sind? In diesem Beispiel ermöglicht das Anhalten eines Diensts in der Regel die Handhabung vorhandener Clients, während der Zugriff auf neue Clients verweigert wird. Wenn Sie dagegen einen Dienst beenden, werden alle Clients sofort getrennt.
-   Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden? Obwohl Diensteigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten davon erst wirksam, wenn der Dienst tatsächlich beendet und neu gestartet wird.

Der Skriptcode, der zum Beenden eines Diensts erforderlich ist, ist fast identisch mit dem Code, der zum Anhalten des Diensts erforderlich ist.

## <a name="examples"></a>Beispiele

Im [](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript-Beispiel Zum Anhalten von Diensten, die unter einem bestimmten Konto ausgeführt werden, werden alle Dienste angehalten, die unter dem hypothetischen Dienstkonto "Netsvc" ausgeführt werden.

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts angehalten \_ wird.**](win32-service.md)

> [!Note]  
> Der Dienst muss anhalten und bereits ausgeführt werden.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



Im folgenden Perl-Codebeispiel wird veranschaulicht, wie ein bestimmter Dienst von Instanzen des [**Win32-Diensts angehalten \_ wird.**](win32-service.md)

> [!Note]  
> Der Dienst muss anhalten und bereits ausgeführt werden.

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Dienst \_**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**StopService**](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

