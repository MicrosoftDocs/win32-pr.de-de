---
title: D3DX11_STATE_BLOCK_MASK-Struktur (D3dx11effect. h)
description: Gibt den Gerätezustand an.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK Struktur Direct3D 11
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
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355357"
---
# <a name="d3dx11_state_block_mask-structure"></a>Bibliothek d3dx11 \_ State \_ Block \_ Mask-Struktur

Gibt den Gerätezustand an.

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

**Jews**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Scheitelpunkt-Shader-Zustand gespeichert werden soll.

</dd> <dt>

**Vssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Vsshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shaderressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Vsconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.

</dd> <dt>

**Vsintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Vertex-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**Jh**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Hull-Shader-Zustand gespeichert werden soll.

</dd> <dt>

**Hssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hull-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Hsshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hull-Shader-Ressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Hsconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hull-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.

</dd> <dt>

**Hsintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Hull-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**DS**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Domänen-shaderzustand gespeichert werden soll.

</dd> <dt>

**Dssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Dsshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Ressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Dsconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Puffer Slot darstellt.

</dd> <dt>

**Dsintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Domänen-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**GS**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Geometrie-Shader-Zustand gespeichert werden soll.

</dd> <dt>

**Gssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Geometry-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Gsshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Geometry-Shaderressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Gsconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Geometry-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Puffer Slot darstellt.

</dd> <dt>

**Gsintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Geometry-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**PS**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Pixelshader-Zustand gespeichert werden soll.

</dd> <dt>

**Pssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Psshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Ressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Psconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array aus Pixel-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.

</dd> <dt>

**Psintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Pixel-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**Psunorderedaccessviews**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Pixel-Shader-Ansicht für ungeordnete Zugriffe gespeichert werden soll.

</dd> <dt>

**CS**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der COMPUTE-Shader-Zustand gespeichert werden soll.

</dd> <dt>

**Cssamplers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-Samplern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.

</dd> <dt>

**Csshaderresources**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shaderressourcen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Csconstantbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-konstantenpuffern. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.

</dd> <dt>

**Csintergesichter**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array von Compute-Shader-Schnittstellen. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.

</dd> <dt>

**Csunorderedaccessviews**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Server-Shader-Ansichten für ungeordnete Zugriffe gespeichert werden sollen.

</dd> <dt>

**Iavertexbuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Array der Scheitelpunkt Puffer. Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.

</dd> <dt>

**Iaindexbuffer**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Status des Index Puffers gespeichert werden soll.

</dd> <dt>

**Iainputlayout**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Eingabe Layoutzustand gespeichert werden soll.

</dd> <dt>

**Iaprimitivetopology**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der primitive topologiezustand gespeichert werden soll.

</dd> <dt>

**Omrendertargets**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die renderzielzustände gespeichert werden sollen.

</dd> <dt>

**Omdepthstencilstate**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Status der tiefen Schablone gespeichert werden soll.

</dd> <dt>

**Omblendstate**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Blend-Zustand gespeichert werden soll.

</dd> <dt>

**Rsviewports**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Viewports-Zustände gespeichert werden sollen.

</dd> <dt>

**Rsscissorrects**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Scheren-Rechtecke Zustände gespeichert werden sollen.

</dd> <dt>

**Rsrasterizerstate**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der Status des Rasterizers gespeichert werden soll.

</dd> <dt>

**Sobuffers**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob die Datenstrom Ausgabepuffer Zustände gespeichert werden sollen.

</dd> <dt>

**Prädikation**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Boolescher Wert, der angibt, ob der prediationstatus gespeichert werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Status Block Maske gibt an, dass das Gerät angibt, dass eine Pass-oder eine Technik geändert wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

