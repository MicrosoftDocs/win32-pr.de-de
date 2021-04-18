---
description: Erstellen Sie eine Textur Ressource aus einer Datei.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: D3DX10CreateTextureFromFile-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355023"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="ba712-103">D3DX10CreateTextureFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba712-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="ba712-104">Erstellen Sie eine Textur Ressource aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ba712-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba712-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba712-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ba712-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba712-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba712-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ba712-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ba712-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba712-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ba712-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba712-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba712-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba712-112">Der Name der Datei, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ba712-112">The name of the file containing the resource.</span></span> <span data-ttu-id="ba712-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ba712-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ba712-114">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ba712-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="ba712-115">Eine Liste der unterstützten Bild Dateiformate finden Sie unter [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ba712-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="ba712-116">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba712-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-117">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba712-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="ba712-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba712-118">Optional.</span></span> <span data-ttu-id="ba712-119">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ba712-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ba712-120">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba712-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-121">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba712-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ba712-122">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ba712-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="ba712-123">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba712-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="ba712-124">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ba712-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-125">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="ba712-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="ba712-126">Die Adresse eines Zeigers auf die Textur Ressource (siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="ba712-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="ba712-127">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ba712-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba712-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ba712-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ba712-129">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ba712-129">A pointer to the return value.</span></span> <span data-ttu-id="ba712-130">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ba712-130">May be **NULL**.</span></span> <span data-ttu-id="ba712-131">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ba712-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba712-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba712-132">Return value</span></span>

<span data-ttu-id="ba712-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba712-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba712-134">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ba712-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba712-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba712-135">Remarks</span></span>

<span data-ttu-id="ba712-136">Eine Liste der unterstützten Bildformate finden Sie unter [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="ba712-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba712-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba712-137">Requirements</span></span>



| <span data-ttu-id="ba712-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba712-138">Requirement</span></span> | <span data-ttu-id="ba712-139">Wert</span><span class="sxs-lookup"><span data-stu-id="ba712-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba712-140">Header</span><span class="sxs-lookup"><span data-stu-id="ba712-140">Header</span></span><br/>  | <dl> <span data-ttu-id="ba712-141"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba712-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba712-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba712-142">Library</span></span><br/> | <dl> <span data-ttu-id="ba712-143"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba712-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba712-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba712-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba712-145">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ba712-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="ba712-146">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="ba712-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
