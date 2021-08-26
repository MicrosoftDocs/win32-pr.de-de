---
description: Enthält Akkuinformationen.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION-Struktur (Poclass.h)
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
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033010"
---
# <a name="battery_information-structure"></a>BATTERY \_ INFORMATION-Struktur

Enthält Akkuinformationen. Diese Struktur wird vom [**IOCTL \_ BATTERY QUERY \_ INFORMATION-Steuerungscode \_**](ioctl-battery-query-information.md) zurückgegeben, wenn die BatteryInformation-Informationsebene angefordert wird.

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

Die Akkufunktionen. Bei diesem Member kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**BATTERY \_ \_RELATIVE**</dt> <dt>0X40000000</dt> DER KAPAZITÄT </dl>                    | Gibt an, dass die Akkukapazitäts- und Rateninformationen relativ und nicht in bestimmten Einheiten sind. Wenn dieses Bit nicht festgelegt ist, sind die Berichtseinheiten millwatt-hours (mWh) für kapazität und milliwatts (mW) für rate. Wenn dieses Bit festgelegt ist, können alle Verweise auf Einheiten in der anderen Akkudokumentation ignoriert werden. Alle Preisinformationen werden in Einheiten pro Stunde gemeldet. Wenn beispielsweise die vollständig geladene Kapazität als 100 gemeldet wird, gibt eine Rate von 200 an, dass der Akku die gesamte Kapazität in einer halben Stunde nutzt.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**BATTERY \_ IS \_ SHORT \_ TERM**</dt> <dt>0x20000000</dt> </dl>                               | Gibt an, dass der normale Vorgang für eine ausfallsichere Funktion vorgesehen ist. Wenn dieses Bit nicht festgelegt ist, wird erwartet, dass der Akku während der normalen Systemnutzung verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**BATTERY \_ SET \_ CHARGE \_ SUPPORTED**</dt> <dt>0x00000001</dt> </dl>          | Gibt an, dass Setinformationsanforderungen vom Typ BatteryCharge von diesem Akkugerät unterstützt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**BATTERY \_ FESTLEGEN \_ \_ DER UNTERSTÜTZTEN**</dt> <dt>0X00000002</dt> </dl> | Gibt an, dass Setinformationsanforderungen vom Typ BatteryDischarge von diesem Akkugerät unterstützt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**BATTERY \_ SYSTEM \_ BATTERY**</dt> <dt>0x80000000</dt> </dl>                             | Gibt an, dass der Akku eine allgemeine Stromversorgung für die Ausführung des Systems bereitstellen kann.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Technologie**
</dt> <dd>

Die Akkutechnologie. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                        | Bedeutung                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nicht verladebarer Akku, z. B. 1-1-1600-Akku.<br/> |
| <dl> <dt>1</dt> </dl> | Akkustand, z. B. Lead acid.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Chemie**
</dt> <dd>

Eine abgekürzte Zeichenfolge, die die Chemie des Akkus angibt. Diese Zeichenfolge ist nicht unbedingt auf null endend. Im Folgenden finden Sie eine partielle Liste der Abkürzungen, die zurückgegeben werden können, sowie die zugehörigen Ries.



| Unicode-Zeichenfolge                                                                                                                                           | Bedeutung                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Lead Acid<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**Löwe**</dt> </dl>                        | Lithium Ion<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Lithium Ion<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**Nicd**</dt> </dl> | Während Dessins<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**Nimh**</dt> </dl> | Metal-Hydride<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**Nizn**</dt> </dl> | Während der 1990er<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese<br/> |



 

In Zukunft werden möglicherweise andere Brüche angezeigt, und Ihr Code sollte in der Lage sein, sie zu verarbeiten.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

Die theoretische Kapazität des Akkus, wenn neu, in mWh, es sei denn, BATTERY \_ CAPACITY \_ RELATIVE ist festgelegt. In diesem Fall sind die Einheiten nicht definiert.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

Die aktuelle, vollständig geladene Kapazität des Akkus in mWh (oder relativ). Vergleichen Sie diesen Wert mit **DesignedCapacity,** um den Akkuverschleiß zu schätzen.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Die vom Hersteller vorgeschlagene Kapazität in mWh, bei der eine Warnung aufgrund niedriger Akkukapazität auftreten sollte. Definitionen von niedrig variieren von Hersteller zu Hersteller. Im Allgemeinen tritt ein Warnungszustand vor einem niedrigen Zustand auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist. Um das Risiko von Datenverlusten zu verringern, wird dieser Wert in der Regel als Standardeinstellung für den kritischen Akkualarm verwendet.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Die vom Hersteller vorgeschlagene Kapazität in mWh, bei der eine Warnung des Akkus ausgegeben werden soll. Definitionen der Warnung variieren von Hersteller zu Hersteller. Im Allgemeinen tritt ein Warnungszustand vor einem niedrigen Zustand auf, aber Sie sollten nicht davon ausgehen, dass dies immer der Fall ist. Um das Risiko von Datenverlusten zu verringern, wird dieser Wert in der Regel als Standardeinstellung für den Alarm mit niedriger Akkukapazität verwendet.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Ein Bias von 0 (null) in mWh, der auf die Akkuberichterstellung angewendet wird. Einige Akkus reservieren eine kleine Gebühr, die von den Kapazitätswerten der Akkus verzerrt ist, um "0" als kritischen Akkustand anzuzeigen. Kritische Voreingenommenheit ist analog zum Festlegen eines Kraftstoffmessgeräts, um "leer" anzuzeigen, wenn mehrere Liter Kraftstoff übrig sind.

</dd> <dt>

**CycleCount**
</dt> <dd>

Die Anzahl der Lade-/Entladungszyklen des Akkus. Dies bietet eine Möglichkeit, den Akkuverschleiß zu bestimmen. Wenn der Akku keinen Zykluszähler unterstützt, ist dieser Member 0 (null).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im Allgemeinen tritt ein Warnungszustand vor einem niedrigen Zustand auf, aber Sie sollten nicht davon ausgehen, dass dies der Fall ist. Es ist möglich, einen Akku abzufragen und zu ermitteln, dass keine Warnungsstufe aufgetreten ist, und den Akku erneut abzufragen und zu ermitteln, dass er in dem Umfang entladen wurde, in dem beide Ebenen erreicht wurden. Dies kann darauf hindeuten, dass Sie nicht oft genug abfragen. Dies kann auch darauf hindeuten, dass der Akku eine Gebühr sehr lange nicht aufnehmen kann und schneller als erwartet entladen wird. Eine solche Akkukapazität kann sich dem Ende ihrer Nutzungsdauer nähern oder beschädigt sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




