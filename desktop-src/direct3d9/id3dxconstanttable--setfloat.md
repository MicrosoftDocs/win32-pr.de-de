---
description: Legt eine Gleit Komma Zahl fest.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'ID3DXConstantTable:: SetFloat-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353369"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="ed7ca-103">ID3DXConstantTable:: SetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="ed7ca-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="ed7ca-104">Legt eine Gleit Komma Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7ca-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="ed7ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed7ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed7ca-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed7ca-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed7ca-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ed7ca-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ed7ca-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Konstanten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ed7ca-110">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed7ca-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed7ca-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ed7ca-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ed7ca-112">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-112">Unique identifier to the constant.</span></span> <span data-ttu-id="ed7ca-113">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ed7ca-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed7ca-114">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed7ca-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed7ca-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed7ca-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed7ca-116">Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed7ca-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed7ca-117">Return value</span></span>

<span data-ttu-id="ed7ca-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed7ca-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed7ca-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed7ca-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ed7ca-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7ca-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed7ca-121">Requirements</span></span>



| <span data-ttu-id="ed7ca-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed7ca-122">Requirement</span></span> | <span data-ttu-id="ed7ca-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ed7ca-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7ca-124">Header</span><span class="sxs-lookup"><span data-stu-id="ed7ca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ed7ca-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ca-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ed7ca-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed7ca-126">Library</span></span><br/> | <dl> <span data-ttu-id="ed7ca-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed7ca-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed7ca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed7ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7ca-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ed7ca-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
