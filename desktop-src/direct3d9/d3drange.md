---
description: Definiert einen Bereich.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: D3DRANGE-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355812"
---
# <a name="d3drange-structure"></a><span data-ttu-id="a02a6-103">D3DRANGE-Struktur</span><span class="sxs-lookup"><span data-stu-id="a02a6-103">D3DRANGE structure</span></span>

<span data-ttu-id="a02a6-104">Definiert einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="a02a6-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a02a6-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="a02a6-106">Member</span><span class="sxs-lookup"><span data-stu-id="a02a6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a02a6-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="a02a6-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="a02a6-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a02a6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a02a6-109">Offset (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="a02a6-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a02a6-110">**Größe**</span><span class="sxs-lookup"><span data-stu-id="a02a6-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a02a6-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a02a6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a02a6-112">Größe in Byte.</span><span class="sxs-lookup"><span data-stu-id="a02a6-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a02a6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a02a6-113">Requirements</span></span>



| <span data-ttu-id="a02a6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a02a6-114">Requirement</span></span> | <span data-ttu-id="a02a6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a02a6-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a02a6-116">Header</span><span class="sxs-lookup"><span data-stu-id="a02a6-116">Header</span></span><br/> | <dl> <span data-ttu-id="a02a6-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a02a6-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a02a6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a02a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a02a6-119">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a02a6-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
