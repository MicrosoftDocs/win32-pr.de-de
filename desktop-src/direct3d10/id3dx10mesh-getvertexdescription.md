---
description: Zugreifen auf die vertexbeschreibung, die an D3DX10CreateMesh übermittelt wurde. In der Scheitelpunkt Beschreibung wird das Layout der Vertex-Puffer des Netzes beschrieben.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh:: getvertexdescription-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961613"
---
# <a name="id3dx10meshgetvertexdescription-method"></a><span data-ttu-id="f8141-104">ID3DX10Mesh:: getvertexdescription-Methode</span><span class="sxs-lookup"><span data-stu-id="f8141-104">ID3DX10Mesh::GetVertexDescription method</span></span>

<span data-ttu-id="f8141-105">Zugreifen auf die vertexbeschreibung, die an [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f8141-105">Access the vertex description passed into [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span></span> <span data-ttu-id="f8141-106">In der Scheitelpunkt Beschreibung wird das Layout der Vertex-Puffer des Netzes beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8141-106">The vertex description describes the layout of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8141-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8141-107">Syntax</span></span>


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a><span data-ttu-id="f8141-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8141-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8141-109">*PPDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f8141-109">*ppDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8141-110">Type: **Konstanten [**d3d10 input \_ - \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***</span><span class="sxs-lookup"><span data-stu-id="f8141-110">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\*\***</span></span>

<span data-ttu-id="f8141-111">Array von Eingabe Elementen, das das Layout der Vertex-Puffer des Netzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f8141-111">Array of input elements that describe the layout of the mesh's vertex buffers.</span></span> <span data-ttu-id="f8141-112">Weitere Informationen finden Sie unter [**d3d10 \_ input \_ Element \_ ensc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="f8141-112">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="f8141-113">*pdeclcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8141-113">*pDeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8141-114">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8141-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8141-115">Die Anzahl der Eingabeelemente in PPDE SC.</span><span class="sxs-lookup"><span data-stu-id="f8141-115">The number of input elements in ppDesc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8141-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8141-116">Return value</span></span>

<span data-ttu-id="f8141-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8141-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8141-118">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f8141-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8141-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8141-119">Requirements</span></span>



| <span data-ttu-id="f8141-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8141-120">Requirement</span></span> | <span data-ttu-id="f8141-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f8141-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8141-122">Header</span><span class="sxs-lookup"><span data-stu-id="f8141-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f8141-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8141-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8141-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8141-124">Library</span></span><br/> | <dl> <span data-ttu-id="f8141-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8141-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8141-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8141-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8141-127">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f8141-127">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f8141-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8141-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
