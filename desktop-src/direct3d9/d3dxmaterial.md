---
description: Gibt Material Informationen zurück, die in Direct3D-Dateien (. x) gespeichert sind.
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: D3DXMATERIAL-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354984"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="f026b-103">D3DXMATERIAL-Struktur</span><span class="sxs-lookup"><span data-stu-id="f026b-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="f026b-104">Gibt Material Informationen zurück, die in Direct3D-Dateien (. x) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f026b-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="f026b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f026b-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="f026b-106">Member</span><span class="sxs-lookup"><span data-stu-id="f026b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f026b-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="f026b-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="f026b-108">Typ: **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="f026b-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f026b-109">[**D3DMATERIAL9**](d3dmaterial9.md) -Struktur, die die Materialeigenschaften beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f026b-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="f026b-110">**ptexturefilename**</span><span class="sxs-lookup"><span data-stu-id="f026b-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="f026b-111">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="f026b-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f026b-112">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen der Textur angibt.</span><span class="sxs-lookup"><span data-stu-id="f026b-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f026b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f026b-113">Remarks</span></span>

<span data-ttu-id="f026b-114">Die [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) -Funktion und die [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) -Funktion geben ein Array von **D3DXMATERIAL** -Strukturen zurück, die die Material Farbe und den Namen der Textur für jedes Material im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="f026b-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="f026b-115">Die Anwendung muss dann die Textur laden.</span><span class="sxs-lookup"><span data-stu-id="f026b-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="f026b-116">Der LPD3DXMATERIAL-Typ wird als Zeiger auf die **D3DXMATERIAL** -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="f026b-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="f026b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f026b-117">Requirements</span></span>



| <span data-ttu-id="f026b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f026b-118">Requirement</span></span> | <span data-ttu-id="f026b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f026b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f026b-120">Header</span><span class="sxs-lookup"><span data-stu-id="f026b-120">Header</span></span><br/> | <dl> <span data-ttu-id="f026b-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f026b-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f026b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f026b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f026b-123">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f026b-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f026b-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="f026b-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="f026b-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="f026b-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




