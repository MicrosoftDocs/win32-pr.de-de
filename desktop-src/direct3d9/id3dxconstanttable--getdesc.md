---
description: Ruft eine Beschreibung der Konstanten Tabelle ab.
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'ID3DXConstantTable:: getdesc-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71eeb951ec73fbeb9942f52e30ab9ad59e374ee7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870119"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="2ea56-103">ID3DXConstantTable:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="2ea56-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="2ea56-104">Ruft eine Beschreibung der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="2ea56-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ea56-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2ea56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ea56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea56-107">*PDE SC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ea56-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea56-108">Typ: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ea56-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="2ea56-109">Die Beschreibung der Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2ea56-109">Description of the constant table.</span></span> <span data-ttu-id="2ea56-110">Weitere Informationen finden Sie unter [**D3DXCONSTANTTABLE \_**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="2ea56-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea56-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ea56-111">Return value</span></span>

<span data-ttu-id="2ea56-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ea56-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ea56-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ea56-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ea56-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="2ea56-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea56-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ea56-115">Requirements</span></span>



| <span data-ttu-id="2ea56-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ea56-116">Requirement</span></span> | <span data-ttu-id="2ea56-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2ea56-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea56-118">Header</span><span class="sxs-lookup"><span data-stu-id="2ea56-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2ea56-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea56-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ea56-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ea56-120">Library</span></span><br/> | <dl> <span data-ttu-id="2ea56-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ea56-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ea56-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ea56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea56-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2ea56-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="2ea56-124">**ID3DXConstantTable:: getconstantdebug**</span><span class="sxs-lookup"><span data-stu-id="2ea56-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




