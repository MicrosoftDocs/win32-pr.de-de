---
description: Statistiken zur Ressourcenverwendung.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_ResourceManager-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761967"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="a9b76-103">D3DDEVINFO \_ ResourceManager-Struktur</span><span class="sxs-lookup"><span data-stu-id="a9b76-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="a9b76-104">Statistiken zur Ressourcenverwendung.</span><span class="sxs-lookup"><span data-stu-id="a9b76-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b76-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9b76-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="a9b76-106">Member</span><span class="sxs-lookup"><span data-stu-id="a9b76-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9b76-107">**stats**</span><span class="sxs-lookup"><span data-stu-id="a9b76-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="a9b76-108">Typ: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="a9b76-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a9b76-109">Array von Ressourcen Statistik Elementen.</span><span class="sxs-lookup"><span data-stu-id="a9b76-109">Array of resource statistics elements.</span></span> <span data-ttu-id="a9b76-110">Siehe [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="a9b76-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9b76-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9b76-111">Remarks</span></span>

<span data-ttu-id="a9b76-112">D3DRTYPECOUNT bezieht sich auf die Anzahl von Enumerationen in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="a9b76-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b76-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9b76-113">Requirements</span></span>



| <span data-ttu-id="a9b76-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9b76-114">Requirement</span></span> | <span data-ttu-id="a9b76-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b76-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b76-116">Header</span><span class="sxs-lookup"><span data-stu-id="a9b76-116">Header</span></span><br/> | <dl> <span data-ttu-id="a9b76-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b76-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b76-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9b76-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b76-119">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a9b76-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
