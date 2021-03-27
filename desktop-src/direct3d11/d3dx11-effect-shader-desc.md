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
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="e60ad-104">Bibliothek d3dx11 \_ Effect- \_ Shader- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="e60ad-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="e60ad-105">Beschreibt einen Effekt-Shader.</span><span class="sxs-lookup"><span data-stu-id="e60ad-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60ad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e60ad-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="e60ad-107">Member</span><span class="sxs-lookup"><span data-stu-id="e60ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e60ad-108">**pinputsignature**</span><span class="sxs-lookup"><span data-stu-id="e60ad-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-109">Typ: Konstante **[**Byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e60ad-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-110">An "kreateinputlayout" übergeben.</span><span class="sxs-lookup"><span data-stu-id="e60ad-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="e60ad-111">Nur gültig in einem Scheitelpunkt-Shader oder Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="e60ad-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="e60ad-112">Weitere Informationen finden Sie unter [**ID3D11Device:: kreatinput Layout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="e60ad-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="e60ad-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-114">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-115">**True** gibt an, dass der Shader Inline definiert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e60ad-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-116">**pbytecode**</span><span class="sxs-lookup"><span data-stu-id="e60ad-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-117">Typ: Konstante **[**Byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e60ad-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-118">Shader-Bytecode.</span><span class="sxs-lookup"><span data-stu-id="e60ad-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-119">**Bytecodelta ength**</span><span class="sxs-lookup"><span data-stu-id="e60ad-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-121">Die Länge von pbytecode.</span><span class="sxs-lookup"><span data-stu-id="e60ad-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-122">**Sodecls**</span><span class="sxs-lookup"><span data-stu-id="e60ad-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-123">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-124">Stream out-Deklarations Zeichenfolge (für Geometry-Shader mit so).</span><span class="sxs-lookup"><span data-stu-id="e60ad-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-125">**Rasterizedstream**</span><span class="sxs-lookup"><span data-stu-id="e60ad-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-126">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-127">Gibt an, welcher Stream rasteriert ist.</span><span class="sxs-lookup"><span data-stu-id="e60ad-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="e60ad-128">D3D11 Geometry-Shader können bis zu vier Datenströme ausgeben, von denen eine rasteriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e60ad-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-129">**Numinputsignatureentries**</span><span class="sxs-lookup"><span data-stu-id="e60ad-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-130">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-131">Anzahl der Einträge in der Eingabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="e60ad-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-132">**Numoutputsignatureentries**</span><span class="sxs-lookup"><span data-stu-id="e60ad-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-133">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-134">Anzahl der Einträge in der Ausgabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="e60ad-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="e60ad-135">**Numpatchconstantsignatureentries**</span><span class="sxs-lookup"><span data-stu-id="e60ad-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e60ad-136">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e60ad-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e60ad-137">Anzahl der Einträge in der patchkonstantensignatur.</span><span class="sxs-lookup"><span data-stu-id="e60ad-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e60ad-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e60ad-138">Remarks</span></span>

<span data-ttu-id="e60ad-139">Der Bibliothek d3dx11 \_ Effect- \_ Shader- \_ Debugger wird mit [**ID3DX11EffectShaderVariable:: getshaderdebug**](id3dx11effectshadervariable-getshaderdesc.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e60ad-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e60ad-140">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e60ad-140">Requirements</span></span>



| <span data-ttu-id="e60ad-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e60ad-141">Requirement</span></span> | <span data-ttu-id="e60ad-142">Wert</span><span class="sxs-lookup"><span data-stu-id="e60ad-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e60ad-143">Header</span><span class="sxs-lookup"><span data-stu-id="e60ad-143">Header</span></span><br/> | <dl> <span data-ttu-id="e60ad-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e60ad-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60ad-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e60ad-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60ad-146">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e60ad-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

