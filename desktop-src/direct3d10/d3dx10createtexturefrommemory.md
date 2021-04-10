---
description: Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: D3DX10CreateTextureFromMemory-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961578"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="ca2e9-103">D3DX10CreateTextureFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca2e9-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="ca2e9-104">Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca2e9-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ca2e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2e9-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ca2e9-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ca2e9-109">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-111">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca2e9-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca2e9-112">Zeiger auf die Ressource im Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-113">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-114">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca2e9-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca2e9-115">Größe der Ressource im Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-116">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-117">Type: **[ **d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca2e9-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="ca2e9-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-118">Optional.</span></span> <span data-ttu-id="ca2e9-119">Gibt die Merkmale einer Textur an (siehe [**d3dx10 \_ Image \_ Load \_ Info**](d3dx10-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-120">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-121">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca2e9-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ca2e9-122">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ca2e9-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="ca2e9-123">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-124">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-125">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="ca2e9-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="ca2e9-126">Adresse eines Zeigers auf die erstellte Ressource.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="ca2e9-127">Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="ca2e9-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e9-128">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca2e9-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e9-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ca2e9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ca2e9-130">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-130">A pointer to the return value.</span></span> <span data-ttu-id="ca2e9-131">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-131">May be **NULL**.</span></span> <span data-ttu-id="ca2e9-132">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2e9-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca2e9-133">Return value</span></span>

<span data-ttu-id="ca2e9-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca2e9-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca2e9-135">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca2e9-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca2e9-136">Remarks</span></span>

<span data-ttu-id="ca2e9-137">Eine Liste der unterstützten Bildformate finden Sie unter [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e9-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2e9-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca2e9-138">Requirements</span></span>



| <span data-ttu-id="ca2e9-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca2e9-139">Requirement</span></span> | <span data-ttu-id="ca2e9-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ca2e9-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2e9-141">Header</span><span class="sxs-lookup"><span data-stu-id="ca2e9-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ca2e9-142"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e9-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca2e9-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca2e9-143">Library</span></span><br/> | <dl> <span data-ttu-id="ca2e9-144"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e9-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2e9-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca2e9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2e9-146">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ca2e9-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="ca2e9-147">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="ca2e9-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
