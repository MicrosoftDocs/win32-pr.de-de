---
title: XMUINT2-Struktur
description: Beschreibt einen 2D-ganzzahligen Vektor ohne Vorzeichen.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2-Struktur (HLSL)
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ec040a848b3103b4d5070541f025ab9cfb0cfa
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222828"
---
# <a name="xmuint2-structure"></a>XMUINT2-Struktur

Beschreibt einen 2D-ganzzahligen Vektor ohne Vorzeichen.

## <a name="syntax"></a>Syntax


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
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

Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert. Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMUINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint2) in directxmath.



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
