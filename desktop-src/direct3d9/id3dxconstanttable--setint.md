---
description: 'ID3DXConstantTable::SetInt-Methode: Legt einen ganzzahligen Wert fest.'
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: ID3DXConstantTable::SetInt-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: f218a0cd1a0e1858f24ec8cbccb4848c37121086
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115128"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="9a2f3-103">ID3DXConstantTable::SetInt-Methode</span><span class="sxs-lookup"><span data-stu-id="9a2f3-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="9a2f3-104">Legt einen ganzzahligen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a2f3-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="9a2f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a2f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2f3-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9a2f3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2f3-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9a2f3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9a2f3-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="9a2f3-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9a2f3-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2f3-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9a2f3-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9a2f3-112">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-112">Unique identifier to the constant.</span></span> <span data-ttu-id="9a2f3-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a2f3-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a2f3-114">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a2f3-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2f3-115">Typ: **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a2f3-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a2f3-116">Eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2f3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a2f3-117">Return value</span></span>

<span data-ttu-id="9a2f3-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a2f3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a2f3-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9a2f3-120">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="9a2f3-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2f3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a2f3-121">Requirements</span></span>



| <span data-ttu-id="9a2f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a2f3-122">Requirement</span></span> | <span data-ttu-id="9a2f3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9a2f3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2f3-124">Header</span><span class="sxs-lookup"><span data-stu-id="9a2f3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9a2f3-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f3-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9a2f3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a2f3-126">Library</span></span><br/> | <dl> <span data-ttu-id="9a2f3-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f3-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9a2f3-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a2f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2f3-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="9a2f3-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
