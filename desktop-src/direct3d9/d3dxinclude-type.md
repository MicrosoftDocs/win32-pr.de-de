---
description: Beschreibt den Speicherort der Includedatei.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: D3DXINCLUDE_TYPE-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530896"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="b4413-103">D3DXINCLUDE- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="b4413-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="b4413-104">Beschreibt den Speicherort der Includedatei.</span><span class="sxs-lookup"><span data-stu-id="b4413-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4413-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4413-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b4413-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b4413-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4413-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="b4413-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="b4413-108">Suchen Sie im lokalen Projekt nach der Includedatei.</span><span class="sxs-lookup"><span data-stu-id="b4413-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="b4413-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC- \_ System**</span><span class="sxs-lookup"><span data-stu-id="b4413-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="b4413-110">Suchen Sie im Systempfad nach der Includedatei.</span><span class="sxs-lookup"><span data-stu-id="b4413-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="b4413-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b4413-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b4413-112">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="b4413-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b4413-113">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b4413-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b4413-114">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4413-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4413-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4413-115">Requirements</span></span>



| <span data-ttu-id="b4413-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4413-116">Requirement</span></span> | <span data-ttu-id="b4413-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b4413-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4413-118">Header</span><span class="sxs-lookup"><span data-stu-id="b4413-118">Header</span></span><br/> | <dl> <span data-ttu-id="b4413-119"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4413-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4413-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4413-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4413-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="b4413-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




