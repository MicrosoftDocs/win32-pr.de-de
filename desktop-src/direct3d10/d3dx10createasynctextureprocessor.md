---
description: 'D3DX10CreateAsyncTextureProcessor-Funktion: Erstellen Sie einen Datenprozessor, der mit einem Threadpump verwendet werden soll.'
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: D3DX10CreateAsyncTextureProcessor-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102788"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="07812-103">D3DX10CreateAsyncTextureProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="07812-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="07812-104">Erstellen Sie einen Datenprozessor, der mit einem [**Threadpump verwendet werden soll.**](id3dx10threadpump.md)</span><span class="sxs-lookup"><span data-stu-id="07812-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07812-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07812-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="07812-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07812-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07812-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="07812-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07812-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="07812-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="07812-109">Ein Zeiger auf die Devive (siehe [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="07812-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="07812-110">*pLoadInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="07812-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07812-111">Typ: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="07812-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="07812-112">Optional.</span><span class="sxs-lookup"><span data-stu-id="07812-112">Optional.</span></span> <span data-ttu-id="07812-113">Identifiziert die Merkmale einer Textur (siehe [**D3DX10 \_ IMAGE \_ LOAD \_ INFO),**](d3dx10-image-load-info.md)wenn der Datenprozessor erstellt wird. Legen Sie diese auf **NULL** fest, um die Merkmale einer Textur zu lesen, wenn die Textur geladen wird.</span><span class="sxs-lookup"><span data-stu-id="07812-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="07812-114">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="07812-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07812-115">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="07812-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="07812-116">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="07812-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07812-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07812-117">Return value</span></span>

<span data-ttu-id="07812-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07812-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07812-119">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="07812-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07812-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07812-120">Remarks</span></span>

<span data-ttu-id="07812-121">Diese API erstellt eine Datenprozessorschnittstelle und lädt die Textur. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) erstellt die Datenprozessorschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="07812-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="07812-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07812-122">Requirements</span></span>



| <span data-ttu-id="07812-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07812-123">Requirement</span></span> | <span data-ttu-id="07812-124">Wert</span><span class="sxs-lookup"><span data-stu-id="07812-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07812-125">Header</span><span class="sxs-lookup"><span data-stu-id="07812-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07812-126"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="07812-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="07812-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07812-127">Library</span></span><br/> | <dl> <span data-ttu-id="07812-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="07812-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="07812-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07812-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07812-130">Texturfunktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="07812-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




