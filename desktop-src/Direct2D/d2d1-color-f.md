---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Beschreibt die Komponenten rot, grün, blau und Alpha einer Farbe. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361806"
---
# <a name="d2d1_color_f"></a>D2D1- \_ Farbe \_ F

Beschreibt die Komponenten rot, grün, blau und Alpha einer Farbe.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Bemerkungen

**D2D1 \_ Color \_ f** ist eine typedef für [**D2D \_ Color \_ f**](d2d-color-f.md), bei der es sich um eine typedef für [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)handelt. Informationen zu den von **D2D1 \_ Color \_ F** bereitgestellten Membern finden Sie unter [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

Die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse stellt einen Satz vordefinierter Farben und Hilfsfunktionen zum Definieren von Farben bereit. Weitere Informationen finden Sie in der [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Referenz.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwendet, um beim Erstellen eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)eine vordefinierte Farbe (schwarz) anzugeben.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



Im folgenden Beispiel wird die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwendet, um eine Farbe mithilfe von rot-, grün-, blau-und Alpha Werten anzugeben.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (Include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**Colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

