---
description: Funktionsprototyp, der von D3DXComputeIMTFromSignal verwendet wird, um ein benutzerdefiniertes Signal im u,v-Bereich eines Eingabegitters zu beschreiben. Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der bereitgestellten u,v-Koordinate aus.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342835"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="02f2f-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="02f2f-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="02f2f-105">Funktionsprototyp, der von [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) verwendet wird, um ein benutzerdefiniertes Signal im u,v-Bereich eines Eingabegitters zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="02f2f-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="02f2f-106">Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der bereitgestellten u,v-Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="02f2f-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f2f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02f2f-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="02f2f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02f2f-108">Parameters</span></span>

<span data-ttu-id="02f2f-109">\[in \] uv: Ein Zeiger auf einen Vektor, der die Scheitelpunkttexturkoordinate enthält.</span><span class="sxs-lookup"><span data-stu-id="02f2f-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="02f2f-110">\[in \] uPrimitiveId: Der Index des Eingabedreiecks auf dem Gitternetz, für das das Signal berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="02f2f-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="02f2f-111">\[in \] uSignalDimension: Die Anzahl der Gleitkommazahlen, die im Array von Signaldaten (pfSignalOut) gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02f2f-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="02f2f-112">\[in \] pUserData: Der an [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)übergebene pUserData-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="02f2f-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="02f2f-113">\[out \] pfSignalOut: Ein Array von Gleitkommawerten, das die Signaldaten enthält.</span><span class="sxs-lookup"><span data-stu-id="02f2f-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="02f2f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02f2f-114">Return Value</span></span>

<span data-ttu-id="02f2f-115">Diese Funktion muss implementiert werden, um S \_ OK zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="02f2f-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f2f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02f2f-116">Remarks</span></span>

<span data-ttu-id="02f2f-117">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="02f2f-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="02f2f-118">Andernfalls können Stapelüberläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="02f2f-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="02f2f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02f2f-119">Requirement</span></span>               | <span data-ttu-id="02f2f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="02f2f-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="02f2f-121">Header</span><span class="sxs-lookup"><span data-stu-id="02f2f-121">Header</span></span>         | <span data-ttu-id="02f2f-122">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="02f2f-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="02f2f-123">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="02f2f-123">Import Library</span></span> | <span data-ttu-id="02f2f-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="02f2f-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="02f2f-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02f2f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f2f-126">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="02f2f-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
