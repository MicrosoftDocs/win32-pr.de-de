---
description: Identifiziert Ressourcen Daten.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE-Struktur (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366465"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="4e275-103">D3DXF \_ fileloadresource-Struktur</span><span class="sxs-lookup"><span data-stu-id="4e275-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="4e275-104">Identifiziert Ressourcen Daten.</span><span class="sxs-lookup"><span data-stu-id="4e275-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e275-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e275-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="4e275-106">Member</span><span class="sxs-lookup"><span data-stu-id="4e275-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e275-107">**HMODULE**</span><span class="sxs-lookup"><span data-stu-id="4e275-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="4e275-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e275-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e275-109">Handle des Moduls, das die zu ladende Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="4e275-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="4e275-110">Wenn dieser Member **null** ist, muss die Ressource an die ausführbare Datei angefügt werden, von der Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e275-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="4e275-111">**lpname**</span><span class="sxs-lookup"><span data-stu-id="4e275-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="4e275-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e275-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e275-113">Ein Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="4e275-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="4e275-114">Wenn die Ressource z. b. ein Mesh ist, sollte dieser Member den Namen der Mesh-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="4e275-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="4e275-115">**lptype**</span><span class="sxs-lookup"><span data-stu-id="4e275-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="4e275-116">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e275-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e275-117">Ein Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4e275-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e275-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e275-118">Remarks</span></span>

<span data-ttu-id="4e275-119">Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](id3dxfile--createenumobject.md) " verwendet und das Flag " [D3DXF \_ fileload \_ FromResource](d3dxf.md) " angibt.</span><span class="sxs-lookup"><span data-stu-id="4e275-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e275-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e275-120">Requirements</span></span>



| <span data-ttu-id="4e275-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e275-121">Requirement</span></span> | <span data-ttu-id="4e275-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4e275-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e275-123">Header</span><span class="sxs-lookup"><span data-stu-id="4e275-123">Header</span></span><br/> | <dl> <span data-ttu-id="4e275-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e275-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e275-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e275-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e275-126">D3DX X-Dateistrukturen</span><span class="sxs-lookup"><span data-stu-id="4e275-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
