---
description: Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE-Struktur (dxgitype. h)
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
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354757"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>D3DCOLORVALUE-Struktur (dxgitype. h)

Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.

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

Ein Gleit Komma Wert, der die rote Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.

</dd> <dt>

**g**
</dt> <dd>

Ein Gleit Komma Wert, der die grüne Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.

</dd> <dt>

**b**
</dt> <dd>

Ein Gleit Komma Wert, der die blaue Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blue vollständig vorhanden ist.

</dd> <dt>

**ein**
</dt> <dd>

Ein Gleit Komma Wert, der die Alpha Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 vollständig deckend angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um ungewöhnliche Effekte zu implementieren. Werte, die größer als 1 sind, führen zu starken Lichtern, die tendenziell eine Szene auslagern. Durch negative Werte werden dunkle Lichter erzeugt, die das Licht aus einer Szene entfernen.

Der dxgitype. h-Headertyp: definiert [**DXGI \_ RGBA**](dxgi-rgba.md) als Alias von **D3DCOLORVALUE** wie folgt:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Sie können D3DCOLORVALUE oder [**DXGI \_ RGBA**](dxgi-rgba.md) mit [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getbackgroundcolor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und dem [**DXGI \_ alpha- \_ Modus**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**DXGI- \_ RGBA**](dxgi-rgba.md)
</dt> </dl>

 

 




