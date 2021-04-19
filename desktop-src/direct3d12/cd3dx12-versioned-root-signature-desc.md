---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer mit D3D12 \_ versionierten Stamm \_ \_ Signatur- \_ DESC-Struktur ermöglicht wird.
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366618"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="90905-104">CD3DX12-Struktur der Stamm \_ \_ \_ Signatur \_ DESC</span><span class="sxs-lookup"><span data-stu-id="90905-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="90905-105">Eine hilfsstruktur, mit der die einfache Initialisierung einer mit [**D3D12 \_ versionierten Stamm \_ Signatur- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) -Struktur ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="90905-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="90905-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90905-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="90905-107">Member</span><span class="sxs-lookup"><span data-stu-id="90905-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="90905-108">**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="90905-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="90905-109">Erstellt eine neue, nicht initialisierte Instanz einer Stamm \_ \_ \_ Signatur DESC mit CD3DX12 Versionierung \_ .</span><span class="sxs-lookup"><span data-stu-id="90905-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="90905-110">**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="90905-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-111">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer mit [**D3D12 \_ versionierten Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="90905-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90905-112">**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="90905-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-113">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer D3D12-Stamm [**\_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="90905-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90905-114">**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="90905-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-115">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer [**D3D12 \_ root \_ Signature \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="90905-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90905-116">**CD3DX12-Stamm \_ \_ \_ Signatur \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-117">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="90905-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="90905-118">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-118">UINT numParameters</span></span>

<span data-ttu-id="90905-119">Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter</span><span class="sxs-lookup"><span data-stu-id="90905-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="90905-120">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-121">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-122">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-123">**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-124">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="90905-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="90905-125">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-125">UINT numParameters</span></span>

<span data-ttu-id="90905-126">Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters</span><span class="sxs-lookup"><span data-stu-id="90905-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="90905-127">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-128">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-129">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-130">**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC (CD3DX12 \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="90905-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-131">Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit den Standardparametern initialisiert wird:</span><span class="sxs-lookup"><span data-stu-id="90905-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="90905-132">Uint numparameters = 0</span><span class="sxs-lookup"><span data-stu-id="90905-132">UINT numParameters = 0</span></span>

<span data-ttu-id="90905-133">Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="90905-134">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-135">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-136">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-137">**Inline-init \_ 1 \_ 0 (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-138">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="90905-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="90905-139">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-139">UINT numParameters</span></span>

<span data-ttu-id="90905-140">Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter</span><span class="sxs-lookup"><span data-stu-id="90905-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="90905-141">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-142">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-143">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-144">**static Inline init \_ 1 \_ 0 (D3D12 mit Versions Angabe Stamm \_ \_ \_ Signatur \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-145">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="90905-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="90905-146">[**D3D12 \_ \_ \_ \_ DESC mit Versions**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) Angabe für Stamm Signatur &DESC</span><span class="sxs-lookup"><span data-stu-id="90905-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="90905-147">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-147">UINT numParameters</span></span>

<span data-ttu-id="90905-148">Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter</span><span class="sxs-lookup"><span data-stu-id="90905-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="90905-149">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-150">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-151">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-152">**Inline-init \_ 1 \_ 1 (uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-153">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="90905-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="90905-154">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-154">UINT numParameters</span></span>

<span data-ttu-id="90905-155">Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters</span><span class="sxs-lookup"><span data-stu-id="90905-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="90905-156">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-157">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-158">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="90905-159">**static Inline init \_ 1 \_ 1 (D3D12 mit Versions Angabe Stamm \_ \_ \_ Signatur \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="90905-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="90905-160">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="90905-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="90905-161">[**D3D12 \_ \_ \_ \_ DESC mit Versions**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) Angabe für Stamm Signatur &DESC</span><span class="sxs-lookup"><span data-stu-id="90905-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="90905-162">Uint numparameters</span><span class="sxs-lookup"><span data-stu-id="90905-162">UINT numParameters</span></span>

<span data-ttu-id="90905-163">Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters</span><span class="sxs-lookup"><span data-stu-id="90905-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="90905-164">Uint numstaticsamplers = 0</span><span class="sxs-lookup"><span data-stu-id="90905-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="90905-165">Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="90905-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="90905-166">[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None</span><span class="sxs-lookup"><span data-stu-id="90905-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90905-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90905-167">Requirements</span></span>



| <span data-ttu-id="90905-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90905-168">Requirement</span></span> | <span data-ttu-id="90905-169">Wert</span><span class="sxs-lookup"><span data-stu-id="90905-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90905-170">Header</span><span class="sxs-lookup"><span data-stu-id="90905-170">Header</span></span><br/> | <dl> <span data-ttu-id="90905-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="90905-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90905-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90905-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90905-173">**D3D12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="90905-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="90905-174">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="90905-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





