---
description: Legen Sie Scheitelpunkt Daten auf einen der Vertex-Puffer des Netzes fest.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh:: setvertexdata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367467"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="1d4ff-103">ID3DX10Mesh:: setvertexdata-Methode</span><span class="sxs-lookup"><span data-stu-id="1d4ff-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="1d4ff-104">Legen Sie Scheitelpunkt Daten auf einen der Vertex-Puffer des Netzes fest.</span><span class="sxs-lookup"><span data-stu-id="1d4ff-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d4ff-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="1d4ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4ff-107">*ibuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d4ff-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4ff-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d4ff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d4ff-109">Der Vertex-Puffer, der mit pData aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d4ff-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="1d4ff-110">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d4ff-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4ff-111">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="1d4ff-111">Type: **const void\***</span></span>

<span data-ttu-id="1d4ff-112">Die festzulegenden Vertex-Daten.</span><span class="sxs-lookup"><span data-stu-id="1d4ff-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4ff-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d4ff-113">Return value</span></span>

<span data-ttu-id="1d4ff-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d4ff-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d4ff-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1d4ff-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4ff-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4ff-116">Requirements</span></span>



| <span data-ttu-id="1d4ff-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d4ff-117">Requirement</span></span> | <span data-ttu-id="1d4ff-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4ff-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4ff-119">Header</span><span class="sxs-lookup"><span data-stu-id="1d4ff-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1d4ff-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4ff-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d4ff-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d4ff-121">Library</span></span><br/> | <dl> <span data-ttu-id="1d4ff-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d4ff-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4ff-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d4ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4ff-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="1d4ff-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="1d4ff-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1d4ff-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
