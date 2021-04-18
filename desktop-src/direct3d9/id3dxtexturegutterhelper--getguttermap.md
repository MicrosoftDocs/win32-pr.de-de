---
description: Empfängt einen Texel-Klassen Wert, der Texttypen entsprechend der Position jedes Texttyps angibt.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper:: getguttermap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365107"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="a775c-103">ID3DXTextureGutterHelper:: getguttermap-Methode</span><span class="sxs-lookup"><span data-stu-id="a775c-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="a775c-104">Empfängt einen Texel-Klassen Wert, der Texttypen entsprechend der Position jedes Texttyps angibt.</span><span class="sxs-lookup"><span data-stu-id="a775c-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a775c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a775c-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="a775c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a775c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a775c-107">*pgutterdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a775c-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a775c-108">Type: **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a775c-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a775c-109">Zeiger auf die Texel-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a775c-109">Pointer to the texel class.</span></span> <span data-ttu-id="a775c-110">Mögliche Texel-Klassen:</span><span class="sxs-lookup"><span data-stu-id="a775c-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="a775c-111">Es ist keine Texel-Klasse 3 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a775c-111">There is no texel class 3.</span></span>



| <span data-ttu-id="a775c-112">Texel-Klasse</span><span class="sxs-lookup"><span data-stu-id="a775c-112">Texel Class</span></span> | <span data-ttu-id="a775c-113">Textsort</span><span class="sxs-lookup"><span data-stu-id="a775c-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a775c-114">0</span><span class="sxs-lookup"><span data-stu-id="a775c-114">0</span></span>           | <span data-ttu-id="a775c-115">Ungültiger Punkt; Texel wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a775c-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a775c-116">1</span><span class="sxs-lookup"><span data-stu-id="a775c-116">1</span></span>           | <span data-ttu-id="a775c-117">Innerhalb des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="a775c-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a775c-118">2</span><span class="sxs-lookup"><span data-stu-id="a775c-118">2</span></span>           | <span data-ttu-id="a775c-119">Im bundbundbereich.</span><span class="sxs-lookup"><span data-stu-id="a775c-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a775c-120">4</span><span class="sxs-lookup"><span data-stu-id="a775c-120">4</span></span>           | <span data-ttu-id="a775c-121">Im bundbundbereich; Texel wird als vollständiges Beispiel in der [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)-Methode oder der [**ID3DXTextureGutterHelper:: applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md) -Methode ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="a775c-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a775c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a775c-122">Return value</span></span>

<span data-ttu-id="a775c-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a775c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a775c-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a775c-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a775c-125">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="a775c-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a775c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a775c-126">Remarks</span></span>

<span data-ttu-id="a775c-127">Die Anwendung muss pgutterdata zuordnen und verwalten, wobei die Größe von angegeben wird:</span><span class="sxs-lookup"><span data-stu-id="a775c-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="a775c-128">Textur Breite und-Höhe werden von [**ID3DXTextureGutterHelper:: getWidth**](id3dxtexturegutterhelper--getwidth.md) und [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a775c-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a775c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a775c-129">Requirements</span></span>



| <span data-ttu-id="a775c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a775c-130">Requirement</span></span> | <span data-ttu-id="a775c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a775c-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a775c-132">Header</span><span class="sxs-lookup"><span data-stu-id="a775c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a775c-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a775c-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a775c-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a775c-134">Library</span></span><br/> | <dl> <span data-ttu-id="a775c-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a775c-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a775c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a775c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a775c-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="a775c-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
