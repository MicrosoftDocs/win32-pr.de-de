---
description: Ruft die Beschreibung der Renderoberfläche ab.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap:: getdesc-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761997"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="a6ceb-103">ID3DXRenderToEnvMap:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="a6ceb-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="a6ceb-104">Ruft die Beschreibung der Renderoberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="a6ceb-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ceb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6ceb-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a6ceb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6ceb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ceb-107">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6ceb-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ceb-108">Typ: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6ceb-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="a6ceb-109">Zeiger auf eine [**D3DXRTE \_**](d3dxrte-desc.md) -Struktur, die die Renderingoberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a6ceb-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ceb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6ceb-110">Return value</span></span>

<span data-ttu-id="a6ceb-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6ceb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6ceb-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6ceb-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a6ceb-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="a6ceb-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ceb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6ceb-114">Requirements</span></span>



| <span data-ttu-id="a6ceb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6ceb-115">Requirement</span></span> | <span data-ttu-id="a6ceb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6ceb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ceb-117">Header</span><span class="sxs-lookup"><span data-stu-id="a6ceb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a6ceb-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ceb-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a6ceb-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6ceb-119">Library</span></span><br/> | <dl> <span data-ttu-id="a6ceb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6ceb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a6ceb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6ceb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ceb-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a6ceb-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




