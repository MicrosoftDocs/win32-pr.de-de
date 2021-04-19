---
description: Speichert eine Textur im Speicher.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: D3DX10SaveTextureToMemory-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370428"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="4f13d-103">D3DX10SaveTextureToMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f13d-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="4f13d-104">Speichert eine Textur im Speicher.</span><span class="sxs-lookup"><span data-stu-id="4f13d-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f13d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f13d-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4f13d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f13d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f13d-107">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f13d-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13d-108">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="4f13d-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="4f13d-109">Zeiger auf die zu speichernde Textur.</span><span class="sxs-lookup"><span data-stu-id="4f13d-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="4f13d-110">Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="4f13d-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="4f13d-111">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f13d-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13d-112">Type: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="4f13d-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="4f13d-113">Das Format, in dem die Textur gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4f13d-113">The format the texture will be saved as.</span></span> <span data-ttu-id="4f13d-114">Siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="4f13d-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f13d-115">*ppdestbuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f13d-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13d-116">Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="4f13d-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="4f13d-117">Adresse eines Zeigers auf den Speicher, der die gespeicherte Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="4f13d-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="4f13d-118">Siehe [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="4f13d-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="4f13d-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4f13d-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13d-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f13d-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f13d-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f13d-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f13d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f13d-122">Return value</span></span>

<span data-ttu-id="4f13d-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f13d-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f13d-124">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="4f13d-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f13d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f13d-125">Requirements</span></span>



| <span data-ttu-id="4f13d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f13d-126">Requirement</span></span> | <span data-ttu-id="4f13d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4f13d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f13d-128">Header</span><span class="sxs-lookup"><span data-stu-id="4f13d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4f13d-129"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f13d-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4f13d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f13d-130">Library</span></span><br/> | <dl> <span data-ttu-id="4f13d-131"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f13d-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4f13d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f13d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f13d-133">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="4f13d-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="4f13d-134">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="4f13d-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
