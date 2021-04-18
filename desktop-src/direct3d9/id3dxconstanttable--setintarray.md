---
description: Legt ein Array von ganzen Zahlen fest.
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'ID3DXConstantTable:: tartintarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351955"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="d1952-103">ID3DXConstantTable:: tartintarray-Methode</span><span class="sxs-lookup"><span data-stu-id="d1952-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="d1952-104">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="d1952-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1952-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1952-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="d1952-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1952-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1952-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1952-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1952-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d1952-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d1952-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d1952-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d1952-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1952-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1952-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d1952-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d1952-112">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="d1952-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="d1952-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d1952-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1952-114">*PN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1952-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1952-115">Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1952-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1952-116">Array von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="d1952-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="d1952-117">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1952-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1952-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1952-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1952-119">Anzahl von ganzen Zahlen im Array.</span><span class="sxs-lookup"><span data-stu-id="d1952-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1952-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1952-120">Return value</span></span>

<span data-ttu-id="d1952-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1952-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1952-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1952-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1952-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="d1952-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1952-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1952-124">Requirements</span></span>



| <span data-ttu-id="d1952-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1952-125">Requirement</span></span> | <span data-ttu-id="d1952-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d1952-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1952-127">Header</span><span class="sxs-lookup"><span data-stu-id="d1952-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d1952-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1952-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d1952-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1952-129">Library</span></span><br/> | <dl> <span data-ttu-id="d1952-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1952-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d1952-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1952-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1952-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d1952-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
