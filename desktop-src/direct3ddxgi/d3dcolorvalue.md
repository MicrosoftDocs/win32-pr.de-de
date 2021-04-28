---
description: 'D3DCOLORVALUE-Struktur (Dxgitype.h): Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.'
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE-Struktur (Dxgitype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 83ca500493a04f04de5352185c240d20a19009f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107148"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>D3DCOLORVALUE-Struktur (Dxgitype.h)

Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**r**
</dt> <dd>

Gleitkommawert, der die rote Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.

</dd> <dt>

**g**
</dt> <dd>

Gleitkommawert, der die grüne Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.

</dd> <dt>

**b**
</dt> <dd>

Gleitkommawert, der die blaue Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass blau vollständig vorhanden ist.

</dd> <dt>

**Eine**
</dt> <dd>

Gleitkommawert, der die Alphakomponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 für vollständig deckend steht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um einige ungewöhnliche Effekte zu implementieren. Werte größer als 1 erzeugen starke Lichtlichter, die dazu tendieren, eine Szene zu verwaschen. Negative Werte erzeugen dunkle Lichtlichter, die tatsächlich Licht aus einer Szene entfernen.

Der DXGItype.h-Headertyp definiert [**DXGI \_ RGBA**](dxgi-rgba.md) wie folgt als Alias von **D3DCOLORVALUE:**


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Sie können D3DCOLORVALUE oder [**DXGI \_ RGBA**](dxgi-rgba.md) mit [**IDXGISwapChain1::SetBackgroundColor,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**DXGI \_ RGBA**](dxgi-rgba.md)
</dt> </dl>

 

 




