---
title: WINBIO_EXTENDED_ENROLLMENT_STATUS-Struktur (Winbio \_ types.h)
description: Enthält zusätzliche Informationen zum Status einer registrierung, die gerade ausgeführt wird.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS Struktur Windows Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_STATUS Strukturzeiger Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab3736e3ad5b0bcf10bed1fb606d3e6283715a6b10c44dcb4923920597d5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910445"
---
# <a name="winbio_extended_enrollment_status-structure"></a>WINBIO \_ EXTENDED \_ ENROLLMENT \_ STATUS-Struktur

Enthält zusätzliche Informationen zum Status einer registrierung, die gerade ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**TemplateStatus**
</dt> <dd>

Der Status der Beispielsammlung für die Registrierungsvorlage. Die folgenden Werte sind für diesen Member möglich.



| Wert                                                                                                                                                                                                  | Bedeutung                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                     | Die Registrierung kann gespeichert werden.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ INVALID \_ OPERATION**</dt> </dl> | Es wird keine Registrierung ausgeführt.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> </dl>                         | Weitere Beispiele sind erforderlich, um die Vorlage abzuschließen.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ BAD \_ CAPTURE**</dt> </dl>                   | Das neueste Beispiel kann nicht verwendet werden.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Der Grund, warum das letzte Beispiel nicht verwendet werden kann, wenn der Wert des **TemplateStatus-Members** **WINBIO \_ E BAD \_ \_ CAPTURE** ist.

</dd> <dt>

**PercentComplete**
</dt> <dd>

Die beste Schätzung des Engine-Adapters für den Prozentsatz der vorlage, die abgeschlossen ist, als Wert von 0 bis 100.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Struktur Informationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält. Wenn der Wert des **Factor-Members** beispielsweise **WINBIO \_ TYPE \_ FINGERPRINT** ist, gilt die [**WINBIO \_ EXTENDED ENGINE \_ \_ INFO-Struktur**](winbio-extended-engine-info.md) für einen Fingerabdruckleser und enthält die relevanten Informationen in der **Specifc.Fingerprint-Struktur.**

</dd> <dt>

**SubFactor**
</dt> <dd>

Ein **WINBIO \_ BIOMETRIC \_ SUBTYPE-Wert,** der zusätzliche Informationen zur Registrierung bereitstellt.

</dd> <dt>

**Bestimmten**
</dt> <dd>

Informationen zum Status einer Registrierung, die für einen bestimmten biometrischen Faktor ausgeführt wird.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Gesichtsmerkmale ausgeführt wird.

<dl> <dt>

**Boundingbox**
</dt> <dd>

Die Position innerhalb des Kamerarahmens des Gesichts der person, die registriert werden soll, in Pixel. Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Abrufen der **WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuzuordnen.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen der tatsächlichen Position des Gesichts und dem idealen Fokusabstand für das Gesicht. Dieser Wert liegt zwischen -100 und 100. 0 gibt den idealen Abstand an, positive Werte geben an, dass die tatsächliche Position des Gesichts zu weit entfernt ist, und negative Werte geben an, dass die tatsächliche Position zu nah ist.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Fingerabdruckmuster ausgeführt wird.

<dl> <dt>

**AllgemeineSamples**
</dt> <dd>

Die Gesamtzahl der Stichproben, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**Center**
</dt> <dd>

Die Anzahl der Stichproben für die Mitte des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**TopEdge**
</dt> <dd>

Die Anzahl der Stichproben für den oberen Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Die Anzahl der Stichproben für den unteren Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Die Anzahl der Stichproben für den linken Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**RightEdge**
</dt> <dd>

Die Anzahl der Stichproben für den rechten Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Irismuster ausgeführt wird.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Die Position innerhalb des Kamerarahmens einer der Schwertlilien der zu registrierenden Person in Pixel. Wenn das Iriserkennungssystem nur ein Auge überwacht, entspricht diese Position der Iris dieses Auges. Wenn das Iriserkennungssystem beide Augen überwacht, sich aber nur ein Auge im Kamerarahmen befindet, befindet sich diese Position von der Iris des Auges im Kamerarahmen. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, ist diese Position wahrscheinlich die Iris des rechten Auges des Einzelnen.

Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Abrufen der **WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuzuordnen.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Die Position innerhalb des Kamerarahmens einer der Schwertlilien der zu registrierenden Person in Pixel. Wenn das Iriserkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamerarahmen befindet, ist dieser Wert leer. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, ist diese Position wahrscheinlich die Iris des linken Auges des Einzelnen.

Die Größe des Kamerarahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Abrufen der **WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO-Eigenschaft,** um die Größe des Kamerarahmens zu bestimmen. Ein Client, der den Anwesenheitsmonitor verwendet, muss den Skalierungsvorgang ausführen, um die Position dem Kamerarahmen zuzuordnen.

</dd> <dt>

**\_1. 1.**
</dt> <dd>

Die Position des Mittelpunkts eines der Zu registrierenden Personen. Wenn das Schwertlilienerkennungssystem nur ein Auge überwacht, ist diese Position der Mittelpunkt des Auges. Wenn das Iriserkennungssystem beide Augen überwacht, aber nur ein Auge im Kamerarahmen ist, befindet sich diese Position in der Mitte des Mittelpunkts des Auges im Kamerarahmen. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, befindet sich diese Position wahrscheinlich im Mittelpunkt des Rechten Auges des Einzelnen.

</dd> <dt>

**Zu den \_ 2010er-Jahren**
</dt> <dd>

Die Position des Mittelpunkts eines der Zu registrierenden Personen. Wenn das Iriserkennungssystem nur ein Auge überwacht oder sich nur ein Auge im Kamerarahmen befindet, ist dieser Wert leer. Wenn das Iriserkennungssystem beide Augen überwacht und sich beide Augen im Kamerarahmen befinden, befindet sich diese Position wahrscheinlich im Mittelpunkt des Linken Auges des Einzelnen.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen der tatsächlichen Position der Iris und dem idealen Fokusabstand für die Iris. Dieser Wert liegt zwischen -100 und 100. 0 gibt den idealen Abstand an, positive Werte geben an, dass die tatsächliche Position der Iris zu weit entfernt ist, und negative Werte geben an, dass die tatsächliche Position zu nah ist.

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Stimmmuster ausgeführt wird.

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



 

 





