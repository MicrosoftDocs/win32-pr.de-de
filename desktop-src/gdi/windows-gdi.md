---
description: Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979360"
---
# <a name="windows-gdi"></a>Windows GDI

## <a name="purpose"></a>Zweck

Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker. Windows-basierte Anwendungen greifen nicht direkt auf die Grafikhardware zu. Stattdessen interagiert GDI im Auftrag von Anwendungen mit Gerätetreibern.

## <a name="where-applicable"></a>Anwendungsbereich

GDI kann in allen Windows-basierten Anwendungen verwendet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Diese API ist für die Verwendung durch C/C++-Programmierer konzipiert. Es ist eine Vertrautheit mit der [Nachrichten gesteuerten Windows-Architektur](../learnwin32/window-messages.md) erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Bitmaps](bitmaps.md)
-   [Pinsel](brushes.md)
-   [Freistellen](clipping.md)
-   [Farben](colors.md)
-   [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md)
-   [Geräte Kontexte](device-contexts.md)
-   [Gefüllte Formen](filled-shapes.md)
-   [Schriftarten und Text](fonts-and-text.md)
-   [Linien und Kurven](lines-and-curves.md)
-   [Metadateien](metafiles.md)
-   [Mehrere Anzeige Monitore](multiple-display-monitors.md)
-   [Zeichnen und zeichnen](painting-and-drawing.md)
-   [Paths](paths.md)
-   [Stifte](pens.md)
-   [Druck-und Druck Spooler](/previous-versions//dd162860(v=vs.85))
-   [Rechtecke](rectangles.md)
-   [Regionen](regions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[GDI+](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Windows-Abbild Erfassung](../wia/-wia-startpage.md)
</dt> </dl>

 

 
