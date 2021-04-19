---
description: Ruft eine Funktionsbeschreibung ab.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect:: getfunctiondesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360240"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="dca86-103">ID3DXBaseEffect:: getfunctiondesc-Methode</span><span class="sxs-lookup"><span data-stu-id="dca86-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="dca86-104">Ruft eine Funktionsbeschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="dca86-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dca86-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="dca86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dca86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca86-107">*hfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dca86-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca86-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dca86-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dca86-109">Funktions handle.</span><span class="sxs-lookup"><span data-stu-id="dca86-109">Function handle.</span></span> <span data-ttu-id="dca86-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dca86-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dca86-111">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dca86-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dca86-112">Typ: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="dca86-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="dca86-113">Gibt eine Beschreibung der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="dca86-113">Returns a description of the function.</span></span> <span data-ttu-id="dca86-114">Weitere Informationen finden Sie unter [**D3DXFUNCTION \_**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="dca86-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca86-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dca86-115">Return value</span></span>

<span data-ttu-id="dca86-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dca86-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dca86-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dca86-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dca86-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="dca86-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca86-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dca86-119">Requirements</span></span>



| <span data-ttu-id="dca86-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dca86-120">Requirement</span></span> | <span data-ttu-id="dca86-121">Wert</span><span class="sxs-lookup"><span data-stu-id="dca86-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca86-122">Header</span><span class="sxs-lookup"><span data-stu-id="dca86-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dca86-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dca86-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dca86-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dca86-124">Library</span></span><br/> | <dl> <span data-ttu-id="dca86-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dca86-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dca86-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dca86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca86-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dca86-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




