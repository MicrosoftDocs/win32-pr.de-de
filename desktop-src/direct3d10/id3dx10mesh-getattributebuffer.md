---
description: Greifen Sie auf den-Attribut Puffer des Mesh zu.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'ID3DX10Mesh:: getattributebuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353384"
---
# <a name="id3dx10meshgetattributebuffer-method"></a><span data-ttu-id="f98cb-103">ID3DX10Mesh:: getattributebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f98cb-103">ID3DX10Mesh::GetAttributeBuffer method</span></span>

<span data-ttu-id="f98cb-104">Greifen Sie auf den-Attribut Puffer des Mesh zu.</span><span class="sxs-lookup"><span data-stu-id="f98cb-104">Access the mesh's attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f98cb-105">Syntax</span></span>


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f98cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f98cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98cb-107">*ppattributebuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f98cb-107">*ppAttributeBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f98cb-108">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f98cb-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="f98cb-109">Der Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="f98cb-109">The attribute buffer.</span></span> <span data-ttu-id="f98cb-110">Siehe [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f98cb-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98cb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f98cb-111">Return value</span></span>

<span data-ttu-id="f98cb-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f98cb-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f98cb-113">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f98cb-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f98cb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f98cb-114">Requirements</span></span>



| <span data-ttu-id="f98cb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f98cb-115">Requirement</span></span> | <span data-ttu-id="f98cb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f98cb-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f98cb-117">Header</span><span class="sxs-lookup"><span data-stu-id="f98cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f98cb-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98cb-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f98cb-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f98cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="f98cb-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f98cb-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f98cb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f98cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98cb-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f98cb-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f98cb-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f98cb-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




