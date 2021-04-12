---
description: Die ID3DXTextureGutterHelper-Schnittstelle wird verwendet, um bundckbereiche in einer Textur zu erstellen und zu verwalten. Die Struktur der bundbereiche trennt die Texturen und ermöglicht bilineare Interpolationen, um das Rendern von Artefakten an Textur Grenzen zu vermeiden.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: ID3DXTextureGutterHelper-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355616"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="8363c-104">ID3DXTextureGutterHelper-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8363c-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="8363c-105">Die ID3DXTextureGutterHelper-Schnittstelle wird verwendet, um bundckbereiche in einer Textur zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8363c-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="8363c-106">Die Struktur der bundbereiche trennt die Texturen und ermöglicht bilineare Interpolationen, um das Rendern von Artefakten an Textur Grenzen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8363c-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="8363c-107">Der Get... -Methoden ermöglichen den Zugriff auf die Datenstrukturen, die vom Apply... anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="8363c-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="8363c-108">Member</span><span class="sxs-lookup"><span data-stu-id="8363c-108">Members</span></span>

<span data-ttu-id="8363c-109">Die **ID3DXTextureGutterHelper** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8363c-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8363c-110">**ID3DXTextureGutterHelper** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8363c-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="8363c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="8363c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8363c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8363c-112">Methods</span></span>

