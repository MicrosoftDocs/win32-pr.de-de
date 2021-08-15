---
title: D3DX11_PASS_SHADER_DESC -Struktur (D3dx11effect.h)
description: Beschreibt einen Effektpass.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC-Struktur Direct3D 11
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
ms.openlocfilehash: 8ec7328ce346b51c3315086dcc193f421081dd77fc3a169bc448fba10bc7fa3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536836"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>D3DX11 \_ PASS \_ SHADER \_ DESC-Struktur

Beschreibt einen Effektpass.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**pShaderVariable**
</dt> <dd>

Typ: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Die Variable, aus der dieser Shader stammt.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Das Element von pShaderVariable (falls ein Array) oder 0 (falls nicht zutreffend).

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ PASS \_ SHADER \_ DESC wird mit [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc-Methoden verwendet.

Wenn es sich um eine Inline-Shaderzuweisung handelt, handelt es sich bei der zurückgegebenen Schnittstelle um eine anonyme Shadervariable, die auf andere Weise nicht abgerufen werden kann. Der Name in der Variablenbeschreibung ist "$Anonymous". Wenn dieser Typ im Passblock nicht zugeordnet ist, pShaderVariable != **NULL,** aber pShaderVariable->IsValid() == **FALSE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

