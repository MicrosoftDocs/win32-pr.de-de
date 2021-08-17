---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS -Struktur \_ (Winbio-Adapter.h)
description: Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungsvorlage benötigt.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Struktur Windows Biometrieframework-API
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Strukturzeiger für Windows Biometrieframework-API
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
ms.openlocfilehash: 55173b5badfb8764cfc9c681f4ed92e2f0d1c50e5db09075185af9e5db2e6433
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910489"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>STRUKTUR VON WINBIO \_ EXTENDED \_ ENROLLMENT \_ PARAMETERS

Die **WINBIO \_ EXTENDED ENROLLMENT \_ \_ PARAMETERS-Struktur** enthält zusätzliche Informationen, die ein Engine-Adapter benötigt, um eine Registrierungsvorlage zu erstellen.

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

Die Größe (in Bytes) der **WINBIO \_ EXTENDED ENROLLMENT \_ \_ PARAMETERS-Struktur.**

</dd> <dt>

**SubFactor**
</dt> <dd>

Einer der [**WINBIO \_ BIOMETRIC \_ SUBTYPE-Konstantenwerte,**](winbio-biometric-subtype-constants.md) der zusätzliche Informationen zur Registrierung enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Windows Biometric Framework übergibt diese Struktur während eines Registrierungsvorgangs an die [**EngineAdapterSetEnrollmentParameters-Methode.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ adapter.h (winbio \_ adapter.h enthalten)</dt> </dl> |



 

 





