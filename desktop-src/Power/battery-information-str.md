---
description: Enthält Akku Informationen.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356162"
---
# <a name="battery_information-structure"></a>Struktur der Akku \_ Informationen

Enthält Akku Informationen. Diese Struktur wird von dem IOCTL-Steuerelement Code für die [**\_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md) zurückgegeben, wenn die Informationen auf der Ebene "Akku Information" angefordert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Akku Funktionen. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**Akku \_ Kapazitäts \_ Verhältnis**</dt> <dt>0x40000000</dt> </dl>                    | Gibt an, dass die Akkukapazität und die Preisinformationen relativ und nicht in bestimmten Einheiten sind. Wenn dieses Bit nicht festgelegt ist, sind die Berichterstattungs Einheiten Milliwatt-Stunden (MWh) für Kapazität und Milliwatt (MW) für die Rate. Wenn dieses Bit festgelegt ist, können alle Verweise auf Einheiten in der anderen Akku Dokumentation ignoriert werden. Alle rateninformationen werden in Einheiten pro Stunde gemeldet. Wenn z. b. die vollständig berechnete Kapazität als 100 gemeldet wird, bedeutet eine Rate von 200, dass der Akku seine gesamte Kapazität in einer halben Stunde verbrauchen wird.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**Akku \_ Ist \_ kurzfristiger \_**</dt> <dt>0x20000000</dt> </dl>                               | Gibt an, dass der normale Vorgang für eine ausfallsichere Funktion gilt. Wenn dieses Bit nicht festgelegt ist, wird erwartet, dass der Akku während der normalen System Verwendung verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**Akku \_ Set \_ - \_ Unterstützung**</dt> für <dt>0x00000001</dt> </dl>          | Gibt an, dass die Anforderungen zum Festlegen von Informationen vom Typ "Akkuladung" von diesem Akku Gerät unterstützt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**Akku \_ Festlegen von " \_ entladen" \_ unterstützt**</dt> <dt>0x00000002</dt> </dl> | Gibt an, dass Set Information-Anforderungen vom Typ "Akku Entladung" von diesem Akku Gerät unterstützt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**Akku \_ System \_ Batterie**</dt> <dt>0x80000000</dt> </dl>                             | Gibt an, dass der Akku eine allgemeine Stromversorgung zum Ausführen des Systems bereitstellen kann.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Technologie**
</dt> <dd>

Die Akku Technologie. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                        | Bedeutung                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nicht aufladbarer Akku, z. b. "Alkaline".<br/> |
| <dl> <dt>1</dt> </dl> | Akku Akku, z. b. Lead Acid.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Chemi**
</dt> <dd>

Eine abgekürzte Zeichenfolge, die die Chemie des Akkus angibt. Diese Zeichenfolge muss nicht notwendigerweise mit 0 (null) beendet werden. Im folgenden finden Sie eine partielle Liste der Abkürzungen, die zurückgegeben werden können, und die zugeordneten chemisserien.



| Unicode-Zeichenfolge                                                                                                                                           | Bedeutung                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**Pbac**</dt> </dl> | Führende Acid<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**Herz**</dt> </dl>                        | Lithium-Ionen<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Lithium-Ionen<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | Nickel-Kadmium<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**NiMH**</dt> </dl> | Nickel-Metal-Hydride<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Nickel-Zink<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Aufladbare Alkaline-Manganese<br/> |



 

Andere chemisserien werden möglicherweise in der Zukunft angezeigt, und Ihr Code sollte in der Lage sein, Sie zu verarbeiten.

</dd> <dt>

**Designedcapacity**
</dt> <dd>

Die theoretische Kapazität des Akkus, wenn neu, in MWh, es sei denn, die Akku \_ Kapazität \_ ist relativ eingestellt. In diesem Fall sind die Einheiten nicht definiert.

</dd> <dt>

**Fullchargedcapacity**
</dt> <dd>

Die aktuell vollständig berechnete Kapazität des Akkus in MWh (oder relativ). Vergleichen Sie diesen Wert mit **designedcapacity** , um den Akku Verschleiß einzuschätzen.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Die von dem Hersteller vorgeschlagene Kapazität in MWh, bei der eine geringe Akku Warnung auftritt. Die Definitionen niedriger variieren von Hersteller zu Hersteller. Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist. Um das Risiko eines Daten Verlusts zu verringern, wird dieser Wert normalerweise als Standardeinstellung für den Alarm "kritischer Akku" verwendet.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Die von dem Hersteller vorgeschlagene Kapazität in MWh, bei der eine Warnung zu einem Akku ausgelöst werden sollte. Die Definitionen der Warnung variieren von Hersteller zu Hersteller. Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist. Um das Risiko eines Daten Verlusts zu verringern, wird dieser Wert normalerweise als Standardeinstellung für den Alarm mit niedrigem Akku verwendet.

</dd> <dt>

**Criticalbias**
</dt> <dd>

Eine Abweichung von 0 (null) in MWh, die auf die Akku Berichterstattung angewendet wird. Einige Akkus reservieren eine geringe Belastung, die aus den Kapazitäts Werten des Akkus besteht, um "0" als kritischen Akku Pegel anzuzeigen. Kritischer Bias ist analog zum Festlegen eines Kraftstoff Messgerätes, um "Empty" anzuzeigen, wenn mehrere Benzin verbleiben.

</dd> <dt>

**Cyclecount**
</dt> <dd>

Die Anzahl der in der Akku Erfahrung/Entladezyklen. Dies bietet die Möglichkeit, den Akku Verschleiß zu ermitteln. Wenn der Akku keinen Zyklen unterstützt, ist dieser Member 0 (null).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im Allgemeinen tritt ein Warn Status vor einem niedrigen Status auf, aber Sie sollten nicht davon ausgehen, dass dies der Fall ist. Es ist möglich, einen Akku abzufragen und zu ermitteln, dass weder eine Warnstufe aufgetreten ist, noch den Akku abzufragen und ihn so zu finden, dass beide Ebenen erreicht wurden. Dies weist möglicherweise darauf hin, dass Sie nicht oft genug Abfragen. Es kann auch darauf hindeuten, dass der Akku nicht sehr lange eine Abrechnung durchläuft und schneller als erwartet ausgeführt wird. Ein solcher Akku ist möglicherweise am Ende der nützlichen Lebensdauer oder beschädigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




