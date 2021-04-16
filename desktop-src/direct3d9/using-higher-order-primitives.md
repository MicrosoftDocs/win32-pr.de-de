---
description: In diesem Abschnitt wird gezeigt, wie Sie in Ihrer Anwendung höher geordnete primitive verwenden.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Verwenden von Higher-Order primitiven (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567916"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Verwenden von Higher-Order primitiven (Direct3D 9)

In diesem Abschnitt wird gezeigt, wie Sie in Ihrer Anwendung höher geordnete primitive verwenden.

-   [Bestimmen Higher-Order primitiver Unterstützung](#determining-higher-order-primitive-support)
-   [Zeichnen von Patches](#drawing-patches)
-   [Erstellen von normalen und Texturkoordinaten](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Bestimmen Higher-Order primitiver Unterstützung

Der devcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur kann abgefragt werden, um den Grad der Unterstützung für Vorgänge zu bestimmen, die in einer höheren Reihenfolge primitiv sind. In der folgenden Tabelle sind die Gerätefunktionen im Zusammenhang mit höherwertigen primitiven in Direct3D 9 aufgeführt.



| Gerätefunktion             | BESCHREIBUNG                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ npatches          | Das Gerät unterstützt N-Patches und basiert auf [gekrümmten PN-Dreiecken](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (eine besondere Art von kubischer-Dreiecke). |
| D3DDEVCAPS \_ quinticrtpatches  | Das Gerät unterstützt Quintic Bezier-Kurven und B-Splines.                                                                                                         |
| D3DDEVCAPS \_ rtpatches         | Das Gerät unterstützt rechteckige und dreieckige Patches (RT-Patches).                                                                                             |
| D3DDEVCAPS \_ rtpatchlenker NULL | RT-Patches können mithilfe von Handle 0 (null) effizient gezeichnet werden.                                                                                                     |



 

Beachten Sie, dass D3DDEVCAPS \_ rtpatchlenker NULL nicht bedeutet, dass ein Patch mit handle NULL gezeichnet werden kann. Ein Patch für Handle 0 (null) kann immer gezeichnet werden, unabhängig davon, ob diese Geräte Funktion festgelegt ist. Wenn diese Funktion festgelegt ist, muss für die Hardwarearchitektur keine Informationen zwischengespeichert werden, und nicht zwischengespeicherte Patches (handle null) müssen so effizient wie zwischengespeicherte Patches gezeichnet werden.

## <a name="drawing-patches"></a>Zeichnen von Patches

Direct3D 9 unterstützt zwei Typen von primitiven höherer Ordnung oder Patches. Diese werden als N-Patches und Rect/Tri-Patches bezeichnet. N-Patches können mithilfe eines beliebigen Dreiecks Rendering gerendert werden, indem n-Patches durch den Aufrufen von [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)(nsegments) mit dem nsegments-Wert größer als 1,0 aktiviert werden. Rect/Tri-Patches müssen mit den folgenden expliziten Einstiegspunkten gerendert werden.

Sie können die folgenden Methoden verwenden, um Patches zu zeichnen.

-   [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Informationen zum besseren Verständnis der Referenzierung der Patchdaten im Vertex-Puffer finden Sie unter [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D RAW-Patch**](/windows/desktop/api). Informationen zum besseren Verständnis der Referenzierung der Patchdaten im Vertex-Puffer finden Sie unter [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) zeichnet einen rechteckigen, hochwertigen Patch, der durch den prectpatchinfo-Parameter angegeben wird, mithilfe der zurzeit festgelegten Streams. Der handle-Parameter wird verwendet, um den Patch einem Handle zuzuordnen, sodass beim nächsten Zeichnen des Patches keine prectpatchinfo-Angabe mehr erforderlich ist. Dies ermöglicht das vorberechnen und Zwischenspeichern von Forward-Differenz Koeffizienten oder anderen Informationen, die wiederum nachfolgende Aufrufe von **IDirect3DDevice9::D rawrectpatch** mit dem gleichen Handle zur effizienten Ausführungszeit ermöglichen.

Dies ist beabsichtigt, wenn eine Anwendung für statische Patches den Vertex-Shader und entsprechende Streams festlegt, Patchinformationen im prectpatchinfo-Parameter bereitstellt und ein Handle angibt, damit Direct3D Informationen erfassen und Zwischenspeichern kann. Die Anwendung kann anschließend [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) aufrufen, wobei prectpatchinfo auf **null** festgelegt ist, um den Patch effizient zu zeichnen. Beim Zeichnen eines zwischengespeicherten Patches werden die derzeit festgelegten Streams ignoriert. Es ist jedoch möglich, die zwischengespeicherten pnumsekunden zu überschreiben, indem Sie neue Werte für pnumsekunden angeben. Außerdem muss beim Rendern eines zwischengespeicherten Patches, das bei der Erfassung festgelegt wurde, derselbe Vertex-Shader festgelegt werden.

Bei dynamischen Patches werden die Patchdaten für jedes Rendering des Patches geändert, sodass keine Informationen zwischengespeichert werden können. Die Anwendung kann diese an Direct3D übermitteln, indem Handle auf 0 festgelegt wird. In diesem Fall zeichnet Direct3D den Patch mithilfe der zurzeit festgelegten Streams und der pnumsegs-Werte und speichert keine Informationen zwischen. Es ist nicht zulässig, das Handle gleichzeitig auf 0 und ppatch auf **null** festzulegen.

Durch das erneute angeben von prectpatchinfo für das gleiche Handle kann die Anwendung die zuvor zwischengespeicherten Informationen überschreiben.

[**IDirect3DDevice9::D rawdreipatch**](/windows/desktop/api) ähnelt [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) , mit dem Unterschied, dass Sie einen dreieckigen Patch für eine hohe Reihenfolge zeichnet.

## <a name="generating-normals-and-texture-coordinates"></a>Erstellen von normalen und Texturkoordinaten

Wenn Sie einen FVF-Shader (Flexible Vertex-Format) verwenden, ist die automatische Generierung von normalen und Texturkoordinaten nicht möglich.

Bei normalen können Sie Sie entweder direkt bereitstellen oder von Direct3D für Sie berechnen.

Die für rechteckige Patches generierten Koordinaten sind Spline-basierte Koordinaten, wie in den folgenden Abbildungen dargestellt.

![Abbildung einer ursprünglichen Textur und der Textur mit Spline-basierten Koordinaten](images/texturespline.png)

Die für dreieckige Patches generierten Koordinaten sind auf den Seiten basierende Spline-basierte Koordinaten, wie in den folgenden Abbildungen dargestellt.

![Abbildung einer ursprünglichen Textur und der Textur mit nicht auf Spline basierenden Koordinaten](images/texturebarycentricspline.png)

Wenn eine Anwendung den Bereich der generierten Texturkoordinaten ändern muss, kann dies mithilfe von Textur Transformationen erfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitives höherer Ordnung](higher-order-primitives.md)
</dt> </dl>

 

 
