---
description: Beschreibt einen Index Puffer.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961632"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="d4d73-103">D3DINDEXBUFFER- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="d4d73-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="d4d73-104">Beschreibt einen Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="d4d73-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d73-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="d4d73-106">Member</span><span class="sxs-lookup"><span data-stu-id="d4d73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4d73-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="d4d73-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="d4d73-108">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d73-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d73-109">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format der Index Puffer Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d4d73-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="d4d73-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="d4d73-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d4d73-111">Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d73-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d73-112">Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Index Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4d73-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d4d73-113">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="d4d73-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d4d73-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d73-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d73-115">Kombination aus einem oder mehreren der folgenden Flags, die die Verwendung für diese Ressource angeben.</span><span class="sxs-lookup"><span data-stu-id="d4d73-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="d4d73-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d73-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="d4d73-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d4d73-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="d4d73-118"><dt>**D3DUSAGE \_ DoNotClip**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="d4d73-119">Legen Sie fest, um anzugeben, dass der Inhalt des Index Puffers nie abgeschnitten werden muss.</span><span class="sxs-lookup"><span data-stu-id="d4d73-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="d4d73-120"><dt>**D3DUSAGE \_ dynamisch**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="d4d73-121">Legen Sie fest, um anzugeben, dass der Index Puffer eine dynamische Arbeitsspeicher Verwendung erfordert.</span><span class="sxs-lookup"><span data-stu-id="d4d73-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="d4d73-122">Dies ist für Treiber nützlich, da Sie dadurch entscheiden können, wo der Puffer platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d73-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="d4d73-123">Im Allgemeinen werden statische Index Puffer in den Videospeicher eingefügt, und dynamische Index Puffer werden im AGP-Speicher abgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4d73-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="d4d73-124">Beachten Sie, dass es keine separate statische Verwendung gibt. Wenn Sie D3DUSAGE Dynamic nicht angeben, \_ wird der Index Puffer statisch gemacht.</span><span class="sxs-lookup"><span data-stu-id="d4d73-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="d4d73-125">D3DUSAGE \_ Dynamic wird streng durch die \_ Sperr Flags D3DLOCK verwerfen und D3DLOCK \_ noüberschreibung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="d4d73-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="d4d73-126">Daher \_ sind D3DLOCK DISCARD und D3DLOCK \_ noüberschreibung nur für Index Puffer gültig, die mit D3DUSAGE Dynamic erstellt wurden \_ . Sie sind keine gültigen Flags für statische Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="d4d73-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="d4d73-127">Weitere Informationen zur Verwendung dynamischer Index Puffer finden Sie unter [Verwenden von dynamischen Scheitelpunkt-und Index Puffern](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="d4d73-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="d4d73-128">Beachten Sie, dass D3DUSAGE \_ Dynamic nicht für verwaltete Index Puffer angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4d73-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="d4d73-129">Weitere Informationen finden Sie unter [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d4d73-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="d4d73-130"><dt>**D3DUSAGE \_ rtpatches**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="d4d73-131">Legen Sie fest, um anzugeben, wann der Index Puffer zum Zeichnen von grundlegenden primitiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d73-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="d4d73-132"><dt>**D3DUSAGE \_ npatches**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="d4d73-133">Legen Sie fest, um anzugeben, wann der Index Puffer zum Zeichnen von N-Patches verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d73-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="d4d73-134"><dt>**D3DUSAGE \_ Punkte**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="d4d73-135">Legen Sie fest, um anzugeben, wann der Index Puffer für Zeichnungs Punkt Sprites oder indizierte Punkt Listen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d73-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="d4d73-136"><dt>**D3DUSAGE \_ softwareprocessing**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="d4d73-137">Legen Sie fest, um anzugeben, dass der Puffer mit der Software Verarbeitung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d73-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="d4d73-138"><dt>**D3DUSAGE \_ schreiben**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="d4d73-139">Informiert das System, dass die Anwendung nur in den Index Puffer schreibt.</span><span class="sxs-lookup"><span data-stu-id="d4d73-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="d4d73-140">Wenn Sie dieses Flag verwenden, kann der Treiber den optimalen Speicherort für effiziente Schreibvorgänge und Rendering auswählen.</span><span class="sxs-lookup"><span data-stu-id="d4d73-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="d4d73-141">Versuche, aus einem Index Puffer zu lesen, der mit dieser Funktion erstellt wird, können zu Leistungseinbußen führen.</span><span class="sxs-lookup"><span data-stu-id="d4d73-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="d4d73-142">**Pool**</span><span class="sxs-lookup"><span data-stu-id="d4d73-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="d4d73-143">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d73-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d73-144">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für diesen Index Puffer zugeordnete Arbeitsspeicher Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="d4d73-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d4d73-145">**Größe**</span><span class="sxs-lookup"><span data-stu-id="d4d73-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d4d73-146">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d73-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d73-147">Größe des Index Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d4d73-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4d73-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d73-148">Requirements</span></span>



| <span data-ttu-id="d4d73-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d73-149">Requirement</span></span> | <span data-ttu-id="d4d73-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d73-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d73-151">Header</span><span class="sxs-lookup"><span data-stu-id="d4d73-151">Header</span></span><br/> | <dl> <span data-ttu-id="d4d73-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d73-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d73-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4d73-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d73-154">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d4d73-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d4d73-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="d4d73-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="d4d73-156">Index Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4d73-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
