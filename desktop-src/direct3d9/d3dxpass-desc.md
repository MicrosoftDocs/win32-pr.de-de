---
description: Beschreibt einen Durchlauf für ein Effekt Objekt.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354147"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="4bcde-103">D3DXPASS- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="4bcde-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="4bcde-104">Beschreibt einen Durchlauf für ein Effekt Objekt.</span><span class="sxs-lookup"><span data-stu-id="4bcde-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcde-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bcde-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="4bcde-106">Member</span><span class="sxs-lookup"><span data-stu-id="4bcde-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4bcde-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="4bcde-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="4bcde-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bcde-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4bcde-109">Der für den Durchlauf verwendete Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="4bcde-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="4bcde-110">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4bcde-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="4bcde-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bcde-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4bcde-112">Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="4bcde-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="4bcde-113">Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="4bcde-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="4bcde-114">**pvertexshaderfunction**</span><span class="sxs-lookup"><span data-stu-id="4bcde-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="4bcde-115">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4bcde-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="4bcde-116">Zeiger auf die Vertex-Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="4bcde-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="4bcde-117">Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Struktur einen **null** -Zeiger zurück, wenn Sie von [**getpassde**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4bcde-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="4bcde-118">**ppixelshaderfunction**</span><span class="sxs-lookup"><span data-stu-id="4bcde-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="4bcde-119">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4bcde-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="4bcde-120">Zeiger auf die Pixel-Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="4bcde-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="4bcde-121">Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Struktur einen **null** -Zeiger zurück, wenn Sie von [**getpassde**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4bcde-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bcde-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bcde-122">Requirements</span></span>



| <span data-ttu-id="4bcde-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bcde-123">Requirement</span></span> | <span data-ttu-id="4bcde-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4bcde-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcde-125">Header</span><span class="sxs-lookup"><span data-stu-id="4bcde-125">Header</span></span><br/> | <dl> <span data-ttu-id="4bcde-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bcde-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcde-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bcde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcde-128">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="4bcde-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="4bcde-129">**Getpassde SC**</span><span class="sxs-lookup"><span data-stu-id="4bcde-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
