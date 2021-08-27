---
title: WINBIO_BSP_SCHEMA-Struktur (Winbio \_ types.h)
description: Beschreibt die Funktionen eines biometrischen Dienstanbieters.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA Struktur Windows Biometrieframework-API
- PWINBIO_BSP_SCHEMA Strukturzeiger Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff46f5484addb0221d9e441df73ecca3e8283da88ee7849e4362314aa1c375e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080780"
---
# <a name="winbio_bsp_schema-structure"></a>WINBIO \_ BSP \_ SCHEMA-Struktur

Die **WINBIO \_ BSP \_ SCHEMA-Struktur** beschreibt die Funktionen eines biometrischen Dienstanbieters. Diese Struktur wird von der [**WinBioEnumServiceProviders-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Member

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Der Typ der biometrischen Messung, die von diesem Gerät verwendet wird. Derzeit muss dies **WINBIO \_ TYPE \_ FINGERPRINT** sein.

</dd> <dt>

**BspId**
</dt> <dd>

Ein -Wert, der diese Biometrische Dienstanbieterkomponente eindeutig identifiziert.

</dd> <dt>

**Beschreibung**
</dt> <dd>

Eine **Mit NULL** endende Unicode-Zeichenfolge, die eine Beschreibung des biometrischen Dienstanbieters enthält.

</dd> <dt>

**Hersteller**
</dt> <dd>

Eine **Mit NULL** beendete Unicode-Zeichenfolge, die den Namen des Anbieters enthält, der den biometrischen Dienstanbieter an die Hand gibt.

</dd> <dt>

**Version**
</dt> <dd>

Eine [**\_ WINBIO-VERSIONSstruktur,**](winbio-version.md) die die Softwareversion der Komponente des biometrischen Dienstanbieters enthält.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





