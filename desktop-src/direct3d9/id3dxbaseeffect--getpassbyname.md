---
description: Ruft das Handle für einen Durchlauf ab, indem der zugehörige Name gesucht wird.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect:: getpassbyname-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353405"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="e2d27-103">ID3DXBaseEffect:: getpassbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="e2d27-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="e2d27-104">Ruft das Handle für einen Durchlauf ab, indem der zugehörige Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="e2d27-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2d27-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="e2d27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2d27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d27-107">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2d27-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d27-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e2d27-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e2d27-109">Handle des übergeordneten Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="e2d27-109">Handle of the parent technique.</span></span> <span data-ttu-id="e2d27-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e2d27-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2d27-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2d27-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d27-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2d27-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2d27-113">Zeichenfolge, die den Pass Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="e2d27-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d27-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2d27-114">Return value</span></span>

<span data-ttu-id="e2d27-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e2d27-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e2d27-116">Gibt das Handle des ersten Durchlauf innerhalb der angegebenen Technik mit dem angegebenen Namen zurück, oder **null** , wenn der Name nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e2d27-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="e2d27-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e2d27-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d27-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2d27-118">Requirements</span></span>



| <span data-ttu-id="e2d27-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2d27-119">Requirement</span></span> | <span data-ttu-id="e2d27-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e2d27-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d27-121">Header</span><span class="sxs-lookup"><span data-stu-id="e2d27-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e2d27-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2d27-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e2d27-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2d27-123">Library</span></span><br/> | <dl> <span data-ttu-id="e2d27-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2d27-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2d27-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d27-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e2d27-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
