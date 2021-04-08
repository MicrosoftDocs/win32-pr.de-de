---
title: WINBIO_EXTENDED_STORAGE_INFO Struktur (winbio \_ types. h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_STORAGE_INFO Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949523"
---
# <a name="winbio_extended_storage_info-structure"></a>\_Struktur erweiterter winbio- \_ Speicher \_ Informationen

Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Genericstorage-Funktionen**
</dt> <dd>

Die generischen Funktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Strukturinformationen zu Funktionen und Registrierungsanforderungen des Speicher Adapters enthält. Wenn z. b. der Wert des **Factor** -Members **winbio \_ - \_ typfingerabdruck** ist, gilt die **Erweiterte winbio- \_ \_ Speicher \_ Informations** Struktur für einen Fingerabdruckleser und enthält die relevanten Informationen in der **specifc. Fingerabdruck** -Struktur.

</dd> <dt>

**Zugeschnitten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**Fakialfeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Gesichtsmerkmalen.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Gesichts Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruck Mustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Fingerabdruck Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> <dt>

**Augen**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Iris-Mustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Iris-Erkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicher Adapters für eine biometrische Einheit im Zusammenhang mit Sprachmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Spracherkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Winbio- \_ biometrische \_ Typkonstanten**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Winbio-Funktions \_ Konstanten**](winbio-capability-constants.md)
</dt> </dl>

 

 





