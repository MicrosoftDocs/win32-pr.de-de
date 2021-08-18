---
title: D3DX11_EFFECT_TYPE_DESC -Struktur (D3dx11effect.h)
description: Beschreibt einen Effektvariablentyp.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989960"
---
# <a name="d3dx11_effect_type_desc-structure"></a>D3DX11 \_ EFFECT \_ TYPE \_ DESC-Struktur

Beschreibt einen Effektvariablentyp.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**TypeName**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Name des Typs, z. B. "float4" oder "MyStruct".

</dd> <dt>

**Klasse**
</dt> <dd>

Typ: **[ **D3D10 \_ SHADER \_ \_ VARIABLE-KLASSE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

Die Variablenklasse (siehe [**D3D10 \_ SHADER \_ VARIABLE \_ CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3D10 \_ SHADER VARIABLE \_ \_ TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Der Variablentyp (siehe [**D3D10 \_ SHADER \_ VARIABLE \_ TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**CreateUiDefinition-Elemente**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Elemente in diesem Typ (0, wenn kein Array).

</dd> <dt>

**Mitglieder**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Membern (0, wenn keine Struktur).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Zeilen in diesem Typ (0, wenn kein numerischer Primitiver ist).

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Spalten in diesem Typ (0, wenn kein numerischer Primitiver ist).

</dd> <dt>

**PackedSize**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Bytes, die für die Darstellung dieses Datentyps erforderlich sind, wenn sie eng gepackt sind.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Bytes, die von diesem Datentyp belegt werden, wenn sie in einem konstanten Puffer angegeben sind.

</dd> <dt>

**Schritt**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Bytes, die zwischen Elementen durchdringt werden sollen, wenn sie in einem konstanten Puffer angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ EFFECT \_ TYPE \_ DESC wird mit [ **ID3DX11EffectType::GetDesc verwendet.**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

