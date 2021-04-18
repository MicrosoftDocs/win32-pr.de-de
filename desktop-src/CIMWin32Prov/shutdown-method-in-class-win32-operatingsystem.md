---
description: Das Herunterfahren&\# 8194; Die WMI-Klassenmethode entlädt Programme und DLLs, bis der Computer sicher ausgeschaltet wird.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Shutdown-Methode der Win32_OperatingSystem-Klasse
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
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483966"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Shutdown-Methode der Win32- \_ OperatingSystem-Klasse

Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode für das Herunterfahren entlädt Programme und DLLs, bis Sie den Computer sicher ausschalten können.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Shutdown();
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

Computer müssen gelegentlich aus dem Netzwerk entfernt werden, möglicherweise für eine geplante Wartung, weil der Computer nicht ordnungsgemäß funktioniert, oder um einen Konfigurationsprozess abzuschließen. Wenn ein DHCP-Server z. b. fehlerhafte IP-Adressen ausgibt, sollten Sie den Computer Herunterfahren, bis ein Dienst Techniker zur Behebung des Problems weitergeleitet werden kann. Wenn Sie vermuten, dass ein Sicherheits Verstoß aufgetreten ist, müssen Sie möglicherweise bestimmte Server herunterfahren, um sicherzustellen, dass auf Sie nicht zugegriffen werden kann, bis das Sicherheitsproblem behoben wurde. Einige Konfigurations Vorgänge (z. b. das Ändern eines Computer namens) erfordern, dass Sie den Computer neu starten, damit die Änderung wirksam wird.

Mit dieser Methode wird der Computer nach Möglichkeit sofort heruntergefahren. Das System beendet alle laufenden Prozesse, leert alle Datei Puffer auf den Datenträger und schaltet dann das System herunter. Der aufrufende Prozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen, wie im folgenden Beispiel beschrieben.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Weitere Informationen zum Festlegen einer Berechtigung finden Sie unter [Ausführen von privilegierten Vorgängen](/windows/desktop/WmiSdk/executing-privileged-operations) und [Ausführen von privilegierten Vorgängen mit VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript). Weitere Optionen für das Herunterfahren, z. b. ein Abmelde-oder Erzwungenes Herunterfahren, finden Sie unter [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode.

## <a name="examples"></a>Beispiele

Mit dem folgenden VBScript-Code wird der lokale Computer heruntergefahren.

> [!Note]  
> Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Der folgende Perl-Code schaltet den lokalen Computer herunter.

> [!Note]  
> Sie benötigen die Berechtigung zum Herunterfahren, um die Shutdown-Methode erfolgreich aufrufen zu können.

 


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



Mit dem folgenden VBScript-Code wird der angegebene Remote Computer heruntergefahren. Geben Sie den *Remote \_ System \_ Namen* mit dem Namen des Remote Systems ein, das heruntergefahren werden soll.

> [!Note]  
> Sie müssen über die RemoteShutdown-Berechtigung verfügen, um die **Shutdown** -Methode erfolgreich aufrufen zu können.

 


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ OperatingSystem**](win32-operatingsystem.md)
</dt> <dt>

[WMI-Tasks: Desktop Verwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

