---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Ruft die Pixeldaten aus einem Bitmaprenderingziel ab.
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
ms.openlocfilehash: f84959338550722d9ce1d2d7097d652fcb140f1f
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955043"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>IDWriteBitmapRenderTarget2::GetBitmapData-Methode (dwrite_3.h)

Ruft die Pixeldaten aus einem Bitmaprenderingziel ab.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite verfügbar.](../direct-write-portal.md) DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parameter

`bitmapData`

Typ: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Ein Zeiger auf die Pixeldaten.

## <a name="return-value"></a>Rückgabewert

Typ: <b>HRESULT</b>

Wenn diese Methode erfolgreich ist, gibt <b xmlns:loc="http://microsoft.com/wdcml/l10n">sie</b>S_OK. Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT-Fehlercode</b> zurückgegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen finden [Sie im DWriteCore-Übersichtsthema](/windows/win32/directwrite/dwritecore-overview) und in der [DWriteCoreGallery-Beispiel-App.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite_3.h (include dwrite_core.h) |
| **Bibliothek** | Dwrite.lib |
| **Dll** | Dwrite.dll |

## <a name="see-also"></a>Weitere Informationen:

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
