---
description: Überprüft die Parameter für die Textur Erstellung.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: D3DXCheckTextureRequirements-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219558"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="ce37b-103">D3DXCheckTextureRequirements-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce37b-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="ce37b-104">Überprüft die Parameter für die Textur Erstellung.</span><span class="sxs-lookup"><span data-stu-id="ce37b-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce37b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce37b-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="ce37b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce37b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce37b-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ce37b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ce37b-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce37b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce37b-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ce37b-112">Ein Zeiger auf die angeforderte Breite in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ce37b-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="ce37b-113">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="ce37b-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce37b-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ce37b-116">Ein Zeiger auf die angeforderte Höhe in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ce37b-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="ce37b-117">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="ce37b-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-118">*pnummiplevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-119">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce37b-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ce37b-120">Ein Zeiger auf die Anzahl der angeforderten MipMap-Ebenen oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ce37b-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="ce37b-121">Gibt die korrigierte Anzahl von MipMap-Ebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="ce37b-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-122">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce37b-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce37b-124">0 oder [**D3DUSAGE \_ renderTarget**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="ce37b-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="ce37b-125">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce37b-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ce37b-126">Die Ressource kann dann an den pnewrendertarget-Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce37b-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ce37b-127">Wenn **D3DUSAGE \_ renderTarget** angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce37b-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-128">*pformat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-129">Typ: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce37b-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="ce37b-130">Zeiger auf einen Member des [D3DFORMAT](d3dformat.md) -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="ce37b-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="ce37b-131">Gibt das gewünschte Pixel Format oder **null** an.</span><span class="sxs-lookup"><span data-stu-id="ce37b-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="ce37b-132">Gibt das korrigierte Format zurück.</span><span class="sxs-lookup"><span data-stu-id="ce37b-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="ce37b-133">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce37b-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce37b-134">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ce37b-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ce37b-135">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce37b-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce37b-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce37b-136">Return value</span></span>

<span data-ttu-id="ce37b-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce37b-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce37b-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce37b-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce37b-139">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable.</span><span class="sxs-lookup"><span data-stu-id="ce37b-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce37b-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce37b-140">Remarks</span></span>

<span data-ttu-id="ce37b-141">Wenn die Parameter dieser Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="ce37b-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="ce37b-142">Diese Funktion verwendet die folgende Heuristik, wenn die angeforderten Anforderungen mit den verfügbaren Formaten verglichen werden:</span><span class="sxs-lookup"><span data-stu-id="ce37b-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="ce37b-143">Wählen Sie kein Format aus, das über weniger Kanäle verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce37b-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="ce37b-144">Vermeiden Sie [FourCC](d3dformat.md) -und 24-Bit-Formate, sofern diese nicht explizit angefordert werden</span><span class="sxs-lookup"><span data-stu-id="ce37b-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="ce37b-145">Versuchen Sie nicht, neue Kanäle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce37b-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="ce37b-146">Versuchen Sie nicht, die Anzahl von Bits pro Kanal zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce37b-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="ce37b-147">Versuchen Sie, die Typformatierung zwischen Typen von Formaten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ce37b-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="ce37b-148">Vermeiden Sie beispielsweise die Typumwandlung eines ARGB-Formats in ein tiefen Format.</span><span class="sxs-lookup"><span data-stu-id="ce37b-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce37b-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce37b-149">Requirements</span></span>



| <span data-ttu-id="ce37b-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce37b-150">Requirement</span></span> | <span data-ttu-id="ce37b-151">Wert</span><span class="sxs-lookup"><span data-stu-id="ce37b-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce37b-152">Header</span><span class="sxs-lookup"><span data-stu-id="ce37b-152">Header</span></span><br/>  | <dl> <span data-ttu-id="ce37b-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce37b-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ce37b-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce37b-154">Library</span></span><br/> | <dl> <span data-ttu-id="ce37b-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce37b-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce37b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce37b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce37b-157">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ce37b-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
