---
title: WINBIO_PRESENCE_PROPERTIES Union (winbio \_ types. h)
description: Enthält biometrische Werte, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES Union Windows-Biometrieframework-API
- PWINBIO_PRESENCE_PROPERTIES Union-Zeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475663"
---
# <a name="winbio_presence_properties-union"></a>Winbio- \_ Anwesenheits \_ Eigenschaften Union

Enthält biometrische Werte, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.

## <a name="syntax"></a>Syntax


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a>Member

<dl> <dt>

**Fakialfeatures**
</dt> <dd>

Werte für den Speicherort der Gesichts Features, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Die Position innerhalb des Kamera Rahmens der Vorderseite der Person in Pixel. Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens. Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen dem tatsächlichen Speicherort der Vorderseite und dem idealen Fokusabstand für das Gesicht. Dieser Wert liegt zwischen-100 und 100. 0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der Fläche zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.

</dd> </dl> </dd> <dt>

**Augen**
</dt> <dd>

Werte für Iris-Speicherort, die der Windows-Biometrieframework, um zu bestimmen, ob eine Person vorhanden war.

<dl> <dt>

**Eyeboundingbox \_ 1**
</dt> <dd>

Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel. Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Schwert Position. Wenn das Schwert Erkennungssystem beide Augen überwacht, aber nur ein Auge im Kamera Rahmen ist, ist diese Position der Schwert im Kamera-Frame. Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.

Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens. Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.

</dd> <dt>

**Eyeboundingbox \_ 2**
</dt> <dd>

Die Position innerhalb des Kamera Rahmens einer der Irises der zu registrierenden Person in Pixel. Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer. Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen im Kamera Rahmen sind, ist diese Position wahrscheinlich die Schwert Ecke der Person.

Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens. Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.

</dd> <dt>

**Pupilcenter \_ 1**
</dt> <dd>

Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person. Wenn das Schwert Erkennungssystem nur ein Auge überwacht, liegt diese Position in der Mitte der Schülerin dieses Auges. Wenn das Schwert Erkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamera Rahmen befindet, liegt diese Position in der Mitte der Schülerin des Augen Bilds. Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte des Schülers der Person.

</dd> <dt>

**Pupilcenter \_ 2**
</dt> <dd>

Die Position der Mitte eines der zu registrierenden Schüler und/oder der zu registrierenden Person. Wenn das Schwert Erkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamera Rahmen befindet, ist dieser Wert leer. Wenn das Schwert Erkennungssystem beide Augen überwacht und beide Augen sich im Kamera Rahmen befinden, liegt diese Position wahrscheinlich in der Mitte der Schülerin des linken Auges der Person.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen dem tatsächlichen Speicherort der Iris und dem idealen Fokusabstand für die Iris. Dieser Wert liegt zwischen-100 und 100. 0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der IRIS zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



 

 





