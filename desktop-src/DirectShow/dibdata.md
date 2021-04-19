---
description: Die dibdata-Struktur enthält Informationen über eine GDI-geräteunabhängige Bitmap (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Dibdata-Struktur (winutil. h)
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
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352040"
---
# <a name="dibdata-structure"></a>Dibdata-Struktur

Die `DIBDATA` Struktur enthält Informationen über eine GDI-geräteunabhängige Bitmap (DIB).

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

**Paletteversion**
</dt> <dd>

Dieser Member sollte immer dann erhöht werden, wenn die Palette geändert wird.

</dd> <dt>

**DIBsection**
</dt> <dd>

Die **DIBsection** -Struktur, die Informationen über das DIB enthält. Weitere Informationen finden Sie in der GDI-Dokumentation.

</dd> <dt>

**HBITMAP**
</dt> <dd>

Handle für die Bitmap.

</dd> <dt>

**hmapping**
</dt> <dd>

Handle für ein Datei Zuordnungsobjekt, das zum Freigeben von Arbeitsspeicher zwischen GDI und einem [**cimagesample**](cimagesample.md) -Objekt verwendet wird.

</dd> <dt>

**pBase**
</dt> <dd>

Adresse der Bitmap.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl> |



 

 




