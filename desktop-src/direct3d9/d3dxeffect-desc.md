---
description: Beschreibt ein Effect-Objekt.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762054"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="921bd-103">D3DXEFFECT- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="921bd-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="921bd-104">Beschreibt ein Effect-Objekt.</span><span class="sxs-lookup"><span data-stu-id="921bd-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="921bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="921bd-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="921bd-106">Member</span><span class="sxs-lookup"><span data-stu-id="921bd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="921bd-107">**Creator**</span><span class="sxs-lookup"><span data-stu-id="921bd-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="921bd-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="921bd-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="921bd-109">Eine Zeichenfolge, die den Namen des Effekts Erstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="921bd-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="921bd-110">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="921bd-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="921bd-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="921bd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="921bd-112">Die Anzahl der Parameter, die für die Auswirkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="921bd-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="921bd-113">**O**</span><span class="sxs-lookup"><span data-stu-id="921bd-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="921bd-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="921bd-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="921bd-115">Anzahl der Techniken, die den Effekt darstellen können.</span><span class="sxs-lookup"><span data-stu-id="921bd-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="921bd-116">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="921bd-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="921bd-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="921bd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="921bd-118">Anzahl von Funktionen, die den Effekt darstellen können.</span><span class="sxs-lookup"><span data-stu-id="921bd-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="921bd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="921bd-119">Remarks</span></span>

<span data-ttu-id="921bd-120">Ein Effect-Objekt kann mehrere renderingtechniken und-Parameter für denselben Effekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="921bd-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="921bd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="921bd-121">Requirements</span></span>



| <span data-ttu-id="921bd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="921bd-122">Requirement</span></span> | <span data-ttu-id="921bd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="921bd-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="921bd-124">Header</span><span class="sxs-lookup"><span data-stu-id="921bd-124">Header</span></span><br/> | <dl> <span data-ttu-id="921bd-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="921bd-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921bd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="921bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921bd-127">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="921bd-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
