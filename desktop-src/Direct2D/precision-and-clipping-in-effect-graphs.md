---
title: Genauigkeit und numerische Clipping in Effektdiagrammen
description: Anwendungen, die Effekte mit Direct2D rendern, müssen darauf achten, das gewünschte Maß an Qualität und Vorhersagbarkeit in Bezug auf die numerische Genauigkeit zu erreichen.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f2af6fdee4561caa60ea22a0c700593f2333727e6c5a63c5346fdc78bbdb40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160504"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Genauigkeit und numerische Clipping in Effektdiagrammen

Anwendungen, die Effekte mit Direct2D rendern, müssen darauf achten, das gewünschte Maß an Qualität und Vorhersagbarkeit in Bezug auf die numerische Genauigkeit zu erreichen. In diesem Thema werden bewährte Methoden und relevante Einstellungen in Direct2D beschrieben, die in folgenden Situationen nützlich sind:

-   Ihr Effektdiagramm basiert auf hoher numerischer Genauigkeit oder Farben außerhalb des \[ Bereichs 0, \] 1, und Sie möchten sicherstellen, dass diese immer verfügbar sind.
-   Oder Ihr Effektdiagramm basiert auf der Renderingimplementierung, um Zwischenfarben an den \[ Bereich 0, 1 zu klammern, \] und Sie möchten sicherstellen, dass diese Klammer immer auftritt.

Direct2D unterteilt häufig ein Effektdiagramm in Abschnitte und rendert jeden Abschnitt in einem separaten Schritt. Die Ausgabe einiger Schritte kann in Direct3D-Zwischentexturen gespeichert werden, die standardmäßig einen begrenzten numerischen Bereich und eine begrenzte Genauigkeit aufweisen. Direct2D garantiert nicht, ob oder wo diese Zwischentexturen verwendet werden. Dieses Verhalten kann je nach GPU-Funktionen sowie zwischen Windows Versionen variieren.

In Windows 10 verwendet Direct2D aufgrund der Verwendung der Shaderverknüpfung weniger Zwischentexturen. Direct2D erzeugt daher möglicherweise andere Ergebnisse mit Standardeinstellungen als in früheren Windows Releases. Dies betrifft in erster Linie Szenarien, in denen die Shaderverknüpfung in einem Effektdiagramm möglich ist, und dieses Diagramm enthält auch Effekte, die Ausgabefarben mit erweitertem Bereich erzeugen.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Übersicht über Effektrendering und Zwischenstufen

Um ein Effektdiagramm zu rendern, sucht Direct2D zunächst den zugrunde liegenden Graphen von "Transformationen", wobei eine Transformation ein graphischer Knoten ist, der innerhalb eines Effekts verwendet wird. Es gibt verschiedene Arten von Transformationen, einschließlich derjenigen, die Direct3D-Shader für direct2D zur Verwendung bereitstellen.

Beispielsweise kann Direct2D ein Effektdiagramm wie folgt rendern:

![Effektdiagramm mit Zwischentexturen](images/precision-and-clipping-1.png)

Direct2D sucht nach Möglichkeiten, die Anzahl von Zwischentexturen zu reduzieren, die zum Rendern des Effektdiagramms verwendet werden. Diese Logik ist für Anwendungen nicht transparent. Beispielsweise kann das folgende Diagramm von Direct2D mit einem Direct3D-Zeichnen-Aufruf und ohne Zwischentexturen gerendert werden:

![Effektdiagramm ohne Zwischentexturen](images/precision-and-clipping-2.png)

Vor Windows 10 verwendete Direct2D immer Zwischentexturen, wenn mehrere Pixelshader innerhalb desselben Effektdiagramms verwendet wurden. Die meisten integrierten Effekte, die einfach Farbwerte anpassen (z. B. Helligkeit oder Sättigung), verwenden hierfür Pixelshader.

In Windows 10 kann Direct2D jetzt in solchen Fällen die Verwendung von Zwischentexturen vermeiden. Hierzu werden benachbarte Pixel-Shader intern verknüpft. Beispiel:

![Windows 10-Effektdiagramm mit mehreren Pixel-Shadern und ohne Zwischentexturen](images/precision-and-clipping-3.png)

Beachten Sie, dass nicht alle benachbarten Pixel-Shader in einem Diagramm miteinander verknüpft werden können und daher nur bestimmte Diagramme unterschiedliche Ausgaben auf Windows 10 erzeugen. Ausführliche Informationen finden Sie unter [Effekt-Shaderverknüpfung.](effect-shader-linking.md) Die wichtigsten Einschränkungen sind:

