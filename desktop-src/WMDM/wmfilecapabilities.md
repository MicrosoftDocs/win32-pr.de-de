---
title: Wmfilefunktionen-Struktur
description: Die wmfilefunktionalitäten-Struktur beschreibt den MIME-Typ.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Wmfilefunktionen-Struktur Windows Media Device Manager
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
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357529"
---
# <a name="wmfilecapabilities-structure"></a>Wmfilefunktionen-Struktur

Die **wmfilefunktionalitäten** -Struktur beschreibt den MIME-Typ.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Member

<dl> <dt>

**pwszmimetype**
</dt> <dd>

MIME-Typ.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** ist für die zukünftige Verwendung reserviert. Auf NULL (0) festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





