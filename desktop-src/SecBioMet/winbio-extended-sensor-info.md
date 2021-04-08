---
title: WINBIO_EXTENDED_SENSOR_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_SENSOR_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949524"
---
# <a name="winbio_extended_sensor_info-structure"></a>\_Struktur erweiterter winbio- \_ Sensor \_ Informationen

Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Genericsensor-Funktionen**
</dt> <dd>

Die generischen Funktionen der sensorkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Sensor Adapters enthält. Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur **Erweiterter winbio- \_ \_ Sensor \_** für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.

</dd> <dt>

**Zugeschnitten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Fakialfeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.

<dl> <dt>

**FrameSize**
</dt> <dd>

Die Größe des Kamera Rahmens, angegeben als Länge und Breite in Pixel des **rechten** und **unteren** Members der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Der Punkt (0,0) stellt die obere linke Ecke des Frames dar.

</dd> <dt>

**Frameoffset**
</dt> <dd>

Der Offset des Kamera Rahmens für das Gesicht von der Videokamera in Pixel. Der Wert (0,0) gibt an, dass sich der Kamera Rahmen für das Gesicht und die Videokamera vollständig überlappt.

</dd> <dt>

**Mandatoryorientation**
</dt> <dd>

Die bevorzugte Ausrichtung für die Kamera.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.

<dl> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

**Augen**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.

<dl> <dt>

**FrameSize**
</dt> <dd>

Die Größe des Kamera Rahmens, angegeben als Länge und Breite in Pixel des **rechten** und **unteren** Members der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur. Der Punkt (0,0) stellt die obere linke Ecke des Frames dar.

</dd> <dt>

**Frameoffset**
</dt> <dd>

Der Offset des Kamera Rahmens für die Iris von der Videokamera in Pixel. Der Wert (0,0) gibt an, dass sich der Kamera Rahmen für die Iris und die Videokamera vollständig überlappt.

</dd> <dt>

**Mandatoryorientation**
</dt> <dd>

Die bevorzugte Ausrichtung für die Kamera.

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensor Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.

<dl> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Winbio-Funktions \_ Konstanten**](winbio-capability-constants.md)
</dt> <dt>

[**Winbio- \_ biometrische \_ Typkonstanten**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Winbio- \_ Orientierungs Konstanten**](winbio-orientation-constants.md)
</dt> </dl>

 

