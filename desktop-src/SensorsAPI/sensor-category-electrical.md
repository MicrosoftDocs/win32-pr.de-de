---
description: Die Kategorie Kategorie " \_ Kategorie" \_ enthält Sensoren, die Informationen zu elektrischen Systemen bereitstellen.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348758"
---
# <a name="sensor_category_electrical"></a>Sensor \_ Kategorie ( \_ elektrisch)

Die Kategorie Kategorie " \_ Kategorie" \_ enthält Sensoren, die Informationen zu elektrischen Systemen bereitstellen.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                              | BESCHREIBUNG                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Sensor \_ \_Typcapacitance**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Kapazitäts Sensoren.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Sensor \_ Geben \_**</dt> Sie "Current <dt>{5adc9f CE-15a0-4bbe-a1ad-2d38a9ae831c}</dt> " ein. </dl>                             | Aktuelle elektrische Sensoren.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Electric \_ Power**</dt> <dt>{212F f 5-14ab-4376-9a43-a7794098c2fe}</dt> " ein. </dl> | Stromsensoren.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Sensor \_ \_Typhäufigkeit**</dt> <dt>{8cd2cbb6-73e6-4640-a709-72ae8fb60d7f}</dt> </dl>                       | Elektrischer Frequenz Sensor.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Inductance**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> " ein. </dl>                    | Inductance-Sensoren.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Sensor \_ Type- \_ potenzimesser**</dt> <dt>{2b3681a9-CADC-45AA-a6ff-54957c8bb440}</dt> </dl>           | Ein potenzimesser.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Sensor \_ \_Typresistenz**</dt> <dt>{9993d2c8-C157-4a52-a7b5-195c76037231}</dt> </dl>                    | Widerstands Sensoren.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Sensor \_ \_Typspannung**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Spannungs Sensoren.<br/>             |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ elektrischen GUID des Sensor- \_ Datentyps \_ \_ :

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Sensor \_ Datentyp- \_ \_ CAPACITANCE \_ Farad**</dt> <dt> (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> Kapazität in Farads.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Sensor \_ Data \_ Type \_ Current \_ Amps**</dt> <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Aktuell in Amperes.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Sensor \_ Datentyp ( \_ \_ elektrische \_ Frequenz) \_ Hertz**</dt> <dt>(PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Elektrische Frequenz in Hertz.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Strom \_ \_ in Prozent des \_ Bereichs**</dt> <dt>(PID = 8)</dt> </dl> | **VT \_ R8**<br/> Der Wert Messer, der als Prozentsatz des möglichen Bereichs gelesen wird.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Sensor \_ Datentyp Strom Potenz \_ \_ \_ \_ Watt**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Stromversorgung in Watt.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Inductance \_ Henry**</dt> <dt>(PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Inductance in "Henries".<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Resistenz- \_ Ohms**</dt> <dt>(PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Widerstand in Ohms.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Spannungs \_ Volt**</dt> <dt>(PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Das elektrische Potenzial in Volt.<br/>                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




