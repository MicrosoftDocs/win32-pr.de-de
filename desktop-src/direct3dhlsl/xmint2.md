---
title: XMINT2-Struktur
description: Beschreibt einen ganzzahligen 2D-Vektor.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2-Struktur (HLSL)
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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222858"
---
# <a name="xmint2-structure"></a>XMINT2-Struktur

Beschreibt einen ganzzahligen 2D-Vektor.

## <a name="syntax"></a>Syntax


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

x-Komponente des Vektors.

</dd> <dt>

**y**
</dt> <dd>

y-Komponente des Vektors.

</dd> </dl>



## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert. Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in directxmath.



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ dxgiformatconvert. INL</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen](format-conversion-structures.md)
</dt> <dt>

[Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
