---
title: WINBIO_VERSION Struktur (winbio \_ types. h)
description: Enthält die Software Versionsnummer der Komponente eines biometrischen Dienstanbieters.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION Struktur Windows-Biometrieframework-API
- PWINBIO_VERSION Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479125"
---
# <a name="winbio_version-structure"></a>Winbio- \_ Versions Struktur

Die Struktur der **winbio- \_ Version** enthält die Software Versionsnummer der Komponente eines biometrischen Dienstanbieters.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Member

<dl> <dt>

**MajorVersion**
</dt> <dd>

Ein **DWORD** , das die Hauptversionsnummer enthält.

</dd> <dt>

**MinorVersion**
</dt> <dd>

Ein **DWORD** , das die neben Versionsnummer enthält.

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

[**winbio- \_ BSP- \_ Schema**](winbio-bsp-schema.md)
</dt> <dt>

[**winbio- \_ Einheits \_ Schema**](winbio-unit-schema.md)
</dt> </dl>

 

 





