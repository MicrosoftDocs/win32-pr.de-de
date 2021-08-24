---
description: Das Herunterfahren&\# 8194; Die WMI-Klassenmethode entlädt Programme und DLLs, bis der Computer sicher ausgeschaltet werden kann.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Shutdown-Methode der Win32_OperatingSystem Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800840"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Shutdown-Methode der Win32 \_ OperatingSystem-Klasse

Die **Shutdown** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) entlädt Programme und DLLs, bis der Computer sicher ausgeschaltet werden kann.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Shutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt null (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Andere** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Computer müssen gelegentlich aus dem Netzwerk entfernt werden, z. B. zur geplanten Wartung, weil der Computer nicht ordnungsgemäß funktioniert, oder um einen Konfigurationsprozess abschließen zu können. Wenn beispielsweise ein DHCP-Server fehlerhafte IP-Adressen aushing, sollten Sie den Computer herunterfahren, bis ein Servicetechniker zum Beheben des Problems bereitgestellt werden kann. Wenn Sie vermuten, dass eine Sicherheitsverletzung aufgetreten ist, müssen Sie möglicherweise bestimmte Server herunterfahren, um sicherzustellen, dass auf sie erst zugegriffen werden kann, wenn das Sicherheitsproblem behoben wurde. Einige Konfigurationsvorgänge (z. B. das Ändern eines Computernamens) erfordern einen Neustart des Computers, bevor die Änderung wirksam wird.

Mit dieser Methode wird der Computer nach Möglichkeit sofort heruntergefahren. Das System beendet alle ausgeführten Prozesse, leert alle Dateipuffer auf den Datenträger und gibt dann das System aus. Der aufrufende Prozess muss über die SE **\_ SHUTDOWN \_ NAME** verfügen, wie im folgenden Beispiel beschrieben.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Weitere Informationen zum Festlegen einer Berechtigung finden Sie unter Ausführen privilegierter [Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations) und [Ausführen privilegierter Vorgänge mit VBScript.](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript) Weitere Optionen zum Herunterfahren, z. B. abmelden oder erzwungenes Herunterfahren, finden Sie unter [**Win32Shutdown-Methode.**](win32shutdown-method-in-class-win32-operatingsystem.md)

## <a name="examples"></a>Beispiele

Mit dem folgenden VBScript-Code wird der lokale Computer heruntergefahren.

> [!Note]  
> Sie müssen über die Berechtigung Herunterfahren verfügen, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Mit dem folgenden Perl-Code wird der lokale Computer heruntergefahren.

> [!Note]  
> Sie müssen über die Berechtigung Herunterfahren verfügen, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



Mit dem folgenden VBScript-Code wird der angegebene Remotecomputer heruntergefahren. Geben Sie *\_ \_ REMOTESYSTEMNAME* mit dem Namen des Remotesystems ein, das heruntergefahren werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die **Shutdown-Methode erfolgreich aufrufen zu** können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Win32-Betriebssystem**](win32-operatingsystem.md)
</dt> <dt>

[WMI-Aufgaben: Desktopverwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

