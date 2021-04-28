---
description: 'ID3DXTextureShader::GetDesc-Methode: Ruft eine Beschreibung der konstanten Tabelle ab.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: ID3DXTextureShader::GetDesc-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117638"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="8093b-103">ID3DXTextureShader::GetDesc-Methode</span><span class="sxs-lookup"><span data-stu-id="8093b-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="8093b-104">Ruft eine Beschreibung der konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="8093b-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8093b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8093b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8093b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8093b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8093b-107">*pDesc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8093b-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8093b-108">Typ: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8093b-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="8093b-109">Die Attribute der konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8093b-109">The attributes of the constant table.</span></span> <span data-ttu-id="8093b-110">Siehe [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="8093b-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8093b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8093b-111">Return value</span></span>

<span data-ttu-id="8093b-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8093b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8093b-113">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8093b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8093b-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8093b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="8093b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8093b-115">Requirements</span></span>



| <span data-ttu-id="8093b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8093b-116">Requirement</span></span> | <span data-ttu-id="8093b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8093b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8093b-118">Header</span><span class="sxs-lookup"><span data-stu-id="8093b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8093b-119"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8093b-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8093b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8093b-120">Library</span></span><br/> | <dl> <span data-ttu-id="8093b-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8093b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8093b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8093b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8093b-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8093b-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




