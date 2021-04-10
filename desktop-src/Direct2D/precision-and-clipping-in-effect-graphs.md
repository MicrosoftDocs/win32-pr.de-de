---
title: Genauigkeits-und numerische Clipping in Effekt Diagrammen
description: Anwendungen, die Effekte mithilfe von Direct2D renderingeffekte darstellen, müssen darauf achten, dass die gewünschte Qualität und Vorhersagbarkeit hinsichtlich der numerischen Genauigkeit erreicht wird.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90628661ec8cd3f16ff6a6149aecbb7e8be3e5a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039446"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Genauigkeits-und numerische Clipping in Effekt Diagrammen

Anwendungen, die Effekte mithilfe von Direct2D renderingeffekte darstellen, müssen darauf achten, dass die gewünschte Qualität und Vorhersagbarkeit hinsichtlich der numerischen Genauigkeit erreicht wird. In diesem Thema werden bewährte Methoden und relevante Einstellungen in Direct2D beschrieben, die in folgenden Situationen nützlich sind:

-   Das Effekt Diagramm basiert auf hoher numerischer Genauigkeit oder Farben außerhalb des \[ Bereichs 0, 1 \] , und Sie möchten sicherstellen, dass diese stets verfügbar sind.
-   Oder das Effekt Diagramm basiert auf der Rendering-Implementierung, um zwischen Farben an den \[ Bereich 0, 1 zu binden \] , und Sie möchten sicherstellen, dass diese Klammer immer auftritt.

Direct2D unterteilt häufig ein Effekt Diagramm in Abschnitte und rendert jeden Abschnitt in einem separaten Schritt. Die Ausgabe einiger Schritte kann in zwischengeschalteten Direct3D-Texturen gespeichert werden, die standardmäßig einen begrenzten numerischen Bereich und eine begrenzte Genauigkeit aufweisen. Direct2D gibt keine Garantie dafür, ob oder wo diese zwischen Texturen verwendet werden. Dieses Verhalten kann je nach GPU-und Windows-Versionen variieren.

In Windows 10 verwendet Direct2D aufgrund der Verwendung von Shader-Verknüpfungen weniger zwischen Texturen. Direct2D kann daher unterschiedliche Ergebnisse mit Standardeinstellungen als in früheren Windows-Versionen liefern. Dies wirkt sich in erster Linie auf Szenarien aus, in denen Shader-Verknüpfungen in einem Effekt Diagramm möglich sind. dieses Diagramm enthält auch Effekte, die erweiterte Ausgabe Farben erzeugen.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Übersicht über das Rendern von Effekten und Vermittler

Um ein Effekt Diagramm zu rendereln, sucht Direct2D zuerst nach dem zugrunde liegenden Diagramm "Transformationen", bei dem eine Transformation ein in einem Effekt verwendeter Diagramm Knoten ist. Es gibt verschiedene Arten von Transformationen, einschließlich derjenigen, die Direct3D-Shader für Direct2D zur Verwendung bereitstellen.

Beispielsweise kann Direct2D ein Effekt Diagramm wie folgt Rendering:

![Effekt Diagramm mit zwischen Texturen](images/precision-and-clipping-1.png)

Direct2D sucht nach Möglichkeiten, die Anzahl zwischen Texturen zu reduzieren, die zum renderingeffekten verwendet werden. Diese Logik ist für Anwendungen nicht transparent. Das folgende Diagramm kann z. b. von Direct2D mit einem Direct3D Draw-Aufruf und ohne zwischen Texturen gerendert werden:

![Effekt Diagramm ohne zwischen Strukturen](images/precision-and-clipping-2.png)

Vor Windows 10 verwendete Direct2D immer zwischen Texturen, wenn mehrere Pixel-Shader innerhalb desselben Effekt Diagramms verwendet wurden. Die meisten integrierten Effekte, die einfach Farb Werte anpassen (z. b. Helligkeit oder Sättigung), verwenden Pixel-Shader.

In Windows 10 kann Direct2D nun vermeiden, dass in solchen Fällen zwischen Texturen verwendet werden. Dies geschieht, indem angrenzende Pixel-Shader intern verknüpft werden. Beispiel:

![Windows 10-Effekt Diagramm mit mehreren Pixel-Shadern und ohne zwischen Strukturen](images/precision-and-clipping-3.png)

Beachten Sie, dass nicht alle angrenzenden Pixel-Shader in einem Diagramm miteinander verknüpft werden können. aus diesem Grund ergeben nur bestimmte Diagramme unter Windows 10 eine andere Ausgabe. Ausführliche Informationen finden Sie unter [Effect Shader Linking](effect-shader-linking.md). Die wichtigsten Einschränkungen sind:

