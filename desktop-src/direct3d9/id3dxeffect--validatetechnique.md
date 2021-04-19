---
description: Überprüfen Sie eine Technik.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'ID3DXEffect:: validatetechnique-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370413"
---
# <a name="id3dxeffectvalidatetechnique-method"></a><span data-ttu-id="5c81c-103">ID3DXEffect:: validatetechnique-Methode</span><span class="sxs-lookup"><span data-stu-id="5c81c-103">ID3DXEffect::ValidateTechnique method</span></span>

<span data-ttu-id="5c81c-104">Überprüfen Sie eine Technik.</span><span class="sxs-lookup"><span data-stu-id="5c81c-104">Validate a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c81c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c81c-105">Syntax</span></span>


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="5c81c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c81c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c81c-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c81c-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c81c-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5c81c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5c81c-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5c81c-109">Unique identifier.</span></span> <span data-ttu-id="5c81c-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5c81c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c81c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c81c-111">Return value</span></span>

<span data-ttu-id="5c81c-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c81c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c81c-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c81c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5c81c-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ conflictingrenderstate, D3DERR \_ conflictingtexturefilter, D3DERR \_ DeviceLost, D3DERR \_ driverinternalerror, D3DERR \_ toomanyoperations, D3DERR \_ unsupportedalphaarg, D3DERR \_ unsupportedalphaoperation, D3DERR \_ unsupportedcolorarg, D3DERR \_ unsupportedcoloroperation, D3DERR \_ unsupportedfactor Value, D3DERR \_ unsupportedtexturefilter und D3DERR \_ fehlertextureformat.</span><span class="sxs-lookup"><span data-stu-id="5c81c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_CONFLICTINGRENDERSTATE, D3DERR\_CONFLICTINGTEXTUREFILTER, D3DERR\_DEVICELOST, D3DERR\_DRIVERINTERNALERROR, D3DERR\_TOOMANYOPERATIONS, D3DERR\_UNSUPPORTEDALPHAARG, D3DERR\_UNSUPPORTEDALPHAOPERATION, D3DERR\_UNSUPPORTEDCOLORARG, D3DERR\_UNSUPPORTEDCOLOROPERATION, D3DERR\_UNSUPPORTEDFACTORVALUE, D3DERR\_UNSUPPORTEDTEXTUREFILTER, and D3DERR\_WRONGTEXTUREFORMAT.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c81c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c81c-115">Requirements</span></span>



| <span data-ttu-id="5c81c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c81c-116">Requirement</span></span> | <span data-ttu-id="5c81c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5c81c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c81c-118">Header</span><span class="sxs-lookup"><span data-stu-id="5c81c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5c81c-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c81c-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5c81c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c81c-120">Library</span></span><br/> | <dl> <span data-ttu-id="5c81c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c81c-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5c81c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c81c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c81c-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="5c81c-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="5c81c-124">**ID3DXEffect:: settechnique**</span><span class="sxs-lookup"><span data-stu-id="5c81c-124">**ID3DXEffect::SetTechnique**</span></span>](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




