---
title: D3DX11_EFFECT_SHADER_DESC-Struktur (D3dx11effect.h)
description: Beschreibt einen Effekt-Shader.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48695b2e6ff0cca2046606eaad7dbdf137641ce126bd4f5f211e399aaf29d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096350"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>D3DX11 \_ EFFECT \_ SHADER \_ DESC-Struktur

Beschreibt einen Effekt-Shader.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**pInputSignature**
</dt> <dd>

Typ: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Wird an CreateInputLayout übergeben. Nur gültig für einen Scheitelpunkt-Shader oder geometry-Shader. Siehe [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**TRUE** ist, dass der Shader inline definiert ist. andernfalls **FALSE**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Typ: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Shader-Bytecode.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Länge von pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Streamen Sie eine Deklarationszeichenfolge (für geometry shader mit SO).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Gibt an, welcher Stream gerastert wird. D3D11-Geometrie-Shader können bis zu vier Datenströme ausgeben, von denen einer gerastert werden kann.

</dd> <dt>

**NumInputSignature-Einträge**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der Eingabesignatur.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der Ausgabesignatur.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der Patchkonstantensignatur.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ EFFECT \_ SHADER \_ DESC wird mit [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekte 11 Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

