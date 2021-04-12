---
description: Lädt in den Arbeitsspeicher eines komprimierten PRT-Puffers (preberechneten Radiance Transfer), der auf dem Datenträger gespeichert wurde.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: D3DXLoadPRTCompBufferFromFile-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355816"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="53898-103">D3DXLoadPRTCompBufferFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="53898-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="53898-104">Lädt in den Arbeitsspeicher eines komprimierten PRT-Puffers (preberechneten Radiance Transfer), der auf dem Datenträger gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="53898-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="53898-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53898-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="53898-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53898-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53898-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53898-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53898-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53898-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53898-109">Der Name der Datei, aus der die komprimierten Puffer Daten geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53898-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="53898-110">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53898-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53898-111">Typ: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53898-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="53898-112">Adresse eines Zeigers auf das Output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="53898-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53898-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53898-113">Return value</span></span>

<span data-ttu-id="53898-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53898-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53898-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53898-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53898-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="53898-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="53898-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53898-117">Remarks</span></span>

<span data-ttu-id="53898-118">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="53898-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="53898-119">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadPRTCompBufferFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="53898-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="53898-120">Andernfalls wird der Funktions aufrufin D3DXLoadPRTCompBufferFromFileA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="53898-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="53898-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53898-121">Requirements</span></span>



| <span data-ttu-id="53898-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53898-122">Requirement</span></span> | <span data-ttu-id="53898-123">Wert</span><span class="sxs-lookup"><span data-stu-id="53898-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53898-124">Header</span><span class="sxs-lookup"><span data-stu-id="53898-124">Header</span></span><br/>  | <dl> <span data-ttu-id="53898-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53898-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="53898-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53898-126">Library</span></span><br/> | <dl> <span data-ttu-id="53898-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53898-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53898-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53898-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53898-129">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="53898-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
