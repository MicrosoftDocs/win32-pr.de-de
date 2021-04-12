---
description: Kompilieren eines Effekts.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'ID3DXEffectCompiler:: compileeffect-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354347"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="e95f0-103">ID3DXEffectCompiler:: compileeffect-Methode</span><span class="sxs-lookup"><span data-stu-id="e95f0-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="e95f0-104">Kompilieren eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="e95f0-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e95f0-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="e95f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e95f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95f0-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e95f0-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95f0-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e95f0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e95f0-109">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e95f0-109">Compile options identified by various flags.</span></span> <span data-ttu-id="e95f0-110">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="e95f0-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="e95f0-111">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="e95f0-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e95f0-112">*ppeer-ect* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e95f0-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e95f0-113">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e95f0-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e95f0-114">Der Puffer, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="e95f0-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="e95f0-115">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e95f0-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e95f0-116">*pperrormsgs* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e95f0-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e95f0-117">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e95f0-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e95f0-118">Puffer, der mindestens die erste Kompilierungs Fehlermeldung enthält, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e95f0-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="e95f0-119">Dies schließt Compilerfehler und allgemeine sprach Kompilierungsfehler ein.</span><span class="sxs-lookup"><span data-stu-id="e95f0-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="e95f0-120">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e95f0-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95f0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e95f0-121">Return value</span></span>

<span data-ttu-id="e95f0-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e95f0-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e95f0-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e95f0-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="e95f0-124">Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="e95f0-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="e95f0-125">Wenn die Methode fehlschlägt, lautet der Rückgabewert E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="e95f0-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e95f0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e95f0-126">Requirements</span></span>



| <span data-ttu-id="e95f0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e95f0-127">Requirement</span></span> | <span data-ttu-id="e95f0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e95f0-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95f0-129">Header</span><span class="sxs-lookup"><span data-stu-id="e95f0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e95f0-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e95f0-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e95f0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e95f0-131">Library</span></span><br/> | <dl> <span data-ttu-id="e95f0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e95f0-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e95f0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e95f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95f0-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="e95f0-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
