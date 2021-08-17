---
title: Bitmapobjekte
description: In diesem Thema werden die Typen von Bitmapinhalten beschrieben, die DirectComposition unterstützt.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc36253511c060b264039f27975c694272c1c916ad0067c1955fd02f00553d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089050"
---
# <a name="bitmap-objects"></a>Bitmapobjekte

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition ist eine Bitmap-Compositing-Engine. Es ermöglicht Anwendungsentwicklern, mehrere Bitmaps zu kombinieren und auf verschiedene Weise zu bearbeiten, um interessante visuelle Effekte und Animationen in einer Anwendungsoberfläche zu erzielen. In diesem Thema werden die Typen von Bitmapinhalten beschrieben, die DirectComposition unterstützt.

-   [Bitmapinhalt](#bitmap-content)
    -   [Videospeicherbitmaps](#video-memory-bitmaps)
    -   [Fensterbitmaps](#window-bitmaps)
    -   [Zuordnen von Bitmapinhalten zu einem Visual](#associating-bitmap-content-with-a-visual)
    -   [Alphakanal](#alpha-channel)
-   [Zugehörige Themen](#related-topics)

## <a name="bitmap-content"></a>Bitmapinhalt

Anwendungen stellen DirectComposition mit dem Bitmapinhalt bereit, der erstellt und animiert werden soll, indem visuelle Objekte erstellt und dann die [Content-Eigenschaft](basic-concepts.md) dieser Objekte festgelegt wird. DirectComposition bietet keine Rasterungsdienste. Eine Anwendung muss eine andere softwarebasierte oder hardwarebeschleunigte Rasterungsbibliothek wie [Direct2D](../direct2d/direct2d-portal.md) oder [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) verwenden, um die zu erstellenden Bitmaps aufzufüllen. Nach dem Verfassen übergibt DirectComposition zusammengesetzte Bitmapinhalte zum Rendern auf dem Bildschirm an [Desktopfenster-Manager (DWM).](/windows/desktop/dwm/dwm-overview)

**Unterstützte Typen von Bitmapinhalten** Microsoft DirectComposition unterstützt die folgenden Arten von Bitmaps:

-   [Videospeicherbitmaps](#video-memory-bitmaps)
-   [Fensterbitmaps](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Videospeicherbitmaps

Eine Videospeicherbitmap wird mithilfe von Microsoft DirectX-Methoden (einschließlich des DX-to-GDI-Interopmodells) in Hardware gerastert. Sie wird durch prozessübergreifende freigegebene Oberflächen unterstützt, die für die aufrufende Anwendung und DirectComposition sichtbar sind. Eine Videospeicherbitmap wird nicht entfernt, da die Anwendung nur von den Oberflächen lesen kann, von denen DirectComposition-Texturen stammen.

### <a name="video-content"></a>Videoinhalte

Anwendungen können DirectComposition verwenden, um Videoframes zu erstellen, die fensterlose DirectX-Swapketten verwenden, die an eine DirectComposition-Oberfläche gebunden sind. Konzeptionell behandelt DirectComposition Videoinhalte als Folge von Bitmaps. DirectComposition bietet keine Möglichkeit, Videoframes darzustellen.

DirectComposition unterstützt DirectX-Austauschketten ohne Fenster, d. h. Austauschketten, die nicht an ein bestimmtes Fenster gebunden sind, und ermöglicht es zwei verschiedenen Anwendungen, fensterlose Swapketten über Prozessgrenzen hinweg freizugeben. Die Freigabe von fensterlosen Swapketten ermöglicht Videoszenarien, in denen die Swapkette in einem Prozess erstellt und mit DirectComposition in einem zweiten Prozess verwendet wird. Fensterlose Swapketten werden mit der [**IDXGIFactory2::CreateSwapChainForCompositionSurface-Methode**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) erstellt.

Weitere Informationen zu DirectX-Swapketten finden Sie unter [DXGI Overview](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Stereo-Inhalt

Konzeptionell besteht eine Stereo-Swapkette aus Dxgi-Oberflächen (Microsoft DirectX Graphic Infrastructure), die die linken und rechten Kanäle für Stereo-3D-Inhalte darstellen. Wenn eine Stereo-Swapkette als Bitmapressource für ein Visual verwendet wird, wird DirectComposition in Stereo erstellt. Alle Nicht-Stereoinhalte (Mono-Inhalt) gelten als identischer linker und rechter Kanalinhalt. Das heißt, der gleiche Bitmapinhalt wird für beide Kanäle verwendet. DirectComposition erstellt alle linken inhalte und alle richtigen Inhalte separat. Wenn das Anzeigegerät nicht stereofähig ist, behandelt DirectComposition den linken oder rechten Stereokanal (je nach Anwendung) als Mono-Inhalt und erstellt nur diese Daten für die Bitmapressource.

DirectComposition unterstützt weder das Erstellen oder Bearbeiten von Stereoinhalten noch das Heraufstufen einer Mono-Swapkette zu einem Stereopaar. Eine Anwendung muss diese Aufgaben ausführen, bevor DirectX-Stereoinhalte in DirectComposition präsentiert werden. Außerdem muss eine Anwendung die Offsets des linken und rechten Kanals für die Tiefenerkennung bereitstellen. DirectComposition kann die Offsets des linken und rechten Kanals nicht anpassen, um die wahrgenommene Tiefe des DirectX-Stereoinhalts zu ändern.

DirectX-Stereoinhalte werden zusammengesetzt und in DWM beibehalten, wenn stereofähige Hardware verfügbar ist.

### <a name="window-bitmaps"></a>Fensterbitmaps

Eine "Fensterbitmap" ist keine echte Bitmap, sondern ein Platzhalter, den DirectComposition in Echtzeit durch Rasterungen von mehrstufigen oder untergeordneten Fenstern ersetzt. Eine Fensterbitmap ähnelt einer DWM-Miniaturansicht, mit der Ausnahme, dass eine Miniaturansicht Beiträge aus vielen Fenstern enthalten kann, z. B. nicht untergeordnete Fenster, während eine DirectComposition-Fensterbitmap immer eine Darstellung von nur einem Fenster und dessen untergeordneten Fenstern ist.

Da DirectComposition Zugriff auf die Umleitungsoberflächen aller Fenster und aller visuellen Strukturen hat, kann der Inhalt aus einem Fenster in mehreren visuellen Strukturen wiederverwendet werden. Das Fenster muss mehrschichtig sein, da ein nicht überschichtetes Fenster keine dedizierte Umleitungsoberfläche aufweist und daher die Rasterung nicht immer für DirectComposition verfügbar ist.

Um eine Fensterbitmap zu verwenden, ordnet eine Anwendung ein Visual einem Fensterhandle (HWND) zu. Anschließend erstellt DirectComposition das Visual neu, wenn sich der Inhalt des Fensters ändert, einschließlich wenn sich der Inhalt aufgrund von Änderungen an den visuellen Strukturen ändert, die dem Fenster zugeordnet sind. Anders ausgedrückt: DirectComposition-Fensterbitmaps sind wie DWM-Miniaturansichten "live".

### <a name="associating-bitmap-content-with-a-visual"></a>Zuordnen von Bitmapinhalten zu einem Visual

Für alle drei Arten von Bitmaps kann eine Anwendung dieselbe Bitmap mehreren Visuals zuordnen. Dies bedeutet, dass eine einzelne Speicherbelegung verwendet werden kann, um denselben Inhalt mehrmals anzuzeigen.

### <a name="alpha-channel"></a>Alphakanal

Alle Bitmaps weisen ein BPP-Format (32 Bits pro Pixel) auf, das acht Bits für die Transparenz pro Pixel enthält. Eine Anwendung kann jedoch angeben, wie DirectComposition den Alphakanal nutzen soll. Insbesondere kann DirectComposition den Alphakanal berücksichtigen oder Alpha vollständig ignorieren. In diesem Fall wird die Bitmap als vollständig deckend betrachtet.

Ein zusätzlicher Alphamodus ignoriert den Alphakanal, behandelt jedoch die roten, grünen und blauen Werte als Pro-Kanal-Alphawerte anstelle der normalen Interpretation dieser Kanäle als Farbtensitäten. Dieser Modus ist nützlich für das ClearType-Rendering, das Subpixelabdeckungsinformationen erfordert. Um den Kanal-Alphamodus zu verwenden, muss eine Anwendung zuerst [Direct2D](../direct2d/direct2d-portal.md) verwenden und [DirectWrite,](/windows/desktop/DirectWrite/direct-write-portal) um Subpixelabdeckungsdaten in eine Bitmap zu schreiben. Als Nächstes muss die Anwendung den richtigen Alphamodus festlegen und eine Textfarbe angeben, wenn die Bitmap einem Visual zugeordnet wird. DirectComposition kombiniert die Textfarbe mit den Abdeckungsdaten, wodurch ClearType-Mischungen im Hintergrund erzeugt werden.

In Situationen, in denen der ClearType-Algorithmus nicht anwendbar ist, z. B. wenn die Bitmap nicht pixel- und achsenbündig ausgerichtet ist oder auf eine Zwischenoberfläche gezeichnet werden muss, kann DirectComposition die Subpixelabdeckungsdaten in der Bitmap verwenden, um stattdessen automatisch und ohne zusätzliche Kosten eine Graustufenrasterisierung zu erzeugen.

Weitere Informationen finden Sie in der Beschreibung des *alphaMode-Parameters* der [**IDCompositionDevice::CreateSurface-**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) oder [**IDCompositionDevice::CreateVirtualSurface-Funktion.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 