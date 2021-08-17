---
description: In diesem Abschnitt erfahren Sie, wie Sie primitive Typen höherer Ordnung in Ihrer Anwendung verwenden.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Verwenden von Higher-Order Primitiven (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7d7a7b7f619c033665f8cb9894db5d60d5d6ecf9116de4ada230accc476c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797293"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Verwenden von Higher-Order Primitiven (Direct3D 9)

In diesem Abschnitt erfahren Sie, wie Sie primitive Typen höherer Ordnung in Ihrer Anwendung verwenden.

-   [Bestimmen Higher-Order primitiven Supports](#determining-higher-order-primitive-support)
-   [Zeichnen von Patches](#drawing-patches)
-   [Generieren von Normal- und Texturkoordinaten](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Bestimmen Higher-Order primitiven Supports

Der DevCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) kann abgefragt werden, um den Grad der Unterstützung für Vorgänge mit primitiven Typen höherer Ordnung zu bestimmen. In der folgenden Tabelle sind die Gerätefunktionen im Zusammenhang mit primitiven Typen höherer Ordnung in Direct3D 9 aufgeführt.



| Gerätefunktion             | BESCHREIBUNG                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | Das Gerät unterstützt N-Patches und basiert auf [gekrümmten PN-Dreiecken](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (einer besonderen Art kubischer Bézierdreiecke). |
| D3DDEVCAPS- \_ UND -KAPSELUNGSPATCHES  | Das Gerät unterstützt bezierende Bézierkurven und B-Splines.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | Das Gerät unterstützt rechteckige und dreieckige Patches (RT-Patches).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDERO | RT-Patches können effizient mit handle 0 (null) gezeichnet werden.                                                                                                     |



 

Beachten Sie, dass D3DDEVCAPS \_ RTPATCHHANDERO nicht bedeutet, dass ein Patch mit Handle 0 (null) gezeichnet werden kann. Ein Handle ohne Patch kann immer gezeichnet werden, unabhängig davon, ob diese Gerätefunktion festgelegt ist oder nicht. Wenn diese Funktion festgelegt ist, erfordert die Hardwarearchitektur keine Zwischenspeicherung von Informationen, und nicht zwischengespeicherte Patches (Handle null) werden so effizient wie zwischengespeicherte Patches gezeichnet.

## <a name="drawing-patches"></a>Zeichnen von Patches

Direct3D 9 unterstützt zwei Typen von Primitiven höherer Ordnung oder Patches. Diese werden als N-Patches und Rect/Tri-Patches bezeichnet. N-Patches können mit einem beliebigen Dreiecksrenderingaufruf gerendert werden, indem N-Patches durch den Aufruf von [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)( nSegments ) mit einem nSegments-Wert größer als 1.0 aktiviert werden. Rekt/Tri-Patches müssen mit den folgenden expliziten Einstiegspunkten gerendert werden.

Sie können die folgenden Methoden verwenden, um Patches zu zeichnen.

-   [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Weitere Informationen dazu, wie im Scheitelpunktpuffer auf die Patchdaten verwiesen wird, finden Sie unter [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api). Um besser zu verstehen, wie im Scheitelpunktpuffer auf die Patchdaten verwiesen wird, lesen Sie [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) zeichnet einen rechteckigen Patch in hoher Reihenfolge, der durch den pRectPatchInfo-Parameter angegeben wird, und verwendet dabei die aktuell festgelegten Datenströme. Der Handle-Parameter wird verwendet, um den Patch einem Handle zuzuordnen, sodass es beim nächsten Zeichnen des Patches nicht erforderlich ist, pRectPatchInfo neu zu angeben. Dadurch können Differenzkoeffizienten oder andere Informationen vorab berechnet und zwischengespeichert werden, was wiederum nachfolgende Aufrufe von **IDirect3DDevice9::D rawRectPatch** mit dem gleichen Handle ermöglicht, um effizient ausgeführt zu werden.

Für statische Patches soll eine Anwendung den Vertex-Shader und die entsprechenden Streams festlegen, Patchinformationen im pRectPatchInfo-Parameter bereitstellen und ein Handle angeben, damit Direct3D Informationen erfassen und zwischenspeichern kann. Die Anwendung kann anschließend [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) aufrufen, wobei pRectPatchInfo auf **NULL** festgelegt ist, um den Patch effizient zu zeichnen. Beim Zeichnen eines zwischengespeicherten Patches werden die derzeit festgelegten Streams ignoriert. Es ist jedoch möglich, die zwischengespeicherten pNumSegs zu überschreiben, indem Sie neue Werte für pNumSegs angeben. Außerdem muss beim Rendern eines zwischengespeicherten Patches der gleiche Vertex-Shader festgelegt werden wie beim Erfassen.

Bei dynamischen Patches ändern sich die Patchdaten für jedes Rendering des Patches, sodass es nicht effizient ist, Informationen zwischenzuspeichern. Die Anwendung kann dies direct3D vermitteln, indem Handle auf 0 festgelegt wird. In diesem Fall zeichnet Direct3D den Patch mithilfe der derzeit festgelegten Datenströme und der pNumSegs-Werte und speichert keine Informationen zwischen. Es ist nicht gültig, handle gleichzeitig auf 0 und pPatch auf **NULL** festzulegen.

Indem pRectPatchInfo für dasselbe Handle neu angegeben wird, kann die Anwendung die zuvor zwischengespeicherten Informationen überschreiben.

[**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) ähnelt [**IDirect3DDevice9::D rawRectPatch,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) zeichnet jedoch einen dreieckigen Patch in hoher Reihenfolge.

## <a name="generating-normals-and-texture-coordinates"></a>Generieren von Normal- und Texturkoordinaten

Wenn Sie einen FVF-Shader (Flexible Vertex Format) verwenden, ist die automatische Generierung von Normal- und Texturkoordinaten nicht möglich.

Für Normalitäten können Sie sie entweder direkt bereitstellen oder Direct3D für Sie berechnen lassen.

Die für rechteckige Patches generierten Koordinaten sind splinebasierte Koordinaten, wie in den folgenden Abbildungen dargestellt.

![Abbildung einer ursprünglichen Textur und der Textur mit splinebasierten Koordinaten](images/texturespline.png)

Die für dreieckige Patches generierten Koordinaten sind baryzentrische Spline-basierte Koordinaten, wie in den folgenden Abbildungen dargestellt.

![Abbildung einer ursprünglichen Textur und der Textur mit balyzentrischen Spline-basierten Koordinaten](images/texturebarycentricspline.png)

Wenn eine Anwendung den Bereich der generierten Texturkoordinaten ändern muss, kann dies mithilfe von Texturtransformationen erfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive höherer Ordnung](higher-order-primitives.md)
</dt> </dl>

 

 
