---
title: 10Level9 ID3D11DeviceContext-Methoden
description: In diesem Abschnitt werden die Unterschiede zwischen jeder Featureebene 10Level9 und D3D FEATURE LEVEL 11 0 und höher für die \_ \_ \_ \_ ID3D11DeviceContext-Methoden aufgeführt.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cb055e6a290a9500f65ad2d64cdd69b0eaa224e6a81359595688ba1aca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990070"
---
# <a name="10level9-id3d11devicecontext-methods"></a>10Level9 ID3D11DeviceContext-Methoden

In diesem Abschnitt werden die Unterschiede zwischen jeder Featureebene 10Level9 und D3D FEATURE LEVEL 11 0 und höher für die \_ \_ \_ \_ [**ID3D11DeviceContext-Methoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) aufgeführt.

-   [ID3D11DeviceContext::CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext::CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext::CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext::ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext::CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext::CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext::CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext::CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext::CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::D raw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::D rawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext::GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext::GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext::GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext::GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext::HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext::HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext::HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext::HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext::OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext::OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext::RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext::RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext::SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext::SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext::VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext::VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext::VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext::VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Zugehörige Themen](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext::CopySubresourceRegion



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Nur Texture2D und Puffer können in gpu-zugänglichen Arbeitsspeicher kopiert werden.<br/> Texture3D kann nicht aus GPU-zugänglichen Speicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br/> Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus GPU-zugänglichen Arbeitsspeicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br/> Sie können keine Mipmappen-Volumetexturen kopieren. <br/> ${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext::CopyResource



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Nur Texture2D und Puffer können in gpu-zugänglichen Arbeitsspeicher kopiert werden.<br/> Texture3D kann nicht aus GPU-zugänglichen Speicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br/> Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus GPU-zugänglichen Arbeitsspeicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br/> ${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext::CopyStructureCount



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext::ClearUnorderedAccessViewFloat



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext::ClearUnorderedAccessViewUint



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext::ClearRenderTargetView



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nur der erste Arrayslice wird gelöscht. Anwendungen sollten eine Renderzielansicht für jeden Gesichts- oder Arrayslice erstellen und dann jede Ansicht einzeln löschen.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext::CSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext::CSSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext::CSSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext::CSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext::CSSetUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::D raw



| Featureebene             | Verhaltensunterschiede                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Die Anzahl der Primitive darf 65535 nicht überschreiten.<br/> Texturen können sich nicht mehr als 128 Mal über einen Primitiven wiederholen.<br/>    |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Die Anzahl der Primitive darf 1048575 nicht überschreiten.<br/> Texturen können sich nicht mehr als 2048 Mal über einen Primitiven wiederholen.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Die Anzahl der Primitive darf 1048575 nicht überschreiten.<br/> Texturen können sich nicht mehr als 8192 Mal über einen Primitiven wiederholen.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::D rawAuto



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::D rawIndexed



| Featureebene             | Verhaltensunterschiede                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Die Anzahl der Primitive darf 65535 nicht überschreiten.<br/> Texturen können sich nicht mehr als 128 Mal über einen Primitiven wiederholen.<br/> Indexwerte dürfen 65534 nicht überschreiten.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/>      |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Die Anzahl der Primitive darf 1048575 nicht überschreiten.<br/> Texturen können sich nicht mehr als 2048 Mal über einen Primitiven wiederholen.<br/> Indexwerte dürfen 1048575 nicht überschreiten.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Die Anzahl der Primitive darf 1048575 nicht überschreiten.<br/> Texturen können sich nicht mehr als 8192 Mal über einen Primitiven wiederholen.<br/> Indexwerte dürfen 1048575 nicht überschreiten.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::D rawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nicht unterstützt${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Die Anzahl der Primitive darf 1048575 nicht überschreiten.<br/> Texturen können sich nicht mehr als 8192 Mal über einen Primitiven wiederholen.<br/> Indexwerte dürfen 1048575 nicht überschreiten.<br/>
<blockquote>
[!Note]<br />
Wenn Sie die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced-Methode</strong></a> mit einem Vertex-Shader aufrufen, der an die Pipeline gebunden ist und keine Daten pro Instanz importiert, zeichnen einige Direct3D 9-Grafikhardware möglicherweise nichts. Insbesondere wenn der Vertex-Shader keine Instanzdaten verwendet, entspricht der Aufruf von <strong>DrawIndexedInstanced</strong> mit einer Instanz nicht dem Aufruf von <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw.</strong></a>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::D rawInstanced



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext::GSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext::GSSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext::GSSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext::GSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext::HSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext::HSSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext::HSSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext::HSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Das Format darf sich von dem bei der Puffererstellung angegebenen Format unterscheiden, aber es entsteht eine teure Übersetzung.<br/> Lässt nur Indexpuffer mit dem DXGI_FORMAT_R16_UINT-Format zu. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Das Format darf sich von dem bei der Puffererstellung angegebenen Format unterscheiden, aber es entsteht eine teure Übersetzung.<br/> Ermöglicht Indexpuffer mit DXGI_FORMAT_R16_UINT und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher. <br/> ${REMOVE}$<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Primitive Topologien mit Adjazenz werden nicht unterstützt${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext::OMSetBlendState



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">SampleMask darf nicht 0 (null) ${REMOVE}$ sein.<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext::OMSetRenderTargets



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur ein Renderziel wird unterstützt${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Es werden nur vier Renderziele unterstützt, und alle gebundenen Ressourcen müssen dieselbe Bittiefe aufweisen.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Siehe Featureebene 10.0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 32${REMOVE}$ nicht überschreiten.<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Es können nicht mehr als 16 Sampler gebunden werden${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur ps_4_0_level_9_1${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Nur ps_4_0_level_9_3 oder ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nicht mehr als 8 gleichzeitig gebundene Shaderressourcen${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext::RSSetScissorRects



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nur das nullte Scissor-Rect ist verfügbar${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext::RSSetViewports



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nur der nullte Viewport ist verfügbar${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

Obwohl Sie gleitkommawerte für die Elemente der [**\_ VIEWPORT-Struktur D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) für das *pViewports-Array* in einem Aufruf von [](overviews-direct3d-11-devices-downlevel-intro.md) [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für die Featureebenen 9 x angeben, verwendet \_ **RSSetViewports** intern DWORDs. Wenn Sie aufgrund dieses Verhaltens eine negative linke obere Ecke für den Viewport verwenden, tritt beim Aufruf von **RSSetViewports** für die Featureebenen 9 x ein \_ Fehler auf. Dieser Fehler tritt auf, weil **RSSetViewports** für 9 x die Gleitkommawerte ohne Überprüfung in ganze Zahlen ohne Vorzeichen umwandt, was zu einem \_ Ganzzahlüberlauf führt.

Der Aufruf von [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für die [Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 10 x und 11 x funktioniert wie erwartet, auch wenn Sie eine negative linke obere Ecke für den \_ \_ Viewport verwenden.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext::SetPredication



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext::SOSetTargets



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext::VSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Siehe Featureebene 10.0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 255${REMOVE}$ nicht überschreiten$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext::VSSetSamplers



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext::VSSetShader



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur vs_4_0_level_9_1${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Nur vs_4_0_level_9_3 oder vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext::VSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Featureebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[10Level9-Referenz](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





