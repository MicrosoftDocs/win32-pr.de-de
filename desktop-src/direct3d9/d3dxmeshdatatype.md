---
description: Definiert den Typ der Mesh-Daten, die in D3DXMESHDATA vorhanden sind.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: D3DXMESHDATATYPE-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351948"
---
# <a name="d3dxmeshdatatype-enumeration"></a><span data-ttu-id="932dc-103">D3DXMESHDATATYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="932dc-103">D3DXMESHDATATYPE enumeration</span></span>

<span data-ttu-id="932dc-104">Definiert den Typ der Mesh-Daten, die in [**D3DXMESHDATA**](d3dxmeshdata.md)vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="932dc-104">Defines the type of mesh data present in [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="932dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="932dc-105">Syntax</span></span>


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a><span data-ttu-id="932dc-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="932dc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="932dc-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE \_ Mesh**</span><span class="sxs-lookup"><span data-stu-id="932dc-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="932dc-108">Der Datentyp ist ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="932dc-108">The data type is a mesh.</span></span> <span data-ttu-id="932dc-109">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="932dc-109">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="932dc-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE- \_ patchmesh**</span><span class="sxs-lookup"><span data-stu-id="932dc-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE\_PATCHMESH**</span></span>
</dt> <dd>

<span data-ttu-id="932dc-111">Der Datentyp ist ein patchmesh.</span><span class="sxs-lookup"><span data-stu-id="932dc-111">The data type is a patch mesh.</span></span> <span data-ttu-id="932dc-112">Siehe [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="932dc-112">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="932dc-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="932dc-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="932dc-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="932dc-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="932dc-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="932dc-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="932dc-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="932dc-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="932dc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="932dc-117">Requirements</span></span>



| <span data-ttu-id="932dc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="932dc-118">Requirement</span></span> | <span data-ttu-id="932dc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="932dc-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="932dc-120">Header</span><span class="sxs-lookup"><span data-stu-id="932dc-120">Header</span></span><br/> | <dl> <span data-ttu-id="932dc-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="932dc-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="932dc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="932dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932dc-123">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="932dc-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="932dc-124">**D3DXMESHDATA**</span><span class="sxs-lookup"><span data-stu-id="932dc-124">**D3DXMESHDATA**</span></span>](d3dxmeshdata.md)
</dt> </dl>

 

 




