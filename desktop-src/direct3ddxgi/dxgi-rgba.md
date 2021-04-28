---
description: 'DXGI_RGBA Struktur: Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA -Struktur (DXGItype.h)
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
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114268"
---
# <a name="dxgi_rgba-structure"></a>DXGI \_ RGBA-Struktur

Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.

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

Der DXGItype.h-Headertyp definiert **DXGI \_ RGBA** wie folgt als Alias von [**D3DCOLORVALUE:**](d3dcolorvalue.md)


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Sie können **DXGI \_ RGBA** mit [**IDXGISwapChain1::SetBackgroundColor,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 und Plattformupdate für Windows \[ 7-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 und Plattformupdate für Windows Server 2008 \[ R2-Desktop-Apps \| UWP-Apps\]<br/> |
| Header<br/>                   | <dl> <dt>DXGItype.h</dt> </dl>                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (in Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
