---
title: WINBIO_EXTENDED_SENSOR_INFO-Struktur (Winbio \_ types.h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO Struktur Windows Biometrieframework-API
- PWINBIO_EXTENDED_SENSOR_INFO Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: dd8c323b4f4e3847c399e314da22048f658fb68c3b07ecf82f71ce0ed327c368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910418"
---
# <a name="winbio_extended_sensor_info-structure"></a>WINBIO \_ EXTENDED \_ SENSOR \_ INFO-Struktur

Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit.

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

**GenericSensorCapabilities**
</dt> <dd>

Die generischen Funktionen der Sensorkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Struktur Informationen zu Funktionen und Registrierungsanforderungen des Sensoradapters enthält. Wenn der Wert des **Factor-Members** beispielsweise **WINBIO \_ TYPE \_ FINGERPRINT** lautet, gilt die **WINBIO \_ EXTENDED SENSOR \_ \_ INFO-Struktur** für einen Fingerabdruckleser und enthält die relevanten Informationen in der **Specifc.Fingerprint-Struktur.**

</dd> <dt>

**Bestimmten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit im Zusammenhang mit Gesichtsfunktionen.

<dl> <dt>

**FrameSize**
</dt> <dd>

Die Größe des Kamerarahmens, die von den **rechten** und **unteren** Membern der [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) als Länge und Breite in Pixel angegeben wird. Der Punkt (0, 0) stellt die linke obere Ecke des Frames dar.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Der Offset des Kamerarahmens für das Gesicht von der Videokamera in Pixel. Der Wert (0, 0) gibt an, dass sich der Kamerarahmen für das Gesicht und die Videokamera vollständig überlappen.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Die bevorzugte Ausrichtung für die Kamera.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruckmustern.

<dl> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit im Zusammenhang mit Irismustern.

<dl> <dt>

**FrameSize**
</dt> <dd>

Die Größe des Kamerarahmens, die von den **rechten** und **unteren** Membern der [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) als Länge und Breite in Pixel angegeben wird. Der Punkt (0, 0) stellt die linke obere Ecke des Frames dar.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Der Offset des Kamerarahmens für die Iris von der Videokamera in Pixel. Der Wert (0, 0) gibt an, dass sich der Kamerarahmen für die Iris und die Videokamera vollständig überlappen.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Die bevorzugte Ausrichtung für die Kamera.

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Sensoradapters für eine biometrische Einheit im Zusammenhang mit Stimmmustern.

<dl> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WINBIO \_ CAPABILITY-Konstanten**](winbio-capability-constants.md)
</dt> <dt>

[**WINBIO \_ BIOMETRIC \_ TYPE-Konstanten**](winbio-biometric-type-constants.md)
</dt> <dt>

[**WINBIO \_ ORIENTATION-Konstanten**](winbio-orientation-constants.md)
</dt> </dl>

 