-   Ein Effekt wird nicht mit Effekten verknüpft, die seine Ausgabe verbrauchen, wenn der erste Effekt als Eingabe mit mehreren Effekten verbunden ist.
-   Ein Effekt wird nicht mit einem Effekt als Eingabe verknüpft, wenn der erste Effekt seine Eingabe an einer anderen logischen Position als der Ausgabe ablegt. Beispielsweise kann ein Farb Matrix Effekt mit der Eingabe verknüpft werden, aber ein Vergleich ist nicht.

## <a name="built-in-effect-behavior"></a>Verhalten integrierter Effekte

Viele integrierte Effekte können Farben außerhalb von \[ 0, 1 \] Bereich im nicht multiplizierten Farbraum erzeugen, auch wenn sich Ihre Eingabe Farben in diesem Bereich befinden. Wenn dies geschieht, unterliegen diese Farben möglicherweise dem numerischen Clipping. Beachten Sie, dass es wichtig ist, den Farbbereich in einem nicht multiplizierten Bereich zu berücksichtigen, auch wenn integrierte Effekte in der Regel Farben in einem voraus multiplizierten Bereich erzeugen. Dadurch wird sichergestellt, dass die Farben innerhalb des Bereichs liegen, auch wenn Sie von anderen Effekten später nicht multipliziert werden.

Einige der Effekte, die diese out-of-Range-Farben ausgeben können, bieten eine Eigenschaft "klamdungstyp". Dazu gehören:

-   [Farb Matrix](color-matrix.md)
-   [Arithmetischer zusammengesetzter](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Übertragungseffekte](built-in-effects.md)

Wenn die Eigenschaft "SetOutput" für diese Effekte auf true festgelegt wird, wird sichergestellt, dass unabhängig von Faktoren wie shaderverknüpfung ein konsistentes Ergebnis erzielt wird. Beachten Sie, dass im nicht multiplizierten Bereich eine Klammer auftritt.

Andere integrierte Effekte können auch Ausgabe Farben erzeugen, die über den \[ Bereich von 0 bis 1 \] liegen, auch wenn sich die Farben Pixel (und ggf. "Color"-Eigenschaften) in diesem Bereich befinden. Dazu gehören:

