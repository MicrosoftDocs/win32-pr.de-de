---
title: CD3DX12_ROOT_PARAMETER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12-Stamm \_ \_ Parameter Struktur ermöglicht.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- CD3DX12_ROOT_PARAMETER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357220"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="034e4-104">CD3DX12-Stamm \_ \_ Parameter Struktur</span><span class="sxs-lookup"><span data-stu-id="034e4-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="034e4-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="034e4-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="034e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="034e4-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="034e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="034e4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="034e4-108">**CD3DX12 \_ root- \_ Parameter ()**</span><span class="sxs-lookup"><span data-stu-id="034e4-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 root- \_ \_ Parameters.</span><span class="sxs-lookup"><span data-stu-id="034e4-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="034e4-110">**expliziter CD3DX12 \_ root- \_ Parameter (Konstanten D3D12 \_ root- \_ Parameter &o)**</span><span class="sxs-lookup"><span data-stu-id="034e4-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-111">Erstellt eine neue Instanz eines CD3DX12 \_ root- \_ Parameters, der mit dem Inhalt einer anderen [**D3D12-Stamm \_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="034e4-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="034e4-112">**static Inline initasdescriptortable (D3D12 \_ root \_ Parameter &rootparam, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Range \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-113">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-114">[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam</span><span class="sxs-lookup"><span data-stu-id="034e4-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="034e4-115">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="034e4-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="034e4-116">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* pdescriptorranges"</span><span class="sxs-lookup"><span data-stu-id="034e4-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="034e4-117">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-118">**statische initas-Inline Konstanten (D3D12 \_ root \_ Parameter &rootparam, uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-119">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-120">[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam</span><span class="sxs-lookup"><span data-stu-id="034e4-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="034e4-121">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="034e4-121">UINT num32BitValues</span></span>

<span data-ttu-id="034e4-122">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-122">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-123">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-124">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-125">**static Inline initasconstantbufferview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-126">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-127">[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam</span><span class="sxs-lookup"><span data-stu-id="034e4-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="034e4-128">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-128">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-129">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-130">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-131">**static Inline initasshaderresourceview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-132">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-133">[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam</span><span class="sxs-lookup"><span data-stu-id="034e4-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="034e4-134">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-134">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-135">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-136">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-137">**static Inline initasunorderedaccessview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-138">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-139">[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam</span><span class="sxs-lookup"><span data-stu-id="034e4-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="034e4-140">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-140">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-141">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-142">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-143">**Inline initasdescriptortable (uint numdescriptorranges, Konstanten D3D12 \_ \_ Deskriptorbereich \* pdescriptorranges, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-144">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-145">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="034e4-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="034e4-146">[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* pdescriptorranges"</span><span class="sxs-lookup"><span data-stu-id="034e4-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="034e4-147">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-148">**Inline-initas-Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-149">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-150">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="034e4-150">UINT num32BitValues</span></span>

<span data-ttu-id="034e4-151">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-151">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-152">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-153">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-154">**Inline initasconstantbufferview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-155">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-156">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-156">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-157">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-158">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-159">**Inline initasshaderresourceview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-160">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-161">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-161">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-162">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-163">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="034e4-164">**Inline initasunorderedaccessview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="034e4-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="034e4-165">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="034e4-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="034e4-166">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="034e4-166">UINT shaderRegister</span></span>

<span data-ttu-id="034e4-167">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="034e4-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="034e4-168">Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="034e4-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="034e4-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="034e4-169">Requirements</span></span>



| <span data-ttu-id="034e4-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="034e4-170">Requirement</span></span> | <span data-ttu-id="034e4-171">Wert</span><span class="sxs-lookup"><span data-stu-id="034e4-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="034e4-172">Header</span><span class="sxs-lookup"><span data-stu-id="034e4-172">Header</span></span><br/> | <dl> <span data-ttu-id="034e4-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="034e4-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034e4-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="034e4-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034e4-175">**D3D12 \_ root- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="034e4-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="034e4-176">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="034e4-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





