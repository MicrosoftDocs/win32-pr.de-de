---
title: D3DX11ComputeNormalMap-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle dieser Funktion die directxtex-Bibliothek, "computenormalmap", verwenden.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219630"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="341a1-105">D3DX11ComputeNormalMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="341a1-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="341a1-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="341a1-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="341a1-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek " **computenormalmap**" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="341a1-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="341a1-108">Konvertiert eine Höhen Zuordnung in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="341a1-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="341a1-109">Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="341a1-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="341a1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="341a1-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="341a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="341a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341a1-112">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-113">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="341a1-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="341a1-114">Ein Zeiger auf eine [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle, die die Textur der Quell Höhe darstellt.</span><span class="sxs-lookup"><span data-stu-id="341a1-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="341a1-115">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-116">Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="341a1-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="341a1-117">Ein Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle, die die Textur der Quell Höhe darstellt.</span><span class="sxs-lookup"><span data-stu-id="341a1-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="341a1-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-119">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="341a1-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="341a1-120">Ein oder mehrere D3DX \_ normalmap-Flags, die die Generierung normaler Karten steuern.</span><span class="sxs-lookup"><span data-stu-id="341a1-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="341a1-121">*Channel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-122">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="341a1-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="341a1-123">Ein D3DX- \_ kanalflag, das die Quelle der Höheninformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="341a1-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="341a1-124">*Amplitude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-125">Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="341a1-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="341a1-126">Konstanter Wert Multiplikator, der die Werte in der normalen Zuordnung vergrößert (oder verringert).</span><span class="sxs-lookup"><span data-stu-id="341a1-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="341a1-127">Höhere Werte machen in der Regel zu Leistungseinbußen, niedrigere Werte werden in der Regel weniger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="341a1-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="341a1-128">*pdesttexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a1-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a1-129">Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="341a1-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="341a1-130">Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle, die die Ziel Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="341a1-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341a1-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="341a1-131">Return value</span></span>

<span data-ttu-id="341a1-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="341a1-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="341a1-133">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="341a1-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="341a1-134">Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="341a1-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="341a1-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="341a1-135">Remarks</span></span>

<span data-ttu-id="341a1-136">Diese Methode berechnet die normale, indem der zentrale Unterschied mit einer Kernel Größe von 3X3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="341a1-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="341a1-137">RGB-Kanäle im Ziel enthalten unausgewogene (x, y, z) Komponenten der normalen.</span><span class="sxs-lookup"><span data-stu-id="341a1-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="341a1-138">Der zentrale Differenzierungs Nenner ist hart codiert in 2,0.</span><span class="sxs-lookup"><span data-stu-id="341a1-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="341a1-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="341a1-139">Requirements</span></span>



| <span data-ttu-id="341a1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="341a1-140">Requirement</span></span> | <span data-ttu-id="341a1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="341a1-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="341a1-142">Header</span><span class="sxs-lookup"><span data-stu-id="341a1-142">Header</span></span><br/>  | <dl> <span data-ttu-id="341a1-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="341a1-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="341a1-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="341a1-144">Library</span></span><br/> | <dl> <span data-ttu-id="341a1-145"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="341a1-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="341a1-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="341a1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341a1-147">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="341a1-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

