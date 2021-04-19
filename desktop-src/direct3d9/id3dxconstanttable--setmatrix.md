---
description: Legt eine nicht übersetzte Matrix fest.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'ID3DXConstantTable:: setMatrix-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361209"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="55817-103">ID3DXConstantTable:: setMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="55817-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="55817-104">Legt eine nicht übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="55817-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55817-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55817-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="55817-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55817-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55817-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55817-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55817-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="55817-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="55817-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="55817-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="55817-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55817-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55817-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="55817-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="55817-112">Eindeutiger Bezeichner für die Matrix der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="55817-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="55817-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="55817-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="55817-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55817-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55817-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="55817-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="55817-116">Zeiger auf eine nicht umgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="55817-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="55817-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="55817-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55817-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55817-118">Return value</span></span>

<span data-ttu-id="55817-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55817-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55817-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55817-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="55817-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="55817-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="55817-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55817-122">Requirements</span></span>



| <span data-ttu-id="55817-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55817-123">Requirement</span></span> | <span data-ttu-id="55817-124">Wert</span><span class="sxs-lookup"><span data-stu-id="55817-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55817-125">Header</span><span class="sxs-lookup"><span data-stu-id="55817-125">Header</span></span><br/>  | <dl> <span data-ttu-id="55817-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="55817-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="55817-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55817-127">Library</span></span><br/> | <dl> <span data-ttu-id="55817-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55817-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55817-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55817-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55817-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="55817-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
