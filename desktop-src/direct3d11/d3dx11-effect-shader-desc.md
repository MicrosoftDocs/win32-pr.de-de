---
title: D3DX11_EFFECT_SHADER_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt-Shader.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC Struktur Direct3D 11
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
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870183"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>Bibliothek d3dx11 \_ Effect- \_ Shader- \_ Struktur

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

**pinputsignature**
</dt> <dd>

Typ: Konstante **[**Byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

An "kreateinputlayout" übergeben. Nur gültig in einem Scheitelpunkt-Shader oder Geometry-Shader. Weitere Informationen finden Sie unter [**ID3D11Device:: kreatinput Layout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**True** gibt an, dass der Shader Inline definiert ist. andernfalls **false**.

</dd> <dt>

**pbytecode**
</dt> <dd>

Typ: Konstante **[**Byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Shader-Bytecode.

</dd> <dt>

**Bytecodelta ength**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Länge von pbytecode.

</dd> <dt>

**Sodecls**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Stream out-Deklarations Zeichenfolge (für Geometry-Shader mit so).

</dd> <dt>

**Rasterizedstream**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Gibt an, welcher Stream rasteriert ist. D3D11 Geometry-Shader können bis zu vier Datenströme ausgeben, von denen eine rasteriert werden kann.

</dd> <dt>

**Numinputsignatureentries**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der Eingabe Signatur.

</dd> <dt>

**Numoutputsignatureentries**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der Ausgabe Signatur.

</dd> <dt>

**Numpatchconstantsignatureentries**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Einträge in der patchkonstantensignatur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Bibliothek d3dx11 \_ Effect- \_ Shader- \_ Debugger wird mit [**ID3DX11EffectShaderVariable:: getshaderdebug**](id3dx11effectshadervariable-getshaderdesc.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

