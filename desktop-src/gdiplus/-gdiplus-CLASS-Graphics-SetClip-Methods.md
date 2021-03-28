---
description: In diesem Thema werden die SetClip-Methoden der Grafikklasse aufgelistet. Eine umfassende Liste der Methoden für die Grafikklasse finden Sie unter Grafiken.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Graphics. SetClip-Methoden
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 488d617dfb53343fc728fff722c0c0bc1db57335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215625"
---
# <a name="graphicssetclip-methods"></a>Graphics. SetClip-Methoden

In diesem Thema werden die SetClip-Methoden der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufgelistet. Eine umfassende Liste der Methoden für die **Grafik** Klasse finden Sie unter [**Grafiken**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip (hrgn, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | Die [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und einem GDI-Bereich ist.<br/>                                                                                                                                                                                                          |
| [**SetClip (Rect&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | Die [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und einem Rechteck ist.<br/>                                                                                                                                                                                          |
| [**SetClip (RectF&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | Die [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und einem Rechteck ist.<br/>                                                                                                                                                                                         |
| [**SetClip (Region \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | Die [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und dem durch ein [**Regions**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Objekt angegebenen Bereich ist.<br/>                                                                                                                                      |
| [**SetClip (Grafiken \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | Die [**Graphics:: SetClip**](/previous-versions//ms535823(v=vs.85)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und dem Ausschneide Bereich eines anderen **Grafik** Objekts ist.<br/>                                                                                                                                                                       |
| [**SetClip (GraphicsPath \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | Die [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) -Methode aktualisiert den Clippingbereich dieses [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf einen Bereich, der die Kombination aus sich selbst und dem durch einen Grafik Pfad angegebenen Bereich ist. Wenn eine Abbildung im Pfad nicht geschlossen wird, behandelt diese Methode die nicht geschlossene Abbildung so, als ob Sie durch eine gerade Linie geschlossen würde, die die Anfangs-und Endpunkte der Abbildung verbindet.<br/> |



 

 
