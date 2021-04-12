---
description: Konvertiert Gitter Informations Informationen in ein Array von Punkt Vertretern.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh:: convertadjackocytopointreps-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219489"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="c93dc-103">ID3DXBaseMesh:: convertadjackocytopointreps-Methode</span><span class="sxs-lookup"><span data-stu-id="c93dc-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="c93dc-104">Konvertiert Gitter Informations Informationen in ein Array von Punkt Vertretern.</span><span class="sxs-lookup"><span data-stu-id="c93dc-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c93dc-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="c93dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c93dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93dc-107">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c93dc-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93dc-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c93dc-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c93dc-109">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="c93dc-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="c93dc-110">Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**ID3DXBaseMesh:: getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) betragen.</span><span class="sxs-lookup"><span data-stu-id="c93dc-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="c93dc-111">*pprep* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c93dc-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c93dc-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c93dc-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c93dc-113">Zeiger auf ein Array von einem DWORD pro Scheitelpunkt des Netzes, das mit Punkt repräsentativen Daten gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c93dc-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93dc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c93dc-114">Return value</span></span>

<span data-ttu-id="c93dc-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c93dc-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c93dc-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c93dc-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c93dc-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="c93dc-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93dc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c93dc-118">Requirements</span></span>



| <span data-ttu-id="c93dc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c93dc-119">Requirement</span></span> | <span data-ttu-id="c93dc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c93dc-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c93dc-121">Header</span><span class="sxs-lookup"><span data-stu-id="c93dc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c93dc-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93dc-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c93dc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c93dc-123">Library</span></span><br/> | <dl> <span data-ttu-id="c93dc-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c93dc-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c93dc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c93dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93dc-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="c93dc-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
