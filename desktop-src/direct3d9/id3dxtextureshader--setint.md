---
description: 'ID3DXTextureShader::SetInt-Methode: Legt einen ganzzahligen Wert fest.'
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: ID3DXTextureShader::SetInt-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23c347c35b8accd60bdb81c931ebc3d35b48f957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117604"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="a621a-103">ID3DXTextureShader::SetInt-Methode</span><span class="sxs-lookup"><span data-stu-id="a621a-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="a621a-104">Legt einen ganzzahligen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="a621a-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a621a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a621a-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="a621a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a621a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a621a-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a621a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a621a-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a621a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a621a-109">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="a621a-109">Unique identifier to the constant.</span></span> <span data-ttu-id="a621a-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a621a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a621a-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a621a-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a621a-112">Typ: **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a621a-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a621a-113">Wert für ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a621a-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a621a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a621a-114">Return value</span></span>

<span data-ttu-id="a621a-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a621a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a621a-116">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a621a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a621a-117">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="a621a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a621a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a621a-118">Requirements</span></span>



| <span data-ttu-id="a621a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a621a-119">Requirement</span></span> | <span data-ttu-id="a621a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a621a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a621a-121">Header</span><span class="sxs-lookup"><span data-stu-id="a621a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a621a-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="a621a-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a621a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a621a-123">Library</span></span><br/> | <dl> <span data-ttu-id="a621a-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a621a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a621a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a621a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a621a-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a621a-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
