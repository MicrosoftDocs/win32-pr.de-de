---
title: WMFILECAPABILITIES-Struktur
description: Die WMFILECAPABILITIES-Struktur beschreibt den MIME-Typ.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- WMFILECAPABILITIES-Strukturfenster Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f4852eeb7142b92c2c1a4c2073dfc70e5f6a6d74c727a7ab9e63c285796846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903770"
---
# <a name="wmfilecapabilities-structure"></a>WMFILECAPABILITIES-Struktur

Die **WMFILECAPABILITIES-Struktur** beschreibt den MIME-Typ.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Member

<dl> <dt>

**pwszMimeType**
</dt> <dd>

MIME-Typ.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** für die zukünftige Verwendung reserviert. Auf 0 (null) festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





