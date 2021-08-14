---
title: WINBIO_EXTENDED_ENGINE_INFO -Struktur (Winbio \_ types.h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO Struktur Windows Biometrieframework-API
- PWINBIO_EXTENDED_ENGINE_INFO Strukturzeiger für Windows Biometrieframework-API
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
ms.openlocfilehash: df59b10400729150a13f2a8a5476c46507867777f71641a01ea0c08e064b4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910516"
---
# <a name="winbio_extended_engine_info-structure"></a>WINBIO \_ EXTENDED \_ ENGINE \_ INFO-Struktur

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

**GenericEngineCapabilities**
</dt> <dd>

Die generischen Funktionen der Engine-Komponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Struktur Informationen zu Funktionen und Registrierungsanforderungen des Engine-Adapters enthält. Wenn der Wert des  Factor-Mitglieds beispielsweise **WINBIO \_ TYPE \_ FINGERPRINT** ist, gilt die **WINBIO EXTENDED \_ ENGINE \_ \_ INFO-Struktur** für einen Fingerabdruckleser und enthält die relevanten Informationen in der **Specifc.Fingerprint-Struktur.**

</dd> <dt>

**Bestimmten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Gesichtsfeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsfeatures.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruckmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

Die Anzahl der guten Beispiele, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Die Gesamtzahl der guten Stichproben, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**Center**
</dt> <dd>

Die Anzahl der guten Stichproben für die Mitte des Fingerabdrucks, die erforderlich sind, um eine neue Fingerabdruckvorlage zu erstellen.

</dd> <dt>

**TopEdge**
</dt> <dd>

Die Anzahl der guten Stichproben für den oberen Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Die Anzahl der guten Stichproben für den unteren Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Die Anzahl der guten Stichproben für den linken Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> <dt>

**RightEdge**
</dt> <dd>

Die Anzahl der guten Stichproben für den rechten Rand des Fingerabdrucks, die zum Erstellen einer neuen Fingerabdruckvorlage erforderlich sind.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Irismustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Engine-Adapters für eine biometrische Einheit im Zusammenhang mit Stimmmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter enthalten)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WINBIO \_ CAPABILITY-Konstanten**](winbio-capability-constants.md)
</dt> <dt>

[**\_ \_ WINBIO-BIOMETRIETYP-Konstanten**](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





