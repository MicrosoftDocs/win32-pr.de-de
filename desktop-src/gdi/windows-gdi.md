---
description: Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bbdd515379c5c3d1f2c17ff0b991141b3a40a8cb42594be95e391da6dabb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092540"
---
# <a name="windows-gdi"></a>Windows GDI

## <a name="purpose"></a>Zweck

Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker. Windows-basierten Anwendungen greifen nicht direkt auf die Grafikhardware zu. Stattdessen interagiert GDI im Auftrag von Anwendungen mit Gerätetreibern.

## <a name="where-applicable"></a>Anwendungsbereich

GDI kann in allen Windows-basierten Anwendungen verwendet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Diese API ist für die Verwendung durch C/C++-Programmierer konzipiert. Sie müssen mit der Windows [nachrichtengesteuerten Architektur](../learnwin32/window-messages.md) vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt Anforderungen der Dokumentation für die Funktion.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Bitmaps](bitmaps.md)
-   [Pinsel](brushes.md)
-   [Freistellen](clipping.md)
-   [Farben](colors.md)
-   [Koordinatenräume und Transformationen](coordinate-spaces-and-transformations.md)
-   [Gerätekontexte](device-contexts.md)
-   [Gefüllte Formen](filled-shapes.md)
-   [Schriftarten und Text](fonts-and-text.md)
-   [Linien und Kurven](lines-and-curves.md)
-   [Metadateien](metafiles.md)
-   [Mehrere Anzeigemonitore](multiple-display-monitors.md)
-   [Zeichnen und Zeichnen](painting-and-drawing.md)
-   [Paths](paths.md)
-   [Stifte](pens.md)
-   [Druck- und Druckspooler](/previous-versions//dd162860(v=vs.85))
-   [Rechtecke](rectangles.md)
-   [Regionen](regions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[GDI+](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[Opengl](../opengl/opengl.md)
</dt> <dt>

[Windows Bilderfassung](../wia/-wia-startpage.md)
</dt> </dl>

 

 
