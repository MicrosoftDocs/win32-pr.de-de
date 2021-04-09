---
description: Der Neustart&\# 8194; Die WMI-Klassenmethode fährt das Computersystem herunter und startet Sie neu.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Reboot-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958527"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Reboot-Methode der Win32- \_ OperatingSystem-Klasse

Beim **Neustart** der [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode wird das Computersystem heruntergefahren und dann neu gestartet.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstige** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Möglichkeit, einen Computerprogramm gesteuert neu zu starten, können Administratoren viele Computer Verwaltungsaufgaben Remote ausführen.

Wenn Sie z. b. ein Skript zum Installieren von Software erstellen oder eine Konfigurationsänderung vornehmen, für die ein Neustart eines Computers erforderlich ist, können Sie den Restart-Befehl in das Skript einschließen und den gesamten Vorgang Remote ausführen. Die **Neustart** Methode kann zum Neustarten eines Computers verwendet werden. Wie die [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode erfordert die **Reboot** -Methode, dass der Benutzer, dessen Sicherheits Anmelde Informationen vom Skript verwendet werden, das Shutdown-Privileg besitzt.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse aufgerufen.

> [!Note]  
> Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Der folgende Perl-Code Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf.

> [!Note]  
> Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Das folgende VBScript Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf einem Remote System auf. Geben Sie \_ den Remote System \_ Namen mit dem Namen des Remote Systems ein, das neu gestartet werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Neustart Methode erfolgreich aufrufen zu können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



der folgende perl Ruft die Reboot-Methode der [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) -Klasse auf einem Remote System auf. Geben Sie \_ den Remote System \_ Namen mit dem Namen des Remote Systems ein, das neu gestartet werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Neustart Methode erfolgreich aufrufen zu können.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
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

[**Win32- \_ OperatingSystem**](win32-operatingsystem.md)
</dt> <dt>

[**CIM \_ OperatingSystem. Shutdown-Methode**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[WMI-Tasks: Desktop Verwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

