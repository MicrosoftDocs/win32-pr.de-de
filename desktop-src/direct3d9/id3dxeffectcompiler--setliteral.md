---
description: Schaltet den literalstatus eines Parameters um. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler:: setliteralmethode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354356"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="847bc-104">ID3DXEffectCompiler:: setliterale-Methode</span><span class="sxs-lookup"><span data-stu-id="847bc-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="847bc-105">Schaltet den literalstatus eines Parameters um.</span><span class="sxs-lookup"><span data-stu-id="847bc-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="847bc-106">Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="847bc-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="847bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="847bc-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="847bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="847bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="847bc-109">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847bc-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847bc-110">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="847bc-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="847bc-111">Eindeutiger Bezeichner für einen Parameter.</span><span class="sxs-lookup"><span data-stu-id="847bc-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="847bc-112">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="847bc-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="847bc-113">*Literale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847bc-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847bc-114">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="847bc-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="847bc-115">Legen Sie diese Einstellung auf " **true** " fest, um **den-Parameter als** Literalwert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="847bc-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="847bc-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="847bc-116">Return value</span></span>

<span data-ttu-id="847bc-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="847bc-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="847bc-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="847bc-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="847bc-119">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="847bc-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="847bc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="847bc-120">Remarks</span></span>

<span data-ttu-id="847bc-121">Diese Methoden ändern nur, ob der Parameter ein Literalwert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="847bc-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="847bc-122">Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="847bc-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="847bc-123">Diese Funktion muss vor der Kompilierung des Effekts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="847bc-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="847bc-124">Im folgenden finden Sie ein Beispiel dafür, wie Sie diese Funktion verwenden können:</span><span class="sxs-lookup"><span data-stu-id="847bc-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="847bc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="847bc-125">Requirements</span></span>



| <span data-ttu-id="847bc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="847bc-126">Requirement</span></span> | <span data-ttu-id="847bc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="847bc-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="847bc-128">Header</span><span class="sxs-lookup"><span data-stu-id="847bc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="847bc-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="847bc-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="847bc-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="847bc-130">Library</span></span><br/> | <dl> <span data-ttu-id="847bc-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="847bc-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="847bc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="847bc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847bc-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="847bc-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="847bc-134">Verwendungen und Literale (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="847bc-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="847bc-135">**ID3DXEffectCompiler:: getliteral**</span><span class="sxs-lookup"><span data-stu-id="847bc-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
