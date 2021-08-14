---
title: WINBIO_VERSION-Struktur (Winbio \_ types.h)
description: Enthält die Softwareversionsnummer einer Komponente eines biometrischen Dienstanbieters.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION Struktur Windows Biometrieframework-API
- PWINBIO_VERSION Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909115"
---
# <a name="winbio_version-structure"></a>\_WINBIO-VERSIONSstruktur

Die **\_ WINBIO-VERSIONSstruktur** enthält die Softwareversionsnummer einer biometrischen Dienstanbieterkomponente.

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

Ein **DWORD,** das die Hauptversionsnummer enthält.

</dd> <dt>

**MinorVersion**
</dt> <dd>

Ein **DWORD,** das die Nebenversionsnummer enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**\_WINBIO-BSP-SCHEMA \_**](winbio-bsp-schema.md)
</dt> <dt>

[**\_WINBIO-EINHEITENSCHEMA \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





