---
description: Lädt einen PRT-Puffer (preberechneten Radiance Transfer) in den Arbeitsspeicher, der auf dem Datenträger gespeichert wurde.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: D3DXLoadPRTBufferFromFile-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354226"
---
# <a name="d3dxloadprtbufferfromfile-function"></a><span data-ttu-id="19f0e-103">D3DXLoadPRTBufferFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="19f0e-103">D3DXLoadPRTBufferFromFile function</span></span>

<span data-ttu-id="19f0e-104">Lädt einen PRT-Puffer (preberechneten Radiance Transfer) in den Arbeitsspeicher, der auf dem Datenträger gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="19f0e-104">Loads into memory a precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f0e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="19f0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19f0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f0e-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19f0e-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19f0e-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19f0e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19f0e-109">Der Name der Datei, aus der die Puffer Daten geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19f0e-109">Name of the file from which to load the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="19f0e-110">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="19f0e-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19f0e-111">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="19f0e-111">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="19f0e-112">Adresse eines Zeigers auf das Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="19f0e-112">Address of a pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f0e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19f0e-113">Return value</span></span>

<span data-ttu-id="19f0e-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19f0e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19f0e-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19f0e-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19f0e-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="19f0e-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f0e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19f0e-117">Remarks</span></span>

<span data-ttu-id="19f0e-118">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="19f0e-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="19f0e-119">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadPRTBufferFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="19f0e-119">If Unicode is defined, the function call resolves to D3DXLoadPRTBufferFromFileW.</span></span> <span data-ttu-id="19f0e-120">Andernfalls wird der Funktions aufrufin D3DXLoadPRTBufferFromFileA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="19f0e-120">Otherwise, the function call resolves to D3DXLoadPRTBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f0e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19f0e-121">Requirements</span></span>



| <span data-ttu-id="19f0e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19f0e-122">Requirement</span></span> | <span data-ttu-id="19f0e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="19f0e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19f0e-124">Header</span><span class="sxs-lookup"><span data-stu-id="19f0e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="19f0e-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f0e-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19f0e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19f0e-126">Library</span></span><br/> | <dl> <span data-ttu-id="19f0e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19f0e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19f0e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f0e-129">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="19f0e-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
