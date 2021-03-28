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
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="b9c4e-104">Bibliothek d3dx11 \_ State \_ Block \_ Mask-Struktur</span><span class="sxs-lookup"><span data-stu-id="b9c4e-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="b9c4e-105">Gibt den Gerätezustand an.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c4e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9c4e-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="b9c4e-107">Member</span><span class="sxs-lookup"><span data-stu-id="b9c4e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9c4e-108">**Jews**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-109">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-110">Boolescher Wert, der angibt, ob der Scheitelpunkt-Shader-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-111">**Vssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-112">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-113">Array von Vertex-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="b9c4e-114">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-115">**Vsshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-116">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-117">Array von Vertex-Shaderressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="b9c4e-118">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-119">**Vsconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-120">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-121">Array von Vertex-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-122">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-123">**Vsintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-124">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-125">Array von Vertex-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="b9c4e-126">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-127">**Jh**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-128">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-129">Boolescher Wert, der angibt, ob der Hull-Shader-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-130">**Hssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-131">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-132">Array von Hull-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="b9c4e-133">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-134">**Hsshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-135">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-136">Array von Hull-Shader-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-136">Array of hull-shader resources.</span></span> <span data-ttu-id="b9c4e-137">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-138">**Hsconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-139">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-140">Array von Hull-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-141">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-142">**Hsintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-143">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-144">Array von Hull-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="b9c4e-145">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-147">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-148">Boolescher Wert, der angibt, ob der Domänen-shaderzustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-149">**Dssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-150">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-151">Array von Domänen-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="b9c4e-152">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-153">**Dsshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-154">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-155">Array von Domänen-Shader-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-155">Array of domain-shader resources.</span></span> <span data-ttu-id="b9c4e-156">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-157">**Dsconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-158">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-159">Array von Domänen-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-160">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-161">**Dsintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-162">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-163">Array von Domänen-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="b9c4e-164">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-166">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-167">Boolescher Wert, der angibt, ob der Geometrie-Shader-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-168">**Gssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-169">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-170">Array von Geometry-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="b9c4e-171">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-172">**Gsshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-173">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-174">Array von Geometry-Shaderressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="b9c4e-175">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-176">**Gsconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-177">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-178">Array von Geometry-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-179">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-180">**Gsintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-181">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-182">Array von Geometry-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="b9c4e-183">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-184">**PS**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-185">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-186">Boolescher Wert, der angibt, ob der Pixelshader-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-187">**Pssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-188">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-189">Array von Pixel-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="b9c4e-190">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-191">**Psshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-192">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-193">Array von Pixel-Shader-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="b9c4e-194">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-195">**Psconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-196">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-197">Array aus Pixel-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-198">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-199">**Psintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-200">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-201">Array von Pixel-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="b9c4e-202">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-203">**Psunorderedaccessviews**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-204">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-205">Boolescher Wert, der angibt, ob die Pixel-Shader-Ansicht für ungeordnete Zugriffe gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-207">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-208">Boolescher Wert, der angibt, ob der COMPUTE-Shader-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-209">**Cssamplers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-210">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-211">Array von Compute-Shader-Samplern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="b9c4e-212">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen samplingslot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-213">**Csshaderresources**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-214">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-215">Array von Compute-Shaderressourcen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-215">Array of compute-shader resources.</span></span> <span data-ttu-id="b9c4e-216">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-217">**Csconstantbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-218">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-219">Array von Compute-Shader-konstantenpuffern.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="b9c4e-220">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen konstanten Puffer Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-221">**Csintergesichter**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-222">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-223">Array von Compute-Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="b9c4e-224">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Schnittstellen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-225">**Csunorderedaccessviews**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-226">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-227">Boolescher Wert, der angibt, ob die Server-Shader-Ansichten für ungeordnete Zugriffe gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-228">**Iavertexbuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-229">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-230">Array der Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-230">Array of vertex buffers.</span></span> <span data-ttu-id="b9c4e-231">Das Array ist eine multibyte-Bitmaske, bei der jedes Bit einen Ressourcen Slot darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-232">**Iaindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-233">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-234">Boolescher Wert, der angibt, ob der Status des Index Puffers gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-235">**Iainputlayout**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-236">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-237">Boolescher Wert, der angibt, ob der Eingabe Layoutzustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-238">**Iaprimitivetopology**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-239">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-240">Boolescher Wert, der angibt, ob der primitive topologiezustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-241">**Omrendertargets**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-242">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-243">Boolescher Wert, der angibt, ob die renderzielzustände gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-244">**Omdepthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-245">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-246">Boolescher Wert, der angibt, ob der Status der tiefen Schablone gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-247">**Omblendstate**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-248">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-249">Boolescher Wert, der angibt, ob der Blend-Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-250">**Rsviewports**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-251">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-252">Boolescher Wert, der angibt, ob die Viewports-Zustände gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-253">**Rsscissorrects**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-254">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-255">Boolescher Wert, der angibt, ob die Scheren-Rechtecke Zustände gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-256">**Rsrasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-257">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-258">Boolescher Wert, der angibt, ob der Status des Rasterizers gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-259">**Sobuffers**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-260">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-261">Boolescher Wert, der angibt, ob die Datenstrom Ausgabepuffer Zustände gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="b9c4e-262">**Prädikation**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="b9c4e-263">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b9c4e-264">Boolescher Wert, der angibt, ob der prediationstatus gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9c4e-265">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9c4e-265">Remarks</span></span>

<span data-ttu-id="b9c4e-266">Eine Status Block Maske gibt an, dass das Gerät angibt, dass eine Pass-oder eine Technik geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c4e-267">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b9c4e-267">Requirements</span></span>



| <span data-ttu-id="b9c4e-268">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9c4e-268">Requirement</span></span> | <span data-ttu-id="b9c4e-269">Wert</span><span class="sxs-lookup"><span data-stu-id="b9c4e-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c4e-270">Header</span><span class="sxs-lookup"><span data-stu-id="b9c4e-270">Header</span></span><br/> | <dl> <span data-ttu-id="b9c4e-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c4e-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c4e-272">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9c4e-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c4e-273">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b9c4e-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

