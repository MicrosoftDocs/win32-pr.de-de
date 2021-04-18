---
description: Beschreibt eine Funktion, die von einem Effekt verwendet wird.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: D3DXFUNCTION_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354367"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="ad501-103">D3DXFUNCTION- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="ad501-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="ad501-104">Beschreibt eine Funktion, die von einem Effekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad501-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad501-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad501-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="ad501-106">Member</span><span class="sxs-lookup"><span data-stu-id="ad501-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad501-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad501-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="ad501-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad501-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad501-109">Funktionsname</span><span class="sxs-lookup"><span data-stu-id="ad501-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="ad501-110">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ad501-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="ad501-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad501-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad501-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad501-112">Unused.</span></span> <span data-ttu-id="ad501-113">Dieser Member wird von [**getfunctiondebug**](id3dxbaseeffect--getfunctiondesc.md)immer auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad501-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad501-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad501-114">Requirements</span></span>



| <span data-ttu-id="ad501-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad501-115">Requirement</span></span> | <span data-ttu-id="ad501-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ad501-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad501-117">Header</span><span class="sxs-lookup"><span data-stu-id="ad501-117">Header</span></span><br/> | <dl> <span data-ttu-id="ad501-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad501-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad501-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad501-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad501-120">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="ad501-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
