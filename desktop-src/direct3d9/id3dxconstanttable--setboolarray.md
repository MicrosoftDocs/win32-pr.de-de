---
description: 'ID3DXConstantTable::SetBoolArray-Methode: Legt ein Array boolescher Werte fest.'
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: ID3DXConstantTable::SetBoolArray-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c967ffd1a6601144787621628ed1b019e775eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115208"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="68f30-103">ID3DXConstantTable::SetBoolArray-Methode</span><span class="sxs-lookup"><span data-stu-id="68f30-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="68f30-104">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="68f30-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68f30-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="68f30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68f30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f30-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="68f30-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f30-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="68f30-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="68f30-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68f30-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="68f30-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="68f30-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f30-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="68f30-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="68f30-112">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="68f30-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="68f30-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68f30-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="68f30-114">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="68f30-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f30-115">Typ: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="68f30-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68f30-116">Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="68f30-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="68f30-117">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="68f30-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f30-118">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68f30-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68f30-119">Anzahl der booleschen Werte im Array.</span><span class="sxs-lookup"><span data-stu-id="68f30-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f30-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68f30-120">Return value</span></span>

<span data-ttu-id="68f30-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68f30-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68f30-122">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68f30-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68f30-123">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="68f30-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f30-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68f30-124">Requirements</span></span>



| <span data-ttu-id="68f30-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68f30-125">Requirement</span></span> | <span data-ttu-id="68f30-126">Wert</span><span class="sxs-lookup"><span data-stu-id="68f30-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f30-127">Header</span><span class="sxs-lookup"><span data-stu-id="68f30-127">Header</span></span><br/>  | <dl> <span data-ttu-id="68f30-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="68f30-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="68f30-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68f30-129">Library</span></span><br/> | <dl> <span data-ttu-id="68f30-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="68f30-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="68f30-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68f30-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f30-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="68f30-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
