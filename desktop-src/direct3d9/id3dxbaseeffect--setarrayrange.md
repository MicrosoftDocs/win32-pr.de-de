---
description: Legen Sie den Bereich eines Arrays fest, der an das Gerät übergeben werden soll.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'ID3DXBaseEffect:: abtarrayrange-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132285"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="b3425-103">ID3DXBaseEffect:: abtarrayrange-Methode</span><span class="sxs-lookup"><span data-stu-id="b3425-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="b3425-104">Legen Sie den Bereich eines Arrays fest, der an das Gerät übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3425-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3425-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3425-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="b3425-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3425-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3425-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3425-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3425-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3425-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3425-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b3425-109">Unique identifier.</span></span> <span data-ttu-id="b3425-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b3425-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3425-111">*Starten* \[ Sie in\]</span><span class="sxs-lookup"><span data-stu-id="b3425-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3425-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3425-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3425-113">Start Index.</span><span class="sxs-lookup"><span data-stu-id="b3425-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="b3425-114">Wird *beendet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3425-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3425-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3425-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3425-116">Stoppt den Index.</span><span class="sxs-lookup"><span data-stu-id="b3425-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3425-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3425-117">Return value</span></span>

<span data-ttu-id="b3425-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3425-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3425-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3425-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3425-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="b3425-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3425-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3425-121">Requirements</span></span>



| <span data-ttu-id="b3425-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3425-122">Requirement</span></span> | <span data-ttu-id="b3425-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b3425-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3425-124">Header</span><span class="sxs-lookup"><span data-stu-id="b3425-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b3425-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3425-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3425-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3425-126">Library</span></span><br/> | <dl> <span data-ttu-id="b3425-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3425-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3425-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3425-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3425-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b3425-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
