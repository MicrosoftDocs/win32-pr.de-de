---
title: CD3DX12_ROOT_DESCRIPTOR-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12 \_ - \_ stammdeskriptorstruktur ermöglicht.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- CD3DX12_ROOT_DESCRIPTOR Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357279"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="f633a-104">CD3DX12 \_ - \_ stammdeskriptorstruktur</span><span class="sxs-lookup"><span data-stu-id="f633a-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="f633a-105">Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ - \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f633a-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f633a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f633a-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="f633a-107">Member</span><span class="sxs-lookup"><span data-stu-id="f633a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f633a-108">**CD3DX12-Stamm \_ \_ Deskriptor ()**</span><span class="sxs-lookup"><span data-stu-id="f633a-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="f633a-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Stamm \_ \_ Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="f633a-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="f633a-110">**expliziter CD3DX12-Stamm \_ \_ Deskriptor (konstant D3D12 Stamm \_ \_ Deskriptor &o)**</span><span class="sxs-lookup"><span data-stu-id="f633a-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f633a-111">Erstellt eine neue Instanz eines CD3DX12- \_ Stamm \_ Deskriptors, der mit dem Inhalt einer anderen [**D3D12- \_ \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f633a-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f633a-112">**CD3DX12 \_ root \_ Descriptor (uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f633a-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f633a-113">Erstellt eine neue Instanz eines CD3DX12- \_ Stamm \_ Deskriptors und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="f633a-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="f633a-114">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="f633a-114">UINT shaderRegister</span></span>

<span data-ttu-id="f633a-115">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="f633a-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="f633a-116">**Inline-init (uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f633a-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f633a-117">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="f633a-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f633a-118">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="f633a-118">UINT shaderRegister</span></span>

<span data-ttu-id="f633a-119">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="f633a-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="f633a-120">**static Inline init (D3D12 \_ root \_ Descriptor &Table, uint shaderregister, uint registerspace = 0)**</span><span class="sxs-lookup"><span data-stu-id="f633a-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="f633a-121">Gibt eine Funktion an, die die folgenden Parameter initialisiert:</span><span class="sxs-lookup"><span data-stu-id="f633a-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f633a-122">[**D3D12 \_ Stamm \_ Deskriptor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &Tabelle</span><span class="sxs-lookup"><span data-stu-id="f633a-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="f633a-123">Uint-shaderregister</span><span class="sxs-lookup"><span data-stu-id="f633a-123">UINT shaderRegister</span></span>

<span data-ttu-id="f633a-124">Opt Uint registerspace = 0</span><span class="sxs-lookup"><span data-stu-id="f633a-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f633a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f633a-125">Requirements</span></span>



| <span data-ttu-id="f633a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f633a-126">Requirement</span></span> | <span data-ttu-id="f633a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f633a-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f633a-128">Header</span><span class="sxs-lookup"><span data-stu-id="f633a-128">Header</span></span><br/> | <dl> <span data-ttu-id="f633a-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f633a-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f633a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f633a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f633a-131">**D3D12-Stamm \_ \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="f633a-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="f633a-132">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f633a-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





