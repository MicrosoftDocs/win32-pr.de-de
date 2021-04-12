---
description: Einen Zeiger auf die Konstante Tabelle erhalten.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'ID3DXTextureShader:: getconstantbuffer-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354497"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="0915b-103">ID3DXTextureShader:: getconstantbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="0915b-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="0915b-104">Einen Zeiger auf die Konstante Tabelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="0915b-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0915b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0915b-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0915b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0915b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0915b-107">*ppconstantbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0915b-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0915b-108">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0915b-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0915b-109">Zeiger auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die die Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="0915b-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0915b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0915b-110">Return value</span></span>

<span data-ttu-id="0915b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0915b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0915b-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0915b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0915b-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="0915b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0915b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0915b-114">Requirements</span></span>



| <span data-ttu-id="0915b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0915b-115">Requirement</span></span> | <span data-ttu-id="0915b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0915b-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0915b-117">Header</span><span class="sxs-lookup"><span data-stu-id="0915b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0915b-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0915b-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0915b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0915b-119">Library</span></span><br/> | <dl> <span data-ttu-id="0915b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0915b-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0915b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0915b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0915b-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="0915b-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