-   Ein Effekt wird nicht mit Effekten verknüpft, die seine Ausgabe nutzen, wenn der erste Effekt als Eingabe mit mehreren Effekten verbunden ist.
-   Ein Effekt wird nicht mit einem Effekt verknüpft, der als Eingabe festgelegt ist, wenn der erste Effekt seine Eingabe an einer anderen logischen Position als seine Ausgabe abtampt. Beispielsweise kann ein Color Matrix-Effekt mit seiner Eingabe verknüpft werden, aber ein Convolution-Effekt ist dies nicht.

## <a name="built-in-effect-behavior"></a>Integriertes Effektverhalten

Viele integrierte Effekte können Farben außerhalb des \[ Bereichs 0, 1 \] im nicht mehr verwendeten Farbraum erzeugen, auch wenn sich ihre Eingabefarben innerhalb dieses Bereichs befinden. In diesem Fall können solche Farben numerischen Clippings unterliegen. Beachten Sie, dass es wichtig ist, den Farbbereich im nicht prämultiplizieren Bereich zu berücksichtigen, obwohl integrierte Effekte in der Regel Farben im prämultipliierten Raum erzeugen. Dadurch wird sichergestellt, dass farben innerhalb des Bereichs bleiben, auch wenn andere Effekte später unprämultiply sind.

Einige der Effekte, die diese außerhalb des Bereichs enthaltenen Farben ausgeben können, bieten eine "ClampOutput"-Eigenschaft. Dazu gehören:

-   [Farbmatrix](color-matrix.md)
-   [Arithmetische Zusammengesetzte](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Übertragungseffekte](built-in-effects.md)

Wenn Sie die Eigenschaft "ClampOutput" für diese Effekte auf TRUE festlegen, wird sichergestellt, dass unabhängig von Faktoren wie der Shaderverknüpfung ein konsistentes Ergebnis erzielt wird. Beachten Sie, dass die Klammer in einem nicht mehr vorkommenden Bereich auftritt.

Andere integrierte Effekte können auch Ausgabefarben erzeugen, die über den \[ Bereich 0, 1 \] im nicht verallgemeinerten Bereich hinausgehen, auch wenn sich deren Farbpixel (und ggf. "Color"-Eigenschaften) innerhalb dieses Bereichs befinden. Dazu gehören:

-   [Transformations- und Skalierungseffekte](built-in-effects.md) (wenn die Interpolationsmodus-Eigenschaft kubisch oder kubisch von hoher Qualität ist)
-   [Beleuchtungseffekte](built-in-effects.md)
-   [Edgeerkennung](edge-detection-effect.md) (wenn die Overlay Edges-Eigenschaft TRUE ist)
-   [Exposition](exposure-effect.md)
-   [Zusammengesetzt](composite.md) (wenn die Mode-Eigenschaft "Plus" ist)
-   [Temperatur und Tönung](temperature-and-tint-effect.md)
-   [Sepia](sepia-effect.md)
-   [Sättigung](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Erzwingen des numerischen Clippings innerhalb eines Effektdiagramms

Bei der Verwendung der oben aufgeführten Effekte, die über keine "ClampOutput"-Eigenschaft verfügen, sollten Anwendungen erwägen, numerisches Klammern zu erzwingen. Dies kann erreicht werden, indem ein zusätzlicher Effekt in das Diagramm eingefügt wird, der seine Pixel einbindet. Es kann ein Color Matrix-Effekt verwendet werden, bei dem seine "ClampOutput"-Eigenschaft auf TRUE festgelegt ist und die ColorMatrix-Eigenschaft als Standardwert (Pass-Through) belassen wird.

Eine zweite Option, um konsistente Ergebnisse zu erzielen, besteht darin, anzufordern, dass Direct2D Zwischentexturen mit höherer Genauigkeit verwendet. Dies wird im Folgenden beschrieben.

## <a name="controlling-precision-of-intermediate-textures"></a>Steuern der Genauigkeit von Zwischentexturen

Direct2D bietet einige Möglichkeiten, die Genauigkeit eines Diagramms zu steuern. Vor der Verwendung von Formaten mit hoher Genauigkeit in Direct2D müssen Anwendungen sicherstellen, dass sie von der GPU ausreichend unterstützt werden. Um dies zu überprüfen, verwenden Sie [**ID2D1DeviceContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Anwendungen können ein Direct3D-Gerät mit WARP (Softwareemulation) erstellen, um sicherzustellen, dass alle Puffergenauigkeiten unabhängig von der tatsächlichen GPU-Hardware auf dem Gerät unterstützt werden. Dies wird in Szenarien wie dem Anwenden von Effekten auf ein Foto beim Speichern auf dem Datenträger empfohlen. Auch wenn Direct2D Pufferformate mit hoher Genauigkeit auf der GPU unterstützt, wird die Verwendung von WARP in diesem Szenario für GPUs auf Featureebene 9.X empfohlen, da die Arithmetik und Stichprobenentnahme von Shadern bei einigen mobilen GPUs mit geringer Leistung eingeschränkt ist.

In jedem der folgenden Fälle entspricht die angeforderte Genauigkeit der minimalen Genauigkeit, die Direct2D verwendet. Eine höhere Genauigkeit kann verwendet werden, wenn keine Zwischenschritte erforderlich sind. Direct2D kann auch Zwischentexturen für verschiedene Teile desselben Diagramms oder unterschiedliche Diagramme vollständig gemeinsam nutzen. In diesem Fall verwendet Direct2D die maximale Genauigkeit, die für alle beteiligten Vorgänge angefordert wird.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Genauigkeitsauswahl aus ID2D1DeviceContext::SetRenderingControls

Die einfachste Möglichkeit, die Genauigkeit der Zwischentexturen von Direct2D zu steuern, ist die Verwendung von [**ID2D1DeviceContext::SetRenderingControls.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)) Dadurch wird die Genauigkeit aller Zwischentexturen gesteuert, solange eine Genauigkeit nicht auch manuell für Effekte oder Transformationen direkt festgelegt wird.


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>Genauigkeitsauswahl aus Eingaben und Renderzielen

Anwendungen können sich auch auf die Genauigkeit der Eingaben in einem Effektdiagramm verlassen, um die Genauigkeit von Zwischentexturen zu steuern. Dies gilt, solange die Puffergenauigkeit nicht mit [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))angegeben wird und nicht manuell für Effekte und die direkte Transformation festgelegt wird.

