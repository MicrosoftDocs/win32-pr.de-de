---
description: Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: D3DX10GetImageInfoFromResource-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219467"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="64070-103">D3DX10GetImageInfoFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="64070-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="64070-104">Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="64070-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="64070-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64070-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="64070-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64070-107">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64070-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64070-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64070-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64070-109">Das Modul, in dem die Ressource geladen wird.</span><span class="sxs-lookup"><span data-stu-id="64070-109">Module where the resource is loaded.</span></span> <span data-ttu-id="64070-110">Legen Sie diesen Parameter auf **null** fest, um das Modul anzugeben, das dem Image zugeordnet ist, das vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="64070-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="64070-111">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64070-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64070-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64070-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64070-113">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="64070-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="64070-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64070-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="64070-115">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64070-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="64070-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="64070-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="64070-117">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64070-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64070-118">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="64070-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="64070-119">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="64070-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="64070-120">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="64070-120">Can be **NULL**.</span></span> <span data-ttu-id="64070-121">Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="64070-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="64070-122">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64070-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64070-123">Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="64070-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="64070-124">Zeiger auf eine d3dx10 \_ Image \_ Info-Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64070-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="64070-125">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64070-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64070-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="64070-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="64070-127">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="64070-127">A pointer to the return value.</span></span> <span data-ttu-id="64070-128">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="64070-128">May be **NULL**.</span></span> <span data-ttu-id="64070-129">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="64070-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64070-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64070-130">Return value</span></span>

<span data-ttu-id="64070-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64070-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64070-132">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64070-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64070-133">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="64070-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="64070-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64070-134">Remarks</span></span>

<span data-ttu-id="64070-135">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="64070-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="64070-136">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DX10GetImageInfoFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64070-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="64070-137">Andernfalls wird der Funktions Aufruhe in D3DX10GetImageInfoFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64070-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="64070-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64070-138">Requirements</span></span>



| <span data-ttu-id="64070-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64070-139">Requirement</span></span> | <span data-ttu-id="64070-140">Wert</span><span class="sxs-lookup"><span data-stu-id="64070-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64070-141">Header</span><span class="sxs-lookup"><span data-stu-id="64070-141">Header</span></span><br/>  | <dl> <span data-ttu-id="64070-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="64070-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="64070-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64070-143">Library</span></span><br/> | <dl> <span data-ttu-id="64070-144"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64070-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="64070-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64070-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64070-146">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="64070-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
