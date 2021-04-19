---
title: CD3DX12_ROOT_PARAMETER1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ root \_ PARAMETER1-Struktur zu ermöglichen.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355232"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="094f9-104">CD3DX12 \_ root \_ PARAMETER1-Struktur</span><span class="sxs-lookup"><span data-stu-id="094f9-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="094f9-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="094f9-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="094f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="094f9-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="094f9-107">Member</span><span class="sxs-lookup"><span data-stu-id="094f9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="094f9-108">**CD3DX12 \_ root \_ PARAMETER1 ()**</span><span class="sxs-lookup"><span data-stu-id="094f9-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ root \_ PARAMETER1.</span><span class="sxs-lookup"><span data-stu-id="094f9-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="094f9-110">**explizites CD3DX12 \_ root \_ PARAMETER1 (Konstanten D3D12 \_ root \_ PARAMETER1 &o)**</span><span class="sxs-lookup"><span data-stu-id="094f9-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-111">Erstellt eine neue Instanz eines CD3DX12 \_ root \_ PARAMETER1, das mit dem Inhalt einer anderen [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="094f9-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="094f9-112">**static Inline initasdescriptortable (D3D12 \_ root \_ PARAMETER1 &rootparam, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-113">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-114">[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam</span><span class="sxs-lookup"><span data-stu-id="094f9-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="094f9-115">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="094f9-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="094f9-116">Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pdescriptorranges</span><span class="sxs-lookup"><span data-stu-id="094f9-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="094f9-117">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-118">**statische initas-Inline Konstanten (D3D12 \_ root \_ PARAMETER1 &rootparam, uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-119">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-120">[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam</span><span class="sxs-lookup"><span data-stu-id="094f9-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="094f9-121">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="094f9-121">UINT num32BitValues</span></span>

<span data-ttu-id="094f9-122">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-122">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-123">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-124">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-125">**static Inline initasconstantbufferview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-126">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-127">[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam</span><span class="sxs-lookup"><span data-stu-id="094f9-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="094f9-128">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-128">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-129">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-130">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-131">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-132">**static Inline initasshaderresourceview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-133">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-134">[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam</span><span class="sxs-lookup"><span data-stu-id="094f9-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="094f9-135">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-135">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-136">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-137">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-138">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-139">**static Inline initasunorderedaccessview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-140">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-141">[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam</span><span class="sxs-lookup"><span data-stu-id="094f9-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="094f9-142">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-142">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-143">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-144">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-145">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-146">**Inline initasdescriptortable (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-147">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-148">Uint numdescriptor Ranges</span><span class="sxs-lookup"><span data-stu-id="094f9-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="094f9-149">Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pdescriptorranges</span><span class="sxs-lookup"><span data-stu-id="094f9-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="094f9-150">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-151">**Inline-initas-Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-152">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-153">Uint num32BitValues</span><span class="sxs-lookup"><span data-stu-id="094f9-153">UINT num32BitValues</span></span>

<span data-ttu-id="094f9-154">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-154">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-155">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-156">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-157">**Inline initasconstantbufferview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-158">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-159">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-159">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-160">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-161">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-162">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-163">**Inline initasshaderresourceview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-164">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-165">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-165">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-166">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-167">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-168">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="094f9-169">**Inline initasunorderedaccessview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**</span><span class="sxs-lookup"><span data-stu-id="094f9-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="094f9-170">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="094f9-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="094f9-171">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="094f9-171">UINT shaderRegister</span></span>

<span data-ttu-id="094f9-172">Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="094f9-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="094f9-173">[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="094f9-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="094f9-174">[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="094f9-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="094f9-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="094f9-175">Requirements</span></span>



| <span data-ttu-id="094f9-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="094f9-176">Requirement</span></span> | <span data-ttu-id="094f9-177">Wert</span><span class="sxs-lookup"><span data-stu-id="094f9-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="094f9-178">Header</span><span class="sxs-lookup"><span data-stu-id="094f9-178">Header</span></span><br/> | <dl> <span data-ttu-id="094f9-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="094f9-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094f9-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="094f9-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094f9-181">**D3D12 \_ root \_ PARAMETER1**</span><span class="sxs-lookup"><span data-stu-id="094f9-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="094f9-182">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="094f9-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





