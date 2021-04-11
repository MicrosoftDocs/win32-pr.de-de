---
description: Eine hilfsstruktur, die Informationen zur Elementstruktur enthält.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354626"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="13b61-103">D3DXSHADER \_ structmembership Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="13b61-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="13b61-104">Eine hilfsstruktur, die Informationen zur Elementstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="13b61-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13b61-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="13b61-106">Member</span><span class="sxs-lookup"><span data-stu-id="13b61-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="13b61-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="13b61-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="13b61-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13b61-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13b61-109">Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die den Namen des Strukturmembers enthält.</span><span class="sxs-lookup"><span data-stu-id="13b61-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="13b61-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="13b61-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="13b61-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13b61-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13b61-112">Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die die Typinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="13b61-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="13b61-113">Siehe [**D3DXSHADER \_ TypInfo**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="13b61-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13b61-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13b61-114">Requirements</span></span>



| <span data-ttu-id="13b61-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13b61-115">Requirement</span></span> | <span data-ttu-id="13b61-116">Wert</span><span class="sxs-lookup"><span data-stu-id="13b61-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b61-117">Header</span><span class="sxs-lookup"><span data-stu-id="13b61-117">Header</span></span><br/> | <dl> <span data-ttu-id="13b61-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="13b61-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b61-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b61-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b61-120">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="13b61-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="13b61-121">**D3DXSHADER \_ TypInfo**</span><span class="sxs-lookup"><span data-stu-id="13b61-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
