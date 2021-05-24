---
description: Sie erhalten einen Zeiger auf den Gitternetzpufferspeicher, um dessen Inhalt zu ändern.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: ID3DX10MeshBuffer::Map-Methode (D3DX10.h)
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
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335354"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="48297-103">ID3DX10MeshBuffer::Map-Methode</span><span class="sxs-lookup"><span data-stu-id="48297-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="48297-104">Sie erhalten einen Zeiger auf den Gitternetzpufferspeicher, um dessen Inhalt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="48297-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="48297-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48297-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="48297-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48297-107">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48297-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48297-108">Typ: **\* \* void**</span><span class="sxs-lookup"><span data-stu-id="48297-108">Type: **void\*\***</span></span>

<span data-ttu-id="48297-109">Zeiger auf die Pufferdaten.</span><span class="sxs-lookup"><span data-stu-id="48297-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="48297-110">*pSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48297-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48297-111">Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48297-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48297-112">Größe des Puffers in Byte.</span><span class="sxs-lookup"><span data-stu-id="48297-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48297-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48297-113">Return value</span></span>

<span data-ttu-id="48297-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48297-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48297-115">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="48297-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48297-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48297-116">Remarks</span></span>



 <span data-ttu-id="48297-117">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="48297-117">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="48297-118">Map() in Direct3D 10 entspricht der Ressourcenzuordnung () in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="48297-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="48297-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48297-119">Requirements</span></span>



| <span data-ttu-id="48297-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48297-120">Requirement</span></span> | <span data-ttu-id="48297-121">Wert</span><span class="sxs-lookup"><span data-stu-id="48297-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48297-122">Header</span><span class="sxs-lookup"><span data-stu-id="48297-122">Header</span></span><br/>  | <dl> <span data-ttu-id="48297-123"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="48297-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="48297-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48297-124">Library</span></span><br/> | <dl> <span data-ttu-id="48297-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="48297-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48297-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="48297-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48297-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="48297-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="48297-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="48297-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
