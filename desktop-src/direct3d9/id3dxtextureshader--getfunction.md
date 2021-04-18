---
description: Ruft einen Zeiger auf die Funktion DWORD-Stream ab.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'ID3DXTextureShader:: GetFunction-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355046"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="e2219-103">ID3DXTextureShader:: GetFunction-Methode</span><span class="sxs-lookup"><span data-stu-id="e2219-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="e2219-104">Ruft einen Zeiger auf die Funktion DWORD-Stream ab.</span><span class="sxs-lookup"><span data-stu-id="e2219-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2219-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2219-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="e2219-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2219-107">*ppfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2219-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2219-108">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2219-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e2219-109">Ein Zeiger auf die Funktion DWORD-Stream.</span><span class="sxs-lookup"><span data-stu-id="e2219-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="e2219-110">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e2219-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2219-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2219-111">Return value</span></span>

<span data-ttu-id="e2219-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2219-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2219-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2219-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e2219-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="e2219-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2219-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2219-115">Requirements</span></span>



| <span data-ttu-id="e2219-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2219-116">Requirement</span></span> | <span data-ttu-id="e2219-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e2219-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2219-118">Header</span><span class="sxs-lookup"><span data-stu-id="e2219-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e2219-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2219-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e2219-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2219-120">Library</span></span><br/> | <dl> <span data-ttu-id="e2219-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2219-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2219-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2219-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2219-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e2219-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




