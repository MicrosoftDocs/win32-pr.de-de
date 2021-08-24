---
description: Enthält Informationen zur Akkuabfrage.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: BATTERY_QUERY_INFORMATION -Struktur (Poclass.h)
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
ms.openlocfilehash: 9049517108cbb31df1164cc88640a78e104e2902d3a8a4b8dec4b8bfb48e8a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143683"
---
# <a name="battery_query_information-structure"></a>BATTERY \_ QUERY \_ INFORMATION-Struktur

Enthält Informationen zur Akkuabfrage. Diese Struktur wird mit dem [**IOCTL \_ BATTERY \_ QUERY INFORMATION-Steuerungscode \_**](ioctl-battery-query-information.md) verwendet, um den Typ der zurück zu gebenden Informationen anzugeben.

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

**BatteryTag**
</dt> <dd>

Das aktuelle Akkutag für den Akku. Es können nur Informationen für einen Akku zurückgegeben werden, der mit dem Tag übereinstimmen kann. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus übereinstimmen, wird die IOCTL-Anforderung mit ERROR \_ FILE \_ NOT FOUND \_ abgeschlossen. Dies weist den Aufrufer darauf hin, dass der dem Tag zugeordnete Akku länger vorhanden ist. Der Aufrufer kann den [**IOCTL \_ BATTERY QUERY \_ \_ TAG-Vorgang**](ioctl-battery-query-tag.md) verwenden, um das Tag des neu installierten Akkus zu bestimmen, sofern vorhanden. (Weitere [Informationen finden Sie unter Akkutags.)](battery-information.md)

Wenn eine Abfrageinformationsanforderung erfolgt, wird dieser Wert überprüft. Wenn die Anforderung noch in Bearbeitung ist, während sich dieser Wert ändert, wird die Anforderung mit dem Status ERROR \_ FILE NOT FOUND \_ (FEHLERDATEI NICHT \_ GEFUNDEN) abgebrochen.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Die Ebene der abgefragten Akkuinformationen. Die von IOCTL zurückgegebenen Daten hängen von diesem Wert ab. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Mit NULL beendete Unicode-Zeichenfolge, die den Namen des Akkus enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | Ein **ULONG-Wert,** der die geschätzte Akkulaufzeit in Sekunden angibt. Wenn die im **AtRate-Member** der **BATTERY \_ QUERY \_ INFORMATION-Struktur** bereitgestellte Entleerungsrate null ist, basiert diese Berechnung auf der aktuellen Entleerungsrate. Wenn **AtRate** ungleich 0 (null) ist, ist die zurückgegebene Zeit die erwartete Laufzeit für die gegebene Rate. Wenn die geschätzte Zeit unbekannt ist (z. B. wird der Akku nicht entladen, und der angegebene **AtRate-Wert** war null), ist der Rückgabewert BATTERY \_ UNKNOWN \_ TIME. Beachten Sie, dass dieser Wert bei einigen Akkusystemen nicht sehr genau ist und je nach aktuellem Energieverbrauch stark variieren kann, was von der Datenträgeraktivität und anderen Faktoren beeinflusst werden kann. Es gibt keinen Benachrichtigungsmechanismus für Änderungen an diesem Wert.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Ein Array von [**BATTERY \_ REPORTING \_ SCALE-Strukturen,**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) nie mehr als vier Einträge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Eine [**BATTERY \_ INFORMATION-Struktur.**](battery-information-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Eine [**BATTERY \_ MANUFACTURE \_ DATE-Struktur.**](battery-manufacture-date-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Mit NULL beendete Unicode-Zeichenfolge, die den Namen des Herstellers des Akkus angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Mit NULL beendete Unicode-Zeichenfolge, die die Seriennummer des Akkus angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | Ein **ULONG-Wert,** der die aktuelle Temperatur des Akkus in 10 Grad Kelvin angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Mit NULL beendete Unicode-Zeichenfolge, die den Akku eindeutig identifiziert. Dieser Wert kann zum Nachverfolgen eines bestimmten Akkus verwendet werden. Bei intelligenten Akkus wäre diese ID die Verkettung des Herstellernamens, des Gerätenamens, des Herstellungsdatums und einer druckbaren Darstellung der Seriennummer. <br/> Dieser Wert soll dem Benutzer nicht angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Dieser Member wird nur verwendet, **wenn InformationLevel** batteryEstimatedTime ist.

Wenn dieses Mitglied ungleich 0 (null) ist, handelt es sich um eine Leerlaufzeit, die verwendet wird, um die Zeit zu berechnen, bis der Akku für batteryEstimatedTime eines einzelnen Akkus entladen wird. Sie muss in mW angegeben werden und muss ein negativer Wert sein, um eine Akkuladerate anzugeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Einige Informationen zu Akkus sind optional oder für einige Akkus bedeutungslos. Wenn der angeforderte Datentyp für den aktuellen Akku nicht verfügbar ist, wird ERROR \_ INVALID \_ FUNCTION zurückgegeben.

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

[**HERSTELLUNGSDATUM \_ DER \_ AKKUKAPAZITÄT**](battery-manufacture-date-str.md)
</dt> <dt>

[**BATTERY \_ REPORTING \_ SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




