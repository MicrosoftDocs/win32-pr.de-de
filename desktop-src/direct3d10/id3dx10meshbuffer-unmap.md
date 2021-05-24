---
description: Aufheben der Zuordnung eines Puffers.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: ID3DX10MeshBuffer::Unmap-Methode (D3DX10.h)
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
ms.openlocfilehash: 11b15f8bc1e4103503b183672ebd31e92b4daea7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335374"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="af6e6-103">ID3DX10MeshBuffer::Unmap-Methode</span><span class="sxs-lookup"><span data-stu-id="af6e6-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="af6e6-104">Aufheben der Zuordnung eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="af6e6-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af6e6-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="af6e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af6e6-106">Parameters</span></span>

<span data-ttu-id="af6e6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="af6e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af6e6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af6e6-108">Return value</span></span>

<span data-ttu-id="af6e6-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af6e6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af6e6-110">Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.</span><span class="sxs-lookup"><span data-stu-id="af6e6-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af6e6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af6e6-111">Remarks</span></span>



<span data-ttu-id="af6e6-112">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="af6e6-112">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="af6e6-113">Unmap() in Direct3D 10 entspricht der Ressource Unlock() in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="af6e6-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="af6e6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af6e6-114">Requirements</span></span>



| <span data-ttu-id="af6e6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af6e6-115">Requirement</span></span> | <span data-ttu-id="af6e6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="af6e6-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af6e6-117">Header</span><span class="sxs-lookup"><span data-stu-id="af6e6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af6e6-118"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="af6e6-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="af6e6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af6e6-119">Library</span></span><br/> | <dl> <span data-ttu-id="af6e6-120"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="af6e6-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6e6-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="af6e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6e6-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="af6e6-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="af6e6-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="af6e6-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




