---
title: D3DX11GetImageInfoFromResource-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle der Verwendung dieser Funktion Ressourcen Funktionen verwenden und dann die directxtex-Bibliothek (Tools), loadfromxxxmemory (wobei xxx für WIC, DDS oder TGA verwendet wird) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- D3DX11GetImageInfoFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982329"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="1060f-106">D3DX11GetImageInfoFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="1060f-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="1060f-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1060f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="1060f-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, [Ressourcen Funktionen](/windows/desktop/menurc/resources-functions)zu verwenden und anschließend die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek (Tools), **loadfromxxxmemory** (wobei xxx für WIC, DDS oder TGA steht) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="1060f-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="1060f-109">Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="1060f-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1060f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1060f-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="1060f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1060f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1060f-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1060f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1060f-113">Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1060f-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1060f-114">Das Modul, in dem die Ressource geladen wird.</span><span class="sxs-lookup"><span data-stu-id="1060f-114">Module where the resource is loaded.</span></span> <span data-ttu-id="1060f-115">Legen Sie diesen Parameter auf **null** fest, um das Modul anzugeben, das dem Image zugeordnet ist, das vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1060f-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="1060f-116">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1060f-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1060f-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1060f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1060f-118">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="1060f-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="1060f-119">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="1060f-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1060f-120">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="1060f-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="1060f-121">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1060f-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1060f-122">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1060f-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1060f-123">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1060f-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="1060f-124">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="1060f-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="1060f-125">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1060f-125">Can be **NULL**.</span></span> <span data-ttu-id="1060f-126">Siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="1060f-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="1060f-127">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1060f-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1060f-128">Type: **[ **Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1060f-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="1060f-129">Zeiger auf eine Bibliothek d3dx11 \_ Image \_ Info-Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1060f-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="1060f-130">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1060f-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1060f-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1060f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1060f-132">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1060f-132">A pointer to the return value.</span></span> <span data-ttu-id="1060f-133">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1060f-133">May be **NULL**.</span></span> <span data-ttu-id="1060f-134">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1060f-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1060f-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1060f-135">Return value</span></span>

<span data-ttu-id="1060f-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1060f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1060f-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1060f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1060f-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="1060f-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="1060f-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1060f-139">Remarks</span></span>

<span data-ttu-id="1060f-140">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="1060f-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1060f-141">Wenn Unicode definiert ist, wird der Funktions aufrufin **D3DX11GetImageInfoFromResourceW** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="1060f-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="1060f-142">Andernfalls wird der Funktions Aufruhe in **D3DX11GetImageInfoFromResourceA** aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1060f-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1060f-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1060f-143">Requirements</span></span>



| <span data-ttu-id="1060f-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1060f-144">Requirement</span></span> | <span data-ttu-id="1060f-145">Wert</span><span class="sxs-lookup"><span data-stu-id="1060f-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1060f-146">Header</span><span class="sxs-lookup"><span data-stu-id="1060f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="1060f-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1060f-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1060f-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1060f-148">Library</span></span><br/> | <dl> <span data-ttu-id="1060f-149"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1060f-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1060f-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1060f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1060f-151">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1060f-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

