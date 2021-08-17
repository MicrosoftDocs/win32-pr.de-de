---
description: Enthält den aktuellen Zustand des Akkus.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS -Struktur (Poclass.h)
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
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143603"
---
# <a name="battery_status-structure"></a>BATTERY \_ STATUS-Struktur

Enthält den aktuellen Zustand des Akkus. Diese Struktur wird vom [**IOCTL \_ BATTERY QUERY \_ \_ STATUS-Steuerungscode**](ioctl-battery-query-status.md) verwendet.

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

Der Akkuzustand. Dieser Member kann null, einer oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**AKKU \_ GEBÜHREN**</dt> <dt>0X00000004</dt> </dl>                  | Gibt an, dass der Akku gerade geladen wird.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**AKKU \_ CRITICAL**</dt> <dt>0x00000008</dt> </dl>                  | Gibt an, dass ein Akkuausfall bevorsteht. Weitere Informationen finden Sie im Abschnitt Hinweise.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**AKKU \_ ENTLADEN 0X00000002**</dt> <dt></dt> </dl>         | Gibt an, dass der Akku derzeit entladen wird.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**AKKU \_ \_ \_ EIN-/AUS-0X00000001**</dt> <dt></dt> </dl> | Gibt an, dass das System Zugriff auf die Stromversorgung hat, sodass keine Akkus entladen werden.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

Die aktuelle Akkukapazität in mWh (oder relativ). Dieser Wert kann verwendet werden, um eine "Gasmessgerätanzeige" zu generieren, indem sie durch **den FullChargedCapacity-Member** der [**BATTERY \_ INFORMATION-Struktur dividiert**](battery-information-str.md) wird. Wenn die Kapazität nicht verfügbar ist, ist dieses Mitglied BATTERY \_ UNKNOWN \_ CAPACITY.

</dd> <dt>

**Spannung**
</dt> <dd>

Die aktuelle Akkuspannung über die Akkuterminals in Millisekunden (mv). Wenn die Spannung nicht verfügbar ist, ist dieses Mitglied BATTERY \_ UNKNOWN \_ VOLTAGE.

</dd> <dt>

**Rate**
</dt> <dd>

Die aktuelle Rate der Akkuladung oder -entladung. Dieser Wert wird in Milliwatt angegeben, es sei denn, die Akkurateninformationen sind relativ. In diesem Fall werden beliebige Einheiten pro Stunde angegeben. Um festzustellen, ob Akkuinformationen relativ sind, überprüfen Sie das Flag BATTERY CAPACITY RELATIVE im \_ \_ **Capabilities-Member** der [**BATTERY \_ INFORMATION-Struktur.**](battery-information-str.md) Eine positive Rate ungleich 0 (null) gibt die Gebühren an. eine negative Rate gibt die Entladung an. Einige Akkus melden nur Dietladungsraten. Wenn die Rate nicht verfügbar ist, ist dieses Mitglied BATTERY \_ UNKNOWN \_ RATE. Wenn sich der Zustand des Akkus oder der Stromquelle ändert, kann die Rate verfügbar werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das BATTERY \_ CRITICAL-Flag im **PowerState-Member** dieser Struktur gibt eine "akkukritische" Hardwarebedingung an. Diese kritische Stufe wird vom Akkuhersteller festgelegt, nicht vom Benutzer im "kritischen Akkualarm". Dies bedeutet in der Regel, dass das Akkusystem berechnet hat, dass der Akku vollständig ausgeleert ist, und dass der stromgezogene Strom über dem erwarteten Wert liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003</dt> und Windows XP </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_AKKUINFORMATIONEN**](battery-information-str.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




