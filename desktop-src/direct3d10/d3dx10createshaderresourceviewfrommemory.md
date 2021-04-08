---
description: Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: D3DX10CreateShaderResourceViewFromMemory-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761973"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="4f07e-103">D3DX10CreateShaderResourceViewFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f07e-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="4f07e-104">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4f07e-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f07e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f07e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4f07e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f07e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f07e-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="4f07e-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="4f07e-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f07e-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-111">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f07e-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f07e-112">Ein Zeiger auf die Datei im Arbeitsspeicher, die die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="4f07e-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-113">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-114">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f07e-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f07e-115">Größe der Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4f07e-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-116">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-117">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f07e-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="4f07e-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f07e-118">Optional.</span></span> <span data-ttu-id="4f07e-119">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="4f07e-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-120">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-121">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f07e-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="4f07e-122">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4f07e-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="4f07e-123">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f07e-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-124">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-125">Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="4f07e-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="4f07e-126">Adresse eines Zeigers auf die neu erstellte Shader-Ressourcen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="4f07e-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="4f07e-127">Siehe [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="4f07e-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="4f07e-128">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f07e-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f07e-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4f07e-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4f07e-130">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4f07e-130">A pointer to the return value.</span></span> <span data-ttu-id="4f07e-131">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4f07e-131">May be **NULL**.</span></span> <span data-ttu-id="4f07e-132">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4f07e-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f07e-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f07e-133">Return value</span></span>

<span data-ttu-id="4f07e-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f07e-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f07e-135">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="4f07e-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f07e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f07e-136">Requirements</span></span>



| <span data-ttu-id="4f07e-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f07e-137">Requirement</span></span> | <span data-ttu-id="4f07e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="4f07e-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f07e-139">Header</span><span class="sxs-lookup"><span data-stu-id="4f07e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4f07e-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f07e-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4f07e-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f07e-141">Library</span></span><br/> | <dl> <span data-ttu-id="4f07e-142"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f07e-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4f07e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f07e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f07e-144">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="4f07e-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="4f07e-145">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="4f07e-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
