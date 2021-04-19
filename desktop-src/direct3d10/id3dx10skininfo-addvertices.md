---
description: Zuweisen von Speicherplatz für weitere Scheitel Punkte.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'ID3DX10SkinInfo:: addvertices-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357284"
---
# <a name="id3dx10skininfoaddvertices-method"></a><span data-ttu-id="793dc-103">ID3DX10SkinInfo:: addvertices-Methode</span><span class="sxs-lookup"><span data-stu-id="793dc-103">ID3DX10SkinInfo::AddVertices method</span></span>

<span data-ttu-id="793dc-104">Zuweisen von Speicherplatz für weitere Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="793dc-104">Allocate space for additional vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="793dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="793dc-105">Syntax</span></span>


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="793dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="793dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="793dc-107">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="793dc-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793dc-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="793dc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="793dc-109">Die Anzahl der hinzu zufügenden Vertices.</span><span class="sxs-lookup"><span data-stu-id="793dc-109">The number of vertices to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="793dc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="793dc-110">Return value</span></span>

<span data-ttu-id="793dc-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="793dc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="793dc-112">Wenn diese Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="793dc-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="793dc-113">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="793dc-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="793dc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="793dc-114">Requirements</span></span>



| <span data-ttu-id="793dc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="793dc-115">Requirement</span></span> | <span data-ttu-id="793dc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="793dc-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="793dc-117">Header</span><span class="sxs-lookup"><span data-stu-id="793dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="793dc-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="793dc-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="793dc-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="793dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="793dc-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="793dc-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793dc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="793dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793dc-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="793dc-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="793dc-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="793dc-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
