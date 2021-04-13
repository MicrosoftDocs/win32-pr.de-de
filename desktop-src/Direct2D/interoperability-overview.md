---
title: Überblick über die Interoperabilität
description: Fasst die verschiedenen Technologien zusammen, die Sie mit Direct2D verwenden können.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, GDI-Interoperation
- Direct2D, GDI+-Interoperation
- Direct2D, Interoperabilität
- Direct2D, DirectWrite-Interoperation
- Interoperabilität, Direct2D
- Interoperabilität, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
- Interoperabilität, GDI+
- DirectWrite-Interoperabilität
- Interoperabilität, DirectWrite
- Windows Imaging-Komponente (WIC)
- WIC (Windows Imaging-Komponente)
- Interoperabilität, Windows Imaging Component (WIC)
- Direct2D, WIC-Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390490"
---
# <a name="interoperability-overview"></a>Überblick über die Interoperabilität

Eines der wichtigsten Features von renderingkonventionen ist die Aktivierung der Interoperabilität zwischen Direct2D und anderen renderingplattformen, damit Entwickler die spezifischen Stärken der einzelnen Plattformen nutzen können, ohne dass Sie zu Kompromittierungen gezwungen werden, indem Sie eine Plattform für alle Anforderungen auswählen. In diesem Thema werden die verschiedenen Plattformen zusammengefasst, mit denen Direct2D interoperabel ist. Der Abschnitt ist wie folgt gegliedert.

-   [GDI-Interoperabilität](#gdi-interoperability)
-   [GDI+-Interoperabilität](#gdi-interoperability)
-   [Direct3D-Interoperabilität](#direct3d-interoperability)
-   [DirectWrite-Interoperabilität](#directwrite-interoperability)
-   [Interoperabilität von Windows Imaging Component (WIC)](#windows-imaging-component-wic-interoperability)
-   [Zugehörige Themen](#related-topics)

Das folgende Diagramm fasst die verschiedenen Plattformen zusammen, mit denen Direct2D interoperabel ist, und listet einige Methoden und Schnittstellen auf, die Interoperabilität bereitstellen.

![Diagramm der Plattformen, mit denen Direct2D interagiert, einschließlich Direct3D 10,1, DirectWrite, WIC, GDI+ und GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>GDI-Interoperabilität

Direct2D ermöglicht die bidirektionale Interoperabilität mit GDI. Sie können ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekt verwenden, um Direct2D-Inhalte in einen GDI- [Gerätekontext](/windows/desktop/gdi/device-contexts) (DC) zu schreiben, oder Sie können [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um eine DC-Darstellung eines Renderziels zu erhalten.

Weitere Informationen und Beispiele finden Sie in der [Übersicht über die Interoperabilität zwischen Direct2D und GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>GDI+-Interoperabilität

Sie können GDI+ mit Direct2D auf die gleiche Weise wie GDI verwenden. Sie können ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekt verwenden, um Direct2D-Inhalte auf denselben Domänen Controller wie den GDI+-Inhalt zu schreiben. Mit diesem Ansatz können Sie Anwendungen hinzufügen, die in erster Linie mithilfe von GDI+ durch Rendering von Direct2D-Inhalten verwendet werden.

Sie können auch einen [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um Zugriff auf einen GDI-Domänen Controller bereitzustellen, der mithilfe von Direct2D schreibt, und dann die [**FromHdc**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) -Methode verwenden, um ein-Objekt zu erstellen. Diese Vorgehensweise ist nützlich für Anwendungen, die in erster Linie mit Direct2D Rendering, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendering mit GDI+ erfordern.

## <a name="direct3d-interoperability"></a>Direct3D-Interoperabilität

Direct2D kann ein DXGI-Oberflächen Renderziel (erstellt von der Methode " [**kreatedxgisurfacerender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ") verwenden, um in eine [idxgisurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface)zu schreiben. Diese Aktion ermöglicht Ihnen das Hinzufügen von 2D-Hintergründen und-Schnittstellen zu 3D-Szenen und die Verwendung von Direct2D-Inhalten als Textur für ein 3D-Modell. Direct2D kann auch eine [idxgisurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) -Methode verwenden und die Methode " [**kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) " verwenden, um eine Bitmap-Darstellung zu erstellen.

Weitere Informationen und Beispiele finden Sie unter [Übersicht über die Interoperabilität mit Direct2D und Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>DirectWrite-Interoperabilität

Direct2D ist eng in DirectWrite integriert. Direct2D erleichtert das Rendering von DirectWrite-Inhalten durch Bereitstellen der Methoden [**DrawText**](id2d1rendertarget-drawtext.md), [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Interoperabilität von Windows Imaging Component (WIC)

Direct2D [**stellt die Methoden**](id2d1rendertarget-createbitmapfromwicbitmap.md)"", "" "" "" "" "" "" "" "" "" "" "" "" "" "," "", "" [**","**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)"", " [**" und "**](id2d1factory-createwicbitmaprendertarget.md) "

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Direct2D-und GDI-Interoperabilität](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Übersicht über die Interoperabilität von Direct2D und Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 