---
description: Durchsucht einen Shader nach einem bestimmten Kommentar. Der Kommentar wird durch einen vierstelligen Code (FourCC) im ersten DWORD-Wert des Kommentars identifiziert.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: D3DXFindShaderComment-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367367"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="38de9-104">D3DXFindShaderComment-Funktion</span><span class="sxs-lookup"><span data-stu-id="38de9-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="38de9-105">Durchsucht einen Shader nach einem bestimmten Kommentar.</span><span class="sxs-lookup"><span data-stu-id="38de9-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="38de9-106">Der Kommentar wird durch einen vierstelligen Code (FourCC) im ersten DWORD-Wert des Kommentars identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38de9-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="38de9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="38de9-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="38de9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="38de9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38de9-109">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38de9-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de9-110">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="38de9-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38de9-111">Zeiger auf den DWORD-Datenstrom der Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="38de9-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="38de9-112">*FourCC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38de9-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de9-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38de9-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38de9-114">FourCC-Code, der den Kommentar Block identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38de9-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="38de9-115">Siehe [FourCC-Formate](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="38de9-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="38de9-116">*ppData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38de9-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38de9-117">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38de9-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38de9-118">Gibt einen Zeiger auf die Kommentar Daten zurück (ohne das Kommentar Token und den FourCC-Code).</span><span class="sxs-lookup"><span data-stu-id="38de9-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="38de9-119">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="38de9-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38de9-120">*psizin Bytes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="38de9-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38de9-121">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38de9-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38de9-122">Gibt die Größe der Kommentar Daten in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="38de9-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="38de9-123">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="38de9-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38de9-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38de9-124">Return value</span></span>

<span data-ttu-id="38de9-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38de9-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38de9-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38de9-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38de9-127">Wenn der Kommentar nicht gefunden wird und kein anderer Fehler aufgetreten ist, wird S \_ false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38de9-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="38de9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38de9-128">Requirements</span></span>



| <span data-ttu-id="38de9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38de9-129">Requirement</span></span> | <span data-ttu-id="38de9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="38de9-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38de9-131">Header</span><span class="sxs-lookup"><span data-stu-id="38de9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="38de9-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="38de9-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="38de9-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38de9-133">Library</span></span><br/> | <dl> <span data-ttu-id="38de9-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38de9-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="38de9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38de9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38de9-136">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="38de9-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
