---
title: WINBIO_PRESENCE_PROPERTIES Union (Winbio \_ types.h)
description: Enthält biometrische Werte, die das Windows biometrische Framework verwendet hat, um zu bestimmen, ob eine Person vorhanden war.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES union Windows Biometric Framework-API
- PWINBIO_PRESENCE_PROPERTIES Union-Zeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 6a3964883f5dcd5b00c6f3eb6929c9deec99e58db014d18e51a192180a4d11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909655"
---
# <a name="winbio_presence_properties-union"></a>WINBIO \_ PRESENCE \_ PROPERTIES union

Enthält biometrische Werte, die das Windows biometrische Framework verwendet hat, um zu bestimmen, ob eine Person vorhanden war.

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

**Gesichtsfeatures**
</dt> <dd>

Werte für den Ort der Gesichtsfeatures, die das Windows biometrische Framework verwendet hat, um zu bestimmen, ob eine Person vorhanden war.

<dl> <dt>

**Boundingbox**
</dt> <dd>

Die Position innerhalb des Kamerarahmens des Gesichts der Einzelperson in Pixel. Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl von Pixeln für diese Position. Verwenden Sie die **WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuordnen zu können.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen der tatsächlichen Position des Gesichts und dem idealen Fokusabstand für das Gesicht. Dieser Wert liegt zwischen -100 und 100. 0 gibt den idealen Abstand an, positive Werte geben an, dass die tatsächliche Position des Gesichts zu weit entfernt ist, und negative Werte zeigen an, dass die tatsächliche Position zu nah ist.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Werte für den Iris-Standort, Windows biometrisches Framework verwendet wurde, um zu bestimmen, ob eine Person vorhanden war.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Die Position innerhalb des Kamerarahmens einer der Iris der zu registrierenden Person in Pixel. Wenn das Iriserkennungssystem nur ein Auge überwacht, ist diese Position die Iris dieses Auges. Wenn das Iriserkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamerarahmen befindet, ist diese Position die Iris des Auges im Kamerarahmen. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, ist diese Position wahrscheinlich die Iris des rechten Auges der Person.

Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl von Pixeln für diese Position. Verwenden Sie die **WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuordnen zu können.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Die Position innerhalb des Kamerarahmens einer der Iris der zu registrierenden Person in Pixel. Wenn das Iriserkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamerarahmen befindet, ist dieser Wert leer. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, ist diese Position wahrscheinlich die Iris des linken Auges der Person.

Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl von Pixeln für diese Position. Verwenden Sie die **WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuordnen zu können.

</dd> <dt>

**Center \_ 1**
</dt> <dd>

Die Position des Mittelpunkts eines der zu registrierenden Personen. Wenn das Iriserkennungssystem nur ein Auge überwacht, befindet sich diese Position in der Mitte des Auges. Wenn das Iriserkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamerarahmen befindet, befindet sich diese Position in der Mitte des Auges im Kamerarahmen. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, liegt diese Position wahrscheinlich in der Mitte des Rechten Auges des Einzelnen.

</dd> <dt>

**Center \_ 2**
</dt> <dd>

Die Position des Mittelpunkts eines der zu registrierenden Personen. Wenn das Iriserkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamerarahmen befindet, ist dieser Wert leer. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, liegt diese Position wahrscheinlich in der Mitte des Linken Auges der Person.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen der tatsächlichen Position der Iris und dem idealen Fokusabstand für die Iris. Dieser Wert liegt zwischen -100 und 100. 0 gibt den idealen Abstand an, positive Werte geben an, dass die tatsächliche Position der Iris zu weit entfernt ist, und negative Werte zeigen an, dass die tatsächliche Position zu nah ist.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter enthalten)</dt> </dl> |



 

 





