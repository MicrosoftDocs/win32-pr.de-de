---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Ruft die Pixeldaten aus einem Bitmap-Renderziel ab.
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373408"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>IDWriteBitmapRenderTarget2:: getbitmapdata-Methode (dwrite_3. h)

Ruft die Pixeldaten aus einem Bitmap-Renderziel ab.

> [!IMPORTANT]
> Diese API ist als Teil der dwrite-Core-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parameter

`bitmapData`

Typ: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Ein Zeiger auf die Pixeldaten.

## <a name="return-value"></a>Rückgabewert

Typ: <b>HRESULT</b>

Wenn diese Methode erfolgreich ausgeführt wird, wird <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>zurückgegeben. Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> -Fehlercode zurückgegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie im Thema [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der Beispiel-App für [dwrite-coregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion 0,1-Vorabversion [Win32-Apps] |
| **Header** | dwrite_3. h (dwrite_core. h einschließen) |
| **Bibliothek** | Dwrite. lib |
| **DLL** | Dwrite.dll |

## <a name="see-also"></a>Siehe auch

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)