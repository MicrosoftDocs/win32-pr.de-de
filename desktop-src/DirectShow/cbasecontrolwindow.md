---
description: Die CBaseControlWindow-Klasse implementiert die IVideoWindow-Schnittstelle und steuert den externen Zugriff auf den zugehörigen Filter.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: CBaseControlWindow-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: 500706531d7e7a934681dabe3bcd00b7de0d80e42b8bbf27a5456a8fd4415f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017233"
---
# <a name="cbasecontrolwindow-class"></a>CBaseControlWindow-Klasse

![cbasecontrolwindow-Klassenhierarchie](images/wctrl01.png)

Die **CBaseControlWindow-Klasse** implementiert die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) und steuert den externen Zugriff auf den zugehörigen Filter. Sie müssen das **CBaseControlWindow-Objekt** mit dem Filter synchronisieren, indem Sie ihm einen Zeiger auf ein kritisches Abschnittssynchronisierungsobjekt übergeben. Die **CBaseControlWindow-Klasse** bietet eine Reihe von Methoden, die Eigenschafteneinstellungen zurückgeben, ohne diesen kritischen Abschnitt zu bearbeiten. Wenn Sie beispielsweise [**CBaseControlWindow::get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) aufrufen, um den Wert des **Datenmitglieds m \_ bAutoShow** abzurufen, wird der kritische Abschnitt gesperrt. Der Filter kann jedoch bereits über einen gesperrten internen kritischen Abschnitt verfügen, der gegen die Sperrhierarchie des Filters verstoßen könnte. Stattdessen gibt der Aufruf der [**CBaseControlWindow::IsAutoShowEnabled-Memberfunktion**](cbasecontrolwindow-isautoshowenabled.md) den erforderlichen Wert zurück, ohne den kritischen Abschnitt zu beeinflussen.

Alle **in CBaseControlWindow implementierten** [**IVideoWindow-Methoden**](/windows/desktop/api/Control/nn-control-ivideowindow) erfordern, dass der Filter ordnungsgemäß mit dem Upstreamfilter verbunden ist. Aus diesem Grund erfordern Klassenobjekte einen Synchronisierungspin, den Sie durch Aufrufen der [**CBaseControlWindow::SetControlWindowPin-Methode**](cbasecontrolwindow-setcontrolwindowpin.md) festlegen. Jedes Mal, wenn Sie eine **IVideoWindow-Methode** aufrufen, überprüft das **CBaseControlWindow-Objekt,** ob der Pin noch verbunden ist.



