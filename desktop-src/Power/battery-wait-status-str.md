---
description: Enthält Informationen zu den Bedingungen, unter denen der Akku Status abgerufen werden soll.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS-Struktur (poclass. h)
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
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351677"
---
# <a name="battery_wait_status-structure"></a>\_ \_ Status Struktur der Akku Wartezeit

Enthält Informationen zu den Bedingungen, unter denen der Akku Status abgerufen werden soll. Diese Struktur wird vom Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung verwendet.

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

**Batterytag**
</dt> <dd>

Das aktuelle Akku Kennzeichen für den Akku. Es können nur Informationen zu einem Akku zurückgegeben werden, der mit dem Tag übereinstimmt. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus identisch ist, misslingt der [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Vorgang mit dem Fehlercode "Fehler \_ Datei \_ nicht \_ gefunden", was dem Aufrufer anzeigt, dass der Akku, für den er ein Tag besitzt, nicht mehr installiert ist. der Aufrufer kann den [**IOCTL- \_ Akku \_ abfragetagvorgang \_**](ioctl-battery-query-tag.md) verwenden, um ggf Außerdem wird der Vorgang abgebrochen, wenn die Anforderung beim Entfernen des Akkus oder das Tag geändert wird, und der Status der Fehler \_ Datei wurde \_ nicht \_ gefunden. (Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)

</dd> <dt>

**Timeout**
</dt> <dd>

Die Anzahl der Millisekunden, die die Anforderung auf die von den Elementen " **PowerState**", " **lowcapacity**" und " **highcapacity** " angegebene Bedingung wartet, bevor Sie abgeschlossen wird. Der Wert-1 gibt an, dass die Anforderung unbegrenzt wartet, bis die Bedingungen erfüllt sind. Der Wert 0 (null) gibt an, dass die angeforderten Akku Informationen unabhängig von den anderen Bedingungen sofort zurückgegeben werden sollen. Jeder andere Wert gibt an, dass die Anforderung auf die Zeitspanne warten soll, oder bis eine der anderen Bedingungen erfüllt ist.

Wenn sich der Computer im Energiesparmodus befindet, wird die Uhr weiterhin ausgeführt, aber die Anzahl der Ausschöpfung wird den Computer nicht verbleiben. Wenn die Anzahl erschöpft ist, wenn der Computer aktiviert ist, und andere Bedingungen erfüllt sind, wird der-Rückruf sofort beim Erwachen zurückgegeben.

</dd> <dt>

**PowerState**
</dt> <dd>

NULL, mindestens eine der folgenden Status Bits, die den Zustand des Akkus angeben. Es ist identisch mit dem **PowerState** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Akku \_ Berechnen**</dt> von <dt>0x00000004</dt> </dl>                  | Gibt an, dass der Akku zurzeit berechnet wird.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Akku \_ Kritisch**</dt> <dt>0x00000008</dt> </dl>                  | Gibt an, dass Akku Fehler bevorstehend ist. Weitere Informationen finden Sie im Abschnitt Hinweise.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Akku \_**</dt>" <dt>0x00000002</dt> " wird entladen </dl>         | Gibt an, dass der Akku gerade entladen wird.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Akku \_ Netzteil \_ der \_ Zeile**</dt> <dt>0x00000001</dt> </dl> | Gibt an, dass der Akku Zugang zur Stromversorgung hat.<br/>                                        |



 

</dd> <dt>

**Lowcapacity**
</dt> <dd>

Die aktuelle Akkukapazität in MWh (oder relativ). Dieser Wert ist identisch mit dem **Capacity** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.

</dd> <dt>

**Highcapacity**
</dt> <dd>

Die aktuelle Akkukapazität in MWh (oder relativ). Dieser Wert ist identisch mit dem **Capacity** -Member der [**Akku \_ Status**](battery-status-str.md) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Anforderungen für Akku Informationen werden bis zu einem der folgenden Punkte verschoben:

-   Das Timeout läuft ab (vorausgesetzt, **Timeout** ist nicht-1).
-   Der aktuelle Status des Akkus stimmt nicht mit dem **PowerState**-Wert.
-   Die Kapazität des Akkus liegt unter **lowcapacity**.
-   Die Kapazität des Akkus liegt über der **highcapacity**.
-   Das Akku-Tag ändert sich.

Wenn eine dieser Bedingungen erfüllt ist, werden die Daten gesammelt und der Vorgang zurückgegeben. Dadurch können Anwendungen typische dynamische Akku Informationen überwachen, ohne das Gerät abzufragen.

Bevor Sie eine der beiden Kapazitäts Bedingungen verwenden, stellen Sie sicher, dass der Akku diese unterstützt, indem Sie den Code der [**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md) Steuerung mit einem Timeout von 0 (null) verwenden. Überprüfen Sie die Ergebnisse, um zu bestimmen, ob das **Kapazitäts** Mitglied unterstützt wird \_ \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Akku \_ Status**](battery-status-str.md)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> </dl>

 

