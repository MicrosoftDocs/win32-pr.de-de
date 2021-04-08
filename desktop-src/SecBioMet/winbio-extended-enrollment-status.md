---
title: WINBIO_EXTENDED_ENROLLMENT_STATUS Struktur (winbio \_ types. h)
description: Enthält weitere Informationen zum Status einer aktuell ausgeführten Registrierung.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_STATUS Struktur Zeiger Windows-Biometrieframework API
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
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103114"
---
# <a name="winbio_extended_enrollment_status-structure"></a>Struktur der erweiterten winbio-Registrierungs \_ \_ \_ Status

Enthält weitere Informationen zum Status einer aktuell ausgeführten Registrierung.

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

Der Status der Beispiel Auflistung für die Registrierungs Vorlage. Die folgenden Werte sind für diesen Member möglich.



| Wert                                                                                                                                                                                                  | Bedeutung                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                     | Die Registrierung kann jetzt gespeichert werden.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**\_Ungültiger winbio E- \_ \_ Vorgang**</dt> </dl> | Es wird keine Registrierung durchgeführt.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**winbio \_ I \_ more \_ Data**</dt> </dl>                         | Weitere Beispiele sind erforderlich, um die Vorlage abzuschließen.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**winbio \_ E ungültige \_ \_ Erfassung**</dt> </dl>                   | Das aktuelle Beispiel kann nicht verwendet werden.<br/>               |



 

</dd> <dt>

**Rejectdetail**
</dt> <dd>

Der Grund, warum das aktuellste Beispiel nicht verwendbar ist, wenn der Wert des **templatestatus** -Members **winbio E ungültige \_ \_ \_ Erfassung** ist.

</dd> <dt>

**PercentComplete**
</dt> <dd>

Die beste Schätzung vom Modul Adapter für den Prozentsatz der abgeschlossenen Vorlage als Wert zwischen 0 und 100.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält. Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur der [**\_ erweiterten \_ Engine \_**](winbio-extended-engine-info.md) -Informationen von winbio für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.

</dd> <dt>

**Teilfaktor**
</dt> <dd>

Ein Wert des **\_ \_ Subtyps "winbio biometrische** ", der zusätzliche Informationen über die Registrierung bereitstellt.

</dd> <dt>

**Zugeschnitten**
</dt> <dd>

Informationen zum Status einer Registrierung, die für einen bestimmten biometrischen Faktor ausgeführt wird.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Fakialfeatures**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Gesichts Features ausgeführt wird.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Die Position innerhalb des Kamera Rahmens der Vorderseite der zu registrierenden Person in Pixel. Die Größe des Kamera Rahmens bestimmt die Obergrenze für die Anzahl der Pixel für diese Position. Die Eigenschaft " **\_ \_ erweiterter \_ Sensor \_ Info" der winbio-Eigenschaft** zum Bestimmen der Größe des Kamera Rahmens. Ein Client, der den Anwesenheits Monitor verwendet, muss den Skalierungs Vorgang ausführen, um die Position dem Kamera Rahmen zuzuordnen.

</dd> <dt>

**Entfernung**
</dt> <dd>

Der Abstand zwischen dem tatsächlichen Speicherort der Vorderseite und dem idealen Fokusabstand für das Gesicht. Dieser Wert liegt zwischen-100 und 100. 0 gibt die ideale Entfernung an, positive Werte geben an, dass der tatsächliche Speicherort der Fläche zu weit entfernt ist, und negative Werte geben an, dass der tatsächliche Speicherort zu nah ist.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Fingerabdruck Muster in Bearbeitung ist.

<dl> <dt>

**Generalsamples**
</dt> <dd>

Die Gesamtanzahl der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlichen Stichproben.

</dd> <dt>

**Tagesstätte**
</dt> <dd>

Die Anzahl der Abtastungen für die Mitte des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Topedge**
</dt> <dd>

Die Anzahl der Abtastungen für den oberen Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Bottomedge**
</dt> <dd>

Die Anzahl der Abtastungen für den unteren Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Leftedge**
</dt> <dd>

Die Anzahl der Abtastungen für den linken Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Rechtschaffdge**
</dt> <dd>

Die Anzahl der Abtastungen für den rechten Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> </dl> </dd> <dt>

**Augen**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Iris-Muster ausgeführt wird.

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

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zum Status einer Registrierung, die für Sprachmuster in Bearbeitung ist.

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



 

 





