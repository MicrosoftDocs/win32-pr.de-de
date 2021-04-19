---
description: Ruft das Handle einer Technik Durchsuchen des Namens ab.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect:: gettechniquebyname-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353404"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="ec70f-103">ID3DXBaseEffect:: gettechniquebyname-Methode</span><span class="sxs-lookup"><span data-stu-id="ec70f-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="ec70f-104">Ruft das Handle einer Technik Durchsuchen des Namens ab.</span><span class="sxs-lookup"><span data-stu-id="ec70f-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec70f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec70f-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="ec70f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec70f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec70f-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec70f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec70f-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec70f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec70f-109">Zeichenfolge, die den Namen der Technik enthält.</span><span class="sxs-lookup"><span data-stu-id="ec70f-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec70f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec70f-110">Return value</span></span>

<span data-ttu-id="ec70f-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ec70f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ec70f-112">Gibt das Handle der ersten Technik mit dem angegebenen Namen zurück, oder **null** , wenn der Name nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="ec70f-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="ec70f-113">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ec70f-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec70f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec70f-114">Requirements</span></span>



| <span data-ttu-id="ec70f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec70f-115">Requirement</span></span> | <span data-ttu-id="ec70f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ec70f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec70f-117">Header</span><span class="sxs-lookup"><span data-stu-id="ec70f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ec70f-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec70f-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ec70f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec70f-119">Library</span></span><br/> | <dl> <span data-ttu-id="ec70f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec70f-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ec70f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec70f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec70f-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ec70f-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