-   [Transformieren und Skalieren von Effekten](built-in-effects.md) (wenn es sich bei der Interpolations Modus-Eigenschaft um eine kubische oder eine hochwertige
-   [Beleuchtungseffekte](built-in-effects.md)
-   [Edge-Erkennung](edge-detection-effect.md) (wenn die Eigenschaft der Überlagerungs Ränder true ist)
-   [Offenlegung](exposure-effect.md)
-   [Composite](composite.md) (wenn die Mode-Eigenschaft Plus ist)
-   [Temperatur und tint](temperature-and-tint-effect.md)
-   [Sepia](sepia-effect.md)
-   [Sättigung](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Erzwingen des numerischen Clipping innerhalb eines Effekt Diagramms

Wenn Sie die oben aufgeführten Effekte verwenden, die nicht über eine Eigenschaft für die Eigenschaft "Eigenschaft" verfügen, sollten Anwendungen eine numerische Klammer erzwingen. Dies kann durch Einfügen eines zusätzlichen Effekts in das Diagramm erreicht werden, das seine Pixel bindet. Ein Farb Matrix Effekt kann verwendet werden, wenn die Eigenschaft "SetOutput" auf "true" festgelegt ist und die Eigenschaft "ColorMatrix" als Standardwert (Pass-Through) belassen wird.

Eine zweite Möglichkeit, konsistente Ergebnisse zu erzielen, besteht darin, dass Direct2D zwischen Texturen verwenden, die eine höhere Genauigkeit aufweisen. Dies wird nachfolgend beschrieben.

## <a name="controlling-precision-of-intermediate-textures"></a>Steuern der Genauigkeit von zwischen Texturen

Direct2D bietet einige Möglichkeiten, um die Genauigkeit eines Diagramms zu steuern. Vor der Verwendung von Formaten mit hoher Genauigkeit in Direct2D müssen Anwendungen sicherstellen, dass Sie von der GPU ausreichend unterstützt werden. Um dies zu überprüfen, verwenden Sie [**ID2D1DeviceContext:: isbufferprecisionsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Anwendungen können mithilfe von Warp (Software Emulation) ein Direct3D-Gerät erstellen, um sicherzustellen, dass alle Puffer präzigmachen unabhängig von der eigentlichen GPU-Hardware auf dem Gerät unterstützt werden. Dies wird in Szenarien wie dem Anwenden von Effekten auf ein Foto beim Speichern auf einem Datenträger empfohlen. Selbst wenn Direct2D Puffer Formate mit hoher Genauigkeit auf der GPU unterstützt, wird die Verwendung von Warp in diesem Szenario auf Featureebene 9. X-GPUs empfohlen, aufgrund der begrenzten Genauigkeit der shaderarithmetik und der Stichprobenentnahme für einige Low-Power-Mobil-GPUs.

In jedem Fall unten ist die angeforderte Genauigkeit tatsächlich die minimale Genauigkeit, die Direct2D verwenden wird. Wenn keine Vermittler erforderlich sind, kann eine höhere Genauigkeit verwendet werden. Direct2D kann auch zwischen Texturen für verschiedene Teile desselben Diagramms oder für verschiedene Diagramme freigeben. In diesem Fall verwendet Direct2D die für alle Beteiligten Vorgänge angeforderte maximale Genauigkeit.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Genauigkeits Auswahl aus ID2D1DeviceContext:: "".

Die einfachste Methode, um die Genauigkeit von renderingkonventionen-zwischen Texturen zu steuern, ist die Verwendung von [**ID2D1DeviceContext:: abtrenderingcontrols**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Dadurch wird die Genauigkeit aller zwischen Texturen gesteuert, solange eine Genauigkeit nicht auch manuell bei Effekten oder Transformationen festgelegt wird.


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



### <a name="precision-selection-from-inputs-and-render-targets"></a>Genauigkeits Auswahl aus Eingaben und renderzielen

Anwendungen können auch auf die Genauigkeit der Eingaben in einem Effekt Diagramm zurückgreifen, um die Genauigkeit von zwischen Texturen zu steuern. Dies ist der Fall, wenn eine Puffer Genauigkeit nicht mithilfe von [**ID2D1DeviceContext:: setrenderingcontrols**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))angegeben wird und nicht manuell bei Effekten und transformieren festgelegt wird.

Die Genauigkeit der Eingaben in Effekte werden durch das Diagramm weitergegeben, um die Genauigkeit von downstreamzwischengängen auszuwählen. Wenn verschiedene Verzweigungen im Effekt Diagramm übereinstimmen, wird die höchste Genauigkeit der Eingaben verwendet.

Die Genauigkeit, die basierend auf einer Direct2D Bitmap ausgewählt wird, wird aus dem Pixel Format bestimmt. Die für eine [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) ausgewählte Genauigkeit wird anhand des WIC-Pixel Formats der zugrunde liegenden IWICBitmapSource bestimmt, die zum Erstellen des **ID2D1ImageSource** verwendet wird. Beachten Sie, dass Direct2D nicht zulässt, dass Bildquellen mit WIC-Quellen erstellt werden, die nicht von Direct2D und der GPU unterstützt werden.

Es ist möglich, dass Direct2D auf der Grundlage der Eingaben keinen Effekt auf eine Genauigkeit zuweist. Dies geschieht, wenn ein Effekt keine Eingaben aufweist oder wenn eine [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) verwendet wird, die keine bestimmte Genauigkeit aufweist. In diesem Fall wird die Genauigkeit von zwischen Texturen von der Bitmap bestimmt, die als Aktuelles Renderziel des Kontexts festgelegt ist.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Genauigkeits Auswahl direkt in den Effekten und Transformationen

Die minimale Genauigkeit für zwischen Texturen kann auch an expliziten Positionen innerhalb eines Effekt Diagramms festgelegt werden. Dies wird nur für erweiterte Szenarien empfohlen.

Die minimale Genauigkeit kann mit einer Eigenschaft eines Effekts wie folgt festgelegt werden:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Innerhalb einer Effekt Implementierung kann die minimale Genauigkeit mit ID2D1RenderInfo:: setoutputprecision wie folgt festgelegt werden:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Beachten Sie, dass die Genauigkeit, die für einen Effekt festgelegt wird, im gleichen Effekt Diagramm an DOWNSTREAMEFFEKTE weitergegeben wird, sofern für diese DOWNSTREAMEFFEKTE keine andere Genauigkeit festgelegt ist. Die Genauigkeit, die für eine Transformation innerhalb eines Effekts festgelegt wird, hat keine Auswirkung auf die Genauigkeit von downstreamtransformierknoten.

Im folgenden finden Sie die vollständige rekursive Logik, die verwendet wird, um die minimale Genauigkeit eines zwischen Puffers zu bestimmen, der die Ausgabe eines bestimmten Transformations Knotens

![Logik für Zwischenpuffer-minimal Genauigkeit](images/precision-and-clipping-4.png)

 

 