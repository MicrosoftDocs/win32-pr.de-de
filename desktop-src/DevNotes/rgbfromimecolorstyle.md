---
description: Konvertiert eine imecolorsty-Struktur in eine COLORREF-Struktur.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: Rgbfromimecolorstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369389"
---
# <a name="rgbfromimecolorstyle-function"></a>Rgbfromimecolorstyle-Funktion

Konvertiert eine **imecolorsty** -Struktur in eine [**COLORREF**](../gdi/colorref.md) -Struktur.

## <a name="syntax"></a>Syntax


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcolorstyle* \[ in\]
</dt> <dd>

Eine **imecolorsty** -Struktur, die von einer [**pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md) -oder [**pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine [**COLORREF**](../gdi/colorref.md) -Struktur zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COLORREF**](../gdi/colorref.md)
</dt> <dt>

[**Pcolorstylebackfromimestyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**Pcolorstyletextfromimestyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
