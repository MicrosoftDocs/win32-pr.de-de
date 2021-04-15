---
description: Die Unterstützung für Punkt Sprites in Direct3D 9 ermöglicht das Hochleistungs Rendering von Punkten (Partikelsysteme). Punkt Sprite sind verallgemeinungen von generischen Punkten, die es ermöglichen, dass beliebige Formen wie von Texturen definiert gerendert werden.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Punkt Sprites (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521707"
---
# <a name="point-sprites-direct3d-9"></a>Punkt Sprites (Direct3D 9)

Die Unterstützung für Punkt Sprites in Direct3D 9 ermöglicht das Hochleistungs Rendering von Punkten (Partikelsysteme). Punkt Sprite sind verallgemeinungen von generischen Punkten, die es ermöglichen, dass beliebige Formen wie von Texturen definiert gerendert werden.

-   [Primitive renderingsteuerelemente](#point-primitive-rendering-controls)
-   [Punktgrößen Berechnungen](#point-size-computations)
-   [Punkt Rendering](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Primitive renderingsteuerelemente

Direct3D 9 unterstützt zusätzliche Parameter, um das Rendering von Punkt Sprites (Punkt primitiven) zu steuern. Mit diesen Parametern können Punkte variabler Größe aufweisen und eine vollständige Textur Zuordnung angewendet werden. Die Größe jedes Punkts wird durch eine von der Anwendung angegebene Größe in Kombination mit einer von Direct3D berechneten Entfernungs basierten Funktion bestimmt. Die Anwendung kann die Punktgröße entweder als pro-Scheitelpunkt oder durch Festlegen von D3DRS \_ pointsize angeben, die für Punkte ohne pro-Vertex-Größe gilt. Die Punktgröße wird in Kamera Raumeinheiten ausgedrückt, mit der Ausnahme, dass die Anwendung nach dem transformierten FVF (Flexible Vertex Format)-Vertices übergibt. In diesem Fall wird die Entfernungs basierte Funktion nicht angewendet, und die Punktgröße wird in Pixel Einheiten für das Renderziel ausgedrückt.

Welche Texturkoordinaten berechnet und verwendet werden, wenn renderingpunkte verwendet werden, hängt von der Einstellung von D3DRS \_ pointspriteenable ab. Wenn dieser Wert auf **true** festgelegt ist, werden die Texturkoordinaten so festgelegt, dass jeder Punkt die vollständige Textur anzeigt. Im Allgemeinen ist dies nur nützlich, wenn Punkte erheblich größer als ein Pixel sind. Wenn D3DRS \_ pointspriteenable auf **false** festgelegt ist, wird die Vertex-Textur Koordinate jedes Punkts für den gesamten Punkt verwendet.

## <a name="point-size-computations"></a>Punktgrößen Berechnungen

Die Punktgröße wird durch D3DRS \_ pointscaleenable bestimmt. Wenn dieser Wert auf **false** festgelegt ist, wird die von der Anwendung angegebene Punktgröße als Bildschirmraum (posttransformiert) verwendet. Für Scheitel Punkte, die im Bildschirmbereich an Direct3D übermittelt werden, sind keine Punktgrößen berechnet. die angegebene Punktgröße wird als Größe des Bildschirm Raums interpretiert.

Wenn D3DRS \_ pointscaleenable den Wert **true** hat, berechnet Direct3D die Größe des Bildschirm Leerraums gemäß der folgenden Formel. Die von der Anwendung angegebene Punktgröße wird in Kamera Raumeinheiten ausgedrückt.

S = VH \* s <sub>i</sub> \* sqrt (1/(A + B \* D ₑ + C \* (D ₑ ²)))

In dieser Formel ist die Eingabe Punktgröße, S <sub>i</sub>, entweder pro Scheitelpunkt oder der Wert des D3DRS \_ pointsize-Rendering-Zustands. Die Punkt Skalierungsfaktoren D3DRS \_ pointscale \_ a, D3DRS \_ pointscale \_ B und D3DRS \_ pointscale \_ C werden durch die Punkte A, B und c dargestellt. Die Höhe des Viewports, V h, ist der Height-Member der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, der den Viewport darstellt. D ₑ die Entfernung von der Perspektive bis zur Position (das Auge am Ursprung) wird berechnet, indem die Augen Raum Position des Punkts (x ₑ, y ₑ, z ₑ) übernommen und der folgende Vorgang durchgeführt wird.

D ₑ = sqrt (x ₑ ² + Y ₑ ² + Z ₑ ²)

Die maximale Punktgröße, pm ₐ ₓ, wird bestimmt, indem der kleinere des maxpointsize-Members der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur oder der D3DRS \_ pointsize-maximale Rendering-Zustand verwendet wird \_ . Die minimale Punktgröße (P<sub>Min</sub>) wird durch Abfragen des Werts von D3DRS \_ pointsize min bestimmt \_ . Daher wird die endgültige Größe des Bildschirmraum Punkts wie folgt bestimmt.

-   Wenn SS > pm ₐ ₓ, dann S = P m ₐ ₓ
-   Wenn s < P<sub>Min</sub>, dann s = p <sub>Min</sub> .
-   Andernfalls s = s

## <a name="point-rendering"></a>Punkt Rendering

Ein Bildschirmraum Punkt (P = (X, Y, Z, W) der Bildschirmgröße S wird als viereckig der folgenden vier Vertices gerengt.

((X + s/2, y + s/2, z, w), (x + s/2, y-s/2, z, w), (x-s/2, y-s/2, z, w), (x-s/2, y + S/2, z, w))

Die Vertex-Farb Attribute werden bei jedem Scheitelpunkt dupliziert. Daher wird jeder Punkt immer mit Konstanten Farben gerendert.

Die Zuweisung von Textur Indizes wird von der D3DRS \_ pointspriteenable-Rendering-Statuseinstellung gesteuert. Wenn D3DRS \_ pointspriteenable auf **false** festgelegt ist, werden die Scheitelpunkt Texturkoordinaten bei jedem Scheitelpunkt dupliziert. Wenn D3DRS \_ pointspriteenable auf **true** festgelegt ist, werden die Texturkoordinaten an den vier Vertices auf die folgenden Werte festgelegt.

(0. f, 0. f), (0. f, 1. f), (1. f, 0. f), (1. f, 1. f)

Dies wird im folgenden Diagramm veranschaulicht:

![Diagramm eines Quadrats mit beschrifteten Vertices für (u, v) und (x, y)-Koordinaten Werte](images/spritepoint.png)

Wenn Clipping aktiviert ist, werden Punkte wie folgt abgeschnitten. Wenn der Scheitelpunkt den Bereich von tiefen Werten (Minz und MaxZ) der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur überschreitet, in die eine Szene gerendert werden soll, ist der Punkt außerhalb der Ansicht Frustum vorhanden und wird nicht gerendert. Wenn der Punkt, der die Punktgröße berücksichtigt, vollständig außerhalb des Viewports in X und Y liegt, wird der Punkt nicht gerendert. die verbleibenden Punkte werden gerendert. Es ist möglich, dass die Punktposition außerhalb des Viewports in X oder Y liegt und noch teilweise sichtbar ist.

Punkte werden möglicherweise nicht ordnungsgemäß auf benutzerdefinierte Clip-Flächen zugeschnitten. Wenn D3DPMISCCAPS \_ clipplanescaledpoints nicht im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur festgelegt ist, werden die Punkte nur auf der Scheitelpunkt Position auf benutzerdefinierte Clip Flächen zugeschnitten, wobei die Punktgröße ignoriert wird. In diesem Fall werden skalierte Punkte vollständig gerendert, wenn sich die Scheitelpunkt Position innerhalb der Clip Flächen befindet, und verworfen, wenn die Scheitelpunkt Position außerhalb der Ausschneide Ebene liegt. Anwendungen können potenzielle Artefakte vermeiden, indem Sie eine Rahmengeometrie zu Clip-Flächen hinzufügen, die so groß wie die maximale Punktgröße ist.

Wenn das D3DPMISCCAPS \_ clipplanescaledpoints-Bit festgelegt ist, werden die skalierten Punkte korrekt auf benutzerdefinierte Clip Flächen zugeschnitten.

Die Verarbeitung von Hardware Scheitel Punkten kann die Punktgröße unterstützen. Wenn z. b. ein Gerät mit D3DCREATE \_ Hardware \_ vertexprocessing auf einem Hardware Abstraktionsschicht (HAL)-Gerät (D3DDEVTYPE \_ HAL) erstellt wird, das den maxpointsize-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur auf 1,0 oder 0,0 festgelegt hat, sind alle Punkte ein einzelnes Pixel. Zum Rendern von Pixeln, die kleiner als 1,0 sind, müssen Sie entweder FVF TL-Vertices (transformiert und lit) oder die Verarbeitung von Software Scheitel Punkten (D3DCREATE \_ Software \_ vertexprocessing) verwenden. in diesem Fall emuliert die Direct3D-Laufzeit das Punkt Sprite-Rendering.

Ein Hardware Gerät, das die Scheitelpunkt Verarbeitung verarbeitet und Punkt Sprite unterstützt. maxpointsize ist auf einen Wert größer als 1,0 f festgelegt. ist erforderlich, um die Größen Berechnung für nicht transformierte Sprites auszuführen, und muss die pro-Vertex-oder D3DRS \_ POINTSIZED3DRS pointsize für TL-Scheitel Punkte ordnungsgemäß festgelegt werden \_ .

Informationen zu Renderingerweiterungen für Punkte, Linien und Dreiecke finden Sie unter [rasterization Rules (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 



