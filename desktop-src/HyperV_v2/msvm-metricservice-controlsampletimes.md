---
description: Legt die Beispiel Zeiten für das Steuerelement fest.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Controlsampletimes-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215926"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Controlsampletimes-Methode der MSVM \_ metricservice-Klasse

Legt die Beispiel Zeiten für das Steuerelement fest.

## <a name="syntax"></a>Syntax


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Startsampletime* \[ in\]
</dt> <dd>

Der Zeitpunkt, zu dem die Stichprobenentnahme für die Metriken gestartet werden soll.

Der Wert 99990101000000.000000 + 000 gibt an, dass die Stichprobenentnahme bei der nächsten Synchronisierung mit der vollen Stunde gestartet werden soll. Die Stichprobenentnahme wird mit der vollen Stunde synchronisiert, wenn in Sekunden seit Mitternacht Modulo-Stichproben Intervall (in Sekunden) gleich 0 ist.

</dd> <dt>

*Preferredsampleingeterval* \[ in\]
</dt> <dd>

Die bevorzugte Stichproben Intervallzeit. Um korrelierbare Metriken zu erhalten, empfiehlt es sich, das Stichproben Intervall so zu wählen, dass 3600 Modulo Sample Interval Time in Sekunden gleich 0 ist.

Es liegt in der Verantwortung der CIM Metric Service-Implementierung, zu entscheiden, ob die angeforderte Stichproben Intervallzeit berücksichtigt wird.

Der CIM-Client kann überprüfen, ob die metrikanbieter die angeforderte Stichproben Intervallzeit berücksichtigen, indem Sie verwandte basemetricdefinition-Instanzen abrufen und den Inhalt der CIM \_ basemetricdefinition. sampleinterval-Eigenschaft überprüfen.

</dd> <dt>

*Restarterfassung* \[ in\]
</dt> <dd>

Boolescher Wert, der bei Festlegung auf "true" Anforderungen, dass das Sammeln aller Metriken, die dem metrikdienst zugeordnet sind, mit diesem Methoden Aufrufsatz neu gestartet

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Reservierte Methode** (..)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ metricservice**](msvm-metricservice.md)
</dt> </dl>

 

 




