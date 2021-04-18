---
description: Beschreibt einen Rückruf Schlüssel zur Verwendung in Keyframe-Animationen.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: D3DXKEY_CALLBACK-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355008"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="815c5-103">D3DXKEY- \_ Rückruf Struktur</span><span class="sxs-lookup"><span data-stu-id="815c5-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="815c5-104">Beschreibt einen Rückruf Schlüssel zur Verwendung in Keyframe-Animationen.</span><span class="sxs-lookup"><span data-stu-id="815c5-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="815c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="815c5-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="815c5-106">Member</span><span class="sxs-lookup"><span data-stu-id="815c5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="815c5-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="815c5-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="815c5-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="815c5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="815c5-109">Der Keyframe-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="815c5-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="815c5-110">**pcallbackdata**</span><span class="sxs-lookup"><span data-stu-id="815c5-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="815c5-111">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="815c5-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="815c5-112">Zeiger auf Benutzer Rückruf Daten.</span><span class="sxs-lookup"><span data-stu-id="815c5-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="815c5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="815c5-113">Requirements</span></span>



| <span data-ttu-id="815c5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="815c5-114">Requirement</span></span> | <span data-ttu-id="815c5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="815c5-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="815c5-116">Header</span><span class="sxs-lookup"><span data-stu-id="815c5-116">Header</span></span><br/> | <dl> <span data-ttu-id="815c5-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="815c5-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="815c5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="815c5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815c5-119">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="815c5-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
