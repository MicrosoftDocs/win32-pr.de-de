---
description: Legt einen booleschen Wert fest.
ms.assetid: 652e5b68-88f3-4b05-959b-38bb530c546a
title: 'ID3DXConstantTable:: SetBool-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fb38407aeaaf042d8d606c90e075a1891b9557
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762075"
---
# <a name="id3dxconstanttablesetbool-method"></a><span data-ttu-id="c9ce6-103">ID3DXConstantTable:: SetBool-Methode</span><span class="sxs-lookup"><span data-stu-id="c9ce6-103">ID3DXConstantTable::SetBool method</span></span>

<span data-ttu-id="c9ce6-104">Legt einen booleschen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-104">Sets a Boolean value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ce6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9ce6-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] BOOL              b
);
```



## <a name="parameters"></a><span data-ttu-id="c9ce6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9ce6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ce6-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ce6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ce6-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c9ce6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c9ce6-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c9ce6-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ce6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ce6-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c9ce6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c9ce6-112">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-112">Unique identifier to the constant.</span></span> <span data-ttu-id="c9ce6-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c9ce6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9ce6-114">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ce6-114">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ce6-115">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9ce6-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9ce6-116">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-116">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ce6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9ce6-117">Return value</span></span>

<span data-ttu-id="c9ce6-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9ce6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9ce6-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c9ce6-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c9ce6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ce6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9ce6-121">Requirements</span></span>



| <span data-ttu-id="c9ce6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9ce6-122">Requirement</span></span> | <span data-ttu-id="c9ce6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c9ce6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ce6-124">Header</span><span class="sxs-lookup"><span data-stu-id="c9ce6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c9ce6-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ce6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c9ce6-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9ce6-126">Library</span></span><br/> | <dl> <span data-ttu-id="c9ce6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9ce6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c9ce6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9ce6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ce6-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c9ce6-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
