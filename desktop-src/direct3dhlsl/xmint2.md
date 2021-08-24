---
title: XMINT2-Struktur
description: Beschreibt einen 2D-Ganzzahlvektor.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2-Struktur HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc613cd87b212ca21aacf1744b7789bd49732a555630d5cfc6051eaab2b3d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484180"
---
# <a name="xmint2-structure"></a>XMINT2-Struktur

Beschreibt einen 2D-Ganzzahlvektor.

## <a name="syntax"></a>Syntax


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
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

</dd> </dl>



## <a name="remarks"></a>Hinweise

Diese Struktur wird im ``D3DX\_DXGIFormatConvert.inl`` Header im DirectX SDK (Juni 2010) für die Verwendung in C++ definiert. Die neueste Version dieses Headers im [Microsoft.DXSDK.D3DX-NuGet-Paket](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert ihn nicht mehr und basiert stattdessen auf [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen](format-conversion-structures.md)
</dt> <dt>

[Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>