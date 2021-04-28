---
description: 'ID3DXConstantTable::SetVectorArray-Methode: Legt ein Array von 4D-Vektoren fest.'
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: ID3DXConstantTable::SetVectorArray-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: fe93ef7a75cda743399133445a5f6efd34dd5ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115008"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="9bd02-103">ID3DXConstantTable::SetVectorArray-Methode</span><span class="sxs-lookup"><span data-stu-id="9bd02-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="9bd02-104">Legt ein Array von 4D-Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="9bd02-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bd02-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="9bd02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bd02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd02-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9bd02-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd02-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9bd02-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9bd02-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9bd02-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="9bd02-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9bd02-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd02-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd02-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9bd02-112">Eindeutiger Bezeichner für das Array von Vektorkonstanten.</span><span class="sxs-lookup"><span data-stu-id="9bd02-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="9bd02-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9bd02-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bd02-114">*pVector* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9bd02-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd02-115">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="9bd02-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="9bd02-116">Array von 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="9bd02-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="9bd02-117">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9bd02-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd02-118">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd02-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bd02-119">Anzahl der Vektoren im Array.</span><span class="sxs-lookup"><span data-stu-id="9bd02-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bd02-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bd02-120">Return value</span></span>

<span data-ttu-id="9bd02-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bd02-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bd02-122">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9bd02-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9bd02-123">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="9bd02-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd02-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bd02-124">Requirements</span></span>



| <span data-ttu-id="9bd02-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bd02-125">Requirement</span></span> | <span data-ttu-id="9bd02-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9bd02-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd02-127">Header</span><span class="sxs-lookup"><span data-stu-id="9bd02-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9bd02-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="9bd02-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9bd02-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bd02-129">Library</span></span><br/> | <dl> <span data-ttu-id="9bd02-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bd02-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9bd02-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9bd02-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd02-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="9bd02-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
