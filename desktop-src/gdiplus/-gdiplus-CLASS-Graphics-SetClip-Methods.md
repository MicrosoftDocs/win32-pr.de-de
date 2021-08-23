---
description: In diesem Thema werden die SetClip-Methoden der Graphics-Klasse aufgelistet. Eine vollständige Liste der Methoden für die Graphics-Klasse finden Sie unter Grafiken.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Graphics.SetClip-Methoden
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 616a78aa7dd251e888bba1186a3583c5d7f62d188dcc6313560f651ec6558827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037188"
---
# <a name="graphicssetclip-methods"></a>Graphics.SetClip-Methoden

In diesem Thema werden die SetClip-Methoden der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) aufgelistet. Eine vollständige Liste der Methoden für die **Graphics-Klasse** finden Sie unter [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip(HRGN,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | Die [**Graphics::SetClip-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) aktualisiert den Ausschneidebereich dieses [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und einem GDI-Bereich darstellt.<br/>                                                                                                                                                                                                          |
| [**SetClip(Rect&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | Die [**Graphics::SetClip-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) aktualisiert den Ausschneidebereich dieses [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und einem Rechteck darstellt.<br/>                                                                                                                                                                                          |
| [**SetClip(RectF&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | Die [**Graphics::SetClip-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) aktualisiert den Ausschneidebereich dieses [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und einem Rechteck darstellt.<br/>                                                                                                                                                                                         |
| [**SetClip(Region, \* CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | Die [**Graphics::SetClip-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) aktualisiert den Ausschneidebereich dieses [**Graphics-Objekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und dem durch ein [**Region-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) angegebenen Bereich ist.<br/>                                                                                                                                      |
| [**SetClip(Graphics \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | Die [**Graphics::SetClip-Methode**](/previous-versions//ms535823(v=vs.85)) aktualisiert den Ausschneidebereich dieses [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und dem Ausschneidebereich eines anderen **Graphics-Objekts** darstellt.<br/>                                                                                                                                                                       |
| [**SetClip(GraphicsPath, \* CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | Die [**Graphics::SetClip-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) aktualisiert den Ausschneidebereich dieses [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in einen Bereich, der die Kombination aus sich selbst und dem durch einen Grafikpfad angegebenen Bereich darstellt. Wenn eine Figur im Pfad nicht geschlossen ist, behandelt diese Methode die nicht geschlossene Figur so, als ob sie durch eine gerade Linie geschlossen wäre, die die Anfangs- und Endpunkte der Figur verbindet.<br/> |



 

 
