---
description: 'ID3DXConstantTable::SetFloat-Methode: Legt eine Gleitkommazahl fest.'
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: ID3DXConstantTable::SetFloat-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6589d56e0b9dcf8debe14a7c81f86a4972a73405
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115218"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="764fc-103">ID3DXConstantTable::SetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="764fc-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="764fc-104">Legt eine Gleitkommazahl fest.</span><span class="sxs-lookup"><span data-stu-id="764fc-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="764fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="764fc-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="764fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="764fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764fc-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="764fc-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764fc-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="764fc-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="764fc-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Konstantentabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="764fc-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="764fc-110">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="764fc-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764fc-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="764fc-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="764fc-112">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="764fc-112">Unique identifier to the constant.</span></span> <span data-ttu-id="764fc-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="764fc-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="764fc-114">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="764fc-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764fc-115">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="764fc-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="764fc-116">Gleitkommazahl.</span><span class="sxs-lookup"><span data-stu-id="764fc-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764fc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="764fc-117">Return value</span></span>

<span data-ttu-id="764fc-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="764fc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="764fc-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="764fc-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="764fc-120">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="764fc-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="764fc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="764fc-121">Requirements</span></span>



| <span data-ttu-id="764fc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="764fc-122">Requirement</span></span> | <span data-ttu-id="764fc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="764fc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="764fc-124">Header</span><span class="sxs-lookup"><span data-stu-id="764fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="764fc-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="764fc-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="764fc-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="764fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="764fc-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="764fc-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="764fc-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="764fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764fc-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="764fc-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
