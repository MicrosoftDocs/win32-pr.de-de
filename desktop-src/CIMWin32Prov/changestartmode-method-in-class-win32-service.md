---
description: Ändert den Startmodus eines \_ Win32-Diensts.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9444ed76fac18ce018c0ab286966b9fa071dc8108db0f8456271545e19ab1fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322940"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>ChangeStartMode-Methode der Win32_Service -Klasse (CIMWin32 WMI-Anbieter)

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** ändert den Startmodus eines [**Win32-Diensts. \_**](win32-service.md)

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Startstart** ("Start")


</dt> <dd>

Vom Betriebssystemlader gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatischer Start** ("Automatisch")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manuell")


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**Ausgeführte abhängige Dienste**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienststeuerung**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann die Steuerung nicht akzeptieren**
</dt> <dd>

5

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](win32-baseservice.md)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Timeout für Dienstanforderungen**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienstdatenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienstabhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.

</dd> <dt>

**Dienstabhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Dienstanmeldung fehlgeschlagen**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Dienst zum Löschen markiert**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst kein Thread**
</dt> <dd>

17

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**Statuskreisabhängigkeit**
</dt> <dd>

18

Der Dienst verfügt beim Starten über zirkuläre Abhängigkeiten.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**Status Ungültiger Name**
</dt> <dd>

20

Der Dienstname enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Statusparameter**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Status Ungültiges Dienstkonto**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Statusdienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Dienst wurde bereits angehalten**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="examples"></a>Beispiele

Mit dem folgenden [Change StartMode eines Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell-Beispiels, das aus dem TechNet-Katalog abgerufen wurde, wird der Startmodus eines Diensts geändert.


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
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

[**\_Win32-Dienst**](win32-service.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

