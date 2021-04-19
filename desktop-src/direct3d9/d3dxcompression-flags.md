---
description: Definiert den Komprimierungs Modus zum Speichern komprimierter Animations Satz Daten.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: D3DXCOMPRESSION_FLAGS-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364366"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="07dc3-103">D3DXCOMPRESSION \_ Flags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="07dc3-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="07dc3-104">Definiert den Komprimierungs Modus zum Speichern komprimierter Animations Satz Daten.</span><span class="sxs-lookup"><span data-stu-id="07dc3-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07dc3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07dc3-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="07dc3-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="07dc3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="07dc3-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="07dc3-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="07dc3-108">Implementiert eine schnelle Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="07dc3-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="07dc3-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="07dc3-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="07dc3-110">Implementiert eine langsame Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="07dc3-110">Implements slow compression.</span></span> <span data-ttu-id="07dc3-111">Führt in der Regel zu einem komprimierten Animations Satz mit besserer Qualität als bei Verwendung von D3DXCOMPRESS \_ default.</span><span class="sxs-lookup"><span data-stu-id="07dc3-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="07dc3-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07dc3-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="07dc3-113">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="07dc3-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="07dc3-114">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="07dc3-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="07dc3-115">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="07dc3-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07dc3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07dc3-116">Requirements</span></span>



| <span data-ttu-id="07dc3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07dc3-117">Requirement</span></span> | <span data-ttu-id="07dc3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="07dc3-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07dc3-119">Header</span><span class="sxs-lookup"><span data-stu-id="07dc3-119">Header</span></span><br/> | <dl> <span data-ttu-id="07dc3-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="07dc3-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07dc3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07dc3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07dc3-122">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="07dc3-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




