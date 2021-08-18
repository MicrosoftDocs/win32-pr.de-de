---
description: Enthält Informationen zu den Bedingungen, unter denen der Akkustatus abgerufen werden soll.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS-Struktur (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 52885b75c7f9afba7ff336b3210ecf1b852f85b0091afe13026616816e43d7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143593"
---
# <a name="battery_wait_status-structure"></a>BATTERY \_ WAIT \_ STATUS-Struktur

Enthält Informationen zu den Bedingungen, unter denen der Akkustatus abgerufen werden soll. Diese Struktur wird vom [**IOCTL \_ BATTERY QUERY \_ \_ STATUS-Steuerelementcode**](ioctl-battery-query-status.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**BatteryTag**
</dt> <dd>

Das aktuelle Akkutag für den Akku. Es können nur Informationen für einen Akku zurückgegeben werden, der dem Tag entspricht. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus übereinstimmt, schlägt der [**DeviceIoControl-Vorgang**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit dem Fehlercode ERROR \_ FILE NOT FOUND \_ \_ fehl. Dieser gibt dem Aufrufer an, dass der Akku, für den er ein Tag besitzt, nicht mehr installiert ist. Der Aufrufer kann den [**IOCTL \_ BATTERY QUERY \_ \_ TAG-Vorgang**](ioctl-battery-query-tag.md) verwenden, um ggf. das Tag des neu installierten Akkus zu bestimmen. Wenn die Anforderung ausgeführt wird, wenn der Akku entfernt wird oder sich das Tag ändert, wird der Vorgang mit dem Status \_ FEHLERDATEI \_ NICHT GEFUNDEN \_ abgebrochen. (Weitere Informationen finden Sie unter [Akkutags.)](battery-information.md)

</dd> <dt>

**Timeout**
</dt> <dd>

Die Anzahl von Millisekunden, die die Anforderung auf die von den **Membern PowerState,** **LowCapacity** und **HighCapacity** angegebene Bedingung wartet, bevor sie abgeschlossen wird. Der Wert -1 gibt an, dass die Anforderung unbegrenzt wartet, bis die Bedingungen erfüllt sind. Der Wert 0 gibt an, dass die angeforderten Akkuinformationen unabhängig von den anderen Bedingungen sofort zurückgegeben werden sollen. Jeder andere Wert gibt an, dass die Anforderung diese Zeitspanne oder eine der anderen Bedingungen warten soll.

Wenn der Computer in den Standbymodus versetzt wurde, wird die Uhr weiterhin ausgeführt, aber wenn die Anzahl erschöpft ist, wird der Computer nicht aktiviert. Wenn die Anzahl erschöpft ist, wenn der Computer aufgeweckt wird und andere Bedingungen erfüllt sind, wird der Aufruf sofort beim Aufwachen zurückgegeben.

</dd> <dt>

**PowerState**
</dt> <dd>

Null, ein oder mehrere der folgenden Statusbits, die den Zustand des Akkus angeben. Er ist identisch mit dem **PowerState-Member** der [**BATTERY \_ STATUS-Struktur.**](battery-status-str.md)



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**BATTERY \_**</dt> <dt>ABRECHNUNGs-0x00000004</dt> </dl>                  | Gibt an, dass der Akku gerade geladen wird.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**BATTERY \_ CRITICAL**</dt> <dt>0x00000008</dt> </dl>                  | Gibt an, dass ein Akkuausfall bevorsteht. Weitere Informationen finden Sie im Abschnitt Hinweise.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**BATTERY \_ DISCHARGING**</dt> <dt>0x00000002</dt> </dl>         | Gibt an, dass der Akku gerade entladen wird.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**BATTERY \_ POWER \_ ON \_ LINE**</dt> <dt>0x00000001</dt> </dl> | Gibt an, dass der Akku Zugriff auf die Stromversorgung hat.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

Die aktuelle Akkukapazität in mWh (oder relativ). Dieser Wert ist identisch mit dem **Capacity-Member** der [**BATTERY \_ STATUS-Struktur.**](battery-status-str.md)

</dd> <dt>

**HighCapacity**
</dt> <dd>

Die aktuelle Akkukapazität in mWh (oder relativ). Dieser Wert ist identisch mit dem **Capacity-Member** der [**BATTERY \_ STATUS-Struktur.**](battery-status-str.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Anforderungen für Akkuinformationen werden verschoben, bis eine der folgenden Vorgänge eintritt:

-   Das Timeout läuft ab **(vorausgesetzt, timeout** ist nicht -1).
-   Der aktuelle Status des Akkus stimmt nicht mit **PowerState** überein.
-   Die Kapazität des Akkus liegt **unterHalb von LowCapacity.**
-   Die Kapazität des Akkus liegt oberhalb **von HighCapacity.**
-   Das Akkutag ändert sich.

Wenn eine dieser Bedingungen erfüllt ist, werden die Daten gesammelt, und der Vorgang wird zurückgegeben. Dadurch können Anwendungen typische dynamische Akkuinformationen überwachen, ohne das Gerät abzufragen.

Bevor Sie eine der beiden Kapazitätsbedingungen verwenden, stellen Sie sicher, dass der Akku sie unterstützt, indem Sie den [**IOCTL \_ BATTERY \_ QUERY STATUS-Steuerungscode \_**](ioctl-battery-query-status.md) mit einem Time out von 0 (null) verwenden. Überprüfen Sie die Ergebnisse, um zu bestimmen, ob das **Capacity-Element** unterstützt wird (d. b. nicht BATTERY \_ UNKNOWN \_ CAPACITY).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_AKKUSTATUS**](battery-status-str.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md)
</dt> </dl>

 

