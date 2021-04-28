---
description: 'LPD3DXFILL2D: Funktionstyp, der von den Texturfüllfunktionen verwendet wird.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046c324511f2b308243d62fec1b6508a1d483ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087968"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="937c2-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="937c2-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="937c2-104">Funktionstyp, der von den Texturfüllfunktionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="937c2-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="937c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="937c2-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="937c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="937c2-106">Parameters</span></span>

<span data-ttu-id="937c2-107">pOut: Zeiger auf einen Vektor, mit dem die Funktion ihr Ergebnis zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="937c2-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="937c2-108">X, Y, Z und W werden R, G, B bzw. A zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="937c2-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="937c2-109">pTexCoord: Zeiger auf einen Vektor, der die Koordinaten des gerade ausgewerteten Texels enthält.</span><span class="sxs-lookup"><span data-stu-id="937c2-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="937c2-110">Texturkoordinatenkomponenten für Textur- und Volumentexturen liegen zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="937c2-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="937c2-111">Texturkoordinatenkomponenten für Cubetexturen reichen von -1 bis 1.</span><span class="sxs-lookup"><span data-stu-id="937c2-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="937c2-112">pTexelSize: Zeiger auf einen Vektor, der die Abmessungen des aktuellen Texels enthält.</span><span class="sxs-lookup"><span data-stu-id="937c2-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="937c2-113">pData: Zeiger auf Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="937c2-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="937c2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="937c2-114">Return Value</span></span>

<span data-ttu-id="937c2-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="937c2-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="937c2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="937c2-116">Remarks</span></span>

<span data-ttu-id="937c2-117">Achten Sie darauf, die [**Aufrufkonvention für Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben, wenn Sie die Rückruffunktion deklarieren.</span><span class="sxs-lookup"><span data-stu-id="937c2-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="937c2-118">Andernfalls können Stapelüberläufe auftreten.</span><span class="sxs-lookup"><span data-stu-id="937c2-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="937c2-119">Header</span><span class="sxs-lookup"><span data-stu-id="937c2-119">Header</span></span>                   | <span data-ttu-id="937c2-120">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="937c2-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="937c2-121">Importbibliothek</span><span class="sxs-lookup"><span data-stu-id="937c2-121">Import Library</span></span>           | <span data-ttu-id="937c2-122">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="937c2-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="937c2-123">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="937c2-123">Minimum Operating System</span></span> | <span data-ttu-id="937c2-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="937c2-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="937c2-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="937c2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="937c2-126">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="937c2-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="937c2-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="937c2-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
