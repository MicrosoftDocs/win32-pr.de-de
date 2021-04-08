---
description: Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746768"
---
# <a name="dxgi_rgba-structure"></a>DXGI- \_ RGBA-Struktur

Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
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

Der dxgitype. h-Headertyp: definiert **DXGI \_ RGBA** als Alias von [**D3DCOLORVALUE**](d3dcolorvalue.md)wie folgt:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Sie können **DXGI \_ RGBA** mit [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getbackgroundcolor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und dem [**DXGI \_ alpha- \_ Modus**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| UWP-apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 und Platt Form Update für Windows Server 2008 R2 \[ Desktop Apps \| UWP-apps\]<br/> |
| Header<br/>                   | <dl> <dt>Dxgitype. h</dt> </dl>                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (in Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
