---
description: Zeichnet eine Teilmenge eines Mesh.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: ID3DX10Mesh::D rawsubset-Methode (d3dx10. h)
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
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365095"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="3f120-103">ID3DX10Mesh::D rawsubset-Methode</span><span class="sxs-lookup"><span data-stu-id="3f120-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="3f120-104">Zeichnet eine Teilmenge eines Mesh.</span><span class="sxs-lookup"><span data-stu-id="3f120-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f120-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f120-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="3f120-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f120-107">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f120-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f120-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f120-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f120-109">Gibt an, welche Teilmenge des Mesh gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f120-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="3f120-110">Dieser Wert wird verwendet, um Gesichter in einem Mesh als zu einer oder mehreren Attribut Gruppen gehörenden zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="3f120-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f120-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f120-111">Return value</span></span>

<span data-ttu-id="3f120-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f120-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f120-113">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3f120-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f120-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f120-114">Remarks</span></span>

<span data-ttu-id="3f120-115">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3f120-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="3f120-116">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner (atungbid) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f120-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f120-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f120-117">Requirements</span></span>



| <span data-ttu-id="3f120-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f120-118">Requirement</span></span> | <span data-ttu-id="3f120-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3f120-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f120-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f120-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3f120-121"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f120-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f120-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f120-122">Library</span></span><br/> | <dl> <span data-ttu-id="3f120-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f120-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f120-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f120-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f120-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3f120-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3f120-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3f120-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
