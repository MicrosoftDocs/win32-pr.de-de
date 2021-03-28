---
title: D3DX11_GROUP_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Gruppe.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050938"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="db291-104">Struktur der Bibliothek d3dx11- \_ Gruppe \_</span><span class="sxs-lookup"><span data-stu-id="db291-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="db291-105">Beschreibt eine Effekt Gruppe.</span><span class="sxs-lookup"><span data-stu-id="db291-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="db291-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="db291-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="db291-107">Member</span><span class="sxs-lookup"><span data-stu-id="db291-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="db291-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="db291-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="db291-109">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db291-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="db291-110">Der Name dieser Gruppe (nur **null** , wenn Global).</span><span class="sxs-lookup"><span data-stu-id="db291-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="db291-111">**O**</span><span class="sxs-lookup"><span data-stu-id="db291-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="db291-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db291-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="db291-113">Anzahl der in der Gruppe enthaltenen Techniken.</span><span class="sxs-lookup"><span data-stu-id="db291-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="db291-114">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="db291-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="db291-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db291-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="db291-116">Anzahl der Anmerkungen in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="db291-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db291-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db291-117">Remarks</span></span>

<span data-ttu-id="db291-118">Die Bibliothek d3dx11- \_ Gruppe muss \_ mit [**ID3DX11EffectTechnique:: getdebug**](id3dx11effecttechnique-getdesc.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db291-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db291-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="db291-119">Requirements</span></span>



| <span data-ttu-id="db291-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db291-120">Requirement</span></span> | <span data-ttu-id="db291-121">Wert</span><span class="sxs-lookup"><span data-stu-id="db291-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="db291-122">Header</span><span class="sxs-lookup"><span data-stu-id="db291-122">Header</span></span><br/> | <dl> <span data-ttu-id="db291-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db291-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db291-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db291-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db291-125">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="db291-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

