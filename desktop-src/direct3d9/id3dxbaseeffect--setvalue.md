---
description: Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect:: SetValue-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132369"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="0b396-103">ID3DXBaseEffect:: SetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="0b396-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="0b396-104">Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen.</span><span class="sxs-lookup"><span data-stu-id="0b396-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b396-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b396-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="0b396-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b396-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b396-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b396-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b396-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0b396-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0b396-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0b396-109">Unique identifier.</span></span> <span data-ttu-id="0b396-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0b396-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b396-111">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b396-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b396-112">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b396-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b396-113">Zeiger auf einen Puffer, der Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0b396-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="0b396-114">*Bytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b396-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b396-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b396-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b396-116">\[gibt \] die Anzahl der Bytes im Puffer an.</span><span class="sxs-lookup"><span data-stu-id="0b396-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="0b396-117">Übergeben Sie D3DX \_ Default, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie die Größenüberprüfung überspringen möchten.</span><span class="sxs-lookup"><span data-stu-id="0b396-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b396-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b396-118">Return value</span></span>

<span data-ttu-id="0b396-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b396-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b396-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b396-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b396-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="0b396-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b396-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b396-122">Remarks</span></span>

<span data-ttu-id="0b396-123">Diese Methode kann anstelle von fast allen Effekten Satz-API-Aufrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b396-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b396-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b396-124">Requirements</span></span>



| <span data-ttu-id="0b396-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b396-125">Requirement</span></span> | <span data-ttu-id="0b396-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0b396-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b396-127">Header</span><span class="sxs-lookup"><span data-stu-id="0b396-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0b396-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b396-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0b396-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b396-129">Library</span></span><br/> | <dl> <span data-ttu-id="0b396-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b396-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b396-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b396-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b396-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0b396-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0b396-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="0b396-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
