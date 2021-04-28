---
description: 'ResumeService-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter): Versucht, den Dienst, auf den verwiesen wird, im fortgesetzten Zustand zu platzieren.'
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: ResumeService-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73c21f282577207b63bcfa2d624c59ddfa3c9bcb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090978"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>ResumeService-Methode der Win32_Service -Klasse (CIMWin32-WMI-Anbieter)

Die **ResumeService** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) versucht, den Dienst, auf den verwiesen wird, im fortgesetzten Zustand zu platzieren.

In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ResumeService();
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

Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten und einem angehaltenen Dienst zu geben scheint, werden die beiden Zustände im SCM anders angezeigt. Ein beendeter Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienststartprozedur durchgehen muss. Ein angehaltener Dienst wird jedoch noch ausgeführt, hat aber seine Funktion angehalten. Aus diesem Grund muss ein angehaltener Dienst nicht die gesamte Dienststartprozedur durchgehen, sondern benötigt ein anderes Verfahren, um wieder funktionsfähig zu sein.

Sie müssen die richtige Methode verwenden, um einen beendeten Dienst zu starten oder einen angehaltenen Dienst wieder aufzunehmen. Die [**Win32-Dienstmethoden \_**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) und **ResumeService** sollten in den folgenden Situationen verwendet werden:

-   Wenn ein Dienst derzeit beendet wird, müssen Sie ihn mithilfe der [**StartService-Methode**](startservice-method-in-class-win32-service.md) neu starten. **ResumeService** kann keinen Dienst starten, der derzeit beendet ist.
-   Wenn ein Dienst angehalten wird, müssen Sie **ResumeService verwenden.** Wenn Sie die [**StartService-Methode**](startservice-method-in-class-win32-service.md) für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "Der Dienst wird bereits ausgeführt." Der Dienst bleibt jedoch angehalten, bis der Code zum Fortsetzen der Dienststeuerung an ihn gesendet wird.

## <a name="examples"></a>Beispiele

Im [Beispiel AutoStart-Dienste fortsetzen,](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) bei denen es sich um angehaltene VBScript-Dienste handelt, werden alle angehaltenen Automatischstartdienste neu gestartet.

Im folgenden VBScript-Codebeispiel wird beschrieben, wie ein angehaltener Dienst von Instanzen des [**Win32-Diensts fortgesetzt \_ wird.**](win32-service.md)

> [!Note]  
> Der Dienst muss das Anhalten unterstützen und bereits ausgeführt werden.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



Im folgenden Perl-Codebeispiel wird beschrieben, wie ein angehaltener Dienst von Instanzen des [**Win32-Diensts fortgesetzt \_ wird.**](win32-service.md)

> [!Note]  
> Der Dienst muss das Anhalten unterstützen und bereits ausgeführt werden.

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                  |
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

 

