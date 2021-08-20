---
title: WINBIO_EXTENDED_STORAGE_INFO-Struktur (Winbio \_ types.h)
description: Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO Struktur Windows Biometrieframework-API
- PWINBIO_EXTENDED_STORAGE_INFO Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 3e8a9f133baf77a77d3db33001e996accc9574f86ad708037900a5db7c0c5e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910381"
---
# <a name="winbio_extended_storage_info-structure"></a>WINBIO \_ EXTENDED \_ STORAGE \_ INFO-Struktur

Enthält Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit.

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

**GenericStorageCapabilities**
</dt> <dd>

Die generischen Funktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> <dt>

**Aspekt**
</dt> <dd>

Der Typ der biometrischen Einheit, für die diese Struktur Informationen zu Funktionen und Registrierungsanforderungen des Speicheradapters enthält. Wenn der Wert des **Factor-Members** beispielsweise **WINBIO \_ TYPE \_ FINGERPRINT** lautet, gilt die **WINBIO \_ EXTENDED STORAGE \_ \_ INFO-Struktur** für einen Fingerabdruckleser und enthält die relevanten Informationen in der **Specifc.Fingerprint-Struktur.**

</dd> <dt>

**Bestimmten**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit im Zusammenhang mit einem bestimmten biometrischen Faktor.

<dl> <dt>

**NULL**
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit im Zusammenhang mit Gesichtsfeatures.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Gesichtserkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit im Zusammenhang mit Fingerabdruckmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Fingerabdruckerkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit im Zusammenhang mit Irismustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Schwertlilienerkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informationen zu den Funktionen und Registrierungsanforderungen des Speicheradapters für eine biometrische Einheit im Zusammenhang mit Stimmmustern.

<dl> <dt>

**Capabilities**
</dt> <dd>

Die Spracherkennungsfunktionen der Speicherkomponente, die mit einer bestimmten biometrischen Einheit verbunden ist

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WINBIO \_ BIOMETRIC \_ TYPE-Konstanten**](winbio-biometric-type-constants.md)
</dt> <dt>

[**WINBIO \_ CAPABILITY-Konstanten**](winbio-capability-constants.md)
</dt> </dl>

 

 





