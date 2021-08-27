---
title: 10Level9 ID3D11DeviceContext-Methoden
description: In diesem Abschnitt werden die Unterschiede zwischen jeder 10Level9-Featureebene und der Featureebene D3D \_ FEATURE \_ LEVEL \_ 11 \_ 0 und höher für die ID3D11DeviceContext-Methoden aufgelistet.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e268f45465139e49afe0f81a64eeeb93939734e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473126"
---
# <a name="10level9-id3d11devicecontext-methods"></a>10Level9 ID3D11DeviceContext-Methoden

In diesem Abschnitt werden die Unterschiede zwischen jeder 10Level9-Featureebene und der Featureebene D3D \_ FEATURE \_ LEVEL \_ 11 \_ 0 und höher für die [**ID3D11DeviceContext-Methoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) aufgelistet.

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




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Nur Texture2D und Puffer dürfen innerhalb des gpu-zugänglichen Speichers kopiert werden.<br /> Texture3D kann nicht aus gpu-zugänglichem Speicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br /> Ressourcen, die nur über D3D10_BIND_SHADER_RESOURCE verfügen, können nicht aus dem GPU-zugänglichen Speicher in den CPU-zugänglichen Arbeitsspeicher kopiert werden.<br /> Sie können keine Mipmappenvolumetexturen kopieren. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext::CopyResource




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Nur Texture2D und Puffer dürfen innerhalb des gpu-zugänglichen Speichers kopiert werden.<br /> Texture3D kann nicht aus gpu-zugänglichem Speicher in CPU-zugänglichen Arbeitsspeicher kopiert werden.<br /> Ressourcen, die nur über D3D10_BIND_SHADER_RESOURCE verfügen, können nicht aus dem GPU-zugänglichen Speicher in den CPU-zugänglichen Arbeitsspeicher kopiert werden.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext::CopyStructureCount




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext::ClearUnorderedAccessViewFloat




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext::ClearUnorderedAccessViewUint




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext::ClearRenderTargetView




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur der erste Arrayslice wird wieder löschen. Anwendungen sollten eine Renderzielansicht für jedes Gesichts- oder Arrayslice erstellen und dann jede Ansicht einzeln löschen.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext::CSSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext::CSSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext::CSSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext::CSSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext::CSSetUnorderedAccessViews




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::D raw



| Featureebene             | Verhaltensunterschiede                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Die Anzahl der Primitive darf 65535 nicht überschreiten.<br/> Texturen können sich nicht mehr als 128 Mal über einen primitiven Typ wiederholen.<br/>    |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Die Anzahl von Primitiven darf den Wert 1048575.<br/> Texturen können nicht mehr als 2048 Mal pro Primitive wiederholt werden.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Die Anzahl von Primitiven darf den Wert 1048575.<br/> Texturen können sich nicht mehr als 8192 Mal über einen primitiven Typ wiederholen.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::D rawAuto




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::D rawIndexed



| Featureebene             | Verhaltensunterschiede                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Die Anzahl der Primitive darf 65535 nicht überschreiten.<br/> Texturen können sich nicht mehr als 128 Mal über einen primitiven Typ wiederholen.<br/> Indexwerte dürfen 65534 nicht überschreiten.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/>      |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Die Anzahl von Primitiven darf den Wert 1048575.<br/> Texturen können nicht mehr als 2048 Mal pro Primitive wiederholt werden.<br/> Indexwerte dürfen den Wert 1048575.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Die Anzahl von Primitiven darf den Wert 1048575.<br/> Texturen können sich nicht mehr als 8192 Mal über einen primitiven Typ wiederholen.<br/> Indexwerte dürfen den Wert 1048575.<br/> Indizierte Punktlisten werden nicht unterstützt.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::D rawIndexedInstanced




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nicht unterstützt${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Die Anzahl von Primitiven darf den Wert 1048575.<br /> Texturen können sich nicht mehr als 8192 Mal über einen primitiven Typ wiederholen.<br /> Indexwerte dürfen den Wert 1048575.<br /><blockquote>[!Note]<br />Wenn Sie die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced-Methode</strong></a> mit einem Vertex-Shader aufrufen, der an die Pipeline gebunden ist und keine Daten pro Instanz importiert, zeichnen einige Direct3D 9-Grafikhardware möglicherweise nichts. Insbesondere wenn der Vertex-Shader keine Daten pro Instanz verwendet, entspricht das Aufrufen von <strong>DrawIndexedInstanced</strong> mit einer Instanz nicht dem Aufrufen von <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</blockquote><br /> | 




 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::D rawInstanced




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext::GSSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext::GSSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext::GSSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext::GSSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext::HSSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext::HSSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext::HSSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext::HSSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*- oder 10.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Das Format darf sich von dem bei der Puffererstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung erstellt.<br /> Lässt nur Indexpuffer mit dem DXGI_FORMAT_R16_UINT zu. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Das Format darf sich von dem bei der Puffererstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung erstellt.<br /> Ermöglicht Indexpuffer mit den DXGI_FORMAT_R16_UINT und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Primitive Topologien mit Adjacency werden nicht unterstützt${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext::OMSetBlendState




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | SampleMask darf nicht null${REMOVE}$ sein.<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext::OMSetRenderTargets




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur ein Renderziel wird unterstützt${REMOVE}$.<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Nur vier Renderziele werden unterstützt, und alle gebundenen Ressourcen müssen dieselbe Bittiefe haben. | 




 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Siehe Featureebene 10.0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 32${REMOVE}$ nicht überschreiten.<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Es können nicht mehr als 16 Sampler gebunden werden${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur ps_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Nur ps_4_0_level_9_3 oder ps_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nicht mehr als acht gleichzeitig gebundene Shaderressourcen${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext::RSSetScissorRects




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur der nullte Scissor rect ist verfügbar${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext::RSSetViewports




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur der nullte Viewport ist verfügbar${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

Obwohl Sie float-Werte für die Member der [**D3D11 \_ VIEWPORT-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) für das *pViewports-Array* in einem Aufruf von [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für [Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x angeben, verwendet **RSSetViewports** intern DWORDs. Wenn Sie aufgrund dieses Verhaltens eine negative linke obere Ecke für den Viewport verwenden, schlägt der Aufruf von **RSSetViewports** für Featureebenen 9 \_ x fehl. Dieser Fehler tritt auf, weil **RSSetViewports** für 9 \_ x die Gleitkommawerte ohne Validierung in ganze Zahlen ohne Vorzeichen umsetzt, was zu einem Ganzzahlüberlauf führt.

Der Aufruf von [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für [die Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x und 11 \_ x funktioniert wie erwartet, auch wenn Sie eine negative linke obere Ecke für den Viewport verwenden.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext::SetPredication




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext::SOSetTargets




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext::VSSetConstantBuffers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Siehe Featureebene 10.0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 255${REMOVE}$ nicht überschreiten.<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext::VSSetSamplers




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext::VSSetShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Nur vs_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Nur vs_4_0_level_9_3 oder vs_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext::VSSetShaderResources




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[10Level9-Referenz](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





