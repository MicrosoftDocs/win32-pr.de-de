---
description: Erstellen Sie einen Datenprozessor, der mit einem threadpump verwendet werden soll.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: D3DX10CreateAsyncTextureInfoProcessor-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353754"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="d9141-103">D3DX10CreateAsyncTextureInfoProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9141-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="d9141-104">Erstellen Sie einen Datenprozessor, der mit einem [**threadpump**](id3dx10threadpump.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9141-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9141-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9141-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="d9141-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9141-107">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9141-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9141-108">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9141-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="d9141-109">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9141-109">Optional.</span></span> <span data-ttu-id="d9141-110">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d9141-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d9141-111">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d9141-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9141-112">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9141-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="d9141-113">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d9141-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9141-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9141-114">Return value</span></span>

<span data-ttu-id="d9141-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9141-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9141-116">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d9141-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9141-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9141-117">Remarks</span></span>

<span data-ttu-id="d9141-118">Diese API erstellt eine Datenprozessor Schnittstelle. [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) erstellt die Datenprozessor Schnittstelle und lädt die Textur.</span><span class="sxs-lookup"><span data-stu-id="d9141-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9141-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9141-119">Requirements</span></span>



| <span data-ttu-id="d9141-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9141-120">Requirement</span></span> | <span data-ttu-id="d9141-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9141-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9141-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9141-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9141-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9141-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d9141-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9141-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9141-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9141-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d9141-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9141-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9141-127">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="d9141-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




