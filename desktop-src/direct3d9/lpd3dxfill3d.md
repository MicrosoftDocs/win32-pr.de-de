---
description: Der Funktionstyp, der von den Textur Füll Funktionen verwendet wird.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97342895cb119a786aa71626aeea6d93650c6dc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482054"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="96a65-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="96a65-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="96a65-104">Der Funktionstyp, der von den Textur Füll Funktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96a65-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96a65-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="96a65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96a65-106">Parameters</span></span>

<span data-ttu-id="96a65-107">Pout-Zeiger auf einen Vektor, den die Funktion verwendet, um das Ergebnis zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="96a65-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="96a65-108">X, Y, Z und W werden R, G, B bzw. zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="96a65-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="96a65-109">ptexcoord-Zeiger auf einen Vektor, der die Koordinaten des Texels enthält, das derzeit ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="96a65-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="96a65-110">Texturkoordinaten Komponenten für Textur-und volumetexturen reichen von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="96a65-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="96a65-111">Texturkoordinaten Komponenten für cubetexturen reichen von-1 bis 1.</span><span class="sxs-lookup"><span data-stu-id="96a65-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="96a65-112">ptexelsize: Zeiger auf einen Vektor, der die Abmessungen des aktuellen Texels enthält.</span><span class="sxs-lookup"><span data-stu-id="96a65-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="96a65-113">pData-Zeiger auf Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="96a65-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="96a65-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96a65-114">Return Value</span></span>

<span data-ttu-id="96a65-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="96a65-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96a65-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96a65-116">Remarks</span></span>

<span data-ttu-id="96a65-117">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="96a65-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="96a65-118">Andernfalls können Stapel Überläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="96a65-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="96a65-119">Header</span><span class="sxs-lookup"><span data-stu-id="96a65-119">Header</span></span>                   | <span data-ttu-id="96a65-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="96a65-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="96a65-121">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="96a65-121">Import Library</span></span>           | <span data-ttu-id="96a65-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="96a65-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="96a65-123">Mindestens Betriebs System</span><span class="sxs-lookup"><span data-stu-id="96a65-123">Minimum Operating System</span></span> | <span data-ttu-id="96a65-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="96a65-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="96a65-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96a65-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a65-126">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="96a65-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="96a65-127">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="96a65-127">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
