---
description: Die ID3DXPRTEngine-Schnittstelle wird verwendet, um eine PRT-Simulation (Precomputed Radiance Transfer) zu berechnen. Die Methoden werden in der Regel offline verwendet, um vor der 3D-Echtzeitmodellierung Übertragungsvektoren pro Scheitelpunkt oder pro Texel zu berechnen.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: ID3DXPRTEngine-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bef527f9044c01b0696e86b44ddaef7ec72c336771ed136ddd071d11c0d73836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293354"
---
# <a name="id3dxprtengine-interface"></a>ID3DXPRTEngine-Schnittstelle

Die ID3DXPRTEngine-Schnittstelle wird verwendet, um eine PRT-Simulation (Precomputed Radiance Transfer) zu berechnen. Die Methoden werden in der Regel offline verwendet, um vor der 3D-Echtzeitmodellierung Übertragungsvektoren pro Scheitelpunkt oder pro Texel zu berechnen.

## <a name="members"></a>Member

Die **ID3DXPRTEngine-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTEngine** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTEngine-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gitter schneidet. Wenn eine Schnittmenge gefunden wird, gibt die Methode den Index des nächstgelegenen Gittergesichts, das vom Strahl getroffen wird, und die baryzentrierten Koordinaten des Schnittpunkts zurück.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Berechnet die Quellspiegelung, die sich aus einem einzelnen Bounce des gespiegelten Lichts ergibt. Diese Methode kann für jede litierte Szene verwendet werden, einschließlich eines SH-basierten PRT-Modells (Precomputed Radiance Transfer).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Berechnet die Quellausnahme, die sich aus einem einzelnen Bounce des gespiegelten Lichts ergibt, mithilfe der adaptiven Stichprobenentnahme. Diese Methode generiert neue Scheitelzeichen und Gesichter im Gitternetz, um das PRT-Signal (Precomputed Radiance Transfer) genauer zu ungefähren. Diese Methode kann für jede beliebige lit-Szene verwendet werden, einschließlich eines SH-basierten PRT-Modells (Pherical Scene).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quellleistung durch eine pherische Tropenmaße (SH) näherung dargestellt wird.<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quelllichtleistung durch eine Sh-Näherung (Pherical Computing) mit adaptiver Stichprobenentnahme dargestellt wird. Diese Methode generiert neue Scheitelzeichen und Gesichter im Gitternetz, um das PRT-Signal (Precomputed Radiance Transfer) genauer zu ungefähren.<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSLKPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Verwendet die GPU, um den direkten Beleuchtungsbeitrag zu 3D-Objekten zu berechnen, bei denen die Quellleistung durch eine pherische Schwingung (SH) dargestellt wird. Die Berechnung der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Berechnet lokal deformierbare precomputed radiance transfer (LDPRT)-Koeffizienten relativ zu normalen Vektoren pro Stichprobe, um den Fehler mit den geringsten Quadraten in Bezug auf eingabebasierte [**ID3DXPRTBuffer-Daten**](id3dxprtbuffer.md) zu minimieren. Diese Koeffizienten können mit skinnierten oder transformierten normalen Vektoren verwendet werden, um globale Effekte auf dynamische Objekte zu modellieren.<br/>                                                                                                                     |
| [**ComputeSS**](id3dxprtengine--computess.md)                                             | Berechnet die Quellfläche, die sich aus der Subsurface-Punktung ergibt, mithilfe von Materialeigenschaften, die von [**ID3DXPRTEngine::SetMeshMaterials festgelegt werden.**](id3dxprtengine--setmeshmaterials.md) Diese Methode kann nur für Materialien verwendet werden, die pro Scheitelpunkt in einem Gittermodellobjekt definiert sind.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Berechnet einen Übertragungsvektor, der die Quellfläche zu einer Ausgangsfläche zuordnt, die sich aus der Subsurface-Punktung ergibt. Dabei werden die adaptive Stichprobenentnahme und die von [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)festgelegten Materialeigenschaften verwendet. Die -Methode generiert neue Scheitelzeichen und Gesichter im Gitternetz, um das PRT-Signal (Precomputed Radiance Transfer) genauer zu ungefähren. Diese Methode kann nur für Materialien verwendet werden, die pro Scheitelpunkt in einem Gittermodellobjekt definiert sind.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Berechnet PRT-Stichproben (Precomputed Radiance Transfer) für einen beliebigen Punkt (und normalen Vektor).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Berechnet einen Übertragungsvektor an einem beliebigen Punkt, der sich nicht in einem Gitternetz befandt, der die Quellauslassung (dargestellt durch eine pherische Rumpf-SH-Näherung) zu einer Beendigungsauslassung zu ordnet.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Lichtsprung in SH-Basisvektoren (Spherical Computing), die die Darstellung von Vorfällen an bestimmten Stellen darstellen.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Berechnet eine Projektion der weit entfernten Beleuchtung in SH-Basisvektoren (Pherical Computing), die die Darstellung von Vorfällen an bestimmten Stellen darstellen.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Kopiert Albedo-Werte pro Scheitelpunkt aus einem Gitternetz.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Gibt Arbeitsspeicher frei, der für temporäre bounced-light-Simulationsdaten verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Gibt Arbeitsspeicher frei, der für temporäre Simulationsdaten zur Lichts streuendes Unteroberflächenlicht verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Gibt ein Gitternetz mit Änderungen zurück, die sich aus adaptiver räumlicher Stichprobenentnahme ergeben. Das zurückgegebene Gitternetz enthält nur Positionen, Normalstellen und Texturkoordinaten (sofern definiert).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Ruft die Anzahl der Gesichter im Netz ab, einschließlich aller neuen Gesichter, die als Ergebnis der adaptiven räumlichen Stichprobenentnahme hinzugefügt wurden.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Ruft die Anzahl der Scheitelzeichen im Gitternetz ab, einschließlich aller neuen Scheitelzeichen, die als Ergebnis der adaptiven räumlichen Stichprobenentnahme hinzugefügt wurden.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Ruft Albedo-Werte der Gitternetzvertices ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multipliziert jeden vorausbesetzten PRT-Vektor (Radiance Transfer) mit dem Pro-Vertex-Albedo.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Verwendet einen [**ID3DXPRTBuffer-Eingabepuffer neu**](id3dxprtbuffer.md) und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Scheitelpunktpuffer in einen Texturpuffer zu konvertieren und umgekehrt. Sie kann auch zum Konvertieren von Einkanalpuffern in 3-Kanal-Puffer und umgekehrt verwendet werden.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Unterteilt Gesichter in ein Gitternetz, sodass eine konservative adaptive Stichprobenentnahme ermöglicht wird, bei der keine Merkmale im Gitternetz entfernt werden.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Skaliert alle Einem bestimmten Untermesh zugeordneten Stichproben. Die -Methode ist nützlich für das Berechnen von Unteroberflächen-Punktdiagrammen.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz abgeschlossener SH-Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator zu abbrechen.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Legt Gitternetzmaterialeigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Subsurface Scattering-Parameter anzugeben.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest. Diese Entfernungswerte können verwendet werden, um den minimalen oder maximalen Abstand zu steuern, den Objekte überschatten oder Licht reflektieren können. Beispielsweise kann die -Methode verwendet werden, um das Shadowing von Features in der Nähe eines 3D-Modells zu begrenzen.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Legt einen Albedo-Wert für jedes Texel fest und überschreiben vorherige Albedo-Werte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Legt einen normalen Vektor für jedes Texel in einem Texturobjekt fest. Diese Methode wird verwendet, um normale Vertexvektoren aus einem Gitternetz zu speichern (oder interpolierte Scheitelpunktnormle, wenn die pixelbasierte vorab berechnete Bogenübertragung (Precomputed Radiance Transfer, PRT) berechnet wird).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Legt einen Albedo-Wert für jeden Gitternetz-Scheitelpunkt fest und überschreiben vorherige Albedo-Werte.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Legt Samplingeigenschaften fest, die vom PRT-Simulator (Precomputed Radiance Transfer) verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Verwendet effiziente Ray-Tracing in PRT-Simulationen (Precomputed Radiance Transfer), um zu bestimmen, ob ein Strahl ein Gitter schneidet. Wird normalerweise verwendet, um zu bestimmen, ob sich ein angegebener Punkt im Schatten befindet.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Zum Konvertieren von RGB-Werten in Luminanzwerte wird die folgende Formel verwendet:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



Die **ID3DXPRTEngine-Schnittstelle** wird durch Aufrufen der [**D3DXCreatePRTEngine-Funktion**](d3dxcreateprtengine.md) ermittelt.

Der LPD3DXPRTENGINE-Typ ist als Zeiger auf die **ID3DXPRTEngine-Schnittstelle** definiert.


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Vorausberechnungsübertragung der Radiance (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
