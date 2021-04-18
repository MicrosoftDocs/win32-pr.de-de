---
description: Legt einen ganzzahligen Wert fest.
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: 'ID3DXConstantTable:: abtint-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0aa0a213f9f4704a5d557db66aaf360f8baa727
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365317"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="7c47c-103">ID3DXConstantTable:: abtint-Methode</span><span class="sxs-lookup"><span data-stu-id="7c47c-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="7c47c-104">Legt einen ganzzahligen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="7c47c-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c47c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c47c-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="7c47c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c47c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c47c-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c47c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c47c-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7c47c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7c47c-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7c47c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7c47c-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c47c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c47c-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c47c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c47c-112">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="7c47c-112">Unique identifier to the constant.</span></span> <span data-ttu-id="7c47c-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c47c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c47c-114">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c47c-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c47c-115">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c47c-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c47c-116">Eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="7c47c-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c47c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c47c-117">Return value</span></span>

<span data-ttu-id="7c47c-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c47c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c47c-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c47c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c47c-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="7c47c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c47c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c47c-121">Requirements</span></span>



| <span data-ttu-id="7c47c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c47c-122">Requirement</span></span> | <span data-ttu-id="7c47c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7c47c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c47c-124">Header</span><span class="sxs-lookup"><span data-stu-id="7c47c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7c47c-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c47c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7c47c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c47c-126">Library</span></span><br/> | <dl> <span data-ttu-id="7c47c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c47c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c47c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c47c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c47c-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7c47c-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
