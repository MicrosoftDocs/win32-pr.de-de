---
description: Ändert den Start Modus eines Win32- \_ systemtreiberdienstanbieter.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523496"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>ChangeStartMode-Methode der Win32 \_ systemdriver-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines [**Win32 \_ systemdriver**](win32-systemdriver.md) -Dienstanbieter.

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

Der Start Modus des Windows-Basis Dienstanbieter.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


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

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde. der Wert ist 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Abhängige Dienste werden ausgeführt** (3)
</dt> <dt>

**Ungültige Dienst Kontrolle** (4).
</dt> <dt>

Der **Dienst kann die Steuerung nicht akzeptieren** (5).
</dt> <dt>

Der **Dienst ist nicht aktiv** (6).
</dt> <dt>

**Timeout für Dienst Anforderungen** (7)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

Der **Dienst wird bereits ausgeführt** (10).
</dt> <dt>

**Dienst Datenbank gesperrt** (11)
</dt> <dt>

**Dienst Abhängigkeit gelöscht** (12)
</dt> <dt>

**Dienst Abhängigkeitsfehler** (13)
</dt> <dt>

**Dienst deaktiviert** (14)
</dt> <dt>

Fehler bei der **Dienst Anmeldung** (15).
</dt> <dt>

Der **Dienst wurde zum Löschen markiert** (16).
</dt> <dt>

**Dienst ohne Thread** (17)
</dt> <dt>

**Status zirkuläre Abhängigkeit** (18)
</dt> <dt>

**Doppelter Name des Status** (19)
</dt> <dt>

**Ungültiger Name** (20).
</dt> <dt>

**Ungültiger Parameter** (21).
</dt> <dt>

**Ungültiges Dienst Konto** (22).
</dt> <dt>

**Status Dienst vorhanden** (23)
</dt> <dt>

Der **Dienst wurde bereits angeh** alten (24).
</dt> <dt>

**Sonstige** (25 4294967295)
</dt> </dl>

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

[**Win32- \_ System Treiber**](win32-systemdriver.md)
</dt> </dl>

 

