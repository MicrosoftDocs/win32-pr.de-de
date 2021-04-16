---
description: Rendert eine Textur in eine Datei und gibt das Ergebnis asynchron an den Host zurück.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: rendertextureasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521523"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="59652-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: rendertextureasync-Methode</span><span class="sxs-lookup"><span data-stu-id="59652-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="59652-104">Rendert eine Textur in eine Datei und gibt das Ergebnis asynchron an den Host zurück.</span><span class="sxs-lookup"><span data-stu-id="59652-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="59652-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59652-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="59652-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59652-106">Parameters</span></span>

<span data-ttu-id="59652-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="59652-107">*textureId* </span></span>  
<span data-ttu-id="59652-108">Die ID der zu Rendering enden Textur.</span><span class="sxs-lookup"><span data-stu-id="59652-108">The ID of the texture to render.</span></span>

<span data-ttu-id="59652-109">*slicabdex* </span><span class="sxs-lookup"><span data-stu-id="59652-109">*sliceIndex* </span></span>  
<span data-ttu-id="59652-110">Der Index des Slice innerhalb der zu Rendering enden Textur.</span><span class="sxs-lookup"><span data-stu-id="59652-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="59652-111">*formatoverride* </span><span class="sxs-lookup"><span data-stu-id="59652-111">*formatOverride* </span></span>  
<span data-ttu-id="59652-112">Das Farb Format Überschreibung.</span><span class="sxs-lookup"><span data-stu-id="59652-112">The color format override.</span></span>

<span data-ttu-id="59652-113">*günstigere*</span><span class="sxs-lookup"><span data-stu-id="59652-113">*lower*</span></span>   

<span data-ttu-id="59652-114">*weite*</span><span class="sxs-lookup"><span data-stu-id="59652-114">*upper*</span></span>   

<span data-ttu-id="59652-115">*shaderdateiname* </span><span class="sxs-lookup"><span data-stu-id="59652-115">*shaderFileName* </span></span>  
<span data-ttu-id="59652-116">Eine com-Zeichenfolge, die den Pfadnamen der Shader-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="59652-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="59652-117">*numfloatshadervars* </span><span class="sxs-lookup"><span data-stu-id="59652-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="59652-118">Die Anzahl von Gleit Komma-Shader-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59652-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="59652-119">*count6 \_ shaderfloatvarname* </span><span class="sxs-lookup"><span data-stu-id="59652-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="59652-120">COM-Zeichen folgen, die die Namen der Gleit Komma-Shader-Variablen zusammenhängender.</span><span class="sxs-lookup"><span data-stu-id="59652-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="59652-121">*count6 \_ shaderfloatvarvalue* </span><span class="sxs-lookup"><span data-stu-id="59652-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="59652-122">Die Gleit Komma-Shader-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59652-122">The floating-point shader variables.</span></span>

<span data-ttu-id="59652-123">*numboolshadervars* </span><span class="sxs-lookup"><span data-stu-id="59652-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="59652-124">Die Anzahl der booleschen Shader-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59652-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="59652-125">*count9 \_ shaderboolvarname* </span><span class="sxs-lookup"><span data-stu-id="59652-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="59652-126">COM-Zeichen folgen, die die Namen der booleschen shadervariablen zusammen hänchern.</span><span class="sxs-lookup"><span data-stu-id="59652-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="59652-127">*count9 \_ shaderboolvarvalue* </span><span class="sxs-lookup"><span data-stu-id="59652-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="59652-128">Die booleschen Shader-Variablen.</span><span class="sxs-lookup"><span data-stu-id="59652-128">The boolean shader variables.</span></span>

<span data-ttu-id="59652-129">*rendercontentfilename* </span><span class="sxs-lookup"><span data-stu-id="59652-129">*renderContentFileName* </span></span>  
<span data-ttu-id="59652-130">Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die gerenderte Textur geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="59652-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="59652-131">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="59652-131">*callbacks* </span></span>  
<span data-ttu-id="59652-132">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59652-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="59652-133">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="59652-133">*requestCookie* </span></span>  
<span data-ttu-id="59652-134">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="59652-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="59652-135">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="59652-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="59652-136">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59652-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="59652-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59652-137">Return value</span></span>

<span data-ttu-id="59652-138">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="59652-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59652-139">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59652-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59652-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59652-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="59652-141">Header</span><span class="sxs-lookup"><span data-stu-id="59652-141">Header</span></span></p></td><td><span data-ttu-id="59652-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="59652-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="59652-143"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59652-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="59652-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="59652-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
