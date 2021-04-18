---
title: Idschreitetextlayout determineminwidth-Methode
description: Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass ein notfallumbruch zwischen den Zeichen der ganzen Wörter auftritt.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Determineminwidth-Methode direkt schreiben
- Determineminwidth-Methode direkt schreiben, idschreitetextlayout-Schnittstelle
- Idwrite tetextlayout Interface Direct Write, determineminwidth-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371218"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>Idschreitetextlayout::D etermineminwidth-Methode

Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass ein notfallumbruch zwischen den Zeichen der ganzen Wörter auftritt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MinWidth* \[ vorgenommen\]
</dt> <dd>

Typ: **float \***

Minimale Breite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**Idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

