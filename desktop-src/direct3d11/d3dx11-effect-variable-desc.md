---
title: D3DX11_EFFECT_VARIABLE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Variable.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996203"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="7bf00-104">Bibliothek d3dx11 Effect-Variablen (Debug- \_ \_ \_ Struktur)</span><span class="sxs-lookup"><span data-stu-id="7bf00-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="7bf00-105">Beschreibt eine Effekt Variable.</span><span class="sxs-lookup"><span data-stu-id="7bf00-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf00-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bf00-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="7bf00-107">Member</span><span class="sxs-lookup"><span data-stu-id="7bf00-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bf00-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7bf00-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-109">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-110">Der Name dieser Variablen-, Annotation-oder Strukturmember.</span><span class="sxs-lookup"><span data-stu-id="7bf00-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="7bf00-111">**Tischer**</span><span class="sxs-lookup"><span data-stu-id="7bf00-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-112">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-113">Die semantische Zeichenfolge dieses Variablen-oder Strukturmembers (null für Anmerkungen oder, wenn nicht vorhanden).</span><span class="sxs-lookup"><span data-stu-id="7bf00-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="7bf00-114">**Flags**</span><span class="sxs-lookup"><span data-stu-id="7bf00-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-116">Optionale Flags für Effekt Variablen.</span><span class="sxs-lookup"><span data-stu-id="7bf00-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="7bf00-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="7bf00-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-119">Anzahl der Anmerkungen für diese Variable (immer 0 für Anmerkungen).</span><span class="sxs-lookup"><span data-stu-id="7bf00-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="7bf00-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="7bf00-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-122">Offset in enthaltende cBuffer oder tBuffer (immer 0 für Anmerkungen oder Variablen, die nicht in konstantenpuffern enthalten sind).</span><span class="sxs-lookup"><span data-stu-id="7bf00-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="7bf00-123">**Explitbindpoint**</span><span class="sxs-lookup"><span data-stu-id="7bf00-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="7bf00-124">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7bf00-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7bf00-125">Wird verwendet, wenn die Variable mithilfe des Register-Schlüssel Worts explizit gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7bf00-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="7bf00-126">Häkchen für \_ den \_ \_ expliziten \_ Bindungspunkt der Bibliothek d3dx11 Effect-Variable \_ .</span><span class="sxs-lookup"><span data-stu-id="7bf00-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bf00-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bf00-127">Remarks</span></span>

<span data-ttu-id="7bf00-128">Die \_ Variable "Bibliothek d3dx11 Effect" \_ \_ wird mit " [**ID3DX11EffectVariable:: getdebug**](id3dx11effectvariable-getdesc.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="7bf00-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf00-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7bf00-129">Requirements</span></span>



| <span data-ttu-id="7bf00-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bf00-130">Requirement</span></span> | <span data-ttu-id="7bf00-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7bf00-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf00-132">Header</span><span class="sxs-lookup"><span data-stu-id="7bf00-132">Header</span></span><br/> | <dl> <span data-ttu-id="7bf00-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf00-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf00-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7bf00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf00-135">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7bf00-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

