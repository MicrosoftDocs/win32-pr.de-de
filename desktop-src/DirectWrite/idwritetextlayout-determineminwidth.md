---
title: IDWriteTextLayout DetermineMinWidth-Methode
description: Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass zwischen den Zeichen ganzer Wörter ein Notfall auftritt.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- DetermineMinWidth-Methode – Direkter Schreibzugriff
- DetermineMinWidth-Methode Direct Write, IDWriteTextLayout-Schnittstelle
- IDWriteTextLayout-Schnittstelle Direct Write , DetermineMinWidth-Methode
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
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075530"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout::D etermineMinWidth-Methode

Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass zwischen den Zeichen ganzer Wörter ein Notfall auftritt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*minWidth* \[ out\]
</dt> <dd>

Typ: **\* FLOAT**

Mindestbreite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idwritetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**Idwritetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

