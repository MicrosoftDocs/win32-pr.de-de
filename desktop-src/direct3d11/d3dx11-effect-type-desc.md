---
title: D3DX11_EFFECT_TYPE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Variablen-Typ.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC Struktur Direct3D 11
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
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870180"
---
# <a name="d3dx11_effect_type_desc-structure"></a>Bibliothek d3dx11 \_ Effect- \_ Typ ( \_ DESC-Struktur)

Beschreibt einen Effekt Variablen-Typ.

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

Der Name des Typs, z. b. "float4" oder "MyStruct".

</dd> <dt>

**Klasse**
</dt> <dd>

Type: **[ **d3d10 \_ Shader- \_ Variablen \_ Klasse**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

Die Variablen Klasse (siehe [**d3d10 \_ Shader \_ Variable \_ Class**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Typ**
</dt> <dd>

Type: **[ **d3d10 \_ Shader \_ - \_ Variablentyp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Der Variablentyp (siehe [**d3d10 \_ Shader- \_ \_ Variablentyp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elemente**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Elemente in diesem Typ (0, wenn kein Array ist).

</dd> <dt>

**Mitglieder**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Elemente (0, wenn keine Struktur ist).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Zeilen in diesem Typ (0, wenn kein numerischer primitiver Wert).

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Spalten in diesem Typ (0, wenn kein numerischer primitiver Wert).

</dd> <dt>

**Packedsize**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Bytes, die für die Darstellung dieses Datentyps erforderlich sind

</dd> <dt>

**Unpackedsize**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Bytes, die von diesem Datentyp belegt werden, wenn Sie in einem konstanten Puffer angeordnet sind.

</dd> <dt>

**Schritt**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Bytes, die zwischen Elementen gesucht werden sollen, wenn Sie in einem konstanten Puffer angeordnet sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bibliothek d3dx11 \_ Effect \_ Type \_ DESC wird mit [ **ID3DX11EffectType:: getdesc** verwendet.](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

