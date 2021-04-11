---
description: Ändert den Start Modus eines Dienst Objekts, das von Win32 \_ baseservice abgeleitet ist.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126686"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a>ChangeStartMode-Methode der Win32 \_ baseservice-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines Dienst Objekts, das von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter. Der Standardwert ist "automatisch".

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Der Dienst ist deaktiviert.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

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

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**Abhängige Dienste werden ausgeführt**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienst Kontrolle.**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann keine Steuerung akzeptieren.**
</dt> <dd>

5

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32 \_ baseservice**](win32-baseservice.md)[**State**](win32-baseservice.md) -Eigenschaft) gleich 0, 1 oder 2 ist.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Service Request-Timeout**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt.**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienst Datenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienst Abhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**Dienst Abhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Fehler bei der Dienst Anmeldung**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Der Dienst wurde zum Löschen markiert.**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst ohne Thread**
</dt> <dd>

17

Es gibt keinen Ausführungsthread für den Dienst.

</dd> <dt>

**Status zirkuläre Abhängigkeit**
</dt> <dd>

18

Es gibt Ringabhängigkeiten beim Starten des Diensts.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Es wird ein Dienst unter dem gleichen Namen ausgeführt.

</dd> <dt>

**Ungültiger Name**
</dt> <dd>

20

Der Name des diensdienstanbieter enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter.**
</dt> <dd>

21

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**Ungültiges Dienst Konto.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**Status Dienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Der Dienst wurde bereits angehalten.**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

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

[**Win32- \_ baseservice**](win32-baseservice.md)
</dt> </dl>

 

