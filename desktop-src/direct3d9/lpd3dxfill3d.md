---
description: 'LPD3DXFILL3D: Funktionstyp, der von den Texturfüllfunktionen verwendet wird.'
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed5845f04486a6ac9cf1c984178fb0ed98447a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342765"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="84f36-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="84f36-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="84f36-104">Funktionstyp, der von den Texturfüllfunktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84f36-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f36-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="84f36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84f36-106">Parameters</span></span>

<span data-ttu-id="84f36-107">pOut: Zeiger auf einen Vektor, der von der Funktion verwendet wird, um das Ergebnis zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="84f36-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="84f36-108">X, Y, Z und W werden R, G, B bzw. A zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="84f36-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="84f36-109">pTexCoord: Zeiger auf einen Vektor, der die Koordinaten des texel enthält, das gerade ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="84f36-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="84f36-110">Texturkoordinatenkomponenten für Textur- und Volumentexturen reichen von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="84f36-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="84f36-111">Texturkoordinatenkomponenten für Cubetexturen reichen von -1 bis 1.</span><span class="sxs-lookup"><span data-stu-id="84f36-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="84f36-112">pTexelSize: Zeiger auf einen Vektor, der die Abmessungen des aktuellen Texels enthält.</span><span class="sxs-lookup"><span data-stu-id="84f36-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="84f36-113">pData: Zeiger auf Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="84f36-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="84f36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84f36-114">Return Value</span></span>

<span data-ttu-id="84f36-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="84f36-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f36-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84f36-116">Remarks</span></span>

<span data-ttu-id="84f36-117">Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="84f36-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="84f36-118">Andernfalls können Stapelüberläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="84f36-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="84f36-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84f36-119">Requirement</span></span>                         | <span data-ttu-id="84f36-120">Wert</span><span class="sxs-lookup"><span data-stu-id="84f36-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="84f36-121">Header</span><span class="sxs-lookup"><span data-stu-id="84f36-121">Header</span></span>                   | <span data-ttu-id="84f36-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="84f36-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="84f36-123">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="84f36-123">Import Library</span></span>           | <span data-ttu-id="84f36-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="84f36-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="84f36-125">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="84f36-125">Minimum Operating System</span></span> | <span data-ttu-id="84f36-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="84f36-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="84f36-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84f36-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f36-128">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="84f36-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="84f36-129">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="84f36-129">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
