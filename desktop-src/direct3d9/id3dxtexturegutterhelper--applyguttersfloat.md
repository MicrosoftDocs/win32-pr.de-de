---
description: Wendet die-Guster auf einen float-Textur Puffer an.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper:: applyguttersfloat-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355208"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="91a07-103">ID3DXTextureGutterHelper:: applyguttersfloat-Methode</span><span class="sxs-lookup"><span data-stu-id="91a07-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="91a07-104">Wendet die-Guster auf einen float-Textur Puffer an.</span><span class="sxs-lookup"><span data-stu-id="91a07-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91a07-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="91a07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a07-107">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a07-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a07-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91a07-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91a07-109">Zeiger auf einen Puffer von float-Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="91a07-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="91a07-110">*Numkoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a07-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a07-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91a07-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91a07-112">Anzahl der skalare pro Farbkanal, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91a07-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="91a07-113">Jedes textelor enthält numcoeffs float-Werte.</span><span class="sxs-lookup"><span data-stu-id="91a07-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="91a07-114">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a07-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a07-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91a07-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91a07-116">Breite der Textur in Pixel, die von [**ID3DXTextureGutterHelper:: getWidth**](id3dxtexturegutterhelper--getwidth.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="91a07-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="91a07-117">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91a07-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a07-118">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="91a07-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="91a07-119">Die Höhe der Textur in Pixel, die von [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="91a07-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a07-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91a07-120">Return value</span></span>

<span data-ttu-id="91a07-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91a07-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91a07-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91a07-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="91a07-123">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="91a07-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="91a07-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91a07-124">Remarks</span></span>

<span data-ttu-id="91a07-125">[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden durch das erneute Sampling von Class 1 und 4 texeln generiert.</span><span class="sxs-lookup"><span data-stu-id="91a07-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a07-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91a07-126">Requirements</span></span>



| <span data-ttu-id="91a07-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91a07-127">Requirement</span></span> | <span data-ttu-id="91a07-128">Wert</span><span class="sxs-lookup"><span data-stu-id="91a07-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91a07-129">Header</span><span class="sxs-lookup"><span data-stu-id="91a07-129">Header</span></span><br/>  | <dl> <span data-ttu-id="91a07-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a07-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="91a07-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91a07-131">Library</span></span><br/> | <dl> <span data-ttu-id="91a07-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91a07-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91a07-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91a07-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a07-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="91a07-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
