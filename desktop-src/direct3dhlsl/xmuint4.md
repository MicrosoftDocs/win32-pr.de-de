---
title: XMUINT4-Struktur
description: Beschreibt einen 4D-Ganzzahlvektor ohne Vorzeichen.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4-Struktur HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549895"
---
# <a name="xmuint4-structure"></a>XMUINT4-Struktur

Beschreibt einen 4D-Ganzzahlvektor ohne Vorzeichen.

## <a name="syntax"></a>Syntax


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a>Member

<dl> <dt>

**x**
</dt> <dd>

x-component des Vektors.

</dd> <dt>

**y**
</dt> <dd>

y-Komponente des Vektors.

<dl> <dt>

**Z**
</dt> <dd>

z-component des Vektors.

<dl> <dt>

**w**
</dt> <dd>

w-component des Vektors.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Hinweise

Diese Struktur wird im ``D3DX\_DXGIFormatConvert.inl`` Header im DirectX SDK (Juni 2010) für die Verwendung in C++ definiert. Die neueste Version dieses Headers im NuGet-Paket [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert ihn nicht mehr und basiert stattdessen auf [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath.




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen](format-conversion-structures.md)
</dt> <dt>

[Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>