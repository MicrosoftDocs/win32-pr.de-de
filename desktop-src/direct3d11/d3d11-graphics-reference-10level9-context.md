---
title: 10level9 Verknüpfung id3d11devicecontext aus Methoden
description: In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die Verknüpfung id3d11devicecontext aus-Methoden aufgeführt.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036498"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="6dc22-103">10level9 Verknüpfung id3d11devicecontext aus Methoden</span><span class="sxs-lookup"><span data-stu-id="6dc22-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="6dc22-104">In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dc22-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="6dc22-105">Verknüpfung id3d11devicecontext aus:: copysubresourceregion</span><span class="sxs-lookup"><span data-stu-id="6dc22-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="6dc22-106">Verknüpfung id3d11devicecontext aus:: copyresource</span><span class="sxs-lookup"><span data-stu-id="6dc22-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="6dc22-107">Verknüpfung id3d11devicecontext aus:: copystructurecount</span><span class="sxs-lookup"><span data-stu-id="6dc22-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="6dc22-108">Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewfloat</span><span class="sxs-lookup"><span data-stu-id="6dc22-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="6dc22-109">Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewuint</span><span class="sxs-lookup"><span data-stu-id="6dc22-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="6dc22-110">Verknüpfung id3d11devicecontext aus:: clearrendertargetview</span><span class="sxs-lookup"><span data-stu-id="6dc22-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="6dc22-111">Verknüpfung id3d11devicecontext aus:: cssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="6dc22-112">Verknüpfung id3d11devicecontext aus:: cssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="6dc22-113">Verknüpfung id3d11devicecontext aus:: cssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="6dc22-114">Verknüpfung id3d11devicecontext aus:: cssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="6dc22-115">Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews</span><span class="sxs-lookup"><span data-stu-id="6dc22-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="6dc22-116">Verknüpfung id3d11devicecontext aus::D ispatch</span><span class="sxs-lookup"><span data-stu-id="6dc22-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="6dc22-117">Verknüpfung id3d11devicecontext aus::D ispatchindirekte</span><span class="sxs-lookup"><span data-stu-id="6dc22-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="6dc22-118">Verknüpfung id3d11devicecontext aus::D RAW</span><span class="sxs-lookup"><span data-stu-id="6dc22-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="6dc22-119">Verknüpfung id3d11devicecontext aus::D rawauto</span><span class="sxs-lookup"><span data-stu-id="6dc22-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="6dc22-120">Verknüpfung id3d11devicecontext aus::D rawindebug</span><span class="sxs-lookup"><span data-stu-id="6dc22-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="6dc22-121">Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet</span><span class="sxs-lookup"><span data-stu-id="6dc22-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="6dc22-122">Verknüpfung id3d11devicecontext aus::D rawindexedinstancedindirect</span><span class="sxs-lookup"><span data-stu-id="6dc22-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="6dc22-123">Verknüpfung id3d11devicecontext aus::D rawinstanzierte</span><span class="sxs-lookup"><span data-stu-id="6dc22-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="6dc22-124">Verknüpfung id3d11devicecontext aus::D rawinstancedindirect</span><span class="sxs-lookup"><span data-stu-id="6dc22-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="6dc22-125">Verknüpfung id3d11devicecontext aus::D ssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="6dc22-126">Verknüpfung id3d11devicecontext aus::D ssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="6dc22-127">Verknüpfung id3d11devicecontext aus::D ssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="6dc22-128">Verknüpfung id3d11devicecontext aus::D ssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="6dc22-129">Verknüpfung id3d11devicecontext aus:: gssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="6dc22-130">Verknüpfung id3d11devicecontext aus:: gssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="6dc22-131">Verknüpfung id3d11devicecontext aus:: gssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="6dc22-132">Verknüpfung id3d11devicecontext aus:: gssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="6dc22-133">Verknüpfung id3d11devicecontext aus:: hssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="6dc22-134">Verknüpfung id3d11devicecontext aus:: hssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="6dc22-135">Verknüpfung id3d11devicecontext aus:: hssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="6dc22-136">Verknüpfung id3d11devicecontext aus:: hssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="6dc22-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="6dc22-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="6dc22-138">Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology</span><span class="sxs-lookup"><span data-stu-id="6dc22-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="6dc22-139">Verknüpfung id3d11devicecontext aus:: omsetblendstate</span><span class="sxs-lookup"><span data-stu-id="6dc22-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="6dc22-140">Verknüpfung id3d11devicecontext aus:: omgtrendertargets</span><span class="sxs-lookup"><span data-stu-id="6dc22-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="6dc22-141">Verknüpfung id3d11devicecontext aus:: omabtrendertargesorandunorderedaccessviews</span><span class="sxs-lookup"><span data-stu-id="6dc22-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="6dc22-142">Verknüpfung id3d11devicecontext aus::P ssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="6dc22-143">Verknüpfung id3d11devicecontext aus::P ssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="6dc22-144">Verknüpfung id3d11devicecontext aus::P ssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="6dc22-145">Verknüpfung id3d11devicecontext aus::P ssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="6dc22-146">Verknüpfung id3d11devicecontext aus:: rssezcissorrects</span><span class="sxs-lookup"><span data-stu-id="6dc22-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="6dc22-147">Verknüpfung id3d11devicecontext aus:: rssetviewports</span><span class="sxs-lookup"><span data-stu-id="6dc22-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="6dc22-148">Verknüpfung id3d11devicecontext aus:: setprediation</span><span class="sxs-lookup"><span data-stu-id="6dc22-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="6dc22-149">Verknüpfung id3d11devicecontext aus:: sosettargets</span><span class="sxs-lookup"><span data-stu-id="6dc22-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="6dc22-150">Verknüpfung id3d11devicecontext aus:: vssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="6dc22-151">Verknüpfung id3d11devicecontext aus:: vssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="6dc22-152">Verknüpfung id3d11devicecontext aus:: vssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="6dc22-153">Verknüpfung id3d11devicecontext aus:: vssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="6dc22-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dc22-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="6dc22-155">Verknüpfung id3d11devicecontext aus:: copysubresourceregion</span><span class="sxs-lookup"><span data-stu-id="6dc22-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-156">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-156">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-157">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="6dc22-159">Nur Texture2D und Puffer können im Speicher, auf den GPU zugreifen kann, kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-160">Texture3D kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Zugriff kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-161">Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Speicherplatz kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-162">Sie können keine mipzugeordneten volumetexturen kopieren.</span><span class="sxs-lookup"><span data-stu-id="6dc22-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="6dc22-163">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="6dc22-166">Verknüpfung id3d11devicecontext aus:: copyresource</span><span class="sxs-lookup"><span data-stu-id="6dc22-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-167">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-167">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-168">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="6dc22-170">Nur Texture2D und Puffer können im Speicher, auf den GPU zugreifen kann, kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-171">Texture3D kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Zugriff kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-172">Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Speicherplatz kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="6dc22-173">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="6dc22-176">Verknüpfung id3d11devicecontext aus:: copystructurecount</span><span class="sxs-lookup"><span data-stu-id="6dc22-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-177">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-177">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-178">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-180">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="6dc22-183">Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewfloat</span><span class="sxs-lookup"><span data-stu-id="6dc22-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-184">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-184">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-185">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-187">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="6dc22-190">Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewuint</span><span class="sxs-lookup"><span data-stu-id="6dc22-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-191">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-191">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-192">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-194">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="6dc22-197">Verknüpfung id3d11devicecontext aus:: clearrendertargetview</span><span class="sxs-lookup"><span data-stu-id="6dc22-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-198">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-198">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-199">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-201">Nur der erste Array Slice wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6dc22-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="6dc22-202">Anwendungen sollten eine renderzielansicht für jedes Gesicht oder jeden Array Slice erstellen und dann jede Ansicht einzeln löschen. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="6dc22-205">Verknüpfung id3d11devicecontext aus:: cssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-206">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-206">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-207">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-209">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="6dc22-212">Verknüpfung id3d11devicecontext aus:: cssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-213">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-213">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-214">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-216">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="6dc22-219">Verknüpfung id3d11devicecontext aus:: cssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-220">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-220">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-221">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-223">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="6dc22-226">Verknüpfung id3d11devicecontext aus:: cssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-227">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-227">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-228">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-230">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="6dc22-233">Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews</span><span class="sxs-lookup"><span data-stu-id="6dc22-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-234">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-234">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-235">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-237">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="6dc22-240">Verknüpfung id3d11devicecontext aus::D ispatch</span><span class="sxs-lookup"><span data-stu-id="6dc22-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-241">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-241">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-242">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-244">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="6dc22-247">Verknüpfung id3d11devicecontext aus::D ispatchindirekte</span><span class="sxs-lookup"><span data-stu-id="6dc22-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-248">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-248">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-249">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-251">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="6dc22-254">Verknüpfung id3d11devicecontext aus::D RAW</span><span class="sxs-lookup"><span data-stu-id="6dc22-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="6dc22-255">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-255">Feature Level</span></span>             | <span data-ttu-id="6dc22-256">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc22-257">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6dc22-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="6dc22-258">Die Anzahl der primitiven darf 65535 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="6dc22-259">Texturen können nicht mehr als 128 mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="6dc22-260">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="6dc22-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="6dc22-261">Die Anzahl der primitiven darf 1048575 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-262">Texturen können nicht mehr als 2048 mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="6dc22-263">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6dc22-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="6dc22-264">Die Anzahl der primitiven darf 1048575 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-265">Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="6dc22-266">Verknüpfung id3d11devicecontext aus::D rawauto</span><span class="sxs-lookup"><span data-stu-id="6dc22-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-267">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-267">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-268">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-270">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="6dc22-273">Verknüpfung id3d11devicecontext aus::D rawindebug</span><span class="sxs-lookup"><span data-stu-id="6dc22-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="6dc22-274">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-274">Feature Level</span></span>             | <span data-ttu-id="6dc22-275">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc22-276">D3D \_ \_ Featureebene \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6dc22-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="6dc22-277">Die Anzahl der primitiven darf 65535 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="6dc22-278">Texturen können nicht mehr als 128 mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="6dc22-279">Index Werte dürfen nicht größer sein als 65534.</span><span class="sxs-lookup"><span data-stu-id="6dc22-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="6dc22-280">Indizierte Punkt Listen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6dc22-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="6dc22-281">D3D \_ \_ Featureebene \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="6dc22-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="6dc22-282">Die Anzahl der primitiven darf 1048575 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-283">Texturen können nicht mehr als 2048 mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="6dc22-284">Index Werte dürfen nicht größer sein als 1048575.</span><span class="sxs-lookup"><span data-stu-id="6dc22-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-285">Indizierte Punkt Listen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6dc22-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="6dc22-286">D3D \_ \_ Featureebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6dc22-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="6dc22-287">Die Anzahl der primitiven darf 1048575 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-288">Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="6dc22-289">Index Werte dürfen nicht größer sein als 1048575.</span><span class="sxs-lookup"><span data-stu-id="6dc22-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-290">Indizierte Punkt Listen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6dc22-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="6dc22-291">Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet</span><span class="sxs-lookup"><span data-stu-id="6dc22-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-292">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-292">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-293">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="6dc22-295">Nicht unterstützt $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="6dc22-298">Die Anzahl der primitiven darf 1048575 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="6dc22-299">Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="6dc22-300">Index Werte dürfen nicht größer sein als 1048575.</span><span class="sxs-lookup"><span data-stu-id="6dc22-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6dc22-301">Wenn Sie die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>drawindexedinstanbound</strong></a> -Methode mit einem Vertex-Shader aufrufen, der an die Pipeline gebunden ist und keine instanzbezogenen Daten importiert, zeichnet einige Direct3D 9-Grafikhardware möglicherweise nichts.</span><span class="sxs-lookup"><span data-stu-id="6dc22-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="6dc22-302">Insbesondere wenn der Vertex-Shader keine instanzbezogenen Daten verwendet, entspricht das Aufrufen von <strong>drawindexedinstanreceimit</strong> 1 Instance nicht dem aufrufenden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Zeichnen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6dc22-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="6dc22-303">Verknüpfung id3d11devicecontext aus::D rawindexedinstancedindirect</span><span class="sxs-lookup"><span data-stu-id="6dc22-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-304">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-304">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-305">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-307">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="6dc22-312">Verknüpfung id3d11devicecontext aus::D rawinstanzierte</span><span class="sxs-lookup"><span data-stu-id="6dc22-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-313">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-313">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-314">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-316">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="6dc22-319">Verknüpfung id3d11devicecontext aus::D rawinstancedindirect</span><span class="sxs-lookup"><span data-stu-id="6dc22-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-320">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-320">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-321">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-323">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="6dc22-328">Verknüpfung id3d11devicecontext aus::D ssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-329">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-329">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-330">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-332">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="6dc22-337">Verknüpfung id3d11devicecontext aus::D ssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-338">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-338">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-339">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-341">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="6dc22-346">Verknüpfung id3d11devicecontext aus::D ssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-347">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-347">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-348">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-350">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="6dc22-355">Verknüpfung id3d11devicecontext aus::D ssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-356">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-356">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-357">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-359">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="6dc22-364">Verknüpfung id3d11devicecontext aus:: gssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-365">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-365">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-366">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-368">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="6dc22-371">Verknüpfung id3d11devicecontext aus:: gssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-372">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-372">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-373">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-375">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="6dc22-378">Verknüpfung id3d11devicecontext aus:: gssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-379">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-379">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-380">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-382">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="6dc22-385">Verknüpfung id3d11devicecontext aus:: gssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-386">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-386">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-387">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-389">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="6dc22-392">Verknüpfung id3d11devicecontext aus:: hssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-393">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-393">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-394">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-396">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="6dc22-401">Verknüpfung id3d11devicecontext aus:: hssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-402">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-402">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-403">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-405">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="6dc22-410">Verknüpfung id3d11devicecontext aus:: hssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-411">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-411">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-412">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-414">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="6dc22-419">Verknüpfung id3d11devicecontext aus:: hssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-420">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-420">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-421">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="6dc22-423">Wird auf keiner 9. \*-oder 10. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="6dc22-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="6dc22-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="6dc22-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-429">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-429">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-430">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="6dc22-432">Das Format darf sich von dem bei der Puffer Erstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung entstehen.</span><span class="sxs-lookup"><span data-stu-id="6dc22-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="6dc22-433">Ermöglicht nur Index Puffer mit dem DXGI_FORMAT_R16_UINT-Format.</span><span class="sxs-lookup"><span data-stu-id="6dc22-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="6dc22-435">Das Format darf sich von dem bei der Puffer Erstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung entstehen.</span><span class="sxs-lookup"><span data-stu-id="6dc22-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="6dc22-436">Ermöglicht Index Puffer mit den DXGI_FORMAT_R16_UINT-und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher.</span><span class="sxs-lookup"><span data-stu-id="6dc22-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="6dc22-437">$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="6dc22-439">Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology</span><span class="sxs-lookup"><span data-stu-id="6dc22-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-440">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-440">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-441">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-443">Primitive Topologien mit Unterstützung werden nicht unterstützt $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="6dc22-446">Verknüpfung id3d11devicecontext aus:: omsetblendstate</span><span class="sxs-lookup"><span data-stu-id="6dc22-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-447">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-447">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-448">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-450">Samplemask darf nicht NULL $ {Remove} $ sein.</span><span class="sxs-lookup"><span data-stu-id="6dc22-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="6dc22-453">Verknüpfung id3d11devicecontext aus:: omgtrendertargets</span><span class="sxs-lookup"><span data-stu-id="6dc22-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-454">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-454">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-455">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="6dc22-457">Nur ein Renderziel unterstützt $ {Remove} $.</span><span class="sxs-lookup"><span data-stu-id="6dc22-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="6dc22-460">Es werden nur vier Renderziele unterstützt, und alle gebundenen Ressourcen müssen über die gleiche Bittiefe verfügen.</span><span class="sxs-lookup"><span data-stu-id="6dc22-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="6dc22-461">Verknüpfung id3d11devicecontext aus:: omabtrendertargesorandunorderedaccessviews</span><span class="sxs-lookup"><span data-stu-id="6dc22-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-462">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-462">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-463">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-465">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="6dc22-468">Verknüpfung id3d11devicecontext aus::P ssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-469">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-469">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-470">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-472">Siehe Featureebene 10,0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 32 $ {Remove} $ nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="6dc22-475">Verknüpfung id3d11devicecontext aus::P ssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-476">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-476">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-477">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-479">Maximal 16 Samplern können an $ {Remove} $ gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="6dc22-482">Verknüpfung id3d11devicecontext aus::P ssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-483">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-483">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-484">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="6dc22-486">Nur ps_4_0_level_9_1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="6dc22-489">Nur ps_4_0_level_9_3 oder ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="6dc22-490">Verknüpfung id3d11devicecontext aus::P ssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-491">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-491">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-492">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-494">Nicht mehr als 8 gleichzeitig gebundene Shaderressourcen $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="6dc22-497">Verknüpfung id3d11devicecontext aus:: rssezcissorrects</span><span class="sxs-lookup"><span data-stu-id="6dc22-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-498">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-498">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-499">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-501">Es ist nur das NULL "nullte Scheren" verfügbar: $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="6dc22-504">Verknüpfung id3d11devicecontext aus:: rssetviewports</span><span class="sxs-lookup"><span data-stu-id="6dc22-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-505">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-505">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-506">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-508">Nur der nullten nullten ist verfügbar $ {Remove} $.</span><span class="sxs-lookup"><span data-stu-id="6dc22-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="6dc22-511">Obwohl Sie Gleit Komma Werte für die Elemente der [**D3D11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) -Struktur für das *pviewports* -Array in einem-Aufrufe [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für die Featureebene 9 x angeben [](overviews-direct3d-11-devices-downlevel-intro.md) \_ , verwendet **rssetviewports** intern DWORDs.</span><span class="sxs-lookup"><span data-stu-id="6dc22-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="6dc22-512">Aufgrund dieses Verhaltens schlägt der Aufrufe von **rssetviewports** für featureebenen 9 x fehl, wenn Sie für den Viewport eine negative obere linke Ecke verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="6dc22-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="6dc22-513">Dieser Fehler tritt auf, weil **rssetviewports** für 9 \_ x die Gleit Komma Werte ohne Validierung in ganze Zahlen ohne Vorzeichen umwandelt, was zu einem ganzzahligen Überlauf führt.</span><span class="sxs-lookup"><span data-stu-id="6dc22-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="6dc22-514">Der [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) -Befehl für die featureebenen 10 [](overviews-direct3d-11-devices-downlevel-intro.md) \_ x und 11 \_ x funktioniert erwartungsgemäß, auch wenn Sie für den Viewport eine negative obere linke Ecke verwenden.</span><span class="sxs-lookup"><span data-stu-id="6dc22-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="6dc22-515">Verknüpfung id3d11devicecontext aus:: setprediation</span><span class="sxs-lookup"><span data-stu-id="6dc22-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-516">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-516">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-517">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-519">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="6dc22-522">Verknüpfung id3d11devicecontext aus:: sosettargets</span><span class="sxs-lookup"><span data-stu-id="6dc22-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-523">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-523">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-524">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-526">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="6dc22-529">Verknüpfung id3d11devicecontext aus:: vssetconstantbuffers</span><span class="sxs-lookup"><span data-stu-id="6dc22-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-530">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-530">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-531">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-533">Siehe Featureebene 10,0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 255 $ {Remove} $ nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6dc22-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="6dc22-536">Verknüpfung id3d11devicecontext aus:: vssetsamplers</span><span class="sxs-lookup"><span data-stu-id="6dc22-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-537">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-537">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-538">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-540">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="6dc22-543">Verknüpfung id3d11devicecontext aus:: vssetshader</span><span class="sxs-lookup"><span data-stu-id="6dc22-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-544">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-544">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-545">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="6dc22-547">Nur vs_4_0_level_9_1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="6dc22-550">Nur vs_4_0_level_9_3 oder vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="6dc22-551">Verknüpfung id3d11devicecontext aus:: vssetshaderresources</span><span class="sxs-lookup"><span data-stu-id="6dc22-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc22-552">Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="6dc22-552">Feature Level</span></span></th>
<th><span data-ttu-id="6dc22-553">Verhaltensunterschiede</span><span class="sxs-lookup"><span data-stu-id="6dc22-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc22-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="6dc22-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="6dc22-555">Wird auf keiner 9. \*-Funktionsebene unterstützt. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="6dc22-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc22-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="6dc22-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6dc22-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="6dc22-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6dc22-558">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dc22-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dc22-559">10level9-Referenz</span><span class="sxs-lookup"><span data-stu-id="6dc22-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





