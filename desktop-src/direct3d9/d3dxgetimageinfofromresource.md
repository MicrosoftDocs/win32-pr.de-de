---
description: 'D3DXGetImageInfoFromResource-Funktion: Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.'
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114448"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="7ce63-103">D3DXGetImageInfoFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ce63-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="7ce63-104">Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="7ce63-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ce63-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ce63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ce63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce63-107">*hSrcModule* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ce63-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce63-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce63-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce63-109">Modul, in das die Ressource geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7ce63-109">Module where the resource is loaded.</span></span> <span data-ttu-id="7ce63-110">Legen Sie diesen Parameter auf **NULL fest,** um das Modul anzugeben, das dem Image zugeordnet ist, das das Betriebssystem zum Erstellen des aktuellen Prozesses verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="7ce63-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="7ce63-111">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ce63-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce63-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce63-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ce63-113">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="7ce63-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="7ce63-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="7ce63-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7ce63-115">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="7ce63-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7ce63-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7ce63-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7ce63-117">*pSrcInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ce63-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce63-118">Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ce63-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="7ce63-119">Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ce63-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce63-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ce63-120">Return value</span></span>

<span data-ttu-id="7ce63-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ce63-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ce63-122">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ce63-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ce63-123">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="7ce63-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="7ce63-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ce63-124">Remarks</span></span>

<span data-ttu-id="7ce63-125">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="7ce63-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7ce63-126">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXGetImageInfoFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="7ce63-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="7ce63-127">Andernfalls wird der Funktionsaufruf in D3DXGetImageInfoFromResourceA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ce63-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce63-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ce63-128">Requirements</span></span>



| <span data-ttu-id="7ce63-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ce63-129">Requirement</span></span> | <span data-ttu-id="7ce63-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7ce63-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce63-131">Header</span><span class="sxs-lookup"><span data-stu-id="7ce63-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7ce63-132"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce63-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7ce63-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ce63-133">Library</span></span><br/> | <dl> <span data-ttu-id="7ce63-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ce63-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7ce63-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ce63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce63-136">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7ce63-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="7ce63-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="7ce63-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="7ce63-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7ce63-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
