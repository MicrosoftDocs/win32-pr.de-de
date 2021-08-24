---
description: Der Neustart&\# 8194; Die WMI-Klassenmethode fährt das Computersystem herunter und startet es dann neu.
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
ms.openlocfilehash: 700d497650e8950c72467bbad8e11cf450b2302f0b68ef762e8a11e3c6aaceee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752730"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Reboot-Methode der Win32 \_ OperatingSystem-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **Reboot** fährt das Computersystem herunter und startet es dann neu.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstiges** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Durch die Möglichkeit, einen Computer programmgesteuert neu zu starten, können Administratoren viele Computerverwaltungsaufgaben remote ausführen.

Wenn Sie beispielsweise ein Skript zum Installieren von Software erstellen oder eine Konfigurationsänderung vornehmen, die einen Neustart eines Computers erfordert, können Sie den Befehl restart in das Skript einschließen und den gesamten Vorgang remote ausführen. Die **Reboot-Methode** kann verwendet werden, um einen Computer neu zu starten. Wie bei der [**Win32Shutdown-Methode**](win32shutdown-method-in-class-win32-operatingsystem.md) erfordert die **Reboot-Methode,** dass der Benutzer, dessen Sicherheitsanmeldeinformationen vom Skript verwendet werden, über die Berechtigung Herunterfahren verfügt.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die Reboot-Methode der [**Win32 \_ OperatingSystem-Klasse**](win32-operatingsystem.md) aufgerufen.

> [!Note]  
> Sie müssen über die Berechtigung Herunterfahren verfügen, um die Shutdown-Methode erfolgreich aufzurufen.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Der folgende Perl-Code ruft die Reboot-Methode der [**Win32 \_ OperatingSystem-Klasse**](win32-operatingsystem.md) auf.

> [!Note]  
> Sie müssen über die Berechtigung Herunterfahren verfügen, um die Shutdown-Methode erfolgreich aufzurufen.

 


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



Das folgende VBScript ruft die Reboot-Methode der [**Win32 \_ OperatingSystem-Klasse**](win32-operatingsystem.md) auf einem Remotesystem auf. Geben Sie REMOTE \_ SYSTEM NAME mit dem Namen des \_ remoten Systems ein, das neu gestartet werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Reboot-Methode erfolgreich aufrufen zu können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Er folgt perl und ruft die Reboot-Methode der [**Win32 \_ OperatingSystem-Klasse**](win32-operatingsystem.md) auf einem Remotesystem auf. Geben Sie REMOTE \_ SYSTEM NAME mit dem Namen des \_ remoten Systems ein, das neu gestartet werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die Reboot-Methode erfolgreich aufzurufen.

 


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ OperatingSystem**](win32-operatingsystem.md)
</dt> <dt>

[**CIM \_ OperatingSystem.Shutdown-Methode**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[WMI-Aufgaben: Desktopverwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

