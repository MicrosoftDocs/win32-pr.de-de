---
description: Definiert Konstanten, die tiefen Puffer Formate beschreiben.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: D3DZBUFFERTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355811"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="4464f-103">D3DZBUFFERTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4464f-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="4464f-104">Definiert Konstanten, die tiefen Puffer Formate beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4464f-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="4464f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4464f-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="4464f-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4464f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4464f-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="4464f-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="4464f-108">Deaktivieren Sie die tiefen Pufferung.</span><span class="sxs-lookup"><span data-stu-id="4464f-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4464f-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="4464f-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="4464f-110">Aktivieren Sie z-Pufferung.</span><span class="sxs-lookup"><span data-stu-id="4464f-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4464f-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ usew**</span><span class="sxs-lookup"><span data-stu-id="4464f-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="4464f-112">Aktivieren Sie w-Pufferung.</span><span class="sxs-lookup"><span data-stu-id="4464f-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4464f-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4464f-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4464f-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="4464f-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4464f-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="4464f-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4464f-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4464f-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4464f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4464f-117">Remarks</span></span>

<span data-ttu-id="4464f-118">Member dieses Enumerationstyps werden mit dem D3DRS \_ zenable-Rendering-Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="4464f-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4464f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4464f-119">Requirements</span></span>



| <span data-ttu-id="4464f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4464f-120">Requirement</span></span> | <span data-ttu-id="4464f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4464f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4464f-122">Header</span><span class="sxs-lookup"><span data-stu-id="4464f-122">Header</span></span><br/> | <dl> <span data-ttu-id="4464f-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4464f-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4464f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4464f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4464f-125">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4464f-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="4464f-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="4464f-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
