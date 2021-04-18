---
description: Gibt einen Verweis auf eine nicht komprimierte Oberfläche an.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: DXVA_PicEntry_HEVC-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344383"
---
# <a name="dxva_picentry_hevc-structure"></a>DXVA \_ picentry \_ hevc-Struktur

Gibt einen Verweis auf eine nicht komprimierte Oberfläche an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Member

<dl> <dt>

**Index7Bits**
</dt> <dd>

Ein Index, der eine unkomprimierte Oberfläche identifiziert.

</dd> <dt>

**Associatedflag** 
</dt> <dd>

Optionales 1-Bit-Flag, das der Oberfläche zugeordnet ist. Die Bedeutung des Flags hängt vom Kontext ab. Beispielsweise kann festgelegt werden, ob der Verweis Rahmen ein langfristiger Verweis oder ein kurzfristiger Verweis ist.

</dd> <dt>

**bpicentry**
</dt> <dd>

Greift auf die gesamten 8 Bits der Union zu.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Strukturen](media-foundation-structures.md)
</dt> </dl>

 

 




