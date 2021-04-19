---
description: Legt ein Array von booleschen Werten fest.
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'ID3DXConstantTable:: setboolarray-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367375"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="63911-103">ID3DXConstantTable:: setboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="63911-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="63911-104">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="63911-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="63911-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63911-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="63911-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63911-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63911-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63911-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="63911-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="63911-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="63911-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="63911-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63911-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63911-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="63911-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="63911-112">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="63911-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="63911-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="63911-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="63911-114">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63911-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63911-115">Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="63911-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63911-116">Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="63911-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="63911-117">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63911-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63911-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63911-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63911-119">Anzahl von booleschen Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="63911-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63911-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63911-120">Return value</span></span>

<span data-ttu-id="63911-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63911-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63911-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63911-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63911-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="63911-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="63911-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63911-124">Requirements</span></span>



| <span data-ttu-id="63911-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63911-125">Requirement</span></span> | <span data-ttu-id="63911-126">Wert</span><span class="sxs-lookup"><span data-stu-id="63911-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63911-127">Header</span><span class="sxs-lookup"><span data-stu-id="63911-127">Header</span></span><br/>  | <dl> <span data-ttu-id="63911-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="63911-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="63911-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63911-129">Library</span></span><br/> | <dl> <span data-ttu-id="63911-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63911-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="63911-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63911-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63911-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="63911-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
