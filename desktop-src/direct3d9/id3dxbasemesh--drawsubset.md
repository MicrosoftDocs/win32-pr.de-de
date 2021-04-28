---
description: 'ID3DXBaseMesh::D rawSubset-Methode: Zeichnet eine Teilmenge eines Gitters.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh::D rawSubset-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115468"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="8dac8-103">ID3DXBaseMesh::D rawSubset-Methode</span><span class="sxs-lookup"><span data-stu-id="8dac8-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="8dac8-104">Zeichnet eine Teilmenge eines Gitters.</span><span class="sxs-lookup"><span data-stu-id="8dac8-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dac8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dac8-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="8dac8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dac8-107">*AttribId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8dac8-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dac8-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dac8-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dac8-109">DWORD, das angibt, welche Teilmenge des Gitters ge zeichnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dac8-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="8dac8-110">Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als einer oder mehrere Attributgruppen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8dac8-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dac8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8dac8-111">Return value</span></span>

<span data-ttu-id="8dac8-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8dac8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8dac8-113">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8dac8-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8dac8-114">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="8dac8-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dac8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dac8-115">Remarks</span></span>

<span data-ttu-id="8dac8-116">Die von AttribId angegebene Teilmenge wird von der [**IDirect3DDevice9::D rawIndexedPrimitive-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) mithilfe des primitiven D3DPT TRIANGLELIST-Typs gerendert, sodass ein Indexpuffer ordnungsgemäß initialisiert werden \_ muss.</span><span class="sxs-lookup"><span data-stu-id="8dac8-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="8dac8-117">Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8dac8-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="8dac8-118">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (*AttribId*) gezeichnunget wird.</span><span class="sxs-lookup"><span data-stu-id="8dac8-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dac8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dac8-119">Requirements</span></span>



| <span data-ttu-id="8dac8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dac8-120">Requirement</span></span> | <span data-ttu-id="8dac8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8dac8-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dac8-122">Header</span><span class="sxs-lookup"><span data-stu-id="8dac8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8dac8-123"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8dac8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8dac8-124">Library</span></span><br/> | <dl> <span data-ttu-id="8dac8-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8dac8-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8dac8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dac8-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="8dac8-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
