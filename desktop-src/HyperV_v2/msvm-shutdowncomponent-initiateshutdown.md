---
description: Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf dem zugeordneten untergeordneten virtuellen Computer. Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert. Jeder andere Rückgabecode gibt eine Fehlerbedingung an.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: InitiateShutdown-Methode der Msvm_ShutdownComponent-Klasse (Winreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950399"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>InitiateShutdown-Methode der Msvm \_ ShutdownComponent-Klasse

Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf dem zugeordneten untergeordneten virtuellen Computer. Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert. Jeder andere Rückgabecode gibt eine Fehlerbedingung an.

## <a name="syntax"></a>Syntax


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Force (Erzwingen)* \[ In\]
</dt> <dd>

Typ: **boolescher Wert**

Ein Flag, das bei **True** erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten enthalten sind.

</dd> <dt>

*Grund* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Grund für das Herunterfahren. Dies ist eine benutzerdefinierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> <dt>

**Das System ist nicht bereit** (32780)
</dt> <dt>

**Der Computer ist gesperrt und kann nicht ohne die Force-Option** (32781) heruntergefahren werden.
</dt> <dt>

**Das Herunterfahren des Systems wird ausgeführt** (32782)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ ShutdownComponent-Klasse**](msvm-shutdowncomponent.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winreg.h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

