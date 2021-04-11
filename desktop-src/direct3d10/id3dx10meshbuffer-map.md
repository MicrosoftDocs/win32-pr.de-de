---
description: Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer:: Map-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354946"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="f7444-103">ID3DX10MeshBuffer:: Map-Methode</span><span class="sxs-lookup"><span data-stu-id="f7444-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="f7444-104">Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f7444-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7444-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7444-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="f7444-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7444-107">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f7444-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7444-108">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f7444-108">Type: **void\*\***</span></span>

<span data-ttu-id="f7444-109">Zeiger auf die Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="f7444-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="f7444-110">*Psize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f7444-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7444-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7444-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7444-112">Größe des Puffers in Byte.</span><span class="sxs-lookup"><span data-stu-id="f7444-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7444-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7444-113">Return value</span></span>

<span data-ttu-id="f7444-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7444-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7444-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f7444-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7444-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7444-116">Remarks</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7444-117">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="f7444-117">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="f7444-118">Map () in Direct3D 10 entspricht der Ressourcen Zuordnung () in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f7444-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f7444-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7444-119">Requirements</span></span>



| <span data-ttu-id="f7444-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7444-120">Requirement</span></span> | <span data-ttu-id="f7444-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f7444-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7444-122">Header</span><span class="sxs-lookup"><span data-stu-id="f7444-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f7444-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7444-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7444-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7444-124">Library</span></span><br/> | <dl> <span data-ttu-id="f7444-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7444-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7444-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7444-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7444-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="f7444-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="f7444-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f7444-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
