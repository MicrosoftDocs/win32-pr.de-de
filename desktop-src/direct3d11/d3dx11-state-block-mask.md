---
title: D3DX11_STATE_BLOCK_MASK -Struktur (D3dx11effect.h)
description: Gibt den Gerätestatus an.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8087f45ad94fe3e45f78a1be9d86b30f6f7e3f2c9161b9c4498865b12582436e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124935"
---
# <a name="d3dx11_state_block_mask-structure"></a>D3DX11 \_ STATE \_ BLOCK \_ MASK-Struktur

Gibt den Gerätestatus an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Member

<dl> <dt>

**Vs**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Vertex-Shaderzustand zu speichern ist.

</dd> <dt>

**VSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-Samplern. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**VSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-Ressourcen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von konstanten Vertex-Shader-Puffern. Das Array ist eine Mehr-Byte-Bitmaske, bei der jedes Bit einen konstanten Pufferslot darstellt.

</dd> <dt>

**VSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-Schnittstellen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**Hs**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Zustand des Hüllen-Shaders zu speichern ist.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hüllen-Shader-Samplern. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hüllen-Shader-Ressourcen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hüllen-Shader-Konstantenpuffern. Das Array ist eine Mehr-Byte-Bitmaske, bei der jedes Bit einen konstanten Pufferslot darstellt.

</dd> <dt>

**HSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hüllen-Shader-Schnittstellen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**DS**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Domänen-Shaderzustand zu speichern ist.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Samplern. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Ressourcen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Konstantenpuffern. Das Array ist eine Mehr-Byte-Bitmaske, bei der jedes Bit einen Pufferslot darstellt.

</dd> <dt>

**DSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Schnittstellen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**GS**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Zustand des Geometrie-Shaders gespeichert werden soll.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von geometry-shader-Samplern. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von geometry-shader-Ressourcen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von geometry-shader-Konstantenpuffern. Das Array ist eine Mehr-Byte-Bitmaske, bei der jedes Bit einen Pufferslot darstellt.

</dd> <dt>

**GSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Geometry-Shader-Schnittstellen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**Ps**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Shaderzustand des Pixels zu speichern ist.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Samplern. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Ressourcen. Das Array ist eine Multi-Byte-Bitmaske, bei der jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Konstantenpuffern. Das Array ist eine Mehr-Byte-Bitmaske, bei der jedes Bit einen konstanten Pufferslot darstellt.

</dd> <dt>

**PSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Schnittstellen. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die ungeordneten Zugriffsansichten des Pixelshader gespeichert werden sollen.

</dd> <dt>

**CS**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Zustand des Compute-Shaders gespeichert werden soll.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-Samplern. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen Samplerslot darstellt.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-Ressourcen. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Konstantenpuffern für Compute-Shader. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen konstanten Pufferslot darstellt.

</dd> <dt>

**CSInterfaces**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-Schnittstellen. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen Schnittstellenslot darstellt.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die ungeordneten Zugriffsansichten des Compute-Shaders gespeichert werden sollen.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Scheitelpunktpuffern. Das Array ist eine Bitmaske mit mehreren Byte, wobei jedes Bit einen Ressourcenslot darstellt.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Indexpufferzustand gespeichert werden soll.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Eingabelayoutzustand gespeichert werden soll.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der primitive Topologiezustand gespeichert werden soll.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Renderzielzustände gespeichert werden sollen.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Tiefenschablonenzustand gespeichert werden soll.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Mischungszustand gespeichert werden soll.

</dd> <dt>

**RSViewports**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Viewports-Zustände gespeichert werden sollen.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Scissor-Rechteckzustände gespeichert werden sollen.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Rasterizerzustand gespeichert werden soll.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Status der Stream-Out-Puffer gespeichert werden sollen.

</dd> <dt>

**Prädikation**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Prädikationszustand gespeichert werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Zustandsblockmaske gibt den Gerätezustand an, dass sich ein Durchlauf oder eine Technik ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11 Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

