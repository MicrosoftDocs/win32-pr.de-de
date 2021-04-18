---
description: Die ID3DXPRTEngine-Schnittstelle wird verwendet, um eine PRT-Simulation (preberechneten Radiance Transfer) zu berechnen. Die zugehörigen Methoden werden in der Regel offline verwendet, um pro-Vertex-oder pro-texübertragungs-Vektoren im Vorfeld der 3D-Echt Zeit Modellierung zu berechnen.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: ID3DXPRTEngine-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: 5507a79a60b2ffcb3cf801ea0454c7306bcde056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365079"
---
# <a name="id3dxprtengine-interface"></a>ID3DXPRTEngine-Schnittstelle

Die ID3DXPRTEngine-Schnittstelle wird verwendet, um eine PRT-Simulation (preberechneten Radiance Transfer) zu berechnen. Die zugehörigen Methoden werden in der Regel offline verwendet, um pro-Vertex-oder pro-texübertragungs-Vektoren im Vorfeld der 3D-Echt Zeit Modellierung zu berechnen.

## <a name="members"></a>Member

Die **ID3DXPRTEngine** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXPRTEngine** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTEngine** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Closestrayintersekten**](id3dxprtengine--closestrayintersects.md)                       | Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wenn eine Schnittmenge gefunden wird, gibt die Methode den Index der nächstgelegenen Mesh-Oberfläche zurück, die vom Strahl und den baryzentrischen Koordinaten des Schnittstellen Punkts getroffen wird.<br/>                                                                                                                                                                                |
| [**Computebounce**](id3dxprtengine--computebounce.md)                                     | Berechnet den Quell Strahl, der sich aus einem einzelnen Sprung der interreflektierten hell ergibt. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.<br/>                                                                                                                                                                                                                                                    |
| [**Computebounceadaptive**](id3dxprtengine--computebounceadaptive.md)                     | Berechnet den Quell Glanz, der sich aus einem einzelnen Sprung der interreflektierten hell mit adaptiver Stichprobenentnahme ergibt. Diese Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.<br/>                                                                                                                   |
| [**Computedirectlightingsh**](id3dxprtengine--computedirectlightingsh.md)                 | Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung durch eine kugelförmige Näherung (SH) dargestellt wird.<br/>                                                                                                                                                                                                                                                                                                                            |
| [**Computedirectlightingshadaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung mithilfe der adaptiven Stichprobenentnahme durch eine Glanz Näherung (SH) dargestellt wird. Diese Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen.<br/>                                                                                                                                                           |
| [**Computedirectlightingshgpu**](id3dxprtengine--computedirectlightingshgpu.md)           | Verwendet die GPU, um den direkten Beleuchtungs Beitrag zu 3D-Objekten zu berechnen, wobei die Quell Ausstrahlung durch eine Glanz förmige Näherung (SH) dargestellt wird. Das Berechnen der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.<br/>                                                                                                                                                                                                                            |
| [**Computeldprtcoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Berechnet lokal Aufzähl Bare (ldprt-) Koeffizienten (ldprt)-Koeffizienten in Relation zu pro-Sample-normal Vektoren, um den Fehler der geringsten Quadrate in Bezug auf Eingabe [**ID3DXPRTBuffer**](id3dxprtbuffer.md) Daten zu minimieren. Diese Koeffizienten können mit häufenden oder transformierten normalen Vektoren verwendet werden, um globale Effekte auf dynamische Objekte zu modellieren.<br/>                                                                                                                     |
| [**Berechnungen**](id3dxprtengine--computess.md)                                             | Berechnet mithilfe von Materialeigenschaften, die von [**ID3DXPRTEngine:: setmeschmaterials**](id3dxprtengine--setmeshmaterials.md)festgelegt wurden, die Quell Strahlung, die sich aus der unter Oberflächenstruktur ergibt. Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.<br/>                                                                                                                                                                                                       |
| [**Rechen Adaptive**](id3dxprtengine--computessadaptive.md)                             | Berechnet einen Übertragungs Vektor, der die Quell Strahlung zum Beenden von Strahlen zuordnet, die sich aus der unter Surface-Aufteilung ergeben, wobei Adaptive Stichprobenentnahme und Materialeigenschaften verwendet werden, die von [**ID3DXPRTEngine:: setmeschmaterials**](id3dxprtengine--setmeshmaterials.md) Die-Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen. Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.<br/> |
| [**Computesurf samplesbounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Berechnet PRT-Proben (preberechneten Radiance Transfer) für einen beliebigen Punkt (und den normalen Vektor).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**Computesurf samplesdirectsh**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Berechnet an einem beliebigen Punkt, der nicht in einem Mesh ist, einen Übertragungs Vektor, der Quell Strahlen (dargestellt durch eine Glanz Näherung (SH)) zum Beenden der Strahlung zuordnet.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Computevolumesamples**](id3dxprtengine--computevolumesamples.md)                       | Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Licht Sprung in eine kugelförmige (SH) Basis Vektoren, die den Vorfall Glanz an angegebenen Orten darstellen.<br/>                                                                                                                                                                                                                                                                                         |
| [**Computevolumesamplesdirectsh**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Berechnet eine Projektion entfernter Beleuchtung in eine kugelförmige (SH) Basis Vektoren, die die Ereignis Strahlen an angegebenen Orten darstellen.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**Extractpervertexalbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Kopiert pro-Vertex-Albedo-Werte aus einem Mesh.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Freibouncedata**](id3dxprtengine--freebouncedata.md)                                   | Gibt Arbeitsspeicher frei, der für temporäre, bounplizierte Simulationsdaten genutzt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Freess Data**](id3dxprtengine--freessdata.md)                                           | Gibt Arbeitsspeicher frei, der für das temporäre Verteilen von Simulationsdaten auf der Oberfläche verwendet wird<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Getadaptedmesh**](id3dxprtengine--getadaptedmesh.md)                                   | Gibt ein Mesh mit Änderungen zurück, die sich aus der Adaptive räumlichen Stichprobe ergeben Das zurückgegebene Mesh enthält nur Positionen, normale und Texturkoordinaten (sofern definiert).<br/>                                                                                                                                                                                                                                                                                                   |
| [**Getnumgesichter**](id3dxprtengine--getnumfaces.md)                                         | Ruft die Anzahl der Gesichter im Mesh ab, einschließlich aller neuen Flächen, die als Ergebnis der adaptiven räumlichen Stichprobenentnahme hinzugefügt wurden.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**Getnumverts**](id3dxprtengine--getnumverts.md)                                         | Ruft die Anzahl der Scheitel Punkte im Mesh ab, einschließlich aller neuen Scheitel Punkte, die als Ergebnis der adaptiven räumlichen Stichprobenentnahme hinzugefügt wurden.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**Getvertexalbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Ruft Albedo-Werte der Mesh-Scheitel Punkte ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Multiplyalbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multipliziert jeden PRT-Vektor (preberechneten Radiance Transfer) mit dem pro-Vertex-Albedo.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Resamplebuffer**](id3dxprtengine--resamplebuffer.md)                                   | Gibt einen [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer für die Eingabe erneut aus und speichert ihn in einem Ausgabepuffer. Diese Methode kann verwendet werden, um einen Vertex-Puffer in einen Textur Puffer zu konvertieren und umgekehrt. Sie kann auch verwendet werden, um Puffer mit einem Kanal in 3-Kanal-Puffer zu konvertieren und umgekehrt.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Unterteilt Gesichter in einem Mesh und ermöglicht eine konservative Adaptive Stichprobenentnahme, bei der keine Features im Mesh entfernt werden.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**Scalemeschchunk**](id3dxprtengine--scalemeshchunk.md)                                   | Skaliert alle einem angegebenen submesh zugeordneten Beispiele. Die-Methode ist nützlich für das Berechnen der unter Surface-Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallback**](id3dxprtengine--setcallback.md)                                         | Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abzurufenden sphärischen (SH) Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubrechen.<br/>                                                                                                                                                                                                                                                                               |
| [**"*"**](id3dxprtengine--setmeshmaterials.md)                               | Legt gittermaterial Eigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Parameter für die unter Surface-Verteilung anzugeben.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**Setminmaxschnitt Menge**](id3dxprtengine--setminmaxintersection.md)                     | Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest. Diese Entfernungs Werte können verwendet werden, um die minimale oder maximale Entfernung zu steuern, die Objekte durch Schatten oder Licht widerspiegeln können. Beispielsweise kann die-Methode verwendet werden, um den shadodown der in der Nähe befindlichen Funktionen eines 3D-Modells einzuschränken.<br/>                                                                                                                                                                          |
| [**Setpertexelalbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Legt einen Albedo-Wert für jeden Texttyp fest, wobei vorherige Albedo-Werte überschrieben werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Setpertexelnormal**](id3dxprtengine--setpertexelnormal.md)                             | Legt einen normalen Vektor für jeden Texttyp in einem Textur Objekt fest. Diese Methode wird verwendet, um Scheitelpunkt normale Vektoren aus einem Mesh (oder interpoliert Vertex-Normale) zu speichern, wenn die pixelbasierte Voraus berechnete Strahlungs Übertragung (PRT) berechnet wird).<br/>                                                                                                                                                                                                                                          |
| [**Setpervertexalbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Legt einen Albedo-Wert für jeden Gitter Scheitelpunkt fest, wobei vorherige Albedo-Werte überschrieben werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Setsamplinginfo**](id3dxprtengine--setsamplinginfo.md)                                 | Legt Sampling-Eigenschaften fest, die vom PRT-Simulator (preberechnetes Radiance Transfer) verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Shadowrayintersekten**](id3dxprtengine--shadowrayintersects.md)                         | Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wird normalerweise verwendet, um zu bestimmen, ob ein bestimmter Punkt im Schatten ist.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Die folgende Formel wird verwendet, um von RGB in Leuchtkraft Werte zu konvertieren:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



Die **ID3DXPRTEngine** -Schnittstelle wird durch Aufrufen der [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) -Funktion abgerufen.

Der LPD3DXPRTENGINE-Typ wird als Zeiger auf die **ID3DXPRTEngine** -Schnittstelle definiert.


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Voraus berechnete Strahlungs Übertragung (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
