---
description: Ruft das Handle eines Pass-ab.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect:: getpass-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394250"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="002a0-103">ID3DXBaseEffect:: getpass-Methode</span><span class="sxs-lookup"><span data-stu-id="002a0-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="002a0-104">Ruft das Handle eines Pass-ab.</span><span class="sxs-lookup"><span data-stu-id="002a0-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="002a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="002a0-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="002a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="002a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002a0-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="002a0-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002a0-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="002a0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="002a0-109">Handle des übergeordneten Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="002a0-109">Handle of the parent technique.</span></span> <span data-ttu-id="002a0-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="002a0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="002a0-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="002a0-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002a0-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="002a0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="002a0-113">Der Index für den Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="002a0-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002a0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="002a0-114">Return value</span></span>

<span data-ttu-id="002a0-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="002a0-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="002a0-116">Gibt das Handle des angegebenen Durchlauf innerhalb der angegebenen Technik zurück, oder **null** , wenn der Index ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="002a0-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="002a0-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="002a0-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="002a0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="002a0-118">Requirements</span></span>



| <span data-ttu-id="002a0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="002a0-119">Requirement</span></span> | <span data-ttu-id="002a0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="002a0-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="002a0-121">Header</span><span class="sxs-lookup"><span data-stu-id="002a0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="002a0-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="002a0-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="002a0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="002a0-123">Library</span></span><br/> | <dl> <span data-ttu-id="002a0-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="002a0-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="002a0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="002a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002a0-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="002a0-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
