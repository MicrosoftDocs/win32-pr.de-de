---
description: Zeichnet eine Teilmenge eines Mesh.
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh::D rawsubset-Methode (D3DX9Mesh. h)
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
ms.openlocfilehash: d0da6e9fc57e0fc5e7b4b263ba3d97185333881c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363131"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="4b34e-103">ID3DXBaseMesh::D rawsubset-Methode</span><span class="sxs-lookup"><span data-stu-id="4b34e-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="4b34e-104">Zeichnet eine Teilmenge eines Mesh.</span><span class="sxs-lookup"><span data-stu-id="4b34e-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b34e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b34e-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="4b34e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b34e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b34e-107">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b34e-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b34e-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b34e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b34e-109">DWORD, das angibt, welche Teilmenge des Mesh gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b34e-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="4b34e-110">Dieser Wert wird verwendet, um Gesichter in einem Mesh als zu einer oder mehreren Attribut Gruppen gehörenden zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4b34e-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b34e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b34e-111">Return value</span></span>

<span data-ttu-id="4b34e-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b34e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b34e-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b34e-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4b34e-114">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="4b34e-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b34e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b34e-115">Remarks</span></span>

<span data-ttu-id="4b34e-116">Die von atpubid angegebene Teilmenge wird von der [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) -Methode mit dem D3DPT- \_ Typ "testanglelist" gerendert, sodass ein Index Puffer ordnungsgemäß initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4b34e-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="4b34e-117">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4b34e-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="4b34e-118">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner (*atungbid*) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4b34e-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b34e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b34e-119">Requirements</span></span>



| <span data-ttu-id="4b34e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b34e-120">Requirement</span></span> | <span data-ttu-id="4b34e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4b34e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b34e-122">Header</span><span class="sxs-lookup"><span data-stu-id="4b34e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4b34e-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b34e-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4b34e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b34e-124">Library</span></span><br/> | <dl> <span data-ttu-id="4b34e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b34e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b34e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b34e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b34e-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="4b34e-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
