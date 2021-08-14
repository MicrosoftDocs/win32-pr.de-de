---
description: Der Objekttyp.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: D3DXPARAMETER_CLASS -Enumeration (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 10d786dbbb50c44519f4f6bb1239b9fd07dfadeb706c13eca588051a918103cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525239"
---
# <a name="d3dxparameter_class-enumeration"></a>D3DXPARAMETER \_ CLASS-Enumeration

Der Objekttyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC-SKALAR \_**
</dt> <dd>

Die Konstante ist ein Skalar.

</dd> <dt>

<span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC \_ VECTOR**
</dt> <dd>

Die Konstante ist ein Vektor.

</dd> <dt>

<span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC-MATRIXZEILEN \_ \_**
</dt> <dd>

Constant ist eine Zeilenmatrizenmatrix.

</dd> <dt>

<span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC-MATRIXSPALTEN \_ \_**
</dt> <dd>

Constant ist eine Spaltenmatrizenmatrix.

</dd> <dt>

<span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC-OBJEKT \_**
</dt> <dd>

Die Konstante ist entweder eine Textur, ein Shader oder eine Zeichenfolge.

</dd> <dt>

<span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC-STRUKTUR \_**
</dt> <dd>

Die Konstante ist eine -Struktur.

</dd> <dt>

<span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




