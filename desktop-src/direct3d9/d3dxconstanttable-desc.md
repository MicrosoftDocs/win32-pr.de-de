---
description: Eine Beschreibung der Konstanten Tabelle.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: D3DXCONSTANTTABLE_DESC-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762096"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="82c38-103">D3DXCONSTANTTABLE- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="82c38-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="82c38-104">Eine Beschreibung der Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82c38-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82c38-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="82c38-106">Member</span><span class="sxs-lookup"><span data-stu-id="82c38-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82c38-107">**Creator**</span><span class="sxs-lookup"><span data-stu-id="82c38-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="82c38-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82c38-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82c38-109">Der Name des Erstellers der Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82c38-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="82c38-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="82c38-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="82c38-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82c38-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82c38-112">Shader-Version.</span><span class="sxs-lookup"><span data-stu-id="82c38-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="82c38-113">**Konstanten**</span><span class="sxs-lookup"><span data-stu-id="82c38-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="82c38-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82c38-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82c38-115">Anzahl der Konstanten in der Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82c38-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82c38-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82c38-116">Requirements</span></span>



| <span data-ttu-id="82c38-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82c38-117">Requirement</span></span> | <span data-ttu-id="82c38-118">Wert</span><span class="sxs-lookup"><span data-stu-id="82c38-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c38-119">Header</span><span class="sxs-lookup"><span data-stu-id="82c38-119">Header</span></span><br/> | <dl> <span data-ttu-id="82c38-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="82c38-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82c38-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82c38-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c38-122">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="82c38-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="82c38-123">**D3DXCONSTANT- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="82c38-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
