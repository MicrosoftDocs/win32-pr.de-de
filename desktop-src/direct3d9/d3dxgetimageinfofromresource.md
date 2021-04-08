---
description: Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762042"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="0faa7-103">D3DXGetImageInfoFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="0faa7-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="0faa7-104">Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="0faa7-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0faa7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0faa7-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0faa7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0faa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0faa7-107">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0faa7-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faa7-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0faa7-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0faa7-109">Das Modul, in dem die Ressource geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0faa7-109">Module where the resource is loaded.</span></span> <span data-ttu-id="0faa7-110">Legen Sie diesen Parameter auf **null** fest, um das Modul anzugeben, das dem Image zugeordnet ist, das vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0faa7-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="0faa7-111">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0faa7-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faa7-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0faa7-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0faa7-113">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="0faa7-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="0faa7-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0faa7-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0faa7-115">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0faa7-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0faa7-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="0faa7-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0faa7-117">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0faa7-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faa7-118">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0faa7-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="0faa7-119">Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0faa7-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0faa7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0faa7-120">Return value</span></span>

<span data-ttu-id="0faa7-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0faa7-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0faa7-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0faa7-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0faa7-123">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="0faa7-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="0faa7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0faa7-124">Remarks</span></span>

<span data-ttu-id="0faa7-125">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="0faa7-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0faa7-126">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXGetImageInfoFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0faa7-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="0faa7-127">Andernfalls wird der Funktions Aufruhe in D3DXGetImageInfoFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0faa7-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0faa7-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0faa7-128">Requirements</span></span>



| <span data-ttu-id="0faa7-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0faa7-129">Requirement</span></span> | <span data-ttu-id="0faa7-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0faa7-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0faa7-131">Header</span><span class="sxs-lookup"><span data-stu-id="0faa7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0faa7-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0faa7-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0faa7-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0faa7-133">Library</span></span><br/> | <dl> <span data-ttu-id="0faa7-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0faa7-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0faa7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0faa7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faa7-136">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0faa7-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="0faa7-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="0faa7-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="0faa7-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="0faa7-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
