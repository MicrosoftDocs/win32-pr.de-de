---
description: Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: D3DX10CreateShaderResourceViewFromFile-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394161"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="f441e-103">D3DX10CreateShaderResourceViewFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="f441e-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="f441e-104">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="f441e-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f441e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f441e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="f441e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f441e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f441e-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f441e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="f441e-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="f441e-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f441e-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f441e-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f441e-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f441e-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f441e-112">Der Name der Datei, die die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="f441e-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="f441e-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f441e-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f441e-114">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f441e-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f441e-115">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f441e-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-116">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f441e-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="f441e-117">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="f441e-117">Optional.</span></span> <span data-ttu-id="f441e-118">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f441e-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f441e-119">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f441e-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-120">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="f441e-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="f441e-121">Zeiger auf eine Thread-Pump-Schnittstelle (siehe [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="f441e-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="f441e-122">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f441e-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="f441e-123">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f441e-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-124">Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="f441e-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="f441e-125">Adresse eines Zeigers auf die Shader-Ressourcen Ansicht (siehe [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="f441e-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="f441e-126">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f441e-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f441e-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="f441e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="f441e-128">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f441e-128">A pointer to the return value.</span></span> <span data-ttu-id="f441e-129">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f441e-129">May be **NULL**.</span></span> <span data-ttu-id="f441e-130">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f441e-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f441e-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f441e-131">Return value</span></span>

<span data-ttu-id="f441e-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f441e-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f441e-133">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f441e-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f441e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f441e-134">Remarks</span></span>

<span data-ttu-id="f441e-135">Eine Liste der unterstützten Bildformate finden Sie unter [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="f441e-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f441e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f441e-136">Requirements</span></span>



| <span data-ttu-id="f441e-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f441e-137">Requirement</span></span> | <span data-ttu-id="f441e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f441e-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f441e-139">Header</span><span class="sxs-lookup"><span data-stu-id="f441e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="f441e-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f441e-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f441e-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f441e-141">Library</span></span><br/> | <dl> <span data-ttu-id="f441e-142"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f441e-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f441e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f441e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f441e-144">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="f441e-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="f441e-145">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="f441e-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
