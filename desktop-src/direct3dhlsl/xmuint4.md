---
title: XMUINT4-Struktur
description: Beschreibt einen 4D-ganzzahligen Vektor ohne Vorzeichen.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4-Struktur (HLSL)
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222848"
---
# <a name="xmuint4-structure"></a>XMUINT4-Struktur

Beschreibt einen 4D-ganzzahligen Vektor ohne Vorzeichen.

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



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

x-Komponente des Vektors.

</dd> <dt>

**y**
</dt> <dd>

y-Komponente des Vektors.

<dl> <dt>

**z**
</dt> <dd>

z-Komponente des Vektors.

<dl> <dt>

**w**
</dt> <dd>

w-Komponente des Vektors.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in der ``D3DX\_DXGIFormatConvert.inl`` Kopfzeile im DirectX SDK (Juni 2010) für die Verwendung von C++ definiert. Die neueste Version dieses Headers im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) definiert Sie nicht mehr und basiert stattdessen auf [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in directxmath.




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
