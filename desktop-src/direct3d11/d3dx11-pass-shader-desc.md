---
title: D3DX11_PASS_SHADER_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Durchlauf.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982548"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>Bibliothek d3dx11 \_ Pass- \_ Shader- \_ debustruktur

Beschreibt einen Effekt Durchlauf.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**pshadervariable**
</dt> <dd>

Typ: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Die Variable, von der dieser Shader stammt.

</dd> <dt>

**Shaderindex**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Das-Element von pshadervariable (bei einem Array) oder 0 (null), wenn es nicht zutreffend ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC wird mit [**ID3DX11EffectPass**](id3dx11effectpass.md) get \* shaderdesc-Methoden verwendet.

Wenn es sich um eine Inline-shaderzuweisung handelt, ist die zurückgegebene Schnittstelle eine anonyme Shader-Variable, die nicht auf andere Weise abgerufen werden kann. Der Name in der Variablen Beschreibung lautet "$Anonymous". Wenn keine Zuweisung dieses Typs im Pass-Block vorhanden ist, pshadervariable! = **null**, aber pshadervariable->IsValid () = = **false**.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

