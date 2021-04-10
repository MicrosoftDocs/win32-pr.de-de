---
description: Enthält Akku Abfrage Informationen.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: BATTERY_QUERY_INFORMATION-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 511980dd4307077b8b160550c661a15a5714b96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865084"
---
# <a name="battery_query_information-structure"></a>Struktur der Akku \_ Abfrage \_ Informationen

Enthält Akku Abfrage Informationen. Diese Struktur wird zusammen mit dem IOCTL-Steuerelement Code für die [**\_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md) verwendet, um den Typ der zurück zugebende Informationen anzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Batterytag**
</dt> <dd>

Das aktuelle Akku Kennzeichen für den Akku. Es können nur Informationen zu einem Akku zurückgegeben werden, der mit dem Tag übereinstimmt. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus identisch ist, wird die ioctl-Anforderung mit der Fehler \_ Datei \_ nicht \_ gefunden. Dadurch wird dem Aufrufer angezeigt, dass der mit dem Tag verbundene Akku länger vorhanden ist. Der Aufrufer kann den [**IOCTL- \_ Akku- \_ abfragetagvorgang \_**](ioctl-battery-query-tag.md) verwenden, um das Tag des neu installierten Akkus zu ermitteln, sofern vorhanden. (Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)

Wenn eine Abfrage Informationsanforderung erfolgt, wird dieser Wert überprüft. Wenn die Anforderung ausgeführt wird, während sich dieser Wert ändert, wird die Anforderung mit dem Status "Fehler \_ Datei nicht gefunden" abgebrochen \_ \_ .

</dd> <dt>

**Informationlevel**
</dt> <dd>

Die Ebene der Akku Informationen, die abgefragt werden. Die von IOCTL zurückgegebenen Daten hängen von diesem Wert ab. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**Akku-DeviceName**</dt> <dt>4</dt> </dl>                                                 | Eine mit NULL beendete Unicode-Zeichenfolge, die den Akku Namen enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**Batteryestimatedtime**</dt> <dt>3</dt> </dl>                                     | Ein **ulong** -Wert, der die geschätzte Akkulaufzeit in Sekunden angibt. Wenn die für das **atrate** -Element der Struktur der **Akku \_ Abfrage \_ Informationen** angegebene Ausgleichs Rate 0 (null) ist, basiert diese Berechnung auf der aktuellen Rate des Ausgleichs. Wenn **atate** ungleich NULL ist, ist die zurückgegebene Zeit die erwartete Laufzeit für die angegebene Rate. Wenn die geschätzte Zeit unbekannt ist (z. b. wenn der Akku nicht entladen wird und der angegebene **atate** NULL ist), ist der Rückgabewert "Akku- \_ unbekannter \_ Zeit". Beachten Sie, dass dieser Wert für einige Akku Systeme nicht sehr genau ist und abhängig von der aktuellen Stromversorgung, die von der Datenträger Aktivität und anderen Faktoren betroffen sein könnte, stark variieren kann. Es gibt keinen Benachrichtigungs Mechanismus für Änderungen dieses Werts.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**Batterygranularityinformation**</dt> <dt>1</dt> </dl> | Ein Array von [**Akku \_ Berichterstattungs- \_ Skalierungs**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) Strukturen, nie mehr als vier Einträge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**Batteryinformation**</dt> <dt>0</dt> </dl>                                             | Eine [**Akku \_ Informations**](battery-information-str.md) Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**Batterymanufacturedate**</dt> <dt>5</dt> </dl>                             | Eine [**Akku \_ Herstellungs \_ Datums**](battery-manufacture-date-str.md) Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**Batterymanufacturename**</dt> <dt>6</dt> </dl>                             | Eine auf NULL endenden Unicode-Zeichenfolge, die den Namen des Herstellers des Akkus angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**Akku SerialNumber**</dt> <dt>8</dt> </dl>                                         | Eine mit NULL beendete Unicode-Zeichenfolge, die die Seriennummer des Akkus angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**Akku Temperatur**</dt> <dt>2</dt> </dl>                                             | Ein **ulong** -Wert, der die aktuelle Temperatur des Akkus in Zehntel Grad Kelvin angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**Batteryuniqueid**</dt> <dt>7</dt> </dl>                                                         | Eine mit NULL beendete Unicode-Zeichenfolge, die den Akku eindeutig identifiziert. Dieser Wert kann verwendet werden, um einen bestimmten Akku zu verfolgen. Im Fall von intelligenten Akkus wäre diese ID die Verkettung aus dem Namen des Herstellers, dem Gerätenamen, dem Erstellungsdatum und der druckbaren Darstellung der Seriennummer. <br/> Dieser Wert sollte nicht für den Benutzer angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**Nachweis**
</dt> <dd>

Dieser Member wird nur verwendet, wenn **informationlevel den Wert** "batteryestimatedtime" hat.

Wenn dieser Member ungleich 0 (null) ist, handelt es sich um eine ablaufsrate, die verwendet wird, um die Zeit zu berechnen, bis der Akku für die Akku Zeit eines einzelnen Akkus entladen wurde. Es muss in MW angegeben werden, und es muss ein negativer Wert sein, um eine Akku Entlade Rate darzustellen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Einige Informationen zu Akkus sind optional oder für einige Akkus bedeutungslos. Wenn der jeweilige angeforderte Datentyp für den aktuellen Akku nicht verfügbar ist, wird die Fehler \_ Funktion "ungültig" \_ zurückgegeben.

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

[**Akku \_ Herstellungs \_ Datum**](battery-manufacture-date-str.md)
</dt> <dt>

[**\_Skalierung von Akku Berichten \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




