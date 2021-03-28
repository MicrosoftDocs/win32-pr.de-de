---
title: XMINT4-Struktur
description: Beschreibt einen 4D-ganzzahligen Vektor.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4-Struktur (HLSL)
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355377"
---
# <a name="xmint4-structure"></a>XMINT4-Struktur

Beschreibt einen 4D-ganzzahligen Vektor.

## <a name="syntax"></a>Syntax


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
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

 

 





