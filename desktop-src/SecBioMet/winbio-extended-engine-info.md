---
title: WINBIO_EXTENDED_ENGINE_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENGINE_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859267"
---
# <a name="winbio_extended_engine_info-structure"></a>Struktur der erweiterten winbio- \_ \_ Engine- \_ Informationen

Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Genericenginecapabilitäten**
</dt> <dd>

Die generischen Funktionen der Engine-Komponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält. Wenn z. b. der Wert des  **\_ faktermembers winbio- \_ Fingerabdruck** ist, gilt die Struktur der **\_ erweiterten \_ Engine \_** -Informationen von winbio für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.

</dd> <dt>

**Zugeschnitten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Fakialfeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Registrierungsanforderungen**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Registrierungsanforderungen**
</dt> <dd>

Die Anzahl von guten Beispielen, die zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich sind.

<dl> <dt>

**Generalsamples**
</dt> <dd>

Die Gesamtanzahl der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlichen guten Stichproben.

</dd> <dt>

**Tagesstätte**
</dt> <dd>

Die Anzahl von guten Beispielen für den Mittelpunkt des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Topedge**
</dt> <dd>

Die Anzahl von guten Beispielen für den oberen Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Bottomedge**
</dt> <dd>

Die Anzahl von guten Beispielen für den unteren Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Leftedge**
</dt> <dd>

Die Anzahl von guten Beispielen für den linken Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> <dt>

**Rechtschaffdge**
</dt> <dd>

Die Anzahl von guten Beispielen für den rechten Rand des Fingerabdrucks, der zum Erstellen einer neuen Fingerabdruck Vorlage erforderlich ist.

</dd> </dl> </dd> </dl> </dd> <dt>

**Augen**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Registrierungsanforderungen**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Registrierungsanforderungen**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