| Geschützte Datenmember                                                     | Beschreibung                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Ergebnis, wenn sich der Zustand ändert.                                                                                                              |
| m \_ bCursorHidden                                                           | Bestimmung, ob der Cursor angezeigt oder ausgeblendet wird.                                                                                 |
| m \_ BorderColour                                                            | Farbe des aktuellen Fensterrahmens.                                                                                                         |
| m \_ hwndDrain                                                               | Fensterhand handle, an das empfangene Nachrichten gesendet werden.                                                                                        |
| m \_ hwndOwner                                                               | Besitzende Fenster.                                                                                                                              |
| m \_ pFilter                                                                 | Zeiger auf den besitzenden Medienfilter.                                                                                                         |
| m \_ pInterfaceLock                                                          | Extern definierter kritischer Abschnitt.                                                                                                        |
| m \_ pPin                                                                    | Steuerung der Medientypen für die Verbindung.                                                                                                  |
| Elementfunktionen                                                           | Beschreibung                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Erstellt ein **CBaseControlWindow-Objekt.**                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Ruft entweder die typischen oder erweiterten Fensterstile ab.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Legt die typischen oder erweiterten Fensterstile fest.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Ruft die aktuelle Rahmenfarbe ab. Dies ist eine Hilfsfunktion.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Ruft das besitzende Fenster ab. Dies ist eine Hilfsfunktion.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der Renderingfilter angehalten oder ausgeführt wird.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Ruft den aktuellen Zustand des **m \_ bCursorHidden-Datenmitglieds** ab, ohne den kritischen Abschnitt zu sperren. Dies ist eine Hilfsfunktion. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Verteilt Nachrichten an das übergeordnete Fenster.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Benachrichtigt das Objekt der Stecknadel, auf die es angewendet wird.                                                                                         |
| IVideoWindow-Methoden                                                       | Beschreibung                                                                                                                                 |
| [**Get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md)                   | Ruft die aktuelle Einstellung des Flags AutoShow ab.                                                                                                |
| [**Get \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Ruft die realisierte Palette im Hintergrundflag ab.                                                                                      |
| [**Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md)             | Ruft die aktuelle Rahmenfarbe ab.                                                                                                         |
| [**Get \_ Caption**](cbasecontrolwindow-get-caption.md)                     | Ruft die aktuelle Fensterbeschriftung ab.                                                                                                       |
| [**Get \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Ruft den aktuellen Vollbildmodus ab.                                                                                                     |
| [**Get \_ Height**](cbasecontrolwindow-get-height.md)                       | Ruft die aktuelle Fensterhöhe ab.                                                                                                        |
| [**get \_ Left**](cbasecontrolwindow-get-left.md)                           | Ruft die aktuelle linke Fensterkoordinate ab.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Ruft die maximale Größe des idealen Bilds ab.                                                                                              |
| [**get \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Ruft den aktuellen Nachrichtenabfluss ab.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Ruft die Mindestgröße des idealen Bilds ab.                                                                                              |
| [**Besitzer \_ erhalten**](cbasecontrolwindow-get-owner.md)                         | Ruft das übergeordnete Fensterhand handle ab.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Ruft die Position ab, an der das Fenster wiederhergestellt wird, wenn es maximiert oder minimiert wird.                                                    |
| [**Get \_ Top**](cbasecontrolwindow-get-top.md)                             | Ruft die y-Koordinate für den oberen Teil des Fensters ab.                                                                                       |
| [**Get \_ Visible**](cbasecontrolwindow-get-visible.md)                     | Ruft die aktuelle Sichtbarkeitseinstellung des Fensters ab.                                                                                     |
| [**get \_ Width**](cbasecontrolwindow-get-width.md)                         | Ruft die Breite des Fensters ab.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Ruft die aktuellen Fensterkoordinaten ab.                                                                                                   |
| [**Get \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Ruft den aktuellen Zustand des Fensters ab.                                                                                                  |
| [**Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Ruft die Standardfensterstile ab.                                                                                                       |
| [**Get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Ruft die erweiterten Fensterstile ab.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Blendet den Cursor aus oder zeigt den Cursor an.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Ruft den aktuellen Zustand des **m \_ bCursorHidden-Datenmitglieds** ab.                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Übergibt Nachrichten, die an besitzende Fenster gesendet werden.                                                                                         |
| [**put \_ AutoShow**](cbasecontrolwindow-put-autoshow.md)                   | Legt die AutoShow-Eigenschaft fest.                                                                                                                 |
| [**put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Legt ein Flag fest, um die Palette im Hintergrund zu realisieren.                                                                                       |
| [**\_put BorderColor**](cbasecontrolwindow-put-bordercolor.md)             | Legt die aktuelle Rahmenfarbe fest.                                                                                                              |
| [**\_beschriftung put**](cbasecontrolwindow-put-caption.md)                     | Legt die aktuelle Fensterbeschriftung fest.                                                                                                            |
| [**\_put FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Legt den Vollbildmodus fest.                                                                                                                  |
| [**put \_ Height**](cbasecontrolwindow-put-height.md)                       | Legt die aktuelle Fensterhöhe fest.                                                                                                             |
| [**\_put Left**](cbasecontrolwindow-put-left.md)                           | Legt die linke Koordinate für das Fenster fest.                                                                                                    |
| [**put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Legt das Meldungsentleerungsfenster fest.                                                                                                              |
| [**put \_ Owner**](cbasecontrolwindow-put-owner.md)                         | Legt das übergeordnete Microsoft Win32-Fensterhandle fest.                                                                                              |
| [**put \_ Top**](cbasecontrolwindow-put-top.md)                             | Legt die Position für den oberen Rand des Fensters fest.                                                                                                |
| [**\_put Visible**](cbasecontrolwindow-put-visible.md)                     | Blendet das Fenster aus oder zeigt es an.                                                                                                                  |
| [**put \_ Width**](cbasecontrolwindow-put-width.md)                         | Legt die Breite des Fensters fest.                                                                                                               |
| [**\_Put WindowState**](cbasecontrolwindow-put-windowstate.md)             | Legt den Zustand des Fensters fest.                                                                                                               |
| [**\_put WindowStyle**](cbasecontrolwindow-put-windowstyle.md)             | Legt die Standardfensterstile fest.                                                                                                            |
| [**\_Put WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Legt die erweiterten Fensterstile fest.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Legt das Fenster im Vordergrund fest.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Legt die Fensterposition fest.                                                                                                                   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 



