---
description: Beschreibt ein von einer Instanz von ID3DXRenderToEnvMap verwendetes Renderziel von einem Bildschirm.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: D3DXRTE_DESC-Struktur (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219501"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="59bc7-103">D3DXRTE- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="59bc7-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="59bc7-104">Beschreibt ein von einer Instanz von [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)verwendetes Renderziel von einem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="59bc7-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59bc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59bc7-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="59bc7-106">Member</span><span class="sxs-lookup"><span data-stu-id="59bc7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="59bc7-107">**Größe**</span><span class="sxs-lookup"><span data-stu-id="59bc7-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="59bc7-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59bc7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="59bc7-109">Breite und Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="59bc7-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="59bc7-110">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="59bc7-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="59bc7-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59bc7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="59bc7-112">Maximale Detailebene (LOD).</span><span class="sxs-lookup"><span data-stu-id="59bc7-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="59bc7-113">**Format**</span><span class="sxs-lookup"><span data-stu-id="59bc7-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="59bc7-114">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="59bc7-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="59bc7-115">Farb Puffer Format.</span><span class="sxs-lookup"><span data-stu-id="59bc7-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="59bc7-116">**Depthstencil**</span><span class="sxs-lookup"><span data-stu-id="59bc7-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="59bc7-117">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59bc7-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="59bc7-118">Gibt an, ob der z-Puffer benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="59bc7-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="59bc7-119">**Depthstencilformat**</span><span class="sxs-lookup"><span data-stu-id="59bc7-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="59bc7-120">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="59bc7-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="59bc7-121">Das Format des tiefen Puffers.</span><span class="sxs-lookup"><span data-stu-id="59bc7-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59bc7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59bc7-122">Remarks</span></span>

<span data-ttu-id="59bc7-123">Diese Methode wird zum Zurückgeben der Erstellungs Parameter verwendet, die beim Erstellen eines [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) -Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59bc7-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="59bc7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59bc7-124">Requirements</span></span>



| <span data-ttu-id="59bc7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59bc7-125">Requirement</span></span> | <span data-ttu-id="59bc7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="59bc7-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59bc7-127">Header</span><span class="sxs-lookup"><span data-stu-id="59bc7-127">Header</span></span><br/> | <dl> <span data-ttu-id="59bc7-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="59bc7-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bc7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59bc7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bc7-130">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="59bc7-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
