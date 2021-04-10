---
description: Legt die aktive Technik fest.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'ID3DXEffect:: settechnique-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961562"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="44584-103">ID3DXEffect:: settechnique-Methode</span><span class="sxs-lookup"><span data-stu-id="44584-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="44584-104">Legt die aktive Technik fest.</span><span class="sxs-lookup"><span data-stu-id="44584-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="44584-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44584-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="44584-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44584-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44584-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44584-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44584-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="44584-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="44584-109">Eindeutiges Handle für die Technik.</span><span class="sxs-lookup"><span data-stu-id="44584-109">Unique handle to the technique.</span></span> <span data-ttu-id="44584-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="44584-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44584-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44584-111">Return value</span></span>

<span data-ttu-id="44584-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44584-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44584-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44584-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="44584-114">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="44584-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="44584-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44584-115">Requirements</span></span>



| <span data-ttu-id="44584-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44584-116">Requirement</span></span> | <span data-ttu-id="44584-117">Wert</span><span class="sxs-lookup"><span data-stu-id="44584-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44584-118">Header</span><span class="sxs-lookup"><span data-stu-id="44584-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44584-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="44584-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="44584-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44584-120">Library</span></span><br/> | <dl> <span data-ttu-id="44584-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44584-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="44584-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44584-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44584-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="44584-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




