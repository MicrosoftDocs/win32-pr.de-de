---
title: Bitmap-Objekte
description: In diesem Thema werden die Typen von Bitmapinhalten beschrieben, die von directcomposition unterstützt werden.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c390778fef1ee7ad96c90a8b7706fa635f3615ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390946"
---
# <a name="bitmap-objects"></a>Bitmap-Objekte

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft directcomposition ist eine Bitmap-Zusammensetzung-Engine. Sie ermöglicht Anwendungsentwicklern das Kombinieren mehrerer Bitmaps und deren Bearbeitung auf verschiedene Weise, um interessante visuelle Effekte und Animationen in einer Anwendungs Benutzeroberfläche zu erzielen. In diesem Thema werden die Typen von Bitmapinhalten beschrieben, die von directcomposition unterstützt werden.

-   [Bitmapinhalt](#bitmap-content)
    -   [Video Speicher-Bitmaps](#video-memory-bitmaps)
    -   [Fenster Bitmaps](#window-bitmaps)
    -   [Zuordnen von Bitmapinhalten zu einem visuellen Element](#associating-bitmap-content-with-a-visual)
    -   [Alpha Kanal](#alpha-channel)
-   [Zugehörige Themen](#related-topics)

## <a name="bitmap-content"></a>Bitmapinhalt

Anwendungen stellen directcomposition den Bitmapinhalt bereit, um Sie zu verfassen und zu animieren, indem Sie visuelle Objekte erstellen und dann die [Content-Eigenschaft](basic-concepts.md) dieser Objekte festlegen. Directcomposition bietet keine rasterisierungsdienste. Eine Anwendung muss eine andere softwarebasierte oder hardwarebeschleunigte rasterisierungsbibliothek, wie z. b. [Direct2D](../direct2d/direct2d-portal.md) oder [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) , zum Auffüllen der Bitmaps verwenden, die zusammengesetzt werden sollen. Nach dem Verfassen übergibt directcomposition zusammengesetzten Bitmapinhalt an [Desktopfenster-Manager (DWM)](/windows/desktop/dwm/dwm-overview) zum Rendern auf dem Bildschirm.

**Unterstützte Typen von Bitmapinhalten**   Microsoft directcomposition unterstützt die folgenden Arten von Bitmaps:

-   [Video Speicher-Bitmaps](#video-memory-bitmaps)
-   [Fenster Bitmaps](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Video Speicher-Bitmaps

Eine Videospeicher-Bitmap wird in Hardware mithilfe von Microsoft DirectX-Methoden (einschließlich des DX-zu-GDI-Interop-Modells) gerengt. Sie wird durch prozessübergreifende freigegebene Oberflächen unterstützt, die für die aufrufenden Anwendung und directcomposition sichtbar sind. Eine Videospeicher-Bitmap unterliegt nicht dem zerreißen, da die Anwendung nur von den Oberflächen lesen kann, von denen directcomposition-Texturen verwendet werden.

### <a name="video-content"></a>Video Inhalt

Anwendungen können directcomposition verwenden, um Video Frames zu verfassen, die DirectX-fensterlose Austausch Ketten verwenden, die an eine directcomposition-Oberfläche gebunden sind. Konzeptionell behandelt directcomposition Videoinhalte als Sequenz von Bitmaps. Directcomposition bietet keine Möglichkeit zum Darstellen von Video Frames.

Directcomposition unterstützt DirectX fensterlose Austausch Ketten – d. h. Austausch Ketten, die nicht an ein bestimmtes Fenster gebunden sind – und ermöglicht zwei verschiedenen Anwendungen, fensterlose Austausch Ketten über Prozess Grenzen hinweg freizugeben. Die Freigabe von fensterlosen Austausch Ketten ermöglicht Video Szenarios, in denen die Austausch Kette in einem Prozess erstellt und in einem zweiten Prozess mit directcomposition verwendet wird. Fensterlose Austausch Ketten werden mithilfe der [**IDXGIFactory2:: foateswapchainforcompositionsurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) -Methode erstellt.

Weitere Informationen zu DirectX-Austausch Ketten finden Sie unter [Übersicht über DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Stereo Inhalt

Konzeptionell besteht eine Stereo Austausch Kette aus Microsoft DirectX Graphics Infrastructure (DXGI)-Oberflächen, die den linken und rechten Kanal für Stereo-3D-Inhalte darstellen. Wenn eine Stereo Austausch Kette als Bitmap-Ressource für ein visuelles Element verwendet wird, wird directcomposition in Stereo verfasst. Alle nicht Stereo Inhalte (Mono-Inhalt) werden als identischer Linker und rechter Kanal Inhalt betrachtet. Das heißt, der gleiche Bitmapinhalt wird für beide Kanäle verwendet. Directcomposition verfasst den gesamten linken Inhalt und den gesamten richtigen Inhalt separat. Wenn das Anzeigegerät nicht Stereo fähig ist, behandelt directcomposition den linken oder rechten Stereokanal (abhängig von der Anwendung) als Mono-Inhalt und stellt nur die Daten für die Bitmap-Ressource dar.

Directcomposition unterstützt das Erstellen oder Bearbeiten von Stereo Inhalten nicht und kann keine Mono-Swap-Kette zu einem Stereo-Paar herauf Stufen. Eine Anwendung muss diese Aufgaben ausführen, bevor Sie DirectX-Stereo Inhalt für directcomposition präsentieren können. Außerdem muss eine Anwendung die linken und rechten Kanal Offsets für die Tiefenwahrnehmung bereitstellen. Directcomposition kann die linken und rechten Kanal Offsets nicht anpassen, um die wahrgenommene Tiefe von DirectX-Stereo Inhalten zu ändern.

DirectX-Stereo Inhalte werden zusammengesetzt und in DWM persistent gespeichert, wenn eine Stereo fähige Hardware verfügbar ist.

### <a name="window-bitmaps"></a>Fenster Bitmaps

Eine "Fenster Bitmap" ist keine echte Bitmap, sondern ein Platzhalter, der von directcomposition in Echtzeit durch rasterien von Ebenen der obersten Ebene oder von untergeordneten Fenstern ersetzt wird. Eine Fenster Bitmap ähnelt einer DWM-Miniaturansicht, mit der Ausnahme, dass eine Miniaturansicht Beiträge von vielen Fenstern enthalten kann, z. b. eigene nicht untergeordnete Fenster, wohingegen eine directcomposition-Fenster Bitmap immer eine Darstellung nur eines Fensters und ihrer untergeordneten Elemente ist.

Da directcomposition Zugriff auf die Umleitungs Oberflächen von allen Fenstern und allen visuellen Strukturen hat, kann der Inhalt von einem Fenster in mehreren visuellen Strukturen wieder verwendet werden. Das Fenster muss geschichtet werden, da ein nicht geschichtetes Fenster nicht über eine dedizierte Umleitungs Oberfläche verfügt und daher die rasterisierung nicht immer für directcomposition verfügbar ist.

Um eine Fenster Bitmap zu verwenden, ordnet eine Anwendung einem Fenster Handle (HWND) ein visuelles Element zu. Danach führt directcomposition die Visualisierung erneut aus, wenn sich der Inhalt des Fensters ändert, auch wenn sich der Inhalt aufgrund von Änderungen an den visuellen Strukturen ändert, die dem Fenster zugeordnet sind. Anders ausgedrückt, wie bei DWM-Miniaturansichten, sind directcomposition-Fenster Bitmaps "Live".

### <a name="associating-bitmap-content-with-a-visual"></a>Zuordnen von Bitmapinhalten zu einem visuellen Element

Für alle drei Arten von Bitmaps kann eine Anwendung dieselbe Bitmap mehreren visuellen Elementen zuordnen. Dies bedeutet, dass eine einzelne Speicher Belegung verwendet werden kann, um denselben Inhalt mehrmals anzuzeigen.

### <a name="alpha-channel"></a>Alphakanal

Alle Bitmaps verfügen über ein bpp-Format (32 Bits pro Pixel), das acht Bits für die pro-Pixel-Transparenz umfasst. Eine Anwendung kann jedoch angeben, wie directcomposition den Alphakanal nutzen soll. Insbesondere kann directcomposition den Alphakanal berücksichtigen, oder es kann Alpha ganz ignoriert werden. in diesem Fall wird die Bitmap als vollständig deckend angesehen.

Bei einem zusätzlichen Alpha-Modus wird der Alphakanal ignoriert, die roten, grünen und blauen Werte werden jedoch als pro-Kanal-Alpha-Werte und nicht als normale Interpretation dieser Kanäle als Farb Intensitäten behandelt. Dieser Modus ist nützlich für das ClearType-Rendering, das Informationen zur unter-Pixel Abdeckung erfordert. Damit der Alpha Modus pro Kanal verwendet werden kann, muss eine Anwendung zunächst [Direct2D](../direct2d/direct2d-portal.md) und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) verwenden, um Subpixel-Abdeckungs Daten in eine Bitmap zu schreiben. Anschließend muss die Anwendung den korrekten Alpha Modus festlegen und eine Textfarbe angeben, wenn Sie die Bitmap einem visuellen Element zuordnet. Directcomposition kombiniert die Textfarbe mit den Coverage-Daten, die ClearType-blending mit dem Hintergrund erzeugen.

In Situationen, in denen der ClearType-Algorithmus nicht anwendbar ist, z. b. wenn die Bitmap nicht an Pixel ausgerichtet und Achsen ausgerichtet ist, oder wenn Sie auf eine zwischen Oberfläche gezeichnet werden muss, kann directcomposition die subpixelabdeckungs Daten in der Bitmap verwenden, um stattdessen eine Graustufen-rasterisierung zu erstellen, und zwar ohne zusätzliche Kosten.

Weitere Informationen finden Sie in der Beschreibung des *Alpha AMODE* -Parameters der [**idcompositiondevice:: anatesurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) -Funktion oder der [**idcompositiondevice:: deatevirtualsurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface) -Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 