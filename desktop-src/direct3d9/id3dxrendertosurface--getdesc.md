---
description: Ruft die Parameter der Renderoberfläche ab.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface:: getdesc-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219688"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="cf9c8-103">ID3DXRenderToSurface:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="cf9c8-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="cf9c8-104">Ruft die Parameter der Renderoberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="cf9c8-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf9c8-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="cf9c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf9c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9c8-107">*pparameters* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf9c8-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9c8-108">Typ: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf9c8-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="cf9c8-109">Zeiger auf eine [**D3DXRTS \_ DESC**](d3dxrts-desc.md) -Struktur, in der die Parameter der Renderoberfläche beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cf9c8-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9c8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf9c8-110">Return value</span></span>

<span data-ttu-id="cf9c8-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf9c8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf9c8-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf9c8-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf9c8-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="cf9c8-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9c8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf9c8-114">Requirements</span></span>



| <span data-ttu-id="cf9c8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf9c8-115">Requirement</span></span> | <span data-ttu-id="cf9c8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cf9c8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9c8-117">Header</span><span class="sxs-lookup"><span data-stu-id="cf9c8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cf9c8-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf9c8-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cf9c8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf9c8-119">Library</span></span><br/> | <dl> <span data-ttu-id="cf9c8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf9c8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf9c8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf9c8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9c8-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="cf9c8-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




