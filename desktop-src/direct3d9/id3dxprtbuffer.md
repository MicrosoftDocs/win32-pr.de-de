---
description: Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer zum Speichern von Scheitelpunkt-und Pixeldaten für die Verwendung mit PRT-Methoden und-Funktionen verwendet.
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: ID3DXPRTBuffer-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350736"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="52d2c-103">ID3DXPRTBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="52d2c-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="52d2c-104">Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer zum Speichern von Scheitelpunkt-und Pixeldaten für die Verwendung mit PRT-Methoden und-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="52d2c-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="52d2c-105">Member</span><span class="sxs-lookup"><span data-stu-id="52d2c-105">Members</span></span>

<span data-ttu-id="52d2c-106">Die **ID3DXPRTBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52d2c-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="52d2c-107">**ID3DXPRTBuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52d2c-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="52d2c-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="52d2c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52d2c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="52d2c-109">Methods</span></span>

<span data-ttu-id="52d2c-110">Die **ID3DXPRTBuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52d2c-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="52d2c-111">Methode</span><span class="sxs-lookup"><span data-stu-id="52d2c-111">Method</span></span>                                                   | <span data-ttu-id="52d2c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52d2c-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52d2c-113">**Addbuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="52d2c-114">Fügt der **ID3DXPRTBuffer** einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="52d2c-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="52d2c-115">**Attachgh**</span><span class="sxs-lookup"><span data-stu-id="52d2c-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="52d2c-116">Verknüpft ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt mit dem **ID3DXPRTBuffer** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="52d2c-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="52d2c-117">**Evalgh**</span><span class="sxs-lookup"><span data-stu-id="52d2c-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="52d2c-118">Wendet gespeicherte Textur Daten auf einen **ID3DXPRTBuffer** -Textur Puffer an.</span><span class="sxs-lookup"><span data-stu-id="52d2c-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="52d2c-119">**Extracttexture**</span><span class="sxs-lookup"><span data-stu-id="52d2c-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="52d2c-120">Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="52d2c-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="52d2c-121">**Extracttomesh**</span><span class="sxs-lookup"><span data-stu-id="52d2c-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="52d2c-122">Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="52d2c-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="52d2c-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="52d2c-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="52d2c-124">Ruft die Höhe der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="52d2c-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="52d2c-125">**Getnumchannels**</span><span class="sxs-lookup"><span data-stu-id="52d2c-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="52d2c-126">Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52d2c-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="52d2c-127">**Getnumcoeffs**</span><span class="sxs-lookup"><span data-stu-id="52d2c-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="52d2c-128">Ruft die Anzahl der skalare pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52d2c-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="52d2c-129">**Getnumsamples**</span><span class="sxs-lookup"><span data-stu-id="52d2c-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="52d2c-130">Ruft die Anzahl der abtasteten Scheitel Punkte (oder Texels) ab.</span><span class="sxs-lookup"><span data-stu-id="52d2c-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="52d2c-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="52d2c-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="52d2c-132">Ruft die Breite der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="52d2c-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="52d2c-133">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="52d2c-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="52d2c-134">Gibt an, ob der Puffer eine Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="52d2c-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="52d2c-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="52d2c-136">Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.</span><span class="sxs-lookup"><span data-stu-id="52d2c-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="52d2c-137">**Releasegh**</span><span class="sxs-lookup"><span data-stu-id="52d2c-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="52d2c-138">Hebt die Zuordnung eines angefügten [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts zum **ID3DXPRTBuffer** -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="52d2c-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="52d2c-139">**Größe ändern**</span><span class="sxs-lookup"><span data-stu-id="52d2c-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="52d2c-140">Ändert die Anzahl der im Puffer enthaltenen Stichproben.</span><span class="sxs-lookup"><span data-stu-id="52d2c-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="52d2c-141">**Scalebuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="52d2c-142">Multipliziert jeden Wert im Puffer mit einem konstanten Wert.</span><span class="sxs-lookup"><span data-stu-id="52d2c-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="52d2c-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="52d2c-144">Beendet die Lebensdauer des ppData-Zeigers, der von [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="52d2c-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="52d2c-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52d2c-145">Remarks</span></span>

<span data-ttu-id="52d2c-146">Die **ID3DXPRTBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) -Funktion oder der [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="52d2c-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="52d2c-147">Der LPD3DXPRTBUFFER-Typ wird als Zeiger auf die **ID3DXPRTBuffer** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="52d2c-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="52d2c-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52d2c-148">Requirements</span></span>



| <span data-ttu-id="52d2c-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52d2c-149">Requirement</span></span> | <span data-ttu-id="52d2c-150">Wert</span><span class="sxs-lookup"><span data-stu-id="52d2c-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52d2c-151">Header</span><span class="sxs-lookup"><span data-stu-id="52d2c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="52d2c-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d2c-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="52d2c-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52d2c-153">Library</span></span><br/> | <dl> <span data-ttu-id="52d2c-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52d2c-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52d2c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52d2c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d2c-156">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="52d2c-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="52d2c-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="52d2c-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="52d2c-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="52d2c-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="52d2c-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
