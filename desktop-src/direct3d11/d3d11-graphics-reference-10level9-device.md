---
title: 10level9 ID3D11Device Methoden
description: In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die ID3D11Device-Methoden aufgeführt.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390758"
---
# <a name="10level9-id3d11device-methods"></a>10level9 ID3D11Device Methoden

In diesem Abschnitt werden die Unterschiede zwischen den einzelnen 10level9-featureebenen und der D3D \_ \_ Featureebene \_ 11 \_ 0 und höher für die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Methoden aufgeführt.

-   [ID3D11Device:: checkcounter](#id3d11devicecheckcounter)
-   [ID3D11Device:: checkformatsupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device:: checkmultisamplequalitylevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device:: kreateblendstate](#id3d11devicecreateblendstate)
-   [ID3D11Device:: CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device:: up Buffer](#id3d11devicecreatebuffer)
-   [ID3D11Device:: kreatecounter](#id3d11devicecreatecounter)
-   [ID3D11Device:: "dashboardepthstencilview"](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device:: kreatedomainshader](#id3d11devicecreatedomainshader)
-   [ID3D11Device:: kreategeometryshader](#id3d11devicecreategeometryshader)
-   [ID3D11Device:: kreategeometryshaderwithstreamoutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device:: kreatehullshader](#id3d11devicecreatehullshader)
-   [ID3D11Device:: kreatinput Layout](#id3d11devicecreateinputlayout)
-   [ID3D11Device:: kreatepixelshader](#id3d11devicecreatepixelshader)
-   [ID3D11Device:: kreatepredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device:: kreatequery](#id3d11devicecreatequery)
-   [ID3D11Device:: kreaterasterizerstate](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device:: kreaterendertargetview](#id3d11devicecreaterendertargetview)
-   [ID3D11Device:: kreatesamplerstate](#id3d11devicecreatesamplerstate)
-   [ID3D11Device:: kreateshaderresourceview](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device:: CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device:: CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device:: CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device:: kreateunorderedaccessview](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device:: kreatevertexshader](#id3d11devicecreatevertexshader)
-   [ID3D11Device:: opensharedresource](#id3d11deviceopensharedresource)
-   [Zugehörige Themen](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device:: checkcounter



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
<td rowspan="3">Geräte abhängige Leistungsindikatoren werden optional unterstützt. Verwenden Sie <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: checkcounterinfo</strong></a> , um die Unterstützung zu ermitteln. $ {Remove} $<br />
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



 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device:: checkformatsupport



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
<td rowspan="3">Siehe Formatunterstützung nach <a href="overviews-direct3d-11-devices-downlevel-intro.md">Featureebene</a>$ {Remove} $<br />
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



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device:: checkmultisamplequalitylevels



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
<td rowspan="3">Funktionsebenen stellen keine Garantie bezüglich der MSAA-Unterstützung dar. $ {Remove} $<br />
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



 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device:: kreateblendstate



| Funktionsebene              | Verhaltensunterschiede                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1  | Alpha atocoverageenable muss den Wert **false** aufweisen.<br/> Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.<br/> D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.<br/> Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).<br/>                                                                                |
| D3D \_ \_ Featureebene \_ 9 \_ 2  | Alpha atocoverageenable muss den Wert **false** aufweisen.<br/> Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.<br/> Die ersten vier rendertargetschreitemasks müssen alle denselben Wert aufweisen.<br/> D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.<br/> Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).<br/> |
| D3D \_ \_ Featureebene \_ 9 \_ 3  | Alpha atocoverageenable muss den Wert **false** aufweisen.<br/> Die ersten vier blendenables müssen alle den gleichen Wert aufweisen.<br/> D3D11 \_ Blend \_ src \_ Alpha ASAT wird nicht unterstützt.<br/> Die Farbmischung aus zwei Quellen wird nicht unterstützt (srcblend oder destblend mit Quelle1 im Namen).<br/>                                                                                |
| D3D \_ \_ Featureebene \_ 10 \_ 0 | Hinzufügen von Alpha-zu-Abdeckung                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device:: CreateBlendState1



| Funktionsebene              | Verhaltensunterschiede                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ \_ Featureebene \_ 9 \_ 2  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ \_ Featureebene \_ 9 \_ 3  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ \_ Featureebene \_ 10 \_ 0 | Der *outputmergerlogicop* -Member wurde den [**D3D11 \_ Feature \_ Data D3D11- \_ \_ Optionen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)hinzugefügt, um die Unterstützung für logische Vorgänge zu bestimmen (bitweise logische Operationen zwischen der Ausgabe des Pixelshaders und dem Rendern des Ziel Inhalts). Weitere Informationen finden Sie unter [**D3D11 \_ Rendering \_ Target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device:: up Buffer



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
<td>Puffer können keine renderzielsichten aufweisen.<br/> Puffer müssen genau eine D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER aufweisen.<br/> Ermöglicht nur Index Puffer mit dem DXGI_FORMAT_R16_UINT-Format. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Puffer können keine renderzielsichten aufweisen.<br/> Puffer müssen genau eine D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER aufweisen.<br/> Ermöglicht Index Puffer mit den DXGI_FORMAT_R16_UINT-und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher. <br/> $ {Remove} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device:: kreatecounter



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



 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device:: "dashboardepthstencilview"



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
<td rowspan="3">Unterstützt keine zweiseitige Schablone. $ {Remove} $<br />
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



 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device:: kreatedomainshader



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



 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device:: kreategeometryshader



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



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device:: kreategeometryshaderwithstreamoutput



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



 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device:: kreatehullshader



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



 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device:: kreatinput Layout



| Funktionsebene             | Verhaltensunterschiede                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Unterstützt keine D3D11 \_ - \_ Eingaben \_ pro \_ Instanzdaten.                                                                |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Unterstützt keine D3D11 \_ - \_ Eingaben \_ pro \_ Instanzdaten.                                                                |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Der Vertex-Stream 0 (null) muss über D3D11 \_ input \_ pro \_ Scheitelpunkt \_ Daten verfügen, wenn Datenströme D3D11- \_ Eingaben \_ pro \_ Scheitelpunkt \_ Daten aufweisen |



 

Ausführliche Informationen dazu, welche Formate für Scheitelpunkt Daten auf den einzelnen featureebenen verwendet werden können, finden Sie im Diagramm Formatunterstützung nach [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) .

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device:: kreatepixelshader



| Funktionsebene             | Verhaltensunterschiede                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden                          |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden                          |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Muss PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3 oder PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device:: kreatepredicate



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



 

## <a name="id3d11devicecreatequery"></a>ID3D11Device:: kreatequery



| Funktionsebene             | Verhaltensunterschiede                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Ereignis Abfragen werden unterstützt. Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung.               |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Ereignis-und oksions Abfragen werden unterstützt. Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung. |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Ereignis-und oksions Abfragen werden unterstützt. Timestamp-Abfragen sind optional: Aufrufen von " [**kreatequery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) " zum Ermitteln der Unterstützung. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device:: kreaterasterizerstate



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
<td rowspan="3">"Depthclipable" muss " <strong>true</strong>" sein. Depthbiasclamp muss auf 0 festgelegt werden. $ {Remove} $<br />
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



 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device:: kreaterendertargetview



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
<td rowspan="3">Die renderzielsichten von Texture2D-Objekten können nur unterstützt werden. $ {Remove} $<br />
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



 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device:: kreatesamplerstate



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
<td>Der Vergleichs Filter wird nicht unterstützt.<br/> Die Rahmenfarbe muss innerhalb von [0, 1] liegen.<br/> Min. Lod kann nicht in Bruchzahlen stehen.<br/> Der maximale Lod-Wert muss FLT_MAX<br/> Maximale Anisotropie ist 2.<br/> D3D11_TEXTURE_ADDRESS_MIRRORONCE nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Der Vergleichs Filter wird nicht unterstützt.<br/> Die Rahmenfarbe muss innerhalb von [0, 1] liegen.<br/> Min. Lod kann nicht in Bruchzahlen stehen.<br/> Der maximale Lod-Wert muss FLT_MAX<br/> Die maximale Anzahl von Anisotropie beträgt 16.<br/> $ {Remove} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device:: kreateshaderresourceview



| Funktionsebene             | "Wstdetailedmip Plus miplevels" muss die niedrigste "LOD" (kleinste unter Quelle) enthalten. | Die Ansicht muss alle Ressourcen Array Elemente enthalten. |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Ja                                                                          | ja                                           |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Ja                                                                          | Ja                                           |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Ja                                                                          | Ja                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device:: CreateTexture1D



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



 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device:: CreateTexture2D

Für Texture2D-Ressourcen gelten Grenzwerte für Breite und Höhe, die sich über die [Funktionsebenen](overviews-direct3d-11-devices-downlevel-intro.md)unterscheiden. In den featurestufen 9 \_ 3 ist die folgende garantierte minimieren, und einzelne Implementierungen können die Anforderungen überschreiten.



| Funktionsebene             | Wenn mipcount > 1, müssen Dimensionen eine ganzzahlige Potenz von zwei sein. | Mindestens unterstützte Textur Dimension | Cubetexturen-Dimensionen müssen eine Potenz von zwei sein. | Wenn "misc \_ texturecube" festgelegt ist, lautet arraySize: | Wenn "misc \_ texturecube" nicht festgelegt ist, ist "arraySize". |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Ja                                                          | 2048                                | Ja                                           | 6                                              | 1                                                  |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Ja                                                          | 2048                                | Ja                                           | 6                                              | 1                                                  |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Ja                                                          | 4096                                | Ja                                           | 6                                              | 1                                                  |



 

In der vorherigen Tabelle lautet der vollständige Name von **misc \_ texturecube** [**D3D11 \_ Resource \_ misc \_ texturecube**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Folgendes gilt für alle 9 \_ \* [Funktionsebenen](overviews-direct3d-11-devices-downlevel-intro.md):

-   Bei Verwendung von "D3D11 \_ Usage \_ default" oder "D3D11 \_ Usage" kann " \_ bindflags" nicht gleich NULL sein.
-   Bei Verwendung der D3D11 \_ Bind- \_ tiefen \_ Schablone muss miplevels 1 sein.
-   Bei Verwendung der D3D11 \_ Bind- \_ Shader- \_ Ressource muss sampledebug. Count 1 sein.
-   Wenn D3D11 \_ Bind \_ vorhanden ist, kann die Ressource keine D3D11 \_ Bind- \_ Shader-Ressource aufweisen \_ .
-   Bei Verwendung von "d3d10 \_ DDI \_ Resource \_ misc \_ Shared" kann das Format nicht im DXGI- \_ Format vorliegen \_ R8G8B8A8 \_ unorm-oder DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device:: CreateTexture3D



| Funktionsebene             | Maximale Dimension (beliebige Achse) | Dimensionen müssen eine Potenz von zwei sein. |
|---------------------------|------------------------------|---------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | 256                          | Ja                             |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | 512                          | Ja                             |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | 512                          | Ja                             |



 

Wenn Resource D3D11 \_ Usage \_ default oder D3D11 \_ Usage \_ unveränderlich ist, kann bindflags nicht gleich NULL sein.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device:: kreateunorderedaccessview



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



 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device:: kreatevertexshader



| Funktionsebene             | Verhaltensunterschiede                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ \_ Featureebene \_ 9 \_ 1 | Muss vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden                          |
| D3D \_ \_ Featureebene \_ 9 \_ 2 | Muss vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1 verwenden                          |
| D3D \_ \_ Featureebene \_ 9 \_ 3 | Muss vs \_ 4 \_ 0 \_ Level \_ 9 \_ 3 oder vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 verwenden. |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device:: opensharedresource



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
<td rowspan="3"> Verwenden Sie <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: checkfeaturesupport</strong></a> mit dem <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> Wert und der <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> Struktur, um zu bestimmen, ob ein Format freigegeben werden kann. Wenn das Format freigegeben werden kann, gibt <strong>checkfeaturesupport</strong> das <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> -Flag zurück.<br/>
<blockquote>
[!Note]<br />
[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) und <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> sind bei Verwendung von Featureebene 9 niemals freistellbar, auch wenn das Gerät optionale Funktions Unterstützung für <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>angibt. Der Versuch, freigegebene Ressourcen mit DXGI-Formaten <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> und <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> zu erstellen, schlägt immer fehl, es sei denn, die Funktionsebene ist 10_0 oder höher.
</blockquote>
<br/> $ {Remove} $<br />
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

 

