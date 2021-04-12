---
description: Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine. Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert. Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: InitiateShutdown-Methode der Msvm_ShutdownComponent-Klasse (winreg. h)
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
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216763"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>InitiateShutdown-Methode der MSVM \_ shutdowncomponent-Klasse

Initiiert einen Vorgang zum Herunterfahren des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine. Wenn 0 (null) zurückgegeben wird, wurde das Herunterfahren erfolgreich initiiert. Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.

## <a name="syntax"></a>Syntax


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Erzwingen* \[ in\]
</dt> <dd>

Typ: **booleschen**

Ein Flag, das beim Wert " **true**" erzwingt, dass Anwendungen geschlossen werden, obwohl nicht gespeicherte Daten vorhanden sind.

</dd> <dt>

*Grund* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Grund für den Vorgang zum Herunterfahren. Dies ist eine benutzerdefinierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

Das **System wird verwendet** (32774).
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> <dt>

**Das System ist nicht bereit** (32780).
</dt> <dt>

**Der Computer ist gesperrt und kann nicht ohne die Option "Force** " (32781) heruntergefahren werden.
</dt> <dt>

**Ein Herunterfahren des Systems wird** ausgeführt (32782).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ shutdowncomponent**](msvm-shutdowncomponent.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ shutdowncomponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

