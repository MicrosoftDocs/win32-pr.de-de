---
description: Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: D3DXCheckVersion-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366660"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="8398e-103">D3DXCheckVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="8398e-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="8398e-104">Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="8398e-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="8398e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8398e-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="8398e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8398e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8398e-107">*D3DSDKVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8398e-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8398e-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8398e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8398e-109">Verwenden Sie die D3D \_ SDK- \_ Version.</span><span class="sxs-lookup"><span data-stu-id="8398e-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="8398e-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="8398e-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8398e-111">*D3DXSDKVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8398e-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8398e-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8398e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8398e-113">Verwenden Sie die D3DX \_ SDK- \_ Version.</span><span class="sxs-lookup"><span data-stu-id="8398e-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="8398e-114">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="8398e-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8398e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8398e-115">Return value</span></span>

<span data-ttu-id="8398e-116">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8398e-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8398e-117">Gibt **true** zurück, wenn die Version von D3DX, die Sie für kompiliert haben, die Version ist, mit der Sie ausführen. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8398e-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="8398e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8398e-118">Remarks</span></span>

<span data-ttu-id="8398e-119">Verwenden Sie diese Funktion während der Initialisierung der Anwendung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8398e-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="8398e-120">Verwenden Sie [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) , um zu überprüfen, ob die richtige Laufzeit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8398e-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8398e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8398e-121">Requirements</span></span>



| <span data-ttu-id="8398e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8398e-122">Requirement</span></span> | <span data-ttu-id="8398e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8398e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8398e-124">Header</span><span class="sxs-lookup"><span data-stu-id="8398e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8398e-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8398e-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8398e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8398e-126">Library</span></span><br/> | <dl> <span data-ttu-id="8398e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8398e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8398e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8398e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8398e-129">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="8398e-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
