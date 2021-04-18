---
description: Enthält den aktuellen Zustand des Akkus.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351678"
---
# <a name="battery_status-structure"></a>Akku \_ Status Struktur

Enthält den aktuellen Zustand des Akkus. Diese Struktur wird vom Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**PowerState**
</dt> <dd>

Der Akku Zustand. Dieser Member kann NULL, ein oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Akku \_ Berechnen**</dt> von <dt>0x00000004</dt> </dl>                  | Gibt an, dass der Akku zurzeit berechnet wird.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Akku \_ Kritisch**</dt> <dt>0x00000008</dt> </dl>                  | Gibt an, dass Akku Fehler bevorstehend ist. Weitere Informationen finden Sie im Abschnitt Hinweise.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Akku \_**</dt>" <dt>0x00000002</dt> " wird entladen </dl>         | Gibt an, dass der Akku gerade entladen wird.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Akku \_ Netzteil \_ der \_ Zeile**</dt> <dt>0x00000001</dt> </dl> | Gibt an, dass das System auf die Stromversorgung zugreifen kann, sodass keine Akkus entladen werden.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

Die aktuelle Akkukapazität in MWh (oder relativ). Dieser Wert kann verwendet werden, um eine "Benzin Messgerät"-Anzeige zu generieren, indem Sie durch das **fullchargedcapacity** -Element der [**Akku \_ Informations**](battery-information-str.md) Struktur aufgeteilt wird. Wenn die Kapazität nicht verfügbar ist, ist das Mitglied der \_ Kapazität für unbekannte Akku \_ Kapazität.

</dd> <dt>

**Spannungs**
</dt> <dd>

Die aktuelle Akku Spannung in den Akku Terminals in Millivolt (MV). Wenn die Spannung nicht verfügbar ist, ist dieser Member eine Akku- \_ unbekannte \_ Spannung.

</dd> <dt>

**Rate**
</dt> <dd>

Die aktuelle Rate der Akku Gebühren oder-Entladung. Dieser Wert wird in Milliwatt angegeben, es sei denn, die Akku rateninformationen sind relativ. in diesem Fall werden Sie in willkürlichen Einheiten pro Stunde angegeben. Um zu ermitteln, ob die Akku Informationen relativ sind, überprüfen Sie das Flag für die Akkukapazität in den Funktions Elementen der \_ \_ [**Akku \_ Informations**](battery-information-str.md) Struktur.  Ein positiver Wert ungleich 0 (null) gibt das berechnen an; ein negativer Satz weist auf das Entladen hin. Einige Akkus melden nur die Gebühren für die Entladung. Wenn die Rate nicht verfügbar ist, ist dieser Mitglied der Akku- \_ Unknown- \_ Rate. Wenn sich der Zustand des Akkus oder der Stromquelle ändert, kann die Rate verfügbar werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das \_ Flag "Akku kritisch" im **PowerState** -Member dieser Struktur weist auf eine Hardware-"Akku kritisch"-Bedingung hin. Diese kritische Ebene wird vom Akku Hersteller festgelegt, nicht vom Benutzer im "kritischen Akku Alarm". Im Allgemeinen bedeutet dies, dass das Akku System errechnet hat, dass der Akku vollständig erschöpft ist, und jede Stromversorgung überschreitet, was erwartet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Akku \_ Informationen**](battery-information-str.md)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




