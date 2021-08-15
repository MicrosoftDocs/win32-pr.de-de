---
description: Ändert den Startmodus eines Win32 \_ SystemDriver-Diensts.
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
ms.openlocfilehash: 2e2067ae7da8a6f112671237ebc7f77dd26644c5e0b2fa0b77a443c160468581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959129"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>ChangeStartMode-Methode der \_ Win32-SystemDriver-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** ändert den Startmodus eines [**Win32 \_ SystemDriver-Diensts.**](win32-systemdriver.md)

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Vom Betriebssystemladeprogramm gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatischer Start** ("Automatisch")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfsstart** ("manuell")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-systemdriver.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Abhängige Dienste, die ausgeführt werden** (3)
</dt> <dt>

**Ungültige Dienststeuerung** (4)
</dt> <dt>

**Dienst kann Steuerung nicht akzeptieren** (5)
</dt> <dt>

**Dienst nicht aktiv** (6)
</dt> <dt>

**Service Request Timeout** (7)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Pfad nicht gefunden** (9)
</dt> <dt>

**Dienst wird bereits ausgeführt** (10)
</dt> <dt>

**Dienstdatenbank gesperrt** (11)
</dt> <dt>

**Dienstabhängigkeit gelöscht** (12)
</dt> <dt>

**Dienstabhängigkeitsfehler** (13)
</dt> <dt>

**Dienst deaktiviert** (14)
</dt> <dt>

**Fehler bei der Dienstanmeldung** (15)
</dt> <dt>

**Dienst zum Löschen markiert** (16)
</dt> <dt>

**Dienst ohne Thread** (17)
</dt> <dt>

**Statuszirkuläre Abhängigkeit** (18)
</dt> <dt>

**Doppelter Statusname** (19)
</dt> <dt>

**Ungültiger Statusname** (20)
</dt> <dt>

**Ungültiger Statusparameter** (21)
</dt> <dt>

**Status Ungültiges Dienstkonto** (22)
</dt> <dt>

**Statusdienst ist vorhanden** (23)
</dt> <dt>

**Dienst wurde bereits angehalten** (24)
</dt> <dt>

**Sonstige** (25 4294967295)
</dt> </dl>

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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

