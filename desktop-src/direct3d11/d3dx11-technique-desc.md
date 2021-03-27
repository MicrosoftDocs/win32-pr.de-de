---
title: D3DX11_TECHNIQUE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Technik.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762180"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="df149-104">Bibliothek d3dx11 \_ Technique- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="df149-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="df149-105">Beschreibt eine Effekt Technik.</span><span class="sxs-lookup"><span data-stu-id="df149-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="df149-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="df149-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="df149-107">Member</span><span class="sxs-lookup"><span data-stu-id="df149-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="df149-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="df149-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="df149-109">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df149-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="df149-110">Der Name dieser Technik (null, wenn nicht anonym).</span><span class="sxs-lookup"><span data-stu-id="df149-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="df149-111">**Ausweisen**</span><span class="sxs-lookup"><span data-stu-id="df149-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="df149-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df149-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="df149-113">Anzahl der in der Technik enthaltenen Übergänge.</span><span class="sxs-lookup"><span data-stu-id="df149-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="df149-114">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="df149-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="df149-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="df149-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="df149-116">Anzahl der Anmerkungen zu dieser Technik.</span><span class="sxs-lookup"><span data-stu-id="df149-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df149-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df149-117">Remarks</span></span>

<span data-ttu-id="df149-118">Bibliothek d3dx11 \_ Technique \_ wird mit [**ID3DX11EffectTechnique:: getdebug**](id3dx11effecttechnique-getdesc.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="df149-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df149-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="df149-119">Requirements</span></span>



| <span data-ttu-id="df149-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df149-120">Requirement</span></span> | <span data-ttu-id="df149-121">Wert</span><span class="sxs-lookup"><span data-stu-id="df149-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="df149-122">Header</span><span class="sxs-lookup"><span data-stu-id="df149-122">Header</span></span><br/> | <dl> <span data-ttu-id="df149-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="df149-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df149-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="df149-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df149-125">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="df149-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

