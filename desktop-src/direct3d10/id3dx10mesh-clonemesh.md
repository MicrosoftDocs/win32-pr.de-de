---
description: Erstellt ein neues Mesh und füllt es mit den Daten eines zuvor geladenen Mesh.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh:: clonemesh-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363161"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="f88b6-103">ID3DX10Mesh:: clonemesh-Methode</span><span class="sxs-lookup"><span data-stu-id="f88b6-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="f88b6-104">Erstellt ein neues Mesh und füllt es mit den Daten eines zuvor geladenen Mesh.</span><span class="sxs-lookup"><span data-stu-id="f88b6-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f88b6-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f88b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f88b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f88b6-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f88b6-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88b6-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f88b6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f88b6-109">Erstellungsflags, die auf das neue Mesh angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f88b6-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="f88b6-110">Siehe [**d3dx10 \_ Mesh**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="f88b6-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="f88b6-111">*ppossemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f88b6-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88b6-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f88b6-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f88b6-113">Der semantische Name der Positionsdaten.</span><span class="sxs-lookup"><span data-stu-id="f88b6-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="f88b6-114">*PDE SC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f88b6-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88b6-115">Type: **Konstanten [**d3d10 \_ input- \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f88b6-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="f88b6-116">Array von d3d10 \_ input- \_ Element- \_ DESC-Strukturen, das das Vertex-Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f88b6-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="f88b6-117">Weitere Informationen finden Sie unter [**d3d10 \_ input \_ Element \_ ensc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="f88b6-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="f88b6-118">*Declcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f88b6-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88b6-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f88b6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f88b6-120">Die Anzahl der Elemente im PDE-Array.</span><span class="sxs-lookup"><span data-stu-id="f88b6-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="f88b6-121">*ppclonemesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f88b6-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88b6-122">Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f88b6-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="f88b6-123">Das neue Mesh.</span><span class="sxs-lookup"><span data-stu-id="f88b6-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f88b6-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f88b6-124">Return value</span></span>

<span data-ttu-id="f88b6-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f88b6-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f88b6-126">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f88b6-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f88b6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f88b6-127">Requirements</span></span>



| <span data-ttu-id="f88b6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f88b6-128">Requirement</span></span> | <span data-ttu-id="f88b6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f88b6-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f88b6-130">Header</span><span class="sxs-lookup"><span data-stu-id="f88b6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f88b6-131"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f88b6-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f88b6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f88b6-132">Library</span></span><br/> | <dl> <span data-ttu-id="f88b6-133"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f88b6-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f88b6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f88b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f88b6-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f88b6-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f88b6-136">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f88b6-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
