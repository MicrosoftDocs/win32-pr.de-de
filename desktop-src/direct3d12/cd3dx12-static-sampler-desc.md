---
title: CD3DX12_STATIC_SAMPLER_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ static- \_ Sampler- \_ DESC-Struktur zu ermöglichen.
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361841"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="5c8d1-104">CD3DX12 \_ statische \_ Sampler- \_ decoderstruktur</span><span class="sxs-lookup"><span data-stu-id="5c8d1-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="5c8d1-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ static- \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8d1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c8d1-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="5c8d1-107">Member</span><span class="sxs-lookup"><span data-stu-id="5c8d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c8d1-108">**CD3DX12 \_ statischer \_ Sampler- \_ Decoder ()**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ static Sampler- \_ Objekts \_ .</span><span class="sxs-lookup"><span data-stu-id="5c8d1-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="5c8d1-110">**expliziter CD3DX12 \_ statischer Sampler-Debug \_ \_ (konstant D3D12 \_ statischer \_ Sampler- \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-111">Erstellt eine neue Instanz eines CD3DX12 \_ static Sampler-Objekts \_ \_ , das mit dem Inhalt einer anderen [**D3D12 \_ static \_ Sampler \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -Debug-Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c8d1-112">**CD3DX12 \_ statischer \_ Sampler- \_ DESC (uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture \_ Address Mode \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode \_ addressssv = D3D12 Texture Address Mode \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-113">Erstellt eine neue Instanz eines CD3DX12 \_ static \_ Sampler \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="5c8d1-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5c8d1-114">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5c8d1-114">UINT shaderRegister</span></span>

<span data-ttu-id="5c8d1-115">Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="5c8d1-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="5c8d1-116">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-117">Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-118">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-119">Opt FLOAT miplodbias = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="5c8d1-120">Opt Uint MaxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="5c8d1-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="5c8d1-121">Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich</span><span class="sxs-lookup"><span data-stu-id="5c8d1-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="5c8d1-122">Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß</span><span class="sxs-lookup"><span data-stu-id="5c8d1-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="5c8d1-123">Opt FLOAT minlod = 0. f</span><span class="sxs-lookup"><span data-stu-id="5c8d1-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="5c8d1-124">Opt FLOAT maxlod = D3D12 \_ float32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="5c8d1-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="5c8d1-125">Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="5c8d1-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="5c8d1-126">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="5c8d1-127">**static Inline init (D3D12 \_ static \_ Sampler \_ &samplerdebug, uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture \_ Address Mode \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode addressssv = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-128">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="5c8d1-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5c8d1-129">[**D3D12 \_ Statischer \_ Sampler \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -&samplerdebug</span><span class="sxs-lookup"><span data-stu-id="5c8d1-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="5c8d1-130">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5c8d1-130">UINT shaderRegister</span></span>

<span data-ttu-id="5c8d1-131">Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="5c8d1-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="5c8d1-132">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-133">Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-134">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-135">Opt FLOAT miplodbias = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="5c8d1-136">Opt Uint MaxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="5c8d1-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="5c8d1-137">Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich</span><span class="sxs-lookup"><span data-stu-id="5c8d1-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="5c8d1-138">Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß</span><span class="sxs-lookup"><span data-stu-id="5c8d1-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="5c8d1-139">Opt FLOAT minlod = 0. f</span><span class="sxs-lookup"><span data-stu-id="5c8d1-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="5c8d1-140">Opt FLOAT maxlod = D3D12 \_ float32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="5c8d1-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="5c8d1-141">Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="5c8d1-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="5c8d1-142">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="5c8d1-143">**Inline-init (uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture Address Mode \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode addressssv = D3D12 Texture Address Modus \_ \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-144">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="5c8d1-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5c8d1-145">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="5c8d1-145">UINT shaderRegister</span></span>

<span data-ttu-id="5c8d1-146">Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="5c8d1-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="5c8d1-147">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-148">Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-149">Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="5c8d1-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="5c8d1-150">Opt FLOAT miplodbias = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="5c8d1-151">Opt Uint MaxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="5c8d1-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="5c8d1-152">Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich</span><span class="sxs-lookup"><span data-stu-id="5c8d1-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="5c8d1-153">Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß</span><span class="sxs-lookup"><span data-stu-id="5c8d1-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="5c8d1-154">Opt FLOAT minlod = 0. f</span><span class="sxs-lookup"><span data-stu-id="5c8d1-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="5c8d1-155">Opt FLOAT maxlod = D3D12 \_ float32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="5c8d1-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="5c8d1-156">Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all</span><span class="sxs-lookup"><span data-stu-id="5c8d1-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="5c8d1-157">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="5c8d1-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c8d1-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c8d1-158">Requirements</span></span>



| <span data-ttu-id="5c8d1-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c8d1-159">Requirement</span></span> | <span data-ttu-id="5c8d1-160">Wert</span><span class="sxs-lookup"><span data-stu-id="5c8d1-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8d1-161">Header</span><span class="sxs-lookup"><span data-stu-id="5c8d1-161">Header</span></span><br/> | <dl> <span data-ttu-id="5c8d1-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8d1-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8d1-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c8d1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8d1-164">**D3D12 \_ statischer \_ Sampler- \_ Decoder**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="5c8d1-165">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="5c8d1-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





