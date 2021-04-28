---
description: 'ID3DXConstantTable::SetVector-Methode: Legt einen 4D-Vektor fest.'
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: ID3DXConstantTable::SetVector-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d7c464cebb050b9fd54c27656505e6f2221fe4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115018"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="ad848-103">ID3DXConstantTable::SetVector-Methode</span><span class="sxs-lookup"><span data-stu-id="ad848-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="ad848-104">Legt einen 4D-Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="ad848-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad848-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad848-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="ad848-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad848-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad848-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad848-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad848-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ad848-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ad848-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ad848-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ad848-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad848-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad848-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ad848-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ad848-112">Eindeutiger Bezeichner für die Vektorkonst constant.</span><span class="sxs-lookup"><span data-stu-id="ad848-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="ad848-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ad848-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad848-114">*pVector* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad848-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad848-115">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad848-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ad848-116">Zeiger auf einen 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ad848-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad848-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad848-117">Return value</span></span>

<span data-ttu-id="ad848-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad848-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad848-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad848-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad848-120">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="ad848-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad848-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad848-121">Requirements</span></span>



| <span data-ttu-id="ad848-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad848-122">Requirement</span></span> | <span data-ttu-id="ad848-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ad848-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad848-124">Header</span><span class="sxs-lookup"><span data-stu-id="ad848-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ad848-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad848-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ad848-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad848-126">Library</span></span><br/> | <dl> <span data-ttu-id="ad848-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad848-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ad848-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad848-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad848-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ad848-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
