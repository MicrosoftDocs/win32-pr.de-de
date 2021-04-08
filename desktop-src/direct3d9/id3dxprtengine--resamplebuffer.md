---
description: Gibt einen ID3DXPRTBuffer-Puffer für die Eingabe erneut aus und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Vertex-Puffer in einen Textur Puffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Puffer mit einem Kanal in 3-Kanal-Puffer zu konvertieren und umgekehrt.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine:: resamplebuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762291"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="29737-105">ID3DXPRTEngine:: resamplebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="29737-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="29737-106">Gibt einen [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer für die Eingabe erneut aus und speichert ihn in einem Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="29737-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="29737-107">Diese Methode kann verwendet werden, um einen Vertex-Puffer in einen Textur Puffer zu konvertieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="29737-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="29737-108">Sie kann auch verwendet werden, um Puffer mit einem Kanal in 3-Kanal-Puffer zu konvertieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="29737-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="29737-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="29737-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="29737-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29737-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29737-111">*pbufferin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29737-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29737-112">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="29737-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="29737-113">Zeiger auf den [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="29737-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="29737-114">*pbufferout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="29737-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29737-115">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="29737-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="29737-116">Zeiger auf den [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="29737-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29737-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29737-117">Return value</span></span>

<span data-ttu-id="29737-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29737-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29737-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29737-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="29737-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="29737-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="29737-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29737-121">Requirements</span></span>



| <span data-ttu-id="29737-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29737-122">Requirement</span></span> | <span data-ttu-id="29737-123">Wert</span><span class="sxs-lookup"><span data-stu-id="29737-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29737-124">Header</span><span class="sxs-lookup"><span data-stu-id="29737-124">Header</span></span><br/>  | <dl> <span data-ttu-id="29737-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="29737-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="29737-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29737-126">Library</span></span><br/> | <dl> <span data-ttu-id="29737-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29737-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29737-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29737-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="29737-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




