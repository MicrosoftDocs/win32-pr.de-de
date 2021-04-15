---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur (winbio \_ Adapter. h)
description: Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur Windows-Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475666"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>Struktur der erweiterten winbio-Registrierungs \_ \_ \_ Parameter

Die Struktur der **erweiterten winbio-Registrierungs \_ \_ \_ Parameter** enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Die Größe (in Bytes) der Struktur der **erweiterten winbio-Registrierungs \_ \_ \_ Parameter** .

</dd> <dt>

**Teilfaktor**
</dt> <dd>

Einer der Werte für den [**Subtyp "winbio \_ biometrische \_ SubType**](winbio-biometric-subtype-constants.md) ", der zusätzliche Informationen über die Registrierung bereitstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Windows-Biometrieframework übergibt diese Struktur während eines Registrierungsvorgangs an die [**engineadaptersetenrollmentparameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ Adapter. h (Include winbio \_ Adapter. h)</dt> </dl> |



 

 





