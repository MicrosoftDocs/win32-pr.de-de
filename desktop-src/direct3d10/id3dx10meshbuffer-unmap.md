---
description: Aufheben der Zuordnung eines Puffers.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'ID3DX10MeshBuffer:: unmap-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370478"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="56e62-103">ID3DX10MeshBuffer:: unmap-Methode</span><span class="sxs-lookup"><span data-stu-id="56e62-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="56e62-104">Aufheben der Zuordnung eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="56e62-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e62-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="56e62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e62-106">Parameters</span></span>

<span data-ttu-id="56e62-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56e62-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56e62-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56e62-108">Return value</span></span>

<span data-ttu-id="56e62-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56e62-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56e62-110">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="56e62-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56e62-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e62-111">Remarks</span></span>



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e62-112">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="56e62-112">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="56e62-113">Unmap () in Direct3D 10 entspricht der Ressourcen Sperre () in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="56e62-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56e62-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e62-114">Requirements</span></span>



| <span data-ttu-id="56e62-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56e62-115">Requirement</span></span> | <span data-ttu-id="56e62-116">Wert</span><span class="sxs-lookup"><span data-stu-id="56e62-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56e62-117">Header</span><span class="sxs-lookup"><span data-stu-id="56e62-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56e62-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e62-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="56e62-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56e62-119">Library</span></span><br/> | <dl> <span data-ttu-id="56e62-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56e62-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e62-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e62-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="56e62-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="56e62-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="56e62-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




