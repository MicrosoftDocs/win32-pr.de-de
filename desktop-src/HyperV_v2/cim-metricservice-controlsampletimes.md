---
description: Ermöglicht die Angabe des Zeitpunkts, zu dem die Erfassung von Metrikdaten gestartet werden soll, und die Angabe des bevorzugten Stichprobenintervalls für die regelmäßige Datensammlung.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: ControlSampleTimes-Methode der CIM_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 833e828a7622dfcd76a7b061e3890fbe111de10a6b8c3c2d3faf0801429678f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695070"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>ControlSampleTimes-Methode der CIM \_ MetricService-Klasse

Ermöglicht die Angabe des Zeitpunkts, zu dem die Erfassung von Metrikdaten gestartet werden soll, und die Angabe des bevorzugten Stichprobenintervalls für die regelmäßige Datensammlung.

Wenn die Stichprobenentnahme für zusätzliche Metriken gestartet wird, können die von dieser Methode angegebenen Einstellungen verwendet werden.

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

*StartSampleTime* \[ In\]
</dt> <dd>

Zeitpunkt, zu dem die Stichprobenentnahme für die Metriken gestartet werden soll.

Der Wert 999901010000000.000000+000 gibt an, dass die Stichprobenentnahme bei der nächsten Synchronisierung mit der vollen Stunde beginnen soll. Die Stichprobenentnahme wird mit der vollen Stunde synchronisiert, wenn sekunden seit Mitternacht modulo sample interval in seconds gleich 0 ist.

</dd> <dt>

*PreferredSampleInterval* \[ In\]
</dt> <dd>

Bevorzugte Stichprobenintervallzeit. Um korrelierbare Metriken zu erhalten, wird empfohlen, das Stichprobenintervall so zu wählen, dass die Intervallzeit von 3600 Moduleo-Stichproben in Sekunden gleich 0 ist.

Es liegt in der Verantwortung der Implementierung des CIM-Metrikdiensts, zu entscheiden, ob die angeforderte Stichprobenintervallzeit verwendet wird.

Der CIM-Client kann überprüfen, ob die Metrikanbieter die angeforderte Stichprobenintervallzeit verwenden, indem er verwandte BaseMetricDefinition-Instanzen abruft und den Inhalt von [**CIM \_ BaseMetricDefinition überprüft.**](cim-basemetricdefinition.md)**SampleInterval-Eigenschaft.**

</dd> <dt>

*RestartGathering* \[ In\]
</dt> <dd>

**TRUE,** um anzulegen, dass die Erfassung aller Metriken, die dem Metrikdienst zugeordnet sind, mit diesem Methodenaufruf neu gestartet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Reservierte Methode** (..)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