<span data-ttu-id="8363c-113">Die **ID3DXTextureGutterHelper** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8363c-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="8363c-114">Methode</span><span class="sxs-lookup"><span data-stu-id="8363c-114">Method</span></span>                                                                   | <span data-ttu-id="8363c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8363c-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8363c-116">**Applyguttersfloat**</span><span class="sxs-lookup"><span data-stu-id="8363c-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="8363c-117">Wendet die-Guster auf einen float-Textur Puffer an.</span><span class="sxs-lookup"><span data-stu-id="8363c-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="8363c-118">**Applyguttersprt**</span><span class="sxs-lookup"><span data-stu-id="8363c-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="8363c-119">Wendet die-Guster auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8363c-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="8363c-120">**Applygutterstex**</span><span class="sxs-lookup"><span data-stu-id="8363c-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="8363c-121">Wendet die-Guster auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8363c-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="8363c-122">**Getbarymap**</span><span class="sxs-lookup"><span data-stu-id="8363c-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="8363c-123">Ruft texzentrische texzentrische Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="8363c-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="8363c-124">**Getfacemap**</span><span class="sxs-lookup"><span data-stu-id="8363c-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="8363c-125">Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.</span><span class="sxs-lookup"><span data-stu-id="8363c-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="8363c-126">**Getguttermap**</span><span class="sxs-lookup"><span data-stu-id="8363c-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="8363c-127">Empfängt einen Texel-Klassen Wert, der Texttypen entsprechend der Position jedes Texttyps angibt.</span><span class="sxs-lookup"><span data-stu-id="8363c-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="8363c-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="8363c-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="8363c-129">Ruft die Höhe der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="8363c-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="8363c-130">**Gettexelmap**</span><span class="sxs-lookup"><span data-stu-id="8363c-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="8363c-131">Ruft die Texturkoordinaten (u, v) der einzelnen texaus.</span><span class="sxs-lookup"><span data-stu-id="8363c-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="8363c-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="8363c-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="8363c-133">Ruft die Breite der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="8363c-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="8363c-134">**Resampletex**</span><span class="sxs-lookup"><span data-stu-id="8363c-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="8363c-135">Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.</span><span class="sxs-lookup"><span data-stu-id="8363c-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="8363c-136">**Setbarymap**</span><span class="sxs-lookup"><span data-stu-id="8363c-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="8363c-137">Legt texzentrische texse-Koordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="8363c-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="8363c-138">**Setfacemap**</span><span class="sxs-lookup"><span data-stu-id="8363c-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="8363c-139">Legt den Index des Mesh-Blatts fest, zu dem die einzelnen textengehören.</span><span class="sxs-lookup"><span data-stu-id="8363c-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="8363c-140">**Setguttermap**</span><span class="sxs-lookup"><span data-stu-id="8363c-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="8363c-141">Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.</span><span class="sxs-lookup"><span data-stu-id="8363c-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="8363c-142">**Settexelmap**</span><span class="sxs-lookup"><span data-stu-id="8363c-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="8363c-143">Legt die Texturkoordinaten (u, v) der einzelnen textsets fest.</span><span class="sxs-lookup"><span data-stu-id="8363c-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="8363c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8363c-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8363c-145">Bei Verwendung mit preberechneter Radiance Transfer (PRT) erfordert diese Schnittstelle eine eindeutige Parametrisierung des Modells.</span><span class="sxs-lookup"><span data-stu-id="8363c-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="8363c-146">Alle textexendas müssen einem einzelnen Punkt auf der Oberfläche des Modells entsprechen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="8363c-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="8363c-147">Wenn das Modell mehrere Texturen enthält, muss es in separate Teile aufgeteilt werden, die jeweils ein bundfügobjekt pro Textur enthalten.</span><span class="sxs-lookup"><span data-stu-id="8363c-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="8363c-148">Diese Schnittstelle kann verwendet werden, um eine Karte im Textur Bereich zu generieren, in der jeder Texin einer von vier Klassen ist.</span><span class="sxs-lookup"><span data-stu-id="8363c-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="8363c-149">Texel-Klasse</span><span class="sxs-lookup"><span data-stu-id="8363c-149">Texel Class</span></span> | <span data-ttu-id="8363c-150">Textsort</span><span class="sxs-lookup"><span data-stu-id="8363c-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8363c-151">0</span><span class="sxs-lookup"><span data-stu-id="8363c-151">0</span></span>           | <span data-ttu-id="8363c-152">Ungültiger Punkt; Texel wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8363c-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8363c-153">1</span><span class="sxs-lookup"><span data-stu-id="8363c-153">1</span></span>           | <span data-ttu-id="8363c-154">Innerhalb des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="8363c-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8363c-155">2</span><span class="sxs-lookup"><span data-stu-id="8363c-155">2</span></span>           | <span data-ttu-id="8363c-156">Im bundbundbereich.</span><span class="sxs-lookup"><span data-stu-id="8363c-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8363c-157">4</span><span class="sxs-lookup"><span data-stu-id="8363c-157">4</span></span>           | <span data-ttu-id="8363c-158">Im bundbundbereich; Texel wird als vollständiges Beispiel in der [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)-Methode oder der [**ID3DXTextureGutterHelper:: applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md) -Methode ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="8363c-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="8363c-159">Bei den Klassen 1 und 2 wird ein textpaar mit der Fläche gespeichert, zu der es gehört, zusammen mit den nicht auf die ersten beiden Scheitel Punkten der Fläche ausgerichteten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="8363c-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="8363c-160">Der am nächsten liegenden Rand im Textur Bereich zugeordnete bundces.</span><span class="sxs-lookup"><span data-stu-id="8363c-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="8363c-161">Es ist keine Texel-Klasse 3 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8363c-161">There is no texel class 3.</span></span>

<span data-ttu-id="8363c-162">Die **ID3DXTextureGutterHelper** -Schnittstelle wird durch Aufrufen der [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8363c-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="8363c-163">Der LPD3DXTEXTUREGUTTERHELPER-Typ wird als Zeiger auf die **ID3DXTextureGutterHelper** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8363c-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="8363c-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8363c-164">Requirements</span></span>



| <span data-ttu-id="8363c-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8363c-165">Requirement</span></span> | <span data-ttu-id="8363c-166">Wert</span><span class="sxs-lookup"><span data-stu-id="8363c-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8363c-167">Header</span><span class="sxs-lookup"><span data-stu-id="8363c-167">Header</span></span><br/>  | <dl> <span data-ttu-id="8363c-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8363c-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8363c-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8363c-169">Library</span></span><br/> | <dl> <span data-ttu-id="8363c-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8363c-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8363c-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8363c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8363c-172">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8363c-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
