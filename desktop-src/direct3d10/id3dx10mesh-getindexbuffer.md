---
description: 'ID3DX10Mesh::GetIndexBuffer-Methode: Ruft die Daten in einem Indexpuffer ab.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: ID3DX10Mesh::GetIndexBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084028"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="60b12-103">ID3DX10Mesh::GetIndexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="60b12-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="60b12-104">Ruft die Daten in einem Indexpuffer ab.</span><span class="sxs-lookup"><span data-stu-id="60b12-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b12-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="60b12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60b12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b12-107">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60b12-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b12-108">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="60b12-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="60b12-109">Adresse eines Zeigers auf eine ID3DX10MeshBuffer-Schnittstelle, die den Indexpuffer darstellt, der dem Gitternetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="60b12-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b12-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60b12-110">Return value</span></span>

<span data-ttu-id="60b12-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60b12-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60b12-112">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="60b12-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60b12-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b12-113">Requirements</span></span>



| <span data-ttu-id="60b12-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b12-114">Requirement</span></span> | <span data-ttu-id="60b12-115">Wert</span><span class="sxs-lookup"><span data-stu-id="60b12-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b12-116">Header</span><span class="sxs-lookup"><span data-stu-id="60b12-116">Header</span></span><br/>  | <dl> <span data-ttu-id="60b12-117"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="60b12-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="60b12-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60b12-118">Library</span></span><br/> | <dl> <span data-ttu-id="60b12-119"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="60b12-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b12-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60b12-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b12-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="60b12-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="60b12-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60b12-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




