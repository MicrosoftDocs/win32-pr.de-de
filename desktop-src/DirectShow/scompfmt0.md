---
description: Enthält Formatinformationen für die intelligente Neukomprimierung.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: SCompFmt0-Struktur (Qedit.h)
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
ms.openlocfilehash: f02c9cda80acdd42d0687502834a9b2e66f1cf773d02b88eadabdd346850061e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072704"
---
# <a name="scompfmt0-structure"></a>SCompFmt0-Struktur

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

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

**nFormatId**
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> <dt>

**MediaType**
</dt> <dd>

[**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die das Komprimierungsformat beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




