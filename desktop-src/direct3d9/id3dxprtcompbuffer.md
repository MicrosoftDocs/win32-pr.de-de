---
description: Die ID3DXPRTCompBuffer-Schnittstelle speichert eine komprimierte Version eines ID3DXPRTBuffer-Puffers für die Verwendung mit der Principal Component Analysis (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: ID3DXPRTCompBuffer-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365128"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="1cf57-103">ID3DXPRTCompBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1cf57-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="1cf57-104">Die **ID3DXPRTCompBuffer** -Schnittstelle speichert eine komprimierte Version eines [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffers für die Verwendung mit der Principal Component Analysis (PCA).</span><span class="sxs-lookup"><span data-stu-id="1cf57-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="1cf57-105">Member</span><span class="sxs-lookup"><span data-stu-id="1cf57-105">Members</span></span>

<span data-ttu-id="1cf57-106">Die **ID3DXPRTCompBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1cf57-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1cf57-107">**ID3DXPRTCompBuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1cf57-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="1cf57-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1cf57-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1cf57-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1cf57-109">Methods</span></span>

<span data-ttu-id="1cf57-110">Die **ID3DXPRTCompBuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1cf57-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="1cf57-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1cf57-111">Method</span></span>                                                             | <span data-ttu-id="1cf57-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cf57-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cf57-113">**Extractbasis**</span><span class="sxs-lookup"><span data-stu-id="1cf57-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="1cf57-114">Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem **ID3DXPRTCompBuffer** -komprimierten Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="1cf57-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="1cf57-115">**Extractclusterids**</span><span class="sxs-lookup"><span data-stu-id="1cf57-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="1cf57-116">Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="1cf57-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="1cf57-117">**Extractpca**</span><span class="sxs-lookup"><span data-stu-id="1cf57-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="1cf57-118">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="1cf57-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="1cf57-119">**Extracttexture**</span><span class="sxs-lookup"><span data-stu-id="1cf57-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="1cf57-120">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="1cf57-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="1cf57-121">**Extracttomesh**</span><span class="sxs-lookup"><span data-stu-id="1cf57-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="1cf57-122">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="1cf57-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="1cf57-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="1cf57-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="1cf57-124">Ruft die Höhe der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="1cf57-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="1cf57-125">**Getnumchannels**</span><span class="sxs-lookup"><span data-stu-id="1cf57-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="1cf57-126">Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cf57-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="1cf57-127">**Getnumclusters**</span><span class="sxs-lookup"><span data-stu-id="1cf57-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="1cf57-128">Ruft die Anzahl der Cluster ab, die für die Komprimierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1cf57-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="1cf57-129">**Getnumcoeffs**</span><span class="sxs-lookup"><span data-stu-id="1cf57-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="1cf57-130">Ruft die Anzahl der skalare pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cf57-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1cf57-131">**Getnumpca**</span><span class="sxs-lookup"><span data-stu-id="1cf57-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="1cf57-132">Ruft die Anzahl der in jedem Cluster zu verwendenden PCA-Vektoren (Principal Component Analysis) ab.</span><span class="sxs-lookup"><span data-stu-id="1cf57-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1cf57-133">**Getnumsamples**</span><span class="sxs-lookup"><span data-stu-id="1cf57-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="1cf57-134">Ruft die Anzahl der abtasteten Scheitel Punkte (oder Texels) ab.</span><span class="sxs-lookup"><span data-stu-id="1cf57-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="1cf57-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="1cf57-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="1cf57-136">Ruft die Breite der Textur in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="1cf57-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="1cf57-137">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="1cf57-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="1cf57-138">Gibt an, ob der Puffer eine Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf57-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="1cf57-139">**Normalizedata**</span><span class="sxs-lookup"><span data-stu-id="1cf57-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="1cf57-140">Normalisiert alle PCA-Gewichtungen (Principal Component Analysis), sodass Sie zwischen-1 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="1cf57-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="1cf57-141">Basis Vektoren werden geändert, um diese Normalisierung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="1cf57-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="1cf57-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cf57-142">Remarks</span></span>

<span data-ttu-id="1cf57-143">Die **ID3DXPRTCompBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1cf57-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="1cf57-144">Der LPD3DXPRTCOMPBUFFER-Typ wird als Zeiger auf die **ID3DXPRTCompBuffer** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="1cf57-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="1cf57-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cf57-145">Requirements</span></span>



| <span data-ttu-id="1cf57-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cf57-146">Requirement</span></span> | <span data-ttu-id="1cf57-147">Wert</span><span class="sxs-lookup"><span data-stu-id="1cf57-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf57-148">Header</span><span class="sxs-lookup"><span data-stu-id="1cf57-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1cf57-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf57-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1cf57-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cf57-150">Library</span></span><br/> | <dl> <span data-ttu-id="1cf57-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cf57-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cf57-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cf57-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf57-153">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1cf57-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1cf57-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="1cf57-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="1cf57-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="1cf57-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
