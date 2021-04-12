---
description: Ruft eine Technik Beschreibung ab.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect:: gettechniquedesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219693"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="3cea7-103">ID3DXBaseEffect:: gettechniquedesc-Methode</span><span class="sxs-lookup"><span data-stu-id="3cea7-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="3cea7-104">Ruft eine Technik Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="3cea7-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cea7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cea7-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3cea7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cea7-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cea7-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cea7-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3cea7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3cea7-109">Technik handle.</span><span class="sxs-lookup"><span data-stu-id="3cea7-109">Technique handle.</span></span> <span data-ttu-id="3cea7-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="3cea7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cea7-111">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3cea7-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cea7-112">Typ: **[ **D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3cea7-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="3cea7-113">Gibt eine Beschreibung der Technik zurück.</span><span class="sxs-lookup"><span data-stu-id="3cea7-113">Returns a description of the technique.</span></span> <span data-ttu-id="3cea7-114">Weitere Informationen finden Sie unter [**D3DXTECHNIQUE \_**](d3dxtechnique-desc.md).</span><span class="sxs-lookup"><span data-stu-id="3cea7-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cea7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cea7-115">Return value</span></span>

<span data-ttu-id="3cea7-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3cea7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3cea7-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3cea7-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3cea7-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="3cea7-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cea7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cea7-119">Requirements</span></span>



| <span data-ttu-id="3cea7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cea7-120">Requirement</span></span> | <span data-ttu-id="3cea7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3cea7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cea7-122">Header</span><span class="sxs-lookup"><span data-stu-id="3cea7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3cea7-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cea7-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3cea7-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3cea7-124">Library</span></span><br/> | <dl> <span data-ttu-id="3cea7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cea7-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3cea7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cea7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cea7-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="3cea7-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




