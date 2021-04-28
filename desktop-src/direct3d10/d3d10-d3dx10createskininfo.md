---
description: 'D3DX10CreateSkinInfo-Funktion: Erstellt mithilfe eines Deklarators ein leeres Skin mesh-Objekt.'
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: D3DX10CreateSkinInfo-Funktion (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103598"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="97aca-103">D3DX10CreateSkinInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="97aca-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="97aca-104">Erstellt ein leeres Skin mesh-Objekt mithilfe eines Deklarators.</span><span class="sxs-lookup"><span data-stu-id="97aca-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="97aca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97aca-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="97aca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97aca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97aca-107">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97aca-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97aca-108">Typ: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="97aca-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="97aca-109">Adresse eines Zeigers auf eine [**ID3DX10SkinInfo-Schnittstelle,**](id3dx10skininfo.md)die das erstellte Skin mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="97aca-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97aca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97aca-110">Return value</span></span>

<span data-ttu-id="97aca-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97aca-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97aca-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97aca-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="97aca-113">Wenn die Funktion fehlschlägt, kann der Rückgabewert E \_ OUTOFMEMORY sein.</span><span class="sxs-lookup"><span data-stu-id="97aca-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="97aca-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97aca-114">Remarks</span></span>

<span data-ttu-id="97aca-115">Verwenden Sie [**ID3DX10SkinInfo::SetBoneInfluence,**](id3dx10skininfo-setboneinfluence.md) um das leere Skin mesh-Objekt, das von dieser Methode zurückgegeben wird, zu füllen.</span><span class="sxs-lookup"><span data-stu-id="97aca-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="97aca-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97aca-116">Requirements</span></span>



| <span data-ttu-id="97aca-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97aca-117">Requirement</span></span> | <span data-ttu-id="97aca-118">Wert</span><span class="sxs-lookup"><span data-stu-id="97aca-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97aca-119">Header</span><span class="sxs-lookup"><span data-stu-id="97aca-119">Header</span></span><br/>  | <dl> <span data-ttu-id="97aca-120"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="97aca-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="97aca-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97aca-121">Library</span></span><br/> | <dl> <span data-ttu-id="97aca-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="97aca-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97aca-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97aca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97aca-124">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="97aca-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="97aca-125">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="97aca-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




