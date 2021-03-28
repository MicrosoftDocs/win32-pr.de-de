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
# <a name="10level9-id3d11devicecontext-methods"></a>10level9 Verknüpfung id3d11devicecontext aus Methoden

In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden aufgeführt.

-   [Verknüpfung id3d11devicecontext aus:: copysubresourceregion](#id3d11devicecontextcopysubresourceregion)
-   [Verknüpfung id3d11devicecontext aus:: copyresource](#id3d11devicecontextcopyresource)
-   [Verknüpfung id3d11devicecontext aus:: copystructurecount](#id3d11devicecontextcopystructurecount)
-   [Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewfloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewuint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [Verknüpfung id3d11devicecontext aus:: clearrendertargetview](#id3d11devicecontextclearrendertargetview)
-   [Verknüpfung id3d11devicecontext aus:: cssetconstantbuffers](#id3d11devicecontextcssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus:: cssetsamplers](#id3d11devicecontextcssetsamplers)
-   [Verknüpfung id3d11devicecontext aus:: cssetshader](#id3d11devicecontextcssetshader)
-   [Verknüpfung id3d11devicecontext aus:: cssetshaderresources](#id3d11devicecontextcssetshaderresources)
-   [Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews](#id3d11devicecontextcssetunorderedaccessviews)
-   [Verknüpfung id3d11devicecontext aus::D ispatch](#id3d11devicecontextdispatch)
-   [Verknüpfung id3d11devicecontext aus::D ispatchindirekte](#id3d11devicecontextdispatchindirect)
-   [Verknüpfung id3d11devicecontext aus::D RAW](#id3d11devicecontextdraw)
-   [Verknüpfung id3d11devicecontext aus::D rawauto](#id3d11devicecontextdrawauto)
-   [Verknüpfung id3d11devicecontext aus::D rawindebug](#id3d11devicecontextdrawindexed)
-   [Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet](#id3d11devicecontextdrawindexedinstanced)
-   [Verknüpfung id3d11devicecontext aus::D rawindexedinstancedindirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [Verknüpfung id3d11devicecontext aus::D rawinstanzierte](#id3d11devicecontextdrawinstanced)
-   [Verknüpfung id3d11devicecontext aus::D rawinstancedindirect](#id3d11devicecontextdrawinstancedindirect)
-   [Verknüpfung id3d11devicecontext aus::D ssetconstantbuffers](#id3d11devicecontextdssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus::D ssetsamplers](#id3d11devicecontextdssetsamplers)
-   [Verknüpfung id3d11devicecontext aus::D ssetshader](#id3d11devicecontextdssetshader)
-   [Verknüpfung id3d11devicecontext aus::D ssetshaderresources](#id3d11devicecontextdssetshaderresources)
-   [Verknüpfung id3d11devicecontext aus:: gssetconstantbuffers](#id3d11devicecontextgssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus:: gssetsamplers](#id3d11devicecontextgssetsamplers)
-   [Verknüpfung id3d11devicecontext aus:: gssetshader](#id3d11devicecontextgssetshader)
-   [Verknüpfung id3d11devicecontext aus:: gssetshaderresources](#id3d11devicecontextgssetshaderresources)
-   [Verknüpfung id3d11devicecontext aus:: hssetconstantbuffers](#id3d11devicecontexthssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus:: hssetsamplers](#id3d11devicecontexthssetsamplers)
-   [Verknüpfung id3d11devicecontext aus:: hssetshader](#id3d11devicecontexthssetshader)
-   [Verknüpfung id3d11devicecontext aus:: hssetshaderresources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology](#id3d11devicecontextiasetprimitivetopology)
-   [Verknüpfung id3d11devicecontext aus:: omsetblendstate](#id3d11devicecontextomsetblendstate)
-   [Verknüpfung id3d11devicecontext aus:: omgtrendertargets](#id3d11devicecontextomsetrendertargets)
-   [Verknüpfung id3d11devicecontext aus:: omabtrendertargesorandunorderedaccessviews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [Verknüpfung id3d11devicecontext aus::P ssetconstantbuffers](#id3d11devicecontextpssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus::P ssetsamplers](#id3d11devicecontextpssetsamplers)
-   [Verknüpfung id3d11devicecontext aus::P ssetshader](#id3d11devicecontextpssetshader)
-   [Verknüpfung id3d11devicecontext aus::P ssetshaderresources](#id3d11devicecontextpssetshaderresources)
-   [Verknüpfung id3d11devicecontext aus:: rssezcissorrects](#id3d11devicecontextrssetscissorrects)
-   [Verknüpfung id3d11devicecontext aus:: rssetviewports](#id3d11devicecontextrssetviewports)
-   [Verknüpfung id3d11devicecontext aus:: setprediation](#id3d11devicecontextsetpredication)
-   [Verknüpfung id3d11devicecontext aus:: sosettargets](#id3d11devicecontextsosettargets)
-   [Verknüpfung id3d11devicecontext aus:: vssetconstantbuffers](#id3d11devicecontextvssetconstantbuffers)
-   [Verknüpfung id3d11devicecontext aus:: vssetsamplers](#id3d11devicecontextvssetsamplers)
-   [Verknüpfung id3d11devicecontext aus:: vssetshader](#id3d11devicecontextvssetshader)
-   [Verknüpfung id3d11devicecontext aus:: vssetshaderresources](#id3d11devicecontextvssetshaderresources)
-   [Zugehörige Themen](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>Verknüpfung id3d11devicecontext aus:: copysubresourceregion



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Nur Texture2D und Puffer können im Speicher, auf den GPU zugreifen kann, kopiert werden.<br/> Texture3D kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Zugriff kopiert werden.<br/> Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Speicherplatz kopiert werden.<br/> Sie können keine mipzugeordneten volumetexturen kopieren. <br/> $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcopyresource"></a>Verknüpfung id3d11devicecontext aus:: copyresource



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Nur Texture2D und Puffer können im Speicher, auf den GPU zugreifen kann, kopiert werden.<br/> Texture3D kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Zugriff kopiert werden.<br/> Jede Ressource, die nur über D3D10_BIND_SHADER_RESOURCE verfügt, kann nicht aus dem Speicher mit GPU-Zugriff auf den CPU-Speicherplatz kopiert werden.<br/> $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcopystructurecount"></a>Verknüpfung id3d11devicecontext aus:: copystructurecount



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewfloat



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>Verknüpfung id3d11devicecontext aus:: clearunorderedaccessviewuint



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextclearrendertargetview"></a>Verknüpfung id3d11devicecontext aus:: clearrendertargetview



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nur der erste Array Slice wird gelöscht. Anwendungen sollten eine renderzielansicht für jedes Gesicht oder jeden Array Slice erstellen und dann jede Ansicht einzeln löschen. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus:: cssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcssetsamplers"></a>Verknüpfung id3d11devicecontext aus:: cssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcssetshader"></a>Verknüpfung id3d11devicecontext aus:: cssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcssetshaderresources"></a>Verknüpfung id3d11devicecontext aus:: cssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdispatch"></a>Verknüpfung id3d11devicecontext aus::D ispatch



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdispatchindirect"></a>Verknüpfung id3d11devicecontext aus::D ispatchindirekte



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdraw"></a>Verknüpfung id3d11devicecontext aus::D RAW



| Funktionsebene             | Verhaltensunterschiede                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Die Anzahl der primitiven darf 65535 nicht überschreiten.<br/> Texturen können nicht mehr als 128 mal über ein primitiv wiederholt werden.<br/>    |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Die Anzahl der primitiven darf 1048575 nicht überschreiten.<br/> Texturen können nicht mehr als 2048 mal über ein primitiv wiederholt werden.<br/> |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Die Anzahl der primitiven darf 1048575 nicht überschreiten.<br/> Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>Verknüpfung id3d11devicecontext aus::D rawauto



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdrawindexed"></a>Verknüpfung id3d11devicecontext aus::D rawindebug



| Funktionsebene             | Verhaltensunterschiede                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Die Anzahl der primitiven darf 65535 nicht überschreiten.<br/> Texturen können nicht mehr als 128 mal über ein primitiv wiederholt werden.<br/> Index Werte dürfen nicht größer sein als 65534.<br/> Indizierte Punkt Listen werden nicht unterstützt.<br/>      |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Die Anzahl der primitiven darf 1048575 nicht überschreiten.<br/> Texturen können nicht mehr als 2048 mal über ein primitiv wiederholt werden.<br/> Index Werte dürfen nicht größer sein als 1048575.<br/> Indizierte Punkt Listen werden nicht unterstützt.<br/> |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Die Anzahl der primitiven darf 1048575 nicht überschreiten.<br/> Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.<br/> Index Werte dürfen nicht größer sein als 1048575.<br/> Indizierte Punkt Listen werden nicht unterstützt.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>Verknüpfung id3d11devicecontext aus::D rawindexedinstangeleitet



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nicht unterstützt $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Die Anzahl der primitiven darf 1048575 nicht überschreiten.<br/> Texturen können nicht mehr als 8192 Mal über ein primitiv wiederholt werden.<br/> Index Werte dürfen nicht größer sein als 1048575.<br/>
<blockquote>
[!Note]<br />
Wenn Sie die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>drawindexedinstanbound</strong></a> -Methode mit einem Vertex-Shader aufrufen, der an die Pipeline gebunden ist und keine instanzbezogenen Daten importiert, zeichnet einige Direct3D 9-Grafikhardware möglicherweise nichts. Insbesondere wenn der Vertex-Shader keine instanzbezogenen Daten verwendet, entspricht das Aufrufen von <strong>drawindexedinstanreceimit</strong> 1 Instance nicht dem aufrufenden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Zeichnen</strong></a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>Verknüpfung id3d11devicecontext aus::D rawindexedinstancedindirect



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdrawinstanced"></a>Verknüpfung id3d11devicecontext aus::D rawinstanzierte



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>Verknüpfung id3d11devicecontext aus::D rawinstancedindirect



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus::D ssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdssetsamplers"></a>Verknüpfung id3d11devicecontext aus::D ssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdssetshader"></a>Verknüpfung id3d11devicecontext aus::D ssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextdssetshaderresources"></a>Verknüpfung id3d11devicecontext aus::D ssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus:: gssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextgssetsamplers"></a>Verknüpfung id3d11devicecontext aus:: gssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextgssetshader"></a>Verknüpfung id3d11devicecontext aus:: gssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextgssetshaderresources"></a>Verknüpfung id3d11devicecontext aus:: gssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus:: hssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontexthssetsamplers"></a>Verknüpfung id3d11devicecontext aus:: hssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontexthssetshader"></a>Verknüpfung id3d11devicecontext aus:: hssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontexthssetshaderresources"></a>Verknüpfung id3d11devicecontext aus:: hssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Wird auf keiner 9. *-oder 10. *-Funktionsebene unterstützt. $ {Remove} $<br />
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
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Das Format darf sich von dem bei der Puffer Erstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung entstehen.<br/> Ermöglicht nur Index Puffer mit dem DXGI_FORMAT_R16_UINT-Format. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Das Format darf sich von dem bei der Puffer Erstellung angegebenen unterscheiden, es wird jedoch eine teure Übersetzung entstehen.<br/> Ermöglicht Index Puffer mit den DXGI_FORMAT_R16_UINT-und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher. <br/> $ {Remove} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Primitive Topologien mit Unterstützung werden nicht unterstützt $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextomsetblendstate"></a>Verknüpfung id3d11devicecontext aus:: omsetblendstate



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Samplemask darf nicht NULL $ {Remove} $ sein.<br />
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



 

## <a name="id3d11devicecontextomsetrendertargets"></a>Verknüpfung id3d11devicecontext aus:: omgtrendertargets



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur ein Renderziel unterstützt $ {Remove} $.<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Es werden nur vier Renderziele unterstützt, und alle gebundenen Ressourcen müssen über die gleiche Bittiefe verfügen.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>Verknüpfung id3d11devicecontext aus:: omabtrendertargesorandunorderedaccessviews



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus::P ssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Siehe Featureebene 10,0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 32 $ {Remove} $ nicht überschreiten.<br />
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



 

## <a name="id3d11devicecontextpssetsamplers"></a>Verknüpfung id3d11devicecontext aus::P ssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Maximal 16 Samplern können an $ {Remove} $ gebunden werden.<br />
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



 

## <a name="id3d11devicecontextpssetshader"></a>Verknüpfung id3d11devicecontext aus::P ssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur ps_4_0_level_9_1 $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextpssetshaderresources"></a>Verknüpfung id3d11devicecontext aus::P ssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nicht mehr als 8 gleichzeitig gebundene Shaderressourcen $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextrssetscissorrects"></a>Verknüpfung id3d11devicecontext aus:: rssezcissorrects



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Es ist nur das NULL "nullte Scheren" verfügbar: $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextrssetviewports"></a>Verknüpfung id3d11devicecontext aus:: rssetviewports



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Nur der nullten nullten ist verfügbar $ {Remove} $.<br />
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



 

Obwohl Sie Gleit Komma Werte für die Elemente der [**D3D11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) -Struktur für das *pviewports* -Array in einem-Aufrufe [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) für die Featureebene 9 x angeben [](overviews-direct3d-11-devices-downlevel-intro.md) \_ , verwendet **rssetviewports** intern DWORDs. Aufgrund dieses Verhaltens schlägt der Aufrufe von **rssetviewports** für featureebenen 9 x fehl, wenn Sie für den Viewport eine negative obere linke Ecke verwenden \_ . Dieser Fehler tritt auf, weil **rssetviewports** für 9 \_ x die Gleit Komma Werte ohne Validierung in ganze Zahlen ohne Vorzeichen umwandelt, was zu einem ganzzahligen Überlauf führt.

Der [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) -Befehl für die featureebenen 10 [](overviews-direct3d-11-devices-downlevel-intro.md) \_ x und 11 \_ x funktioniert erwartungsgemäß, auch wenn Sie für den Viewport eine negative obere linke Ecke verwenden.

## <a name="id3d11devicecontextsetpredication"></a>Verknüpfung id3d11devicecontext aus:: setprediation



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextsosettargets"></a>Verknüpfung id3d11devicecontext aus:: sosettargets



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>Verknüpfung id3d11devicecontext aus:: vssetconstantbuffers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Siehe Featureebene 10,0, aber die Gesamtzahl der vom Shader verwendeten Konstanten darf 255 $ {Remove} $ nicht überschreiten.<br />
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



 

## <a name="id3d11devicecontextvssetsamplers"></a>Verknüpfung id3d11devicecontext aus:: vssetsamplers



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextvssetshader"></a>Verknüpfung id3d11devicecontext aus:: vssetshader



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Nur vs_4_0_level_9_1 $ {Remove} $<br />
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



 

## <a name="id3d11devicecontextvssetshaderresources"></a>Verknüpfung id3d11devicecontext aus:: vssetshaderresources



<table>
<thead>
<tr class="header">
<th>Funktionsebene</th>
<th>Verhaltensunterschiede</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Wird auf keiner 9. *-Funktionsebene unterstützt. $ {Remove} $<br />
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

[10level9-Referenz](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





