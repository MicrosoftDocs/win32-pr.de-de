---
description: Identifiziert Ressourcen Daten. Veraltet.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Dxfileloadresource-Struktur (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354390"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="132d0-104">Dxfileloadresource-Struktur</span><span class="sxs-lookup"><span data-stu-id="132d0-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="132d0-105">Identifiziert Ressourcen Daten.</span><span class="sxs-lookup"><span data-stu-id="132d0-105">Identifies resource data.</span></span> <span data-ttu-id="132d0-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="132d0-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="132d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="132d0-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="132d0-108">Member</span><span class="sxs-lookup"><span data-stu-id="132d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="132d0-109">**HMODULE**</span><span class="sxs-lookup"><span data-stu-id="132d0-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="132d0-110">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="132d0-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="132d0-111">Handle des Moduls, das die zu ladende Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="132d0-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="132d0-112">Wenn dieser Member **null** ist, muss die Ressource an die ausführbare Datei angefügt werden, von der Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="132d0-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="132d0-113">**lpname**</span><span class="sxs-lookup"><span data-stu-id="132d0-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="132d0-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="132d0-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="132d0-115">Ein Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="132d0-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="132d0-116">Wenn die Ressource z. b. ein Mesh ist, sollte dieser Member den Namen der Mesh-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="132d0-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="132d0-117">**lptype**</span><span class="sxs-lookup"><span data-stu-id="132d0-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="132d0-118">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="132d0-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="132d0-119">Ein Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="132d0-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="132d0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="132d0-120">Remarks</span></span>

<span data-ttu-id="132d0-121">Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](idirectxfile--createenumobject.md) " verwendet und dxfileload \_ FromResource angibt.</span><span class="sxs-lookup"><span data-stu-id="132d0-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="132d0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="132d0-122">Requirements</span></span>



| <span data-ttu-id="132d0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="132d0-123">Requirement</span></span> | <span data-ttu-id="132d0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="132d0-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="132d0-125">Header</span><span class="sxs-lookup"><span data-stu-id="132d0-125">Header</span></span><br/> | <dl> <span data-ttu-id="132d0-126"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="132d0-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="132d0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="132d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="132d0-128">X-Dateistrukturen</span><span class="sxs-lookup"><span data-stu-id="132d0-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="132d0-129">**"Kreateendumuject"**</span><span class="sxs-lookup"><span data-stu-id="132d0-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="132d0-130">Dxfile-Konstanten</span><span class="sxs-lookup"><span data-stu-id="132d0-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
