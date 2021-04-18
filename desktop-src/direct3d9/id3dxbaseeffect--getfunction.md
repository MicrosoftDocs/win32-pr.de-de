---
description: Ruft das Handle einer Funktion ab.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'ID3DXBaseEffect:: GetFunction-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364395"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="76ed8-103">ID3DXBaseEffect:: GetFunction-Methode</span><span class="sxs-lookup"><span data-stu-id="76ed8-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="76ed8-104">Ruft das Handle einer Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="76ed8-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ed8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76ed8-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="76ed8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76ed8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ed8-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ed8-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ed8-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ed8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ed8-109">Funktions Index.</span><span class="sxs-lookup"><span data-stu-id="76ed8-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ed8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76ed8-110">Return value</span></span>

<span data-ttu-id="76ed8-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="76ed8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="76ed8-112">Gibt das Handle der angegebenen Funktion oder **null** zurück, wenn der Index ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="76ed8-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="76ed8-113">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="76ed8-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76ed8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76ed8-114">Requirements</span></span>



| <span data-ttu-id="76ed8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76ed8-115">Requirement</span></span> | <span data-ttu-id="76ed8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="76ed8-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ed8-117">Header</span><span class="sxs-lookup"><span data-stu-id="76ed8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="76ed8-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ed8-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="76ed8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76ed8-119">Library</span></span><br/> | <dl> <span data-ttu-id="76ed8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76ed8-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="76ed8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ed8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ed8-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="76ed8-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
