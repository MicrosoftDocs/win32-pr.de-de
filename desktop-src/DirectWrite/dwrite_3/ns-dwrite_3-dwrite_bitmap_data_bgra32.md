---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Stellt Bitmapdaten im BGRA32-Format dar.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955053"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>DWRITE_BITMAP_DATA_BGRA32 -Struktur (dwrite_3.h)

Stellt Bitmapdaten im BGRA32-Format dar.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite verfügbar.](../direct-write-portal.md) DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="syntax"></a>Syntax

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Member

`width`

Typ: **[UINT32](../../winprog/windows-data-types.md)**

Die Breite der Bitmap in Pixel.


`height`

Typ: **[UINT32](../../winprog/windows-data-types.md)**

Die Höhe der Bitmap in Pixel.


`pixels`

Typ: \_ \_ Feldgröße \_ (Breite * Höhe)**[UINT32](../../winprog/windows-data-types.md)\***

Ein Zeiger auf die Position der Bitwerte für die Bitmap.


## <a name="examples"></a>Beispiele

Weitere Informationen finden [Sie im DWriteCore-Übersichtsthema](/windows/win32/directwrite/dwritecore-overview) und in der [DWriteCoreGallery-Beispiel-App.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite_3.h (include dwrite_core.h) |