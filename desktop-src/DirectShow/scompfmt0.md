---
description: Enthält Formatinformationen für die intelligente Neukomprimierung.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: SCompFmt0-Struktur (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368427"
---
# <a name="scompfmt0-structure"></a>SCompFmt0-Struktur

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Enthält Formatinformationen für die intelligente Neukomprimierung.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Member

<dl> <dt>

**nformatid**
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> <dt>

**MediaType**
</dt> <dd>

[**Am \_ \_Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die das Komprimierungs Format beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinegroup:: gezmartrecompressformat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**Iamtimelinegroup:: *-martrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




