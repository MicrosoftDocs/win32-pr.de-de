---
title: CD3DX12_SHADER_BYTECODE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Shader- \_ Bytecode-Struktur zu ermöglichen.
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370403"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="f951d-104">CD3DX12 \_ Shader- \_ Bytecode-Struktur</span><span class="sxs-lookup"><span data-stu-id="f951d-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="f951d-105">Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f951d-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f951d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f951d-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="f951d-107">Member</span><span class="sxs-lookup"><span data-stu-id="f951d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f951d-108">**CD3DX12 \_ Shader- \_ Bytecode ()**</span><span class="sxs-lookup"><span data-stu-id="f951d-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="f951d-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Shader- \_ Bytecode.</span><span class="sxs-lookup"><span data-stu-id="f951d-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="f951d-110">**expliziter CD3DX12- \_ Shader- \_ Bytecode (konstant D3D12 \_ Shader- \_ Bytecode &o)**</span><span class="sxs-lookup"><span data-stu-id="f951d-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f951d-111">Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode, der mit dem Inhalt einer anderen [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f951d-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f951d-112">**CD3DX12 \_ Shader- \_ Bytecode (ID3DBlob \* pshaderblob)**</span><span class="sxs-lookup"><span data-stu-id="f951d-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="f951d-113">Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="f951d-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="f951d-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pshaderblob</span><span class="sxs-lookup"><span data-stu-id="f951d-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="f951d-115">**CD3DX12 \_ Shader \_ Bytecode (Konstante void \* \_ pshaderbytecode, size \_ T bytecodelta ength)**</span><span class="sxs-lookup"><span data-stu-id="f951d-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="f951d-116">Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode und initialisiert die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="f951d-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="f951d-117">void \* \_ pshaderbytecode</span><span class="sxs-lookup"><span data-stu-id="f951d-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="f951d-118">Größe \_ T bytecodelta ength</span><span class="sxs-lookup"><span data-stu-id="f951d-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="f951d-119">**Operator Konstanten D3D12 \_ Shader- \_ Bytecode& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f951d-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f951d-120">Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.</span><span class="sxs-lookup"><span data-stu-id="f951d-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f951d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f951d-121">Requirements</span></span>



| <span data-ttu-id="f951d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f951d-122">Requirement</span></span> | <span data-ttu-id="f951d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f951d-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f951d-124">Header</span><span class="sxs-lookup"><span data-stu-id="f951d-124">Header</span></span><br/> | <dl> <span data-ttu-id="f951d-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f951d-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f951d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f951d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f951d-127">**D3D12- \_ Shader- \_ Bytecode**</span><span class="sxs-lookup"><span data-stu-id="f951d-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="f951d-128">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f951d-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

