---
description: Beschreibt ein von einem Effekt verwendetes Verfahren.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050846"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="c1af7-103">D3DXTECHNIQUE- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="c1af7-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="c1af7-104">Beschreibt ein von einem Effekt verwendetes Verfahren.</span><span class="sxs-lookup"><span data-stu-id="c1af7-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1af7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1af7-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="c1af7-106">Member</span><span class="sxs-lookup"><span data-stu-id="c1af7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1af7-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="c1af7-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="c1af7-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1af7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1af7-109">Eine Zeichenfolge, die den Namen der Technik enthält.</span><span class="sxs-lookup"><span data-stu-id="c1af7-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="c1af7-110">**Ausweisen**</span><span class="sxs-lookup"><span data-stu-id="c1af7-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="c1af7-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1af7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1af7-112">Die Anzahl von Renderingdurchläufen, die für das</span><span class="sxs-lookup"><span data-stu-id="c1af7-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="c1af7-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="c1af7-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c1af7-114">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="c1af7-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="c1af7-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1af7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c1af7-116">Die Anzahl der Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="c1af7-116">The number of annotations.</span></span> <span data-ttu-id="c1af7-117">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="c1af7-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1af7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1af7-118">Remarks</span></span>

<span data-ttu-id="c1af7-119">Einige Grafikkarten können zwei Texturen in einem einzigen Durchlauf renderingzeichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="c1af7-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="c1af7-120">Wenn eine Karte jedoch nicht über diese Funktion verfügt, ist es oft möglich, denselben Effekt in zwei Durchläufen zu rendern, wobei eine Textur für jeden Durchlauf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1af7-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1af7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1af7-121">Requirements</span></span>



| <span data-ttu-id="c1af7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1af7-122">Requirement</span></span> | <span data-ttu-id="c1af7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c1af7-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1af7-124">Header</span><span class="sxs-lookup"><span data-stu-id="c1af7-124">Header</span></span><br/> | <dl> <span data-ttu-id="c1af7-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1af7-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1af7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1af7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1af7-127">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="c1af7-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
