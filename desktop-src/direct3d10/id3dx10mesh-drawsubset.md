---
description: 'ID3DX10Mesh::D rawSubset-Methode: Zeichnet eine Teilmenge eines Gitters.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: ID3DX10Mesh::D rawSubset-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8441bfe4c5d965733a40816ff2def1015f3eb79c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084038"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="4214a-103">ID3DX10Mesh::D rawSubset-Methode</span><span class="sxs-lookup"><span data-stu-id="4214a-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="4214a-104">Zeichnet eine Teilmenge eines Gitters.</span><span class="sxs-lookup"><span data-stu-id="4214a-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4214a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4214a-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="4214a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4214a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4214a-107">*AttribId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4214a-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4214a-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4214a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4214a-109">Gibt an, welche Teilmenge des Gitters ge zeichnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4214a-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="4214a-110">Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als einer oder mehrere Attributgruppen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4214a-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4214a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4214a-111">Return value</span></span>

<span data-ttu-id="4214a-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4214a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4214a-113">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="4214a-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4214a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4214a-114">Remarks</span></span>

<span data-ttu-id="4214a-115">Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4214a-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="4214a-116">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnunget wird.</span><span class="sxs-lookup"><span data-stu-id="4214a-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4214a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4214a-117">Requirements</span></span>



| <span data-ttu-id="4214a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4214a-118">Requirement</span></span> | <span data-ttu-id="4214a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4214a-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4214a-120">Header</span><span class="sxs-lookup"><span data-stu-id="4214a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4214a-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="4214a-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4214a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4214a-122">Library</span></span><br/> | <dl> <span data-ttu-id="4214a-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4214a-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4214a-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4214a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4214a-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="4214a-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="4214a-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4214a-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
