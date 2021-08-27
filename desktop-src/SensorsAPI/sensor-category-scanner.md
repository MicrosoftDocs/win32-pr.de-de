---
description: Die Kategorie SENSOR \_ CATEGORY \_ SCANNER enthält Sensoren, die Informationen bereitstellen, die durch das Scannen abgerufen werden.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59af4dbcd4ce4687a7fe2853384b4b19287cd95a0dd2033e7af031d2289f3d87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126590"
---
# <a name="sensor_category_scanner"></a>\_ \_ SENSORKATEGORIESCANNER

Die Kategorie SENSOR \_ CATEGORY \_ SCANNER enthält Sensoren, die Informationen bereitstellen, die durch das Scannen abgerufen werden.

**Plattformdefinierte Sensortypen**

Diese Kategorie umfasst die folgenden plattformdefinierte Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                           | Beschreibung                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**SENSOR \_ TYP \_ \_ BARCODESCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Sensoren, die optisches Scannen verwenden, um Balkencodes zu lesen.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**SENSOR \_ TYPE \_ \_ SCANNER SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Radiofrequenz-ID-Scansensoren.<br/>                 |



**Plattformdefinierte Datenfelder**

Plattformdefinierte Eigenschaftsschlüssel für diese Kategorie basieren auf der \_ SENSOR DATA TYPE SCANNER \_ \_ \_ GUID:

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Diese Kategorie umfasst die folgenden plattformdefinierte Datenfelder.



| Datenfeldname und PID                                                                                                                                                                                                                                                                     | Beschreibung                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**SENSOR \_ \_DATENTYP: \_ TAGS \_ \_ 40 \_ BIT**</dt> <dt>(PID = 2)</dt> </dl> | **VT \_ UI8**<br/> Tagwert der 40-Bit-Radiofrequenz-ID.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




