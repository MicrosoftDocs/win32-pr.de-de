---
title: D3DX11_PASS_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Durchlauf, der den Pipeline Zustand enthält.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982549"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="a1590-104">Bibliothek d3dx11 \_ Pass- \_ de-Struktur</span><span class="sxs-lookup"><span data-stu-id="a1590-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="a1590-105">Beschreibt einen Effekt Durchlauf, der den Pipeline Zustand enthält.</span><span class="sxs-lookup"><span data-stu-id="a1590-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1590-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1590-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="a1590-107">Member</span><span class="sxs-lookup"><span data-stu-id="a1590-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1590-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1590-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-109">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-110">Der Name dieses Pass (**null** , wenn nicht anonym).</span><span class="sxs-lookup"><span data-stu-id="a1590-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="a1590-111">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a1590-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-113">Anzahl der Anmerkungen zu diesem Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="a1590-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-114">**piainputsignature**</span><span class="sxs-lookup"><span data-stu-id="a1590-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-115">Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="a1590-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="a1590-116">Signatur aus dem Scheitelpunkt-Shader oder Geometry-Shader (wenn kein Scheitelpunkt-Shader vorhanden ist) oder **null** , wenn keines vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a1590-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-117">**Iainputsignaturesize**</span><span class="sxs-lookup"><span data-stu-id="a1590-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-118">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-119">Größe der Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a1590-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-120">**Schablone Ref**</span><span class="sxs-lookup"><span data-stu-id="a1590-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-122">Der im Status der tiefen Schablone verwendete Schablonen Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="a1590-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-123">**Samplemask**</span><span class="sxs-lookup"><span data-stu-id="a1590-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-124">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-125">Die Beispiel Maske für den Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="a1590-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-126">**Blendfactor**</span><span class="sxs-lookup"><span data-stu-id="a1590-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="a1590-127">Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1590-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a1590-128">Die pro-Komponente-Blend-Faktoren (RGBA) für den Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="a1590-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1590-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1590-129">Remarks</span></span>

<span data-ttu-id="a1590-130">Bibliothek d3dx11 \_ Pass-Debug \_ wird mit [**ID3DX11EffectPass:: getdebug**](id3dx11effectpass-getdesc.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1590-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1590-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a1590-131">Requirements</span></span>



| <span data-ttu-id="a1590-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1590-132">Requirement</span></span> | <span data-ttu-id="a1590-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a1590-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1590-134">Header</span><span class="sxs-lookup"><span data-stu-id="a1590-134">Header</span></span><br/> | <dl> <span data-ttu-id="a1590-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1590-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1590-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1590-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1590-137">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a1590-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

