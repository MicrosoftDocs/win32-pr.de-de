---
description: Ruft eine Beschreibung des Parameters oder einer Anmerkung ab.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect:: getparameterdesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367491"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="22b74-103">ID3DXBaseEffect:: getparameterdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="22b74-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="22b74-104">Ruft eine Beschreibung des Parameters oder einer Anmerkung ab.</span><span class="sxs-lookup"><span data-stu-id="22b74-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b74-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="22b74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b74-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22b74-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b74-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22b74-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22b74-109">Parameter-oder Anmerkung-handle.</span><span class="sxs-lookup"><span data-stu-id="22b74-109">Parameter or annotation handle.</span></span> <span data-ttu-id="22b74-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="22b74-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="22b74-111">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22b74-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b74-112">Typ: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="22b74-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="22b74-113">Gibt eine Beschreibung des angegebenen Parameters oder der angegebenen Anmerkung zurück.</span><span class="sxs-lookup"><span data-stu-id="22b74-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="22b74-114">Weitere Informationen finden Sie unter [**D3DXPARAMETER \_**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="22b74-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b74-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22b74-115">Return value</span></span>

<span data-ttu-id="22b74-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22b74-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22b74-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22b74-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="22b74-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="22b74-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b74-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b74-119">Requirements</span></span>



| <span data-ttu-id="22b74-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b74-120">Requirement</span></span> | <span data-ttu-id="22b74-121">Wert</span><span class="sxs-lookup"><span data-stu-id="22b74-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b74-122">Header</span><span class="sxs-lookup"><span data-stu-id="22b74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="22b74-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b74-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="22b74-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22b74-124">Library</span></span><br/> | <dl> <span data-ttu-id="22b74-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b74-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22b74-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b74-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="22b74-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




