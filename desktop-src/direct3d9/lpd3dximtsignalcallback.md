---
description: Funktionsprototyp, der von D3DXComputeIMTFromSignal verwendet wird, um ein benutzerdefiniertes Signal im u-v-Raum eines Eingabe Netzes zu beschreiben. Die-Funktion wertet ein prozedurales Signal der Dimension usignaldimension bei der angegebenen u-, v-Koordinate aus.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343118"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="8a0bd-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="8a0bd-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="8a0bd-105">Funktionsprototyp, der von [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) verwendet wird, um ein benutzerdefiniertes Signal im u-v-Raum eines Eingabe Netzes zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="8a0bd-106">Die-Funktion wertet ein prozedurales Signal der Dimension usignaldimension bei der angegebenen u-, v-Koordinate aus.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0bd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a0bd-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="8a0bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a0bd-108">Parameters</span></span>

<span data-ttu-id="8a0bd-109">\[in \] UV-ein Zeiger auf einen Vektor, der die Scheitelpunkt Textur Koordinate enthält.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="8a0bd-110">\[in \] uprimitiveid: der Index des Eingabe Dreiecks in dem Mesh, für das das Signal berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="8a0bd-111">\[in \] usignaldimension: die Anzahl von Gleit Komma Zahlen, die im Array von Signaldaten (pfsignalout) gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="8a0bd-112">\[in \] puserdata: der puserdata-Zeiger, der an [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="8a0bd-113">\[Out \] pfsignalout: ein Array von Gleit Komma Zahlen, das die Signaldaten enthält.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a0bd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a0bd-114">Return Value</span></span>

<span data-ttu-id="8a0bd-115">Diese Funktion muss implementiert werden, damit S "OK" zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="8a0bd-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a0bd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a0bd-116">Remarks</span></span>

<span data-ttu-id="8a0bd-117">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="8a0bd-118">Andernfalls können Stapel Überläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="8a0bd-119">Header</span><span class="sxs-lookup"><span data-stu-id="8a0bd-119">Header</span></span>         | <span data-ttu-id="8a0bd-120">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="8a0bd-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="8a0bd-121">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="8a0bd-121">Import Library</span></span> | <span data-ttu-id="8a0bd-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="8a0bd-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="8a0bd-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a0bd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a0bd-124">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="8a0bd-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
