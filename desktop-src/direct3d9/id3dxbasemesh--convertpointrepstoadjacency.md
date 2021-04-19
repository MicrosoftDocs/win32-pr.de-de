---
description: Konvertiert Punkt repräsentative Daten in Gitter Informations Informationen.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'ID3DXBaseMesh:: convertpointrepstoaccessency-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355179"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="ed44b-103">ID3DXBaseMesh:: convertpointrepstoaccessency-Methode</span><span class="sxs-lookup"><span data-stu-id="ed44b-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="ed44b-104">Konvertiert Punkt repräsentative Daten in Gitter Informations Informationen.</span><span class="sxs-lookup"><span data-stu-id="ed44b-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed44b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed44b-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ed44b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed44b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed44b-107">*pprep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed44b-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed44b-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ed44b-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed44b-109">Zeiger auf ein Array von einem DWORD pro Scheitelpunkt des Netzes, das Punkt repräsentative Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ed44b-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="ed44b-110">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ed44b-110">This parameter is optional.</span></span> <span data-ttu-id="ed44b-111">Wenn Sie einen **null** -Wert angeben, wird dieser Parameter als Identitäts Array interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ed44b-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="ed44b-112">*padjacency* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ed44b-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed44b-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed44b-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed44b-114">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="ed44b-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="ed44b-115">Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**ID3DXBaseMesh:: getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) betragen.</span><span class="sxs-lookup"><span data-stu-id="ed44b-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed44b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed44b-116">Return value</span></span>

<span data-ttu-id="ed44b-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed44b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed44b-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed44b-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed44b-119">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="ed44b-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed44b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed44b-120">Requirements</span></span>



| <span data-ttu-id="ed44b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed44b-121">Requirement</span></span> | <span data-ttu-id="ed44b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ed44b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed44b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ed44b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ed44b-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed44b-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed44b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed44b-125">Library</span></span><br/> | <dl> <span data-ttu-id="ed44b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed44b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed44b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed44b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed44b-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="ed44b-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