Die Genauigkeiten der Eingaben für Effekte werden durch das Diagramm weitergegeben, um die Genauigkeit der downstreamen Zwischenstufen auszuwählen. Wenn verschiedene Verzweigungen im Effektdiagramm aufeinander treffen, wird die größte Genauigkeit jeder Eingabe verwendet.

Die auf der Grundlage einer Direct2D-Bitmap ausgewählte Genauigkeit wird anhand des Pixelformats bestimmt. Die für eine [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) ausgewählte Genauigkeit wird anhand des WIC-Pixelformats der zugrunde liegenden IWICBitmapSource bestimmt, die zum Erstellen der **ID2D1ImageSource** verwendet wird. Beachten Sie, dass Direct2D nicht zulässt, dass Bildquellen mit WIC-Quellen mit Genauigkeiten erstellt werden, die von Direct2D und der GPU nicht unterstützt werden.

Es ist möglich, dass Direct2D einem Effekt basierend auf den Eingaben keine Genauigkeit zuweisen kann. Dies geschieht, wenn ein Effekt über keine Eingaben verfügt oder wenn eine [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) verwendet wird, die keine bestimmte Genauigkeit hat. In diesem Fall wird die Genauigkeit von Zwischentexturen anhand der Bitmap bestimmt, die als aktuelles Renderziel des Kontexts festgelegt wird.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Genauigkeitsauswahl direkt auf den Effekt und die Transformationen

Die minimale Genauigkeit für Zwischentexturen kann auch an expliziten Positionen innerhalb eines Effektdiagramms festgelegt werden. Dies wird nur für erweiterte Szenarien empfohlen.

Die minimale Genauigkeit kann mithilfe einer -Eigenschaft für einen Effekt wie folgt festgelegt werden:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Innerhalb einer Effect-Implementierung kann die minimale Genauigkeit mit ID2D1RenderInfo::SetOutputPrecision wie folgt festgelegt werden:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Beachten Sie, dass die für einen Effekt festgelegte Genauigkeit an Downstreameffekte im gleichen Effektdiagramm weiterverteilt wird, es sei denn, für diese Downstreameffekte wird eine andere Genauigkeit festgelegt. Die für eine Transformation innerhalb eines Effekts festgelegte Genauigkeit wirkt sich nicht auf die Genauigkeit für Downstreamtransformationsknoten aus.

Im Folgenden finden Sie die vollständige rekursive Logik, die verwendet wird, um die minimale Genauigkeit für einen Zwischenpuffer zu bestimmen, in dem die Ausgabe eines bestimmten Transformationsknotens gespeichert wird:

![Logik mit minimaler Genauigkeit des Zwischenpuffers](images/precision-and-clipping-4.png)

 

 