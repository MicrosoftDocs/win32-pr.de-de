---
description: Den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen, erhalten. Diese Methode kann anstelle von fast allen GetXXX-aufrufen in ID3DXBaseEffect verwendet werden.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect:: GetValue-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363956"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="1a02b-104">ID3DXBaseEffect:: GetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="1a02b-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="1a02b-105">Den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen, erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a02b-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="1a02b-106">Diese Methode kann anstelle von fast allen GetXXX-aufrufen in [**ID3DXBaseEffect**](id3dxbaseeffect.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a02b-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a02b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a02b-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="1a02b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a02b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a02b-109">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a02b-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02b-110">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1a02b-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1a02b-111">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1a02b-111">Unique identifier.</span></span> <span data-ttu-id="1a02b-112">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1a02b-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a02b-113">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a02b-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02b-114">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a02b-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a02b-115">Gibt einen Puffer zurück, der den Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="1a02b-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="1a02b-116">*Bytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a02b-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02b-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a02b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a02b-118">\[gibt \] die Anzahl der Bytes im Puffer an.</span><span class="sxs-lookup"><span data-stu-id="1a02b-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="1a02b-119">Übergeben Sie D3DX \_ Default, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie die Größenüberprüfung überspringen möchten.</span><span class="sxs-lookup"><span data-stu-id="1a02b-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a02b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a02b-120">Return value</span></span>

<span data-ttu-id="1a02b-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a02b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a02b-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a02b-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1a02b-123">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="1a02b-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a02b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a02b-124">Requirements</span></span>



| <span data-ttu-id="1a02b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a02b-125">Requirement</span></span> | <span data-ttu-id="1a02b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1a02b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a02b-127">Header</span><span class="sxs-lookup"><span data-stu-id="1a02b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1a02b-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a02b-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1a02b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a02b-129">Library</span></span><br/> | <dl> <span data-ttu-id="1a02b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a02b-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1a02b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a02b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a02b-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1a02b-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1a02b-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="1a02b-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
