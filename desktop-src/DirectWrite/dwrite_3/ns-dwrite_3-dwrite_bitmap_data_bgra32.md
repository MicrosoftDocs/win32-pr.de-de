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
ms.openlocfilehash: ea60bbd4933cd890321e0caeb095778922699a46
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106367262"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>DWRITE_BITMAP_DATA_BGRA32 Struktur (dwrite_3. h)

Stellt Bitmapdaten im BGRA32-Format dar.

> [!IMPORTANT]
> Diese API ist als Teil der dwrite-Core-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

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

Typ: **[UInt32](../../winprog/windows-data-types.md)**

Die Breite der Bitmap in Pixel.


`height`

Typ: **[UInt32](../../winprog/windows-data-types.md)**

Die Höhe der Bitmap in Pixel.


`pixels`

Type: \_ Field \_ size \_ (Width * Height)**[UInt32](../../winprog/windows-data-types.md)\***

Ein Zeiger auf den Speicherort der Bitwerte für die Bitmap.


## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie im Thema [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der Beispiel-App für [dwrite-coregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion 0,1-Vorabversion [Win32-Apps] |
| **Header** | dwrite_3. h (dwrite_core. h einschließen) |