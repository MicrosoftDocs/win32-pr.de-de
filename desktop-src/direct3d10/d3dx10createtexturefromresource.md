---
description: Erstellen Sie eine Textur aus einer anderen Ressource.
ms.assetid: 9758968a-652f-42bb-8c81-ad7816c57b17
title: D3DX10CreateTextureFromResource-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 22be3b54c7aa9090fd95624a51bc248b01003dcc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364385"
---
# <a name="d3dx10createtexturefromresource-function"></a><span data-ttu-id="787fa-103">D3DX10CreateTextureFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="787fa-103">D3DX10CreateTextureFromResource function</span></span>

<span data-ttu-id="787fa-104">Erstellen Sie eine Textur aus einer anderen Ressource.</span><span class="sxs-lookup"><span data-stu-id="787fa-104">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="787fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="787fa-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromResource(
  _In_  ID3D10Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="787fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="787fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="787fa-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787fa-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="787fa-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="787fa-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="787fa-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="787fa-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787fa-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="787fa-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="787fa-112">Ein Handle für die Quell Ressource.</span><span class="sxs-lookup"><span data-stu-id="787fa-112">A handle to the source resource.</span></span> <span data-ttu-id="787fa-113">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="787fa-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="787fa-114">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787fa-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="787fa-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="787fa-116">Eine Zeichenfolge, die den Namen der Quell Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="787fa-116">A string that contains the name of the source resource.</span></span> <span data-ttu-id="787fa-117">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="787fa-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="787fa-118">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="787fa-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="787fa-119">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787fa-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-120">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="787fa-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="787fa-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="787fa-121">Optional.</span></span> <span data-ttu-id="787fa-122">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="787fa-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="787fa-123">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787fa-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-124">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="787fa-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="787fa-125">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="787fa-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="787fa-126">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="787fa-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="787fa-127">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="787fa-127">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-128">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="787fa-128">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="787fa-129">Die Adresse eines Zeigers auf die Textur Ressource (siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="787fa-129">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="787fa-130">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="787fa-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="787fa-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="787fa-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="787fa-132">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="787fa-132">A pointer to the return value.</span></span> <span data-ttu-id="787fa-133">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="787fa-133">May be **NULL**.</span></span> <span data-ttu-id="787fa-134">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="787fa-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="787fa-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="787fa-135">Return value</span></span>

<span data-ttu-id="787fa-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="787fa-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="787fa-137">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="787fa-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="787fa-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="787fa-138">Remarks</span></span>

<span data-ttu-id="787fa-139">Eine Liste der unterstützten Bildformate finden Sie unter [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="787fa-139">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="787fa-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="787fa-140">Requirements</span></span>



| <span data-ttu-id="787fa-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="787fa-141">Requirement</span></span> | <span data-ttu-id="787fa-142">Wert</span><span class="sxs-lookup"><span data-stu-id="787fa-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="787fa-143">Header</span><span class="sxs-lookup"><span data-stu-id="787fa-143">Header</span></span><br/>  | <dl> <span data-ttu-id="787fa-144"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="787fa-144"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="787fa-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="787fa-145">Library</span></span><br/> | <dl> <span data-ttu-id="787fa-146"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="787fa-146"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="787fa-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="787fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787fa-148">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="787fa-148">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="787fa-149">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="787fa-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
