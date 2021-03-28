---
title: D3DX11_EFFECT_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982588"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="3f5c7-104">Bibliothek d3dx11 \_ Effect- \_ Struktur Struktur</span><span class="sxs-lookup"><span data-stu-id="3f5c7-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="3f5c7-105">Beschreibt einen Effekt.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5c7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f5c7-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="3f5c7-107">Member</span><span class="sxs-lookup"><span data-stu-id="3f5c7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f5c7-108">**Constantbuffers**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="3f5c7-109">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="3f5c7-110">Die Anzahl der Konstanten Puffer in diesem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="3f5c7-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="3f5c7-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="3f5c7-113">Die Anzahl der globalen Variablen in diesem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="3f5c7-114">**Interfakevariables**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="3f5c7-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="3f5c7-116">Die Anzahl der globalen Schnittstellen in diesem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="3f5c7-117">**O**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="3f5c7-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="3f5c7-119">Die Anzahl der in diesem Effekt beschriebenen Techniken.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="3f5c7-120">**Gruppen**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="3f5c7-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f5c7-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="3f5c7-122">Die Anzahl der Gruppen in diesem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f5c7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f5c7-123">Remarks</span></span>

<span data-ttu-id="3f5c7-124">"Bibliothek d3dx11 Effect Debug" \_ \_ wird mit " [**ID3DX11Effect:: getdebug**](id3dx11effect-getdesc.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f5c7-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5c7-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3f5c7-125">Requirements</span></span>



| <span data-ttu-id="3f5c7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f5c7-126">Requirement</span></span> | <span data-ttu-id="3f5c7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3f5c7-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5c7-128">Header</span><span class="sxs-lookup"><span data-stu-id="3f5c7-128">Header</span></span><br/> | <dl> <span data-ttu-id="3f5c7-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f5c7-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5c7-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f5c7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5c7-131">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3f5c7-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

