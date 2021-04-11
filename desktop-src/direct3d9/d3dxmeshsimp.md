---
description: Gibt Vereinfachungs Optionen für ein Mesh an.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: D3DXMESHSIMP-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132333"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="9f498-103">D3DXMESHSIMP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9f498-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="9f498-104">Gibt Vereinfachungs Optionen für ein Mesh an.</span><span class="sxs-lookup"><span data-stu-id="9f498-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f498-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f498-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="9f498-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9f498-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f498-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP \_ Scheitelpunkt**</span><span class="sxs-lookup"><span data-stu-id="9f498-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="9f498-108">Das Mesh wird um die Anzahl der im MinValue-Parameter angegebenen Scheitel Punkte vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9f498-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9f498-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_**</span><span class="sxs-lookup"><span data-stu-id="9f498-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="9f498-110">Das Mesh wird durch die Anzahl der im MinValue-Parameter angegebenen Gesichter vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9f498-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f498-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f498-111">Requirements</span></span>



| <span data-ttu-id="9f498-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f498-112">Requirement</span></span> | <span data-ttu-id="9f498-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9f498-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f498-114">Header</span><span class="sxs-lookup"><span data-stu-id="9f498-114">Header</span></span><br/> | <dl> <span data-ttu-id="9f498-115"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f498-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f498-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f498-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f498-117">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="9f498-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="9f498-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="9f498-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 




