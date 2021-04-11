---
description: Ruft das Handle einer Technik ab.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'ID3DXBaseEffect:: gettechnique-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132405"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="5e539-103">ID3DXBaseEffect:: gettechnique-Methode</span><span class="sxs-lookup"><span data-stu-id="5e539-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="5e539-104">Ruft das Handle einer Technik ab.</span><span class="sxs-lookup"><span data-stu-id="5e539-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e539-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e539-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="5e539-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e539-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e539-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e539-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e539-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e539-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e539-109">Technik Index.</span><span class="sxs-lookup"><span data-stu-id="5e539-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e539-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e539-110">Return value</span></span>

<span data-ttu-id="5e539-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5e539-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5e539-112">Gibt das Handle der angegebenen Technik oder **null** zurück, wenn der Index ungültig war.</span><span class="sxs-lookup"><span data-stu-id="5e539-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="5e539-113">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5e539-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e539-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e539-114">Requirements</span></span>



| <span data-ttu-id="5e539-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e539-115">Requirement</span></span> | <span data-ttu-id="5e539-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5e539-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e539-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e539-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e539-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e539-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5e539-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e539-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e539-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e539-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5e539-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e539-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e539-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5e539-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
