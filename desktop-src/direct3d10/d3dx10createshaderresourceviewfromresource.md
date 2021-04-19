---
description: Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: D3DX10CreateShaderResourceViewFromResource-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363984"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="0e08f-103">D3DX10CreateShaderResourceViewFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e08f-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="0e08f-104">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="0e08f-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e08f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e08f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0e08f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e08f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e08f-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0e08f-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0e08f-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e08f-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e08f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e08f-112">Handle für das Ressourcen Modul, das die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="0e08f-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="0e08f-113">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0e08f-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-114">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e08f-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e08f-116">Name der Shader-Ressourcen Ansicht in hsrcmodule.</span><span class="sxs-lookup"><span data-stu-id="0e08f-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="0e08f-117">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0e08f-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0e08f-118">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0e08f-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-119">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-120">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e08f-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="0e08f-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e08f-121">Optional.</span></span> <span data-ttu-id="0e08f-122">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="0e08f-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-123">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-124">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e08f-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0e08f-125">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="0e08f-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="0e08f-126">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e08f-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-127">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-128">Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="0e08f-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="0e08f-129">Adresse eines Zeigers auf die Shader-Ressourcen Ansicht (siehe [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="0e08f-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="0e08f-130">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0e08f-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e08f-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0e08f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0e08f-132">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="0e08f-132">A pointer to the return value.</span></span> <span data-ttu-id="0e08f-133">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0e08f-133">May be **NULL**.</span></span> <span data-ttu-id="0e08f-134">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0e08f-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e08f-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e08f-135">Return value</span></span>

<span data-ttu-id="0e08f-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e08f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e08f-137">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="0e08f-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e08f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e08f-138">Requirements</span></span>



| <span data-ttu-id="0e08f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e08f-139">Requirement</span></span> | <span data-ttu-id="0e08f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="0e08f-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e08f-141">Header</span><span class="sxs-lookup"><span data-stu-id="0e08f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0e08f-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e08f-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0e08f-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e08f-143">Library</span></span><br/> | <dl> <span data-ttu-id="0e08f-144"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e08f-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0e08f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e08f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e08f-146">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0e08f-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="0e08f-147">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e08f-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
