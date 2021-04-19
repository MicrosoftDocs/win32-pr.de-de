---
description: Ruft einen booleschen Wert ab.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect:: getBool-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367493"
---
# <a name="id3dxbaseeffectgetbool-method"></a><span data-ttu-id="edd58-103">ID3DXBaseEffect:: getBool-Methode</span><span class="sxs-lookup"><span data-stu-id="edd58-103">ID3DXBaseEffect::GetBool method</span></span>

<span data-ttu-id="edd58-104">Ruft einen booleschen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="edd58-104">Gets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edd58-105">Syntax</span></span>


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a><span data-ttu-id="edd58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edd58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd58-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edd58-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd58-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="edd58-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="edd58-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="edd58-109">Unique identifier.</span></span> <span data-ttu-id="edd58-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="edd58-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="edd58-111">*PB* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="edd58-111">*pb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd58-112">Typ: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="edd58-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="edd58-113">Gibt einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="edd58-113">Returns a Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd58-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edd58-114">Return value</span></span>

<span data-ttu-id="edd58-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edd58-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edd58-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="edd58-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="edd58-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="edd58-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd58-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edd58-118">Requirements</span></span>



| <span data-ttu-id="edd58-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edd58-119">Requirement</span></span> | <span data-ttu-id="edd58-120">Wert</span><span class="sxs-lookup"><span data-stu-id="edd58-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd58-121">Header</span><span class="sxs-lookup"><span data-stu-id="edd58-121">Header</span></span><br/>  | <dl> <span data-ttu-id="edd58-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd58-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="edd58-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="edd58-123">Library</span></span><br/> | <dl> <span data-ttu-id="edd58-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edd58-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="edd58-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd58-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd58-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="edd58-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="edd58-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="edd58-127">**SetBool**</span></span>](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
