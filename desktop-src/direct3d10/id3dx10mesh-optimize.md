---
description: Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh:: optimiert-Methode (d3dx10. h)'
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
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355276"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="78316-103">ID3DX10Mesh:: optimiert-Methode</span><span class="sxs-lookup"><span data-stu-id="78316-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="78316-104">Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="78316-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="78316-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78316-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="78316-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78316-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="78316-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78316-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78316-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78316-109">Gibt den Typ der auszuführenden Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="78316-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="78316-110">Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus D3DXMESHOPT und D3DXMESH festgelegt werden (mit Ausnahme von D3DXMESH \_ 32 Bit, D3DXMESH \_ IB \_ Write only und D3DXMESH \_ Write).</span><span class="sxs-lookup"><span data-stu-id="78316-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="78316-111">*pfakeremap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78316-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78316-112">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78316-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78316-113">Ein Array von uint (eins pro Gesicht), das die ursprüngliche Gitterfläche angibt, die jedem Gesicht im optimierten Mesh entspricht.</span><span class="sxs-lookup"><span data-stu-id="78316-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="78316-114">Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78316-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="78316-115">*ppvertexremap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78316-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78316-116">Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="78316-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="78316-117">Adresse eines Zeigers auf eine [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="78316-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="78316-118">Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="78316-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78316-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78316-119">Return value</span></span>

<span data-ttu-id="78316-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78316-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78316-121">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="78316-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78316-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78316-122">Remarks</span></span>

<span data-ttu-id="78316-123">Diese Methode generiert ein neues Mesh.</span><span class="sxs-lookup"><span data-stu-id="78316-123">This method generates a new mesh.</span></span> <span data-ttu-id="78316-124">Bevor Sie optimieren ausführen, muss eine Anwendung durch Aufrufen von [**ID3DX10Mesh:: generateanpoinencyandpointreps**](id3dx10mesh-generateadjacencyandpointreps.md)einen Ereignis Puffer generieren.</span><span class="sxs-lookup"><span data-stu-id="78316-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="78316-125">Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="78316-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="78316-126">Diese Methode ähnelt der [**ID3DX10Mesh:: clonemesh**](id3dx10mesh-clonemesh.md) -Methode, mit der Ausnahme, dass Sie beim Erzeugen des neuen Klon des Netzes eine Optimierung durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="78316-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="78316-127">Das Ausgabe Mesh erbt alle Erstellungs Parameter des eingabemesh.</span><span class="sxs-lookup"><span data-stu-id="78316-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="78316-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78316-128">Requirements</span></span>



| <span data-ttu-id="78316-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78316-129">Requirement</span></span> | <span data-ttu-id="78316-130">Wert</span><span class="sxs-lookup"><span data-stu-id="78316-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78316-131">Header</span><span class="sxs-lookup"><span data-stu-id="78316-131">Header</span></span><br/>  | <dl> <span data-ttu-id="78316-132"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="78316-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="78316-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78316-133">Library</span></span><br/> | <dl> <span data-ttu-id="78316-134"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78316-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78316-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78316-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78316-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="78316-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="78316-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="78316-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
