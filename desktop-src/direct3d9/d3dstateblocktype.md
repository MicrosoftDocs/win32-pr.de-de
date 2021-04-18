---
description: Vordefinierte Sätze von Pipeline Zuständen, die von Zustands Blöcken verwendet werden (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: D3DSTATEBLOCKTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104551698"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="4ae73-103">D3DSTATEBLOCKTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4ae73-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="4ae73-104">Vordefinierte Sätze von Pipeline Zuständen, die von Zustands Blöcken verwendet werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="4ae73-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae73-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="4ae73-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4ae73-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4ae73-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_**</span><span class="sxs-lookup"><span data-stu-id="4ae73-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="4ae73-108">Erfassen des aktuellen [Geräte Zustands](saving-all-device-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="4ae73-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ae73-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ Pixel State**</span><span class="sxs-lookup"><span data-stu-id="4ae73-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="4ae73-110">Erfassen des aktuellen [Pixel Zustands](saving-pixel-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="4ae73-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ae73-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ vertexstate**</span><span class="sxs-lookup"><span data-stu-id="4ae73-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="4ae73-112">Erfassen des aktuellen [Scheitelpunkt Zustands](saving-vertex-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="4ae73-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ae73-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4ae73-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4ae73-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="4ae73-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4ae73-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="4ae73-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4ae73-116">Verwenden Sie diesen Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="4ae73-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ae73-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae73-117">Remarks</span></span>

<span data-ttu-id="4ae73-118">Wie im folgenden Diagramm gezeigt, sind Scheitelpunkt-und Pixel Status beide Teilmengen des Geräte Zustands.</span><span class="sxs-lookup"><span data-stu-id="4ae73-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![Diagramm des Geräte Zustands mit vertexzustand und Pixel Zustand als Teilmengen](images/statesets.png)

<span data-ttu-id="4ae73-120">Es gibt nur wenige Zustände, die als Scheitelpunkt und Pixel Status betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="4ae73-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="4ae73-121">Folgende Status sind möglich:</span><span class="sxs-lookup"><span data-stu-id="4ae73-121">These states are:</span></span>

-   <span data-ttu-id="4ae73-122">Rendering-Status: D3DRS \_ fogdensity</span><span class="sxs-lookup"><span data-stu-id="4ae73-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="4ae73-123">Rendering-Status: D3DRS \_ fogstart</span><span class="sxs-lookup"><span data-stu-id="4ae73-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="4ae73-124">Rendering-Status: D3DRS \_ fogend</span><span class="sxs-lookup"><span data-stu-id="4ae73-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="4ae73-125">Textur Zustand: D3DTSS \_ texcoordindex</span><span class="sxs-lookup"><span data-stu-id="4ae73-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="4ae73-126">Textur Zustand: D3DTSS \_ texturetransformflags</span><span class="sxs-lookup"><span data-stu-id="4ae73-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae73-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ae73-127">Requirements</span></span>



| <span data-ttu-id="4ae73-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ae73-128">Requirement</span></span> | <span data-ttu-id="4ae73-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4ae73-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae73-130">Header</span><span class="sxs-lookup"><span data-stu-id="4ae73-130">Header</span></span><br/> | <dl> <span data-ttu-id="4ae73-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae73-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae73-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ae73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae73-133">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4ae73-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="4ae73-134">**IDirect3DDevice9:: kreatestateblock**</span><span class="sxs-lookup"><span data-stu-id="4ae73-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="4ae73-135">**IDirect3DDevice9:: kreatestateblock**</span><span class="sxs-lookup"><span data-stu-id="4ae73-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
