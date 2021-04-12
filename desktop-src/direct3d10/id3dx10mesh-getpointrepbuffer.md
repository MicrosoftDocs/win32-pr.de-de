---
description: Gibt den Punkt Rep-Puffer des Netzes an.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh:: getpointrepbuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132349"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="f39df-103">ID3DX10Mesh:: getpointrepbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f39df-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="f39df-104">Gibt den Punkt Rep-Puffer des Netzes an.</span><span class="sxs-lookup"><span data-stu-id="f39df-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f39df-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="f39df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f39df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39df-107">*pppointreps* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f39df-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f39df-108">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f39df-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="f39df-109">Ein Zeiger auf einen Gitter Puffer, der die Punkt-Rep-Daten des Netzes enthält.</span><span class="sxs-lookup"><span data-stu-id="f39df-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="f39df-110">Siehe [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f39df-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39df-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f39df-111">Return value</span></span>

<span data-ttu-id="f39df-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f39df-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f39df-113">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f39df-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f39df-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f39df-114">Requirements</span></span>



| <span data-ttu-id="f39df-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f39df-115">Requirement</span></span> | <span data-ttu-id="f39df-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f39df-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f39df-117">Header</span><span class="sxs-lookup"><span data-stu-id="f39df-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f39df-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f39df-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f39df-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f39df-119">Library</span></span><br/> | <dl> <span data-ttu-id="f39df-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f39df-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f39df-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f39df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39df-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f39df-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f39df-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f39df-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




