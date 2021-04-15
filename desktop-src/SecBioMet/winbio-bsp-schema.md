---
title: WINBIO_BSP_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen eines biometrischen Dienstanbieters.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_BSP_SCHEMA Struktur Zeiger Windows-Biometrieframework API
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
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476875"
---
# <a name="winbio_bsp_schema-structure"></a>Winbio- \_ BSP- \_ Schema Struktur

Die Struktur " **winbio \_ BSP \_ Schema** " beschreibt die Funktionen eines biometrischen Dienstanbieters. Diese Struktur wird von der [**winbioenumserviceproviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) -Funktion verwendet.

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

**Biometricfactor**
</dt> <dd>

Der Typ der von diesem Gerät verwendeten biometrischen Messung. Zurzeit muss dies ein **winbio- \_ \_ typfingerabdruck** sein.

</dd> <dt>

**Bspid**
</dt> <dd>

Ein Wert, der die Komponente des biometrischen Dienstanbieters eindeutig identifiziert.

</dd> <dt>

**Beschreibung**
</dt> <dd>

Eine **null**-terminierte Unicode-Zeichenfolge, die eine Beschreibung des biometrischen Dienstanbieters enthält.

</dd> <dt>

**Hersteller**
</dt> <dd>

Eine **null**-terminierte Unicode-Zeichenfolge, die den Namen des Anbieters enthält, der den biometrischen Dienstanbieter bereitstellt.

</dd> <dt>

**Version**
</dt> <dd>

Eine [**winbio- \_ Versions**](winbio-version.md) Struktur, die die Softwareversion der Komponente des biometrischen Dienstanbieters enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**Winbioenumserviceproviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





