---
title: Idschreitetextlayout getverhangmetrics-Methode
description: Gibt die über schreibungen (in Dips) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Text Glyphen und Inline-Objekten.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Getverhangmetrics-Methode direkt schreiben
- Getverhangmetrics-Methode Direct Write, idwrite tetextlayout-Schnittstelle
- Idwrite tetextlayout Interface Direct Write, getverhangmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370091"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Idwrite tetextlayout:: getverhangmetrics-Methode

Gibt die über schreibungen (in Dips) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Text Glyphen und Inline-Objekten.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*überlastet* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **dwrite- \_ \_ overhängenmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Über schießungen sichtbarer Blöcke (in Dips) außerhalb des Layouts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Unterstriche und strikete tragen nicht zur Bestimmung der Blackbox bei, da diese tatsächlich vom Renderer gezeichnet werden, der in einer Vielzahl von Stilen gezeichnet werden kann.

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

 

