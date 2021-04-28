---
description: 'ID3DX10Mesh::Optimize-Methode: Generiert ein neues Gitter mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: ID3DX10Mesh::Optimize-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108048"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="25abf-103">ID3DX10Mesh::Optimize-Methode</span><span class="sxs-lookup"><span data-stu-id="25abf-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="25abf-104">Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="25abf-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="25abf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25abf-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="25abf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25abf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25abf-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="25abf-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25abf-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25abf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25abf-109">Gibt den Typ der durchzuführenden Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="25abf-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="25abf-110">Dieser Parameter kann auf eine Kombination aus mindestens einem Flag von D3DXMESHOPT und D3DXMESH festgelegt werden (außer D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY und D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="25abf-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="25abf-111">*pFaceRemap* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="25abf-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25abf-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25abf-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25abf-113">Ein Array von UINTs pro Gesicht, das das ursprüngliche Gitternetzgesicht identifiziert, das jedem Gesicht im optimierten Gitter entspricht.</span><span class="sxs-lookup"><span data-stu-id="25abf-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="25abf-114">Wenn der für dieses Argument angegebene Wert **NULL ist,** werden keine Gesichtszuordnungsdaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25abf-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="25abf-115">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25abf-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25abf-116">Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="25abf-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="25abf-117">Adresse eines Zeigers auf eine [**ID3D10Blob-Schnittstelle,**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)die ein DWORD für jeden Scheitelpunkt enthält, das angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="25abf-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="25abf-118">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="25abf-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25abf-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25abf-119">Return value</span></span>

<span data-ttu-id="25abf-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25abf-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25abf-121">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="25abf-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25abf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25abf-122">Remarks</span></span>

<span data-ttu-id="25abf-123">Diese Methode generiert ein neues Gitter.</span><span class="sxs-lookup"><span data-stu-id="25abf-123">This method generates a new mesh.</span></span> <span data-ttu-id="25abf-124">Vor dem Ausführen von Optimize muss eine Anwendung durch Aufrufen von [**ID3DX10Mesh::GenerateAdjacencyAndPointReps einen Adjacency-Puffer generieren.**](id3dx10mesh-generateadjacencyandpointreps.md)</span><span class="sxs-lookup"><span data-stu-id="25abf-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="25abf-125">Der Adjacency-Puffer enthält Adjacency-Daten, z. B. eine Liste von Kanten und die nebeneinander liegenden Gesichter.</span><span class="sxs-lookup"><span data-stu-id="25abf-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="25abf-126">Diese Methode ist der [**ID3DX10Mesh::CloneMesh-Methode**](id3dx10mesh-clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitternetzes Optimierungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="25abf-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="25abf-127">Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.</span><span class="sxs-lookup"><span data-stu-id="25abf-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="25abf-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25abf-128">Requirements</span></span>



| <span data-ttu-id="25abf-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25abf-129">Requirement</span></span> | <span data-ttu-id="25abf-130">Wert</span><span class="sxs-lookup"><span data-stu-id="25abf-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25abf-131">Header</span><span class="sxs-lookup"><span data-stu-id="25abf-131">Header</span></span><br/>  | <dl> <span data-ttu-id="25abf-132"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="25abf-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="25abf-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25abf-133">Library</span></span><br/> | <dl> <span data-ttu-id="25abf-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="25abf-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25abf-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25abf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25abf-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="25abf-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="25abf-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="25abf-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
