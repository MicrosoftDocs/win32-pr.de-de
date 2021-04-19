---
description: Legt ein Array von 4D-Vektoren fest.
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'ID3DXConstantTable:: setvectorarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361869"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="2eb70-103">ID3DXConstantTable:: setvectorarray-Methode</span><span class="sxs-lookup"><span data-stu-id="2eb70-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="2eb70-104">Legt ein Array von 4D-Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="2eb70-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eb70-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="2eb70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eb70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb70-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eb70-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb70-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2eb70-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2eb70-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2eb70-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2eb70-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eb70-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb70-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2eb70-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2eb70-112">Eindeutiger Bezeichner für das Array von Vektor Konstanten.</span><span class="sxs-lookup"><span data-stu-id="2eb70-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="2eb70-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2eb70-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eb70-114">*pvector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eb70-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb70-115">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2eb70-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2eb70-116">Array von 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="2eb70-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="2eb70-117">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eb70-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb70-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eb70-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2eb70-119">Anzahl der Vektoren im Array.</span><span class="sxs-lookup"><span data-stu-id="2eb70-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb70-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2eb70-120">Return value</span></span>

<span data-ttu-id="2eb70-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2eb70-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2eb70-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2eb70-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2eb70-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="2eb70-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb70-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2eb70-124">Requirements</span></span>



| <span data-ttu-id="2eb70-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2eb70-125">Requirement</span></span> | <span data-ttu-id="2eb70-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2eb70-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb70-127">Header</span><span class="sxs-lookup"><span data-stu-id="2eb70-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2eb70-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb70-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2eb70-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2eb70-129">Library</span></span><br/> | <dl> <span data-ttu-id="2eb70-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eb70-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2eb70-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eb70-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb70-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2eb70-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
