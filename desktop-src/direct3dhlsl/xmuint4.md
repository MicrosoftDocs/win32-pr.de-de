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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982096"
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



## <a name="members"></a>Member

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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ dxgiformatconvert. INL</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen](format-conversion-structures.md)
</dt> <dt>

[Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





