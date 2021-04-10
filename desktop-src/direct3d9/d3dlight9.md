---
description: Definiert einen Satz von Beleuchtungs Eigenschaften.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: D3DLIGHT9-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219569"
---
# <a name="d3dlight9-structure"></a>D3DLIGHT9-Struktur

Definiert einen Satz von Beleuchtungs Eigenschaften.

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

**Type**
</dt> <dd>

Typ: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Der Typ der Lichtquelle. Dieser Wert ist einer der Member des [**D3DLIGHTTYPE**](./d3dlighttype.md) -Enumerationstyps.

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Vom Licht ausgegebene diffuse Farbe. Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Glanz Farbe, die vom Licht ausgegeben wird. Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.

</dd> <dt>

**Umgebend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Umgebungs Farbe, die vom Licht ausgegeben wird. Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.

</dd> <dt>

**Position**
</dt> <dd>

Typ: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Die Position des Lichts im Raum, der durch eine [**D3DVECTOR**](d3dvector.md) -Struktur angegeben wird. Dieser Member hat keine Bedeutung für direktionale Lichter und wird in diesem Fall ignoriert.

</dd> <dt>

**Richtung**
</dt> <dd>

Typ: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Die Richtung, die das Licht im Raum der Welt zeigt, die durch eine [**D3DVECTOR**](d3dvector.md) -Struktur angegeben wird. Dieser Member hat nur für direktionale und Scheinwerfer Bedeutung. Dieser Vektor muss nicht normalisiert werden, er sollte jedoch eine Länge ungleich NULL aufweisen.

</dd> <dt>

**Bereich**
</dt> <dd>

Typ: **float**

</dd> <dd>

Der Abstand, über den das Licht keine Auswirkung hat. Der maximal zulässige Wert für diesen Member ist die Quadratwurzel von FLT \_ Max. Dieser Member wirkt sich nicht auf direktionale Lichter aus.

</dd> <dt>

**Übergang**
</dt> <dd>

Typ: **float**

</dd> <dd>

Verringerung der Beleuchtung zwischen dem inneren Kegel eines Spotlight (dem von der TA angegebenen Winkel) und dem äußeren Rand des äußeren Kegel (der von Phi angegebene Winkel).

Die Auswirkung von "atzuweisung" auf die Beleuchtung ist sehr gering. Darüber hinaus wird eine geringe Leistungs Einbuße durch die Strukturierung der "f-Zuweisung"-Kurve verursacht. Aus diesen Gründen legen die meisten Entwickler diesen Wert auf 1,0 fest.

</dd> <dt>

**Attenuation0**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert. Dieser Member stellt eine Dämpfungs Konstante dar. Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md). Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Attenuation1**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert. Dieser Member stellt eine Dämpfungs Konstante dar. Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md). Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Attenuation2**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert. Dieser Member stellt eine Dämpfungs Konstante dar. Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md). Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich. Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.

</dd> <dt>

**Theta**
</dt> <dd>

Typ: **float**

</dd> <dd>

Der Winkel im Bogenmaße des inneren Kegel eines Spotlight, d. h. der vollständig beleuchtete Spotlight-Kegel. Dieser Wert muss zwischen 0 und dem von Phi angegebenen Wert liegen.

</dd> <dt>

**Patientendaten**
</dt> <dd>

Typ: **float**

</dd> <dd>

Der Winkel im Bogenmaße, der den äußeren Rand des äußeren Rands des Spotlight definiert. Punkte außerhalb dieses Kegel werden nicht durch das Spotlight beleuchtet. Dieser Wert muss zwischen 0 und PI liegen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**Setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
