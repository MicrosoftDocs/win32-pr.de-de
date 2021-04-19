---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ CPU- \_ Deskriptorhandle-Struktur zu ermöglichen \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- CD3DX12_CPU_DESCRIPTOR_HANDLE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350666"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a><span data-ttu-id="2b46c-104">CD3DX12- \_ CPU- \_ \_ Deskriptorhandle-Struktur</span><span class="sxs-lookup"><span data-stu-id="2b46c-104">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="2b46c-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2b46c-105">A helper structure to enable easy initialization of a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b46c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b46c-106">Syntax</span></span>


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="2b46c-107">Member</span><span class="sxs-lookup"><span data-stu-id="2b46c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b46c-108">**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle ()**</span><span class="sxs-lookup"><span data-stu-id="2b46c-108">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ CPU- \_ \_ Deskriptorhandles.</span><span class="sxs-lookup"><span data-stu-id="2b46c-109">Creates a new, uninitialized, instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-110">**explizites CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (konstant D3D12 \_ CPU- \_ \_ Deskriptorhandle &o)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-110">**explicit CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-111">Erstellt eine neue Instanz eines CD3DX12- \_ CPU- \_ \_ Deskriptorhandles, das mit dem Inhalt einer anderen [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2b46c-111">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-112">**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (CD3DX12 \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-112">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-113">Erstellt eine neue Instanz eines CD3DX12- \_ CPU- \_ \_ Deskriptorhandles, das mit Standardparametern initialisiert wird (Zeiger auf NULL festgelegt).</span><span class="sxs-lookup"><span data-stu-id="2b46c-113">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (pointer set to zero).</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-114">**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (konstant D3D12 \_ CPU- \_ Deskriptorhandle \_ &Sonstiges, int offsetscaledbyincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-114">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-115">Erstellt eine neue Instanz eines CD3DX12- \_ CPU- \_ \_ Deskriptorhandles und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-115">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="2b46c-116">D3D12- \_ CPU- \_ \_ Deskriptorhandle &anderer</span><span class="sxs-lookup"><span data-stu-id="2b46c-116">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="2b46c-117">INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2b46c-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-118">**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (const D3D12 \_ CPU- \_ Deskriptorhandle \_ &Sonstiges, int offsetindescriptors, uint descriptorincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-118">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-119">Erstellt eine neue Instanz eines CD3DX12- \_ CPU- \_ \_ Deskriptorhandles und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-119">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="2b46c-120">D3D12- \_ CPU- \_ \_ Deskriptorhandle &anderer</span><span class="sxs-lookup"><span data-stu-id="2b46c-120">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="2b46c-121">INT offsetindescriptors: die Anzahl der Deskriptoren, um die Inkrement erhöht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="2b46c-122">Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.</span><span class="sxs-lookup"><span data-stu-id="2b46c-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-123">**Offset (int offsetindescriptors, uint descriptorincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-124">Legt den Offset basierend auf der angegebenen Anzahl von Deskriptoren und dem für jeden Deskriptor zu Inkrement enden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="2b46c-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="2b46c-125">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-125">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-126">INT offsetindescriptors: die Anzahl der Deskriptoren, um die Inkrement erhöht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="2b46c-127">Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.</span><span class="sxs-lookup"><span data-stu-id="2b46c-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-128">**Offset (int offsetscaledbyincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-129">Legt den Offset basierend auf der angegebenen Anzahl von Inkrementen fest.</span><span class="sxs-lookup"><span data-stu-id="2b46c-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="2b46c-130">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-130">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-131">INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2b46c-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-132">**Operator = = ( \_ in \_ Konstanten D3D12 \_ CPU- \_ \_ Deskriptorhandle& anderen) Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2b46c-132">**operator==( \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-133">Testet auf Gleichheit zwischen dem aktuellen CD3DX12 \_ \_ -CPU-Deskriptorhandle \_ und dem angegebenen D3D12-CPU-Deskriptorhandle \_ \_ \_ oder CD3DX12-CPU- \_ \_ Deskriptorhandle \_ .</span><span class="sxs-lookup"><span data-stu-id="2b46c-133">Tests for equality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-134">**Operator! = ( \_ in \_ Konstanten D3D12 \_ CPU- \_ \_ Deskriptorhandle& anderen) Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2b46c-134">**operator!=(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-135">Prüft auf Ungleichheit zwischen dem aktuellen CD3DX12 \_ \_ -CPU-Deskriptorhandle \_ und dem angegebenen D3D12-CPU-Deskriptorhandle \_ \_ \_ oder CD3DX12-CPU- \_ \_ Deskriptorhandle \_ .</span><span class="sxs-lookup"><span data-stu-id="2b46c-135">Tests for inequality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-136">**Operator = (konstant D3D12 \_ CPU- \_ \_ Deskriptorhandle &andere)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-136">**operator=(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-137">Legt das aktuelle CD3DX12- \_ CPU- \_ \_ Deskriptorhandle auf die gleichen Werte wie das angegebene D3D12- \_ CPU- \_ \_ Deskriptorhandle oder CD3DX12- \_ CPU- \_ Deskriptorhandle fest \_ .</span><span class="sxs-lookup"><span data-stu-id="2b46c-137">Sets the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-138">**Inline-initoffsetted ( \_ in \_ Konstanten D3D12 \_ CPU- \_ Deskriptorhandle \_ &Basis, int offsetscaledbyincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-138">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-139">Initialisiert eine [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur mit der angegebenen Anzahl von Elementen.</span><span class="sxs-lookup"><span data-stu-id="2b46c-139">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="2b46c-140">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-140">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-141">\_Im \_ Konstanten D3D12- \_ CPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-141">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="2b46c-142">INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2b46c-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-143">**Inline-initoffsetted ( \_ in \_ const D3D12 \_ CPU- \_ Deskriptorhandle \_ &Base, int offsetindescriptors, uint descriptorincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-143">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-144">Initialisiert eine [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe.</span><span class="sxs-lookup"><span data-stu-id="2b46c-144">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="2b46c-145">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-145">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-146">\_Im \_ Konstanten D3D12- \_ CPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-146">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="2b46c-147">INT offsetindescriptors: die Anzahl der Deskriptoren, nach denen versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="2b46c-148">Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.</span><span class="sxs-lookup"><span data-stu-id="2b46c-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-149">**statischer Inline-initoffsetted ( \_ out \_ D3D12 \_ CPU- \_ \_ Deskriptorhandle &handle, \_ in \_ konstant D3D12 \_ CPU- \_ \_ Deskriptorhandle &Base, int offsetscaledbyincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-149">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-150">Initialisiert eine [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe.</span><span class="sxs-lookup"><span data-stu-id="2b46c-150">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="2b46c-151">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-151">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-152">\_Out \_ D3D12 \_ CPU- \_ \_ Deskriptorhandle &handle: gibt das resultierende D3D12- \_ CPU- \_ \_ Deskriptorhandle aus.</span><span class="sxs-lookup"><span data-stu-id="2b46c-152">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="2b46c-153">\_Im \_ Konstanten D3D12- \_ CPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-153">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="2b46c-154">INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2b46c-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="2b46c-155">**statischer Inline-initoffsetted ( \_ out \_ D3D12 \_ CPU- \_ \_ Deskriptorhandle &handle, \_ in \_ const D3D12 \_ CPU- \_ \_ Deskriptorhandle &Base, int offsetindescriptors, uint descriptorincrementsize)**</span><span class="sxs-lookup"><span data-stu-id="2b46c-155">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="2b46c-156">Initialisiert eine [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe.</span><span class="sxs-lookup"><span data-stu-id="2b46c-156">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="2b46c-157">Verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2b46c-157">Uses the following parameters:</span></span>

<span data-ttu-id="2b46c-158">\_Out \_ D3D12 \_ CPU- \_ \_ Deskriptorhandle &handle: gibt das resultierende D3D12- \_ CPU- \_ \_ Deskriptorhandle aus.</span><span class="sxs-lookup"><span data-stu-id="2b46c-158">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="2b46c-159">\_Im \_ Konstanten D3D12- \_ CPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-159">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="2b46c-160">INT offsetindescriptors: die Anzahl der Deskriptoren, nach denen versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b46c-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="2b46c-161">Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.</span><span class="sxs-lookup"><span data-stu-id="2b46c-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b46c-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b46c-162">Requirements</span></span>



| <span data-ttu-id="2b46c-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b46c-163">Requirement</span></span> | <span data-ttu-id="2b46c-164">Wert</span><span class="sxs-lookup"><span data-stu-id="2b46c-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b46c-165">Header</span><span class="sxs-lookup"><span data-stu-id="2b46c-165">Header</span></span><br/> | <dl> <span data-ttu-id="2b46c-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b46c-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b46c-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b46c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b46c-168">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="2b46c-168">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





