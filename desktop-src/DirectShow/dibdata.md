---
description: Die DIBDATA-Struktur enthält Informationen zu einer geräteunabhängigen GDI-Bitmap (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: DIBDATA-Struktur (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653817"
---
# <a name="dibdata-structure"></a>DIBDATA-Struktur

Die `DIBDATA` -Struktur enthält Informationen zu einer geräteunabhängigen GDI-Bitmap (DIB).

## <a name="syntax"></a>Syntax


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**PaletteVersion**
</dt> <dd>

Dieser Member sollte immer dann erhöht werden, wenn sich die Palette ändert.

</dd> <dt>

**DibSection**
</dt> <dd>

**DIBSECTION-Struktur,** die Informationen zum DIB enthält. Weitere Informationen finden Sie in der GDI-Dokumentation.

</dd> <dt>

**hBitmap**
</dt> <dd>

Handle für die Bitmap.

</dd> <dt>

**hMapping**
</dt> <dd>

Handle für ein Dateizuordnungsobjekt, das zum Freigeben von Arbeitsspeicher zwischen GDI und einem [**CImageSample-Objekt verwendet**](cimagesample.md) wird.

</dd> <dt>

**Pbase**
</dt> <dd>

Adresse der Bitmap.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl> |



 

 




