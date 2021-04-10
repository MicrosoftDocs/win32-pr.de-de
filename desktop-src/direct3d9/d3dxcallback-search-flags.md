---
description: Flags, die zum Abrufen von Rückruf Informationen verwendet werden.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: D3DXCALLBACK_SEARCH_FLAGS-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050872"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="ab814-103">D3DXCALLBACK \_ \_ Suchflags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ab814-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="ab814-104">Flags, die zum Abrufen von Rückruf Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab814-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab814-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab814-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="ab814-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ab814-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab814-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK \_ Suche \_ ohne \_ anfangs \_ Position**</span><span class="sxs-lookup"><span data-stu-id="ab814-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="ab814-108">Schließt Rückrufe an der ursprünglichen Position aus der Suche aus.</span><span class="sxs-lookup"><span data-stu-id="ab814-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="ab814-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ Suche \_ hinter \_ ursprünglicher \_ Position**</span><span class="sxs-lookup"><span data-stu-id="ab814-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="ab814-110">Umkehren der Rückruf Suchrichtung.</span><span class="sxs-lookup"><span data-stu-id="ab814-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="ab814-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ Search \_ \_ DWORD erzwingen**</span><span class="sxs-lookup"><span data-stu-id="ab814-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ab814-112">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="ab814-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ab814-113">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ab814-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ab814-114">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab814-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab814-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab814-115">Requirements</span></span>



| <span data-ttu-id="ab814-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab814-116">Requirement</span></span> | <span data-ttu-id="ab814-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ab814-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab814-118">Header</span><span class="sxs-lookup"><span data-stu-id="ab814-118">Header</span></span><br/> | <dl> <span data-ttu-id="ab814-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab814-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab814-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab814-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab814-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ab814-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




