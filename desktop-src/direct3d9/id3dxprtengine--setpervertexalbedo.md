---
description: Legt einen Albedo-Wert für jeden Gitter Scheitelpunkt fest, wobei vorherige Albedo-Werte überschrieben werden.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine:: setpervertexalbedo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361218"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="2e16c-103">ID3DXPRTEngine:: setpervertexalbedo-Methode</span><span class="sxs-lookup"><span data-stu-id="2e16c-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="2e16c-104">Legt einen Albedo-Wert für jeden Gitter Scheitelpunkt fest, wobei vorherige Albedo-Werte überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2e16c-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e16c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e16c-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="2e16c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e16c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e16c-107">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e16c-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e16c-108">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="2e16c-108">Type: **const VOID\***</span></span>

<span data-ttu-id="2e16c-109">Zeiger auf float Albedo-Daten des ersten Beispiels.</span><span class="sxs-lookup"><span data-stu-id="2e16c-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="2e16c-110">*Numchannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e16c-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e16c-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e16c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e16c-112">Anzahl der festzulegenden Farbkanäle.</span><span class="sxs-lookup"><span data-stu-id="2e16c-112">Number of color channels to set.</span></span> <span data-ttu-id="2e16c-113">Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2e16c-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="2e16c-114">*Stride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e16c-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e16c-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e16c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e16c-116">Der Schritt in Bytes, der benötigt wird, um den Albedo-Wert des nächsten Beispiels zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e16c-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="2e16c-117">Siehe [Breite und Tonhöhe (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="2e16c-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e16c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e16c-118">Return value</span></span>

<span data-ttu-id="2e16c-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e16c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e16c-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e16c-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2e16c-121">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="2e16c-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e16c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e16c-122">Requirements</span></span>



| <span data-ttu-id="2e16c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e16c-123">Requirement</span></span> | <span data-ttu-id="2e16c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2e16c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e16c-125">Header</span><span class="sxs-lookup"><span data-stu-id="2e16c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e16c-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e16c-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2e16c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e16c-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e16c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e16c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e16c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e16c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e16c-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="2e16c-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
