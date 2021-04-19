---
description: Ruft Informationen zu einer angegebenen Bilddatei im Arbeitsspeicher ab.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: D3DXGetImageInfoFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361204"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="0a67a-103">D3DXGetImageInfoFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a67a-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="0a67a-104">Ruft Informationen zu einer angegebenen Bilddatei im Arbeitsspeicher ab.</span><span class="sxs-lookup"><span data-stu-id="0a67a-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a67a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a67a-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0a67a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a67a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a67a-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a67a-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a67a-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a67a-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a67a-109">VOID-Zeiger auf die Quelldatei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0a67a-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0a67a-110">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a67a-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a67a-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a67a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a67a-112">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0a67a-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="0a67a-113">.</span><span class="sxs-lookup"><span data-stu-id="0a67a-113">.</span></span>

</dd> <dt>

<span data-ttu-id="0a67a-114">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a67a-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a67a-115">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a67a-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="0a67a-116">Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a67a-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a67a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a67a-117">Return value</span></span>

<span data-ttu-id="0a67a-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a67a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a67a-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a67a-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a67a-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="0a67a-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="0a67a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a67a-121">Requirements</span></span>



| <span data-ttu-id="0a67a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a67a-122">Requirement</span></span> | <span data-ttu-id="0a67a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0a67a-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a67a-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a67a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a67a-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a67a-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0a67a-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a67a-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a67a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a67a-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0a67a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a67a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a67a-129">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0a67a-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="0a67a-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="0a67a-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="0a67a-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="0a67a-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
