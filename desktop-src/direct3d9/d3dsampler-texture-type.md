---
description: Definiert die samplingtexttypen für Scheitelpunkt-Shader.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: D3DSAMPLER_TEXTURE_TYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394062"
---
# <a name="d3dsampler_texture_type-enumeration"></a>D3DSAMPLER \_ Texture \_ Type-Enumeration

Definiert die samplingtexttypen für Scheitelpunkt-Shader.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ unbekannt**
</dt> <dd>

Nicht initialisierter Wert. Der Wert dieses Elements ist 0 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Deklarieren einer 2D-Textur. Der Wert dieses Elements ist 2 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT- \_ Cube**
</dt> <dd>

Deklarieren einer Cube-Textur. Der Wert dieses Elements ist 3 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT- \_ Volume**
</dt> <dd>

Deklarieren einer volumetextur. Der Wert dieses Elements ist 4 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




