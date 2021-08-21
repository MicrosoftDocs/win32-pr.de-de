---
description: Definiert einen Satz von Beleuchtungseigenschaften.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: D3DLIGHT9-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e38cd5b6cfaba4822ddecf121aa2b03c86e2a3a899e464df18bfa473322f41f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804837"
---
# <a name="d3dlight9-structure"></a>D3DLIGHT9-Struktur

Definiert einen Satz von Beleuchtungseigenschaften.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>Member

<dl> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Typ der Lichtquelle. Dieser Wert ist einer der Member des [**D3DLIGHTTYPE-Enumerationstyps.**](./d3dlighttype.md)

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Diffuse Farbe, die vom Licht ausgegeben wird. Dieser Member ist eine [**D3DCOLORVALUE-Struktur.**](d3dcolorvalue.md)

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Vom Licht ausgegebene Glanzfarbe. Dieser Member ist eine [**D3DCOLORVALUE-Struktur.**](d3dcolorvalue.md)

</dd> <dt>

**Umgebend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Umgebungsfarbe, die vom Licht ausgegeben wird. Dieser Member ist eine [**D3DCOLORVALUE-Struktur.**](d3dcolorvalue.md)

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Position des Lichts im Weltraum, angegeben durch eine [**D3DVECTOR-Struktur.**](d3dvector.md) Dieser Member hat keine Bedeutung für richtungsweises Licht und wird in diesem Fall ignoriert.

</dd> <dt>

**Richtung**
</dt> <dd>

Typ: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Richtung, in der das Licht auf den Weltraum verweist, angegeben durch eine [**D3DVECTOR-Struktur.**](d3dvector.md) Dieser Member hat nur für richtungs- und Spotlights eine Bedeutung. Dieser Vektor muss nicht normalisiert werden, sollte jedoch eine Länge ungleich 0 (null) aufweisen.

</dd> <dt>

**Bereich**
</dt> <dd>

Typ: **float**

</dd> <dd>

Entfernung, über die das Licht keine Auswirkung hat. Der maximal zulässige Wert für diesen Member ist die Quadratwurzel von FLT \_ MAX. Dieser Member wirkt sich nicht auf richtungsrichtungslichter aus.

</dd> <dt>

**Abfall**
</dt> <dd>

Typ: **float**

</dd> <dd>

Verringern sie die Neigung zwischen dem inneren Kegel eines Blickpunkts (dem durch Theta angegebenen Winkel) und dem äußeren Rand des äußeren Kegels (dem durch Phi angegebenen Winkel).

Die Auswirkung eines Falloffs auf die Beleuchtung ist dezent. Darüber hinaus kommt es durch die Strukturierung der Falloffkurve zu geringfügigen Leistungseinbußen. Aus diesen Gründen legen die meisten Entwickler diesen Wert auf 1.0 fest.

</dd> <dt>

**Dämpfung0**
</dt> <dd>

Typ: **float**

</dd> <dd>

Wert, der angibt, wie sich die Lichtdichte über die Entfernung ändert. Dämpfungswerte werden für gerichtete Beleuchtung ignoriert. Dieser Member stellt eine Dämpfungskonstante dar. Informationen zur Dämpfung finden Sie unter [Lichteigenschaften (Direct3D 9).](light-properties.md) Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht gerichteten Beleuchtungen sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Dämpfung1**
</dt> <dd>

Typ: **float**

</dd> <dd>

Wert, der angibt, wie sich die Lichtdichte über die Entfernung ändert. Dämpfungswerte werden für gerichtete Beleuchtung ignoriert. Dieser Member stellt eine Dämpfungskonstante dar. Informationen zur Dämpfung finden Sie unter [Lichteigenschaften (Direct3D 9).](light-properties.md) Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht gerichteten Beleuchtungen sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Dämpfung2**
</dt> <dd>

Typ: **float**

</dd> <dd>

Wert, der angibt, wie sich die Lichtdichte über die Entfernung ändert. Dämpfungswerte werden für gerichtete Beleuchtung ignoriert. Dieser Member stellt eine Dämpfungskonstante dar. Informationen zur Dämpfung finden Sie unter [Lichteigenschaften (Direct3D 9).](light-properties.md) Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht gerichteten Beleuchtungen sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Theta**
</dt> <dd>

Typ: **float**

</dd> <dd>

Winkel im Bogenmaß des inneren Kegels eines Blickpunkts, d. h. der vollständigen Blickpunktkegel. Dieser Wert muss im Bereich von 0 bis zum von Phi angegebenen Wert liegen.

</dd> <dt>

**Phi**
</dt> <dd>

Typ: **float**

</dd> <dd>

Winkel im Bogenmaß, der den äußeren Rand des äußeren Kegels des Blickpunkts definiert. Punkte außerhalb dieses Kegels werden nicht durch den Blickpunkt entfacht. Dieser Wert muss zwischen 0 und pi sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
