---
description: Beschreibt ein gesperrtes Feld (Volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219568"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="188ff-103">D3DLOCKED \_ Box-Struktur</span><span class="sxs-lookup"><span data-stu-id="188ff-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="188ff-104">Beschreibt ein gesperrtes Feld (Volume).</span><span class="sxs-lookup"><span data-stu-id="188ff-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="188ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="188ff-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="188ff-106">Member</span><span class="sxs-lookup"><span data-stu-id="188ff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="188ff-107">**Rowpitch**</span><span class="sxs-lookup"><span data-stu-id="188ff-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="188ff-108">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="188ff-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="188ff-109">Byte Offset vom linken Rand einer Zeile bis zum linken Rand der nächsten Zeile.</span><span class="sxs-lookup"><span data-stu-id="188ff-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="188ff-110">**Slicepitch**</span><span class="sxs-lookup"><span data-stu-id="188ff-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="188ff-111">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="188ff-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="188ff-112">Der Byte Offset von der linken oberen Ecke eines Slice bis zum oberen linken Rand des nächst tiefsten Slice.</span><span class="sxs-lookup"><span data-stu-id="188ff-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="188ff-113">**PBITS**</span><span class="sxs-lookup"><span data-stu-id="188ff-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="188ff-114">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="188ff-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="188ff-115">Zeiger auf den Anfang des volumefelds.</span><span class="sxs-lookup"><span data-stu-id="188ff-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="188ff-116">Wenn ein [**D3DBOX**](d3dbox.md) für den Lockbox-Befehl bereitgestellt wurde, ist PBITS entsprechend vom Start des Volumes abweicht.</span><span class="sxs-lookup"><span data-stu-id="188ff-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="188ff-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="188ff-117">Remarks</span></span>

<span data-ttu-id="188ff-118">Volumes können so visualisiert werden, dass Sie in Slices der Breite x Höhe 2D-Oberflächen angeordnet sind, um ein Volume mit einer Breite x-Tiefe zu bilden.</span><span class="sxs-lookup"><span data-stu-id="188ff-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="188ff-119">Weitere Informationen finden Sie unter [volumetextur-Ressourcen (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="188ff-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="188ff-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="188ff-120">Requirements</span></span>



| <span data-ttu-id="188ff-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="188ff-121">Requirement</span></span> | <span data-ttu-id="188ff-122">Wert</span><span class="sxs-lookup"><span data-stu-id="188ff-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="188ff-123">Header</span><span class="sxs-lookup"><span data-stu-id="188ff-123">Header</span></span><br/> | <dl> <span data-ttu-id="188ff-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="188ff-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="188ff-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="188ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188ff-126">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="188ff-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="188ff-127">**IDirect3DVolume9:: Lockbox**</span><span class="sxs-lookup"><span data-stu-id="188ff-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="188ff-128">**IDirect3DVolumeTexture9:: Lockbox**</span><span class="sxs-lookup"><span data-stu-id="188ff-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
