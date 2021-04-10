---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem der zugehörige Name gesucht wird.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect:: getparameterbyname-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961754"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="6917d-103">ID3DXBaseEffect:: getparameterbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="6917d-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="6917d-104">Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem der zugehörige Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="6917d-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6917d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6917d-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="6917d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6917d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6917d-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6917d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917d-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6917d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6917d-109">Handle des-Parameters oder **null** für Parameter der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="6917d-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="6917d-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6917d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6917d-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6917d-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917d-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6917d-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6917d-113">Zeichenfolge, die den Parameternamen enthält.</span><span class="sxs-lookup"><span data-stu-id="6917d-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6917d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6917d-114">Return value</span></span>

<span data-ttu-id="6917d-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6917d-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6917d-116">Gibt das Handle des angegebenen Parameters oder **null** zurück, wenn der Index ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="6917d-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="6917d-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6917d-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6917d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6917d-118">Requirements</span></span>



| <span data-ttu-id="6917d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6917d-119">Requirement</span></span> | <span data-ttu-id="6917d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6917d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6917d-121">Header</span><span class="sxs-lookup"><span data-stu-id="6917d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6917d-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6917d-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6917d-123">Library</span></span><br/> | <dl> <span data-ttu-id="6917d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6917d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6917d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6917d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6917d-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6917d-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
