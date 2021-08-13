---
title: IDWriteTextLayout GetOverhangMetrics-Methode
description: Gibt die Überhänge (in DIPs) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Textglyphen und Inlineobjekten.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- GetOverhangMetrics-Methode Direct Write
- GetOverhangMetrics-Methode Direct Write , IDWriteTextLayout-Schnittstelle
- IDWriteTextLayout-Schnittstelle Direct Write , GetOverhangMetrics-Methode
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
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649745"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>IDWriteTextLayout::GetOverhangMetrics-Methode

Gibt die Überhänge (in DIPs) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Textglyphen und Inlineobjekten.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Überhänge* \[ out\]
</dt> <dd>

Typ: **[ **DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Überschreitungen von sichtbaren Erweiterungen (in DIPs) außerhalb des Layouts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Unterstreichungen und Durchstreichungen tragen nicht zur Blackbox-Bestimmung bei, da diese tatsächlich vom Renderer gezeichnet werden, der sie in verschiedenen Stilen zeichnen darf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Idwritetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**Idwritetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

