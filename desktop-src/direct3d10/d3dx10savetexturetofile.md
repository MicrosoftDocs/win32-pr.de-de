---
description: Speichert eine Textur in einer Datei.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: D3DX10SaveTextureToFile-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351997"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="01209-103">D3DX10SaveTextureToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="01209-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="01209-104">Speichert eine Textur in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="01209-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="01209-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01209-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="01209-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01209-107">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01209-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01209-108">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="01209-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="01209-109">Zeiger auf die zu speichernde Textur.</span><span class="sxs-lookup"><span data-stu-id="01209-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="01209-110">Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="01209-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="01209-111">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01209-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01209-112">Type: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="01209-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="01209-113">Das Format, in dem die Textur gespeichert wird (siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="01209-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="01209-114">D3dx10 \_ IFF \_ DDS ist das bevorzugte Format, da es die einzige Option ist, die alle Formate im [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01209-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="01209-115">*pdestfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01209-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01209-116">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01209-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01209-117">Der Name der Ziel Ausgabedatei, in der die Textur gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="01209-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="01209-118">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="01209-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="01209-119">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="01209-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01209-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01209-120">Return value</span></span>

<span data-ttu-id="01209-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01209-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01209-122">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind. Verwenden Sie den Rückgabewert, um festzustellen, ob *destformat* unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01209-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="01209-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01209-123">Remarks</span></span>

<span data-ttu-id="01209-124">**D3DX10SaveTextureToFile** schreibt die zusätzliche [**DDS- \_ Header \_ DXT10**](../direct3ddds/dds-header-dxt10.md) -Struktur nur bei Bedarf für die Eingabe Textur (z. b. weil die Eingabe Textur im Standard-RGB-Format (sRGB) vorliegt).</span><span class="sxs-lookup"><span data-stu-id="01209-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="01209-125">Wenn **D3DX10SaveTextureToFile** die **DDS- \_ Header \_ DXT10** -Struktur ausgibt, wird der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](../direct3ddds/dds-pixelformat.md) -Struktur für die Textur auf **DX10** festgelegt, um die präscense des **DDS- \_ Headers \_ DXT10** Extended-Header anzugeben.</span><span class="sxs-lookup"><span data-stu-id="01209-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="01209-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01209-126">Requirements</span></span>



| <span data-ttu-id="01209-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01209-127">Requirement</span></span> | <span data-ttu-id="01209-128">Wert</span><span class="sxs-lookup"><span data-stu-id="01209-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01209-129">Header</span><span class="sxs-lookup"><span data-stu-id="01209-129">Header</span></span><br/>  | <dl> <span data-ttu-id="01209-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="01209-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="01209-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01209-131">Library</span></span><br/> | <dl> <span data-ttu-id="01209-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01209-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="01209-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01209-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01209-134">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="01209-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="01209-135">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="01209-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
