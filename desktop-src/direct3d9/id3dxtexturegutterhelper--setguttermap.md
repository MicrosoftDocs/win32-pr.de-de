---
description: Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper:: setguttermap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355830"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="5839b-103">ID3DXTextureGutterHelper:: setguttermap-Methode</span><span class="sxs-lookup"><span data-stu-id="5839b-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="5839b-104">Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.</span><span class="sxs-lookup"><span data-stu-id="5839b-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5839b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5839b-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="5839b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5839b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5839b-107">*pgutterdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5839b-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5839b-108">Type: **[ **Byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5839b-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5839b-109">Zeiger auf die Texel-Klasse.</span><span class="sxs-lookup"><span data-stu-id="5839b-109">Pointer to the texel class.</span></span> <span data-ttu-id="5839b-110">Mögliche Texel-Klassen:</span><span class="sxs-lookup"><span data-stu-id="5839b-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="5839b-111">Es ist keine Texel-Klasse 3 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5839b-111">There is no texel class 3.</span></span>



| <span data-ttu-id="5839b-112">Texel-Klasse</span><span class="sxs-lookup"><span data-stu-id="5839b-112">Texel Class</span></span> | <span data-ttu-id="5839b-113">Textsort</span><span class="sxs-lookup"><span data-stu-id="5839b-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5839b-114">0</span><span class="sxs-lookup"><span data-stu-id="5839b-114">0</span></span>           | <span data-ttu-id="5839b-115">Ungültiger Punkt; Texel wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5839b-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5839b-116">1</span><span class="sxs-lookup"><span data-stu-id="5839b-116">1</span></span>           | <span data-ttu-id="5839b-117">Innerhalb des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="5839b-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5839b-118">2</span><span class="sxs-lookup"><span data-stu-id="5839b-118">2</span></span>           | <span data-ttu-id="5839b-119">Im bundbundbereich.</span><span class="sxs-lookup"><span data-stu-id="5839b-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5839b-120">4</span><span class="sxs-lookup"><span data-stu-id="5839b-120">4</span></span>           | <span data-ttu-id="5839b-121">Im bundbundbereich; Texel wird als vollständiges Beispiel in der [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)-Methode oder der [**ID3DXTextureGutterHelper:: applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md) -Methode ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="5839b-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5839b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5839b-122">Return value</span></span>

<span data-ttu-id="5839b-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5839b-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5839b-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5839b-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5839b-125">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="5839b-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="5839b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5839b-126">Requirements</span></span>



| <span data-ttu-id="5839b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5839b-127">Requirement</span></span> | <span data-ttu-id="5839b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5839b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5839b-129">Header</span><span class="sxs-lookup"><span data-stu-id="5839b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5839b-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5839b-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5839b-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5839b-131">Library</span></span><br/> | <dl> <span data-ttu-id="5839b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5839b-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5839b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5839b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5839b-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="5839b-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
