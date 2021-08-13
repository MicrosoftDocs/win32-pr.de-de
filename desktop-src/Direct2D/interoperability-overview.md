---
title: Überblick über die Interoperabilität
description: Fasst die verschiedenen Technologien zusammen, die Sie mit Direct2D verwenden können.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D,GDI-Interoperation
- Direct2D,GDI+ Interoperation
- Direct2D, Interoperabilität
- Direct2D,DirectWrite Interoperation
- Interoperabilität,Direct2D
- Interoperabilität,Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperability,Graphics Device Interface (GDI)
- Interoperabilität,GDI+
- DirectWrite Interoperabilität
- Interoperabilität,DirectWrite
- Windows Imaging-Komponente (WIC)
- WIC (Windows Imaging Component)
- Interoperability,Windows Imaging Component (WIC)
- Direct2D,WIC-Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385324"
---
# <a name="interoperability-overview"></a>Überblick über die Interoperabilität

Eines der wichtigsten Features von Direct2D ist die Aktivierung der Interoperabilität zwischen Direct2D und anderen Renderingplattformen, sodass Entwickler die spezifischen Stärken jeder Plattform nutzen können, ohne dass sie zu Kompromittierungsanforderungen gezwungen werden, indem sie eine Plattform für alle Anforderungen auswählen. In diesem Thema werden die verschiedenen Plattformen zusammengefasst, mit denen Direct2D interoperabel ist. Der Abschnitt ist wie folgt gegliedert.

-   [GDI-Interoperabilität](#gdi-interoperability)
-   [GDI+ Interoperabilität](#gdi-interoperability)
-   [Direct3D-Interoperabilität](#direct3d-interoperability)
-   [DirectWrite Interoperabilität](#directwrite-interoperability)
-   [Windows WIC-Interoperabilität (Imaging Component)](#windows-imaging-component-wic-interoperability)
-   [Zugehörige Themen](#related-topics)

Das folgende Diagramm fasst die verschiedenen Plattformen zusammen, mit denen Direct2D interoperabel ist, und listet einige Methoden und Schnittstellen auf, die Interoperabilität bieten.

![Diagramm der Plattformen, mit denen direct2d interoperiert, einschließlich direct3d 10.1, directwrite, wic, gdi+ und gdi](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>GDI-Interoperabilität

Direct2D ermöglicht die zweigeteilte Interoperabilität mit GDI. Sie können [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) verwenden, um Direct2D-Inhalt in einen GDI-Gerätekontext (DC) zu schreiben, oder Sie können [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um eine DC-Darstellung eines Renderziels zu erhalten. [](/windows/desktop/gdi/device-contexts)

Weitere Informationen und Beispiele finden Sie unter Direct2D und GDI Interoperability Overview ( Übersicht über die [Direct2D- und GDI-Interoperabilität).](direct2d-and-gdi-interoperation-overview.md)

## <a name="gdi-interoperability"></a>GDI+ Interoperabilität

Sie können GDI+ mit Direct2D auf die gleiche Weise wie GDI verwenden. Sie können ein [**ID2D1DCRenderTarget-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) verwenden, um Direct2D-Inhalte auf denselben Domänencontroller zu schreiben, auf dem sich GDI+. Mit diesem Ansatz können Sie mit dem Hinzufügen von Direct2D-Inhalten zu Anwendungen beginnen, die hauptsächlich mithilfe von GDI+.

Sie können auch ein [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um Zugriff auf einen GDI-DC zu ermöglichen, der mit Direct2D schreibt, und dann die [**FromHDC-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) verwenden, um ein -Objekt zu erstellen. Dieser Ansatz ist nützlich für Anwendungen, die in erster Linie mit Direct2D gerendert werden, aber über ein Erweiterbarkeitsmodell oder andere Legacyinhalte verfügen, die die Möglichkeit zum Rendern mit GDI+.

## <a name="direct3d-interoperability"></a>Direct3D-Interoperabilität

Direct2D kann ein DXGI-Oberflächenrenderingziel verwenden (erstellt von der [**CreateDxgiSurfaceRender-Methode),**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um in eine [IDXGISurface zu schreiben.](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) Mit dieser Aktion können Sie 2D-Hintergründe und -Schnittstellen zu 3D-Szenen hinzufügen und Direct2D-Inhalt als Textur für ein 3D-Modell verwenden. Direct2D kann auch eine [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) verwenden und die [**CreateSharedBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) verwenden, um eine Bitmapdarstellung zu erstellen.

Weitere Informationen und Beispiele finden Sie unter [Direct2D und Direct3D Interoperability Overview ( Übersicht über die Direct2D- und Direct3D-Interoperabilität).](direct2d-and-direct3d-interoperation-overview.md)

## <a name="directwrite-interoperability"></a>DirectWrite Interoperabilität

Direct2D ist eng in die DirectWrite. Direct2D erleichtert das Rendern DirectWrite Inhalt, indem die [**Methoden DrawText,**](id2d1rendertarget-drawtext.md) [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)und [**DrawGlyphRun zur Verfügung stehen.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

## <a name="windows-imaging-component-wic-interoperability"></a>Windows WIC-Interoperabilität (Imaging Component)

Direct2D stellt die [**Methoden CreateBitmapFromWicBitmap,**](id2d1rendertarget-createbitmapfromwicbitmap.md) [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)und [**CreateWicBitmapRenderTarget zum**](id2d1factory-createwicbitmaprendertarget.md) Bearbeiten von WIC-Bitmaps zur Auswahl.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Direct2D- und GDI-Interoperabilität](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Übersicht über die Interoperabilität von Direct2D und Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 