---
description: Definiert Transformations Werte für Texturkoordinaten.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: D3DTEXTURETRANSFORMFLAGS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219455"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="69461-103">D3DTEXTURETRANSFORMFLAGS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="69461-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="69461-104">Definiert Transformations Werte für Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="69461-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="69461-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69461-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="69461-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="69461-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="69461-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="69461-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="69461-108">Texturkoordinaten werden direkt an den Rasterizer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="69461-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="69461-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="69461-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="69461-110">Der Raster sollte 1D-Texturkoordinaten erwarten.</span><span class="sxs-lookup"><span data-stu-id="69461-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="69461-111">Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69461-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="69461-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="69461-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="69461-113">Der Raster sollte 2D-Texturkoordinaten erwarten.</span><span class="sxs-lookup"><span data-stu-id="69461-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="69461-114">Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69461-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="69461-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="69461-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="69461-116">Der Raster sollte 3D-Texturkoordinaten erwarten.</span><span class="sxs-lookup"><span data-stu-id="69461-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="69461-117">Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69461-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="69461-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="69461-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="69461-119">Der Raster sollte 4D-Texturkoordinaten erwarten.</span><span class="sxs-lookup"><span data-stu-id="69461-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="69461-120">Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69461-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="69461-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ projiziert**</span><span class="sxs-lookup"><span data-stu-id="69461-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="69461-122">Dieses Flag wird durch die Pixel Pipeline der Fixed-Funktion und die programmierbare Pixel Pipeline in den Versionen PS \_ 1 \_ 1 bis PS \_ 1 \_ 3 berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="69461-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="69461-123">Wenn die Textur Projektion für eine Textur Phase aktiviert ist, müssen alle vier Gleit Komma Werte in das entsprechende Textur Register geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="69461-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="69461-124">Jede Textur Koordinate wird durch das letzte Element dividiert, bevor Sie an den Rasterizer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="69461-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="69461-125">Wenn dieses Flag z. b. mit dem D3DTTFF \_ COUNT3-Flag angegeben wird, werden die erste und zweite Textur Koordinate durch die dritte Koordinate dividiert, bevor Sie an den Rasterizer übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="69461-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="69461-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="69461-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="69461-127">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="69461-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="69461-128">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="69461-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="69461-129">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="69461-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69461-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69461-130">Remarks</span></span>

<span data-ttu-id="69461-131">Texturkoordinaten können mithilfe einer 4 x 4-Matrix transformiert werden, bevor die Ergebnisse an den Rasterizer übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="69461-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="69461-132">Die Texturkoordinaten Transformationen werden durch Aufrufen von [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api)und durch Übergeben des D3DTSS \_ texturetransformflags-Textur Phasen Zustands und eines der Werte aus **D3DTEXTURETRANSFORMFLAGS** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69461-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="69461-133">Weitere Informationen zu Textur Transformationen finden Sie unter [Texturkoordinaten Transformationen (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="69461-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69461-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69461-134">Requirements</span></span>



| <span data-ttu-id="69461-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69461-135">Requirement</span></span> | <span data-ttu-id="69461-136">Wert</span><span class="sxs-lookup"><span data-stu-id="69461-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69461-137">Header</span><span class="sxs-lookup"><span data-stu-id="69461-137">Header</span></span><br/> | <dl> <span data-ttu-id="69461-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="69461-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69461-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69461-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69461-140">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="69461-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="69461-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="69461-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
