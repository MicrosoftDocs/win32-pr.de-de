---
description: Die cbasecontrolwindow-Klasse implementiert die IVideoWindow-Schnittstelle und steuert den externen Zugriff auf den zugehörigen Filter.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: Cbasecontrolwindow-Klasse
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
ms.openlocfilehash: c4b53cc5ce1b209cc7de9d68648b68096e5c4911
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213947"
---
# <a name="cbasecontrolwindow-class"></a>Cbasecontrolwindow-Klasse

![cbasecontrolwindow-Klassenhierarchie](images/wctrl01.png)

Die **cbasecontrolwindow** -Klasse implementiert die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle und steuert den externen Zugriff auf den zugehörigen Filter. Sie müssen das **cbasecontrolwindow** -Objekt mit dem Filter synchronisieren, indem Sie ihm einen Zeiger auf ein kritisches Abschnitts Synchronisierungs Objekt übergeben. Die **cbasecontrolwindow** -Klasse stellt eine Reihe von Methoden bereit, die Eigenschafts Einstellungen zurückgeben, ohne dass dieser kritische Abschnitt behandelt wird. Wenn Sie z. b. [**cbasecontrolwindow:: get \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) aufrufen, um den Wert des Datenmembers **m \_ bautoshow** abzurufen, sperrt den kritischen Abschnitt. Der Filter verfügt jedoch möglicherweise bereits über einen gesperrten internen kritischen Abschnitt, der gegen die Sperr Hierarchie des Filters verstoßen könnte. Stattdessen wird durch Aufrufen der [**cbasecontrolwindow:: isautoshowenabled**](cbasecontrolwindow-isautoshowenabled.md) -Member-Funktion der erforderliche Wert zurückgegeben, ohne dass sich dies auf den kritischen Abschnitt auswirkt.

Alle **cbasecontrolwindow** implementierten [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Methoden erfordern, dass der Filter mit dem upstreamfilter ordnungsgemäß verbunden ist. Aus diesem Grund erfordern Klassen Objekte eine Synchronisierungs-PIN, die Sie durch Aufrufen der [**cbasecontrolwindow:: setcontrolwindowpin**](cbasecontrolwindow-setcontrolwindowpin.md) -Methode festlegen. Jedes Mal, wenn Sie eine **IVideoWindow** -Methode aufgerufen haben, prüft das **cbasecontrolwindow** -Objekt, ob die PIN noch verbunden ist.



| Geschützte Datenmember                                                     | BESCHREIBUNG                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bauum anzeigen                                                               | Ergebnis, wenn sich der Status ändert.                                                                                                              |
| m \_ bcurrsorhidden                                                           | Bestimmung, ob der Cursor angezeigt oder ausgeblendet wird.                                                                                 |
| m \_ BorderColor                                                            | Farbe des aktuellen Fensterrahmens.                                                                                                         |
| m \_ hwnddrain                                                               | Fenster Handle, an das empfangene Nachrichten gesendet werden.                                                                                        |
| m \_ hwndOwner                                                               | Besitz Endes Fenster.                                                                                                                              |
| m \_ pFilter                                                                 | Zeiger auf den besitzenden Medienfilter.                                                                                                         |
| m \_ pinterfakelock                                                          | Extern definierter kritischer Abschnitt.                                                                                                        |
| m \_ ppin                                                                    | Steuerung der Medientypen für die Verbindung.                                                                                                  |
| Elementfunktionen                                                           | BESCHREIBUNG                                                                                                                                 |
| [**Cbasecontrolwindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Erstellt ein **cbasecontrolwindow** -Objekt.                                                                                                 |
| [**Dogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Ruft entweder den typischen oder den erweiterten Fenster Stil ab.                                                                                     |
| [**Dosetwindowstyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Legt die typischen oder erweiterten Fenster Stile fest.                                                                                                 |
| [**GetBorderColor**](cbasecontrolwindow-getbordercolour.md)              | Ruft die aktuelle Rahmenfarbe ab. Dies ist eine Hilfsmember-Funktion.                                                                       |
| [**Getownerwindow**](cbasecontrolwindow-getownerwindow.md)                | Ruft das besitzende Fenster ab. Dies ist eine Hilfsmember-Funktion.                                                                              |
| [**Isautoshowenabled**](cbasecontrolwindow-isautoshowenabled.md)          | Ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der renderingfilter anhält oder ausgeführt wird.                        |
| [**Iscurrsorhidden**](cbasecontrolwindow-iscursorhidden.md)                | Ruft den aktuellen Zustand des **m \_ bcurrsorhidden** -Datenmembers ab, ohne den kritischen Abschnitt zu sperren. Dies ist eine Hilfsmember-Funktion. |
| [**Possiblyeatmessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Verteilt Meldungen an das übergeordnete Fenster.                                                                                                  |
| [**Setcontrolwindowpin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Benachrichtigt das-Objekt über die PIN, auf die es angewendet wird.                                                                                         |
| IVideoWindow-Methoden                                                       | BESCHREIBUNG                                                                                                                                 |
| [**\_AutoShow anzeigen**](cbasecontrolwindow-get-autoshow.md)                   | Ruft die aktuelle Autoshow-Flag-Einstellung ab.                                                                                                |
| [**\_backgroundpalette erhalten**](cbasecontrolwindow-get-backgroundpalette.md) | Ruft die realisierte Palette im hintergrundflag ab.                                                                                      |
| [**\_BorderColor erhalten**](cbasecontrolwindow-get-bordercolor.md)             | Ruft die aktuelle Rahmenfarbe ab.                                                                                                         |
| [**\_Beschriftung erhalten**](cbasecontrolwindow-get-caption.md)                     | Ruft die aktuelle Fenster Beschriftung ab.                                                                                                       |
| [**\_Vollbildmodus erhalten**](cbasecontrolwindow-get-fullscreenmode.md)      | Ruft den aktuellen Vollbildmodus ab.                                                                                                     |
| [**\_Höhe erhalten**](cbasecontrolwindow-get-height.md)                       | Ruft die aktuelle Fensterhöhe ab.                                                                                                        |
| [**nach \_ Links**](cbasecontrolwindow-get-left.md)                           | Ruft die aktuelle linke Fenster Koordinate ab.                                                                                               |
| [**Getmaxidealimagesize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Ruft die maximale Größe des idealen Bilds ab.                                                                                              |
| [**\_messagedrain erhalten**](cbasecontrolwindow-get-messagedrain.md)           | Ruft den aktuellen Nachrichten Ausgleich ab.                                                                                                        |
| [**Getminide alimagesize**](cbasecontrolwindow-getminidealimagesize.md)    | Ruft die Mindestgröße des idealen Bilds ab.                                                                                              |
| [**\_Besitzer erhalten**](cbasecontrolwindow-get-owner.md)                         | Ruft das übergeordnete Fenster Handle ab.                                                                                                         |
| [**Getrestoreposition**](cbasecontrolwindow-getrestoreposition.md)        | Ruft die Position ab, an der das Fenster wieder hergestellt wird, wenn es maximiert oder minimiert wird.                                                    |
| [**get \_ Top**](cbasecontrolwindow-get-top.md)                             | Ruft die y-Koordinate für den oberen Rand des Fensters ab.                                                                                       |
| [**\_sichtbar machen**](cbasecontrolwindow-get-visible.md)                     | Ruft die aktuelle Sichtbarkeits Einstellung des Fensters ab.                                                                                     |
| [**\_Breite erhalten**](cbasecontrolwindow-get-width.md)                         | Ruft die Breite des Fensters ab.                                                                                                          |
| [**Getwindowposition**](cbasecontrolwindow-getwindowposition.md)          | Ruft die aktuellen Fenster Koordinaten ab.                                                                                                   |
| [**\_Windows State herunterladen**](cbasecontrolwindow-get-windowstate.md)             | Ruft den aktuellen Zustand des Fensters ab.                                                                                                  |
| [**\_WindowStyle herunterladen**](cbasecontrolwindow-get-windowstyle.md)             | Ruft die Standardfenster Stile ab.                                                                                                       |
| [**\_windowstyleex herunterladen**](cbasecontrolwindow-get-windowstyleex.md)         | Ruft die erweiterten Fenster Stile ab.                                                                                                       |
| [**Hidecursor**](cbasecontrolwindow-hidecursor.md)                        | Blendet den Cursor aus oder zeigt ihn an.                                                                                                               |
| [**Iscurrsorhidden**](cbasecontrolwindow-iscursorhidden.md)                | Ruft den aktuellen Zustand des **m \_ bcurrsorhidden** -Datenmembers ab.                                                                        |
| [**Notierte Meldung**](cbasecontrolwindow-notifyownermessage.md)        | Übergibt Nachrichten, die an besitzende Fenster gesendet werden.                                                                                         |
| [**\_AutoShow platzieren**](cbasecontrolwindow-put-autoshow.md)                   | Legt die Autoshow-Eigenschaft fest.                                                                                                                 |
| [**\_backgroundpalette ablegen**](cbasecontrolwindow-put-backgroundpalette.md) | Legt ein Flag fest, um die Palette im Hintergrund zu erkennen.                                                                                       |
| [**\_BorderColor platzieren**](cbasecontrolwindow-put-bordercolor.md)             | Legt die aktuelle Rahmenfarbe fest.                                                                                                              |
| [**\_Beschriftung platzieren**](cbasecontrolwindow-put-caption.md)                     | Legt die aktuelle Fenster Beschriftung fest.                                                                                                            |
| [**\_Fullscreenmode platzieren**](cbasecontrolwindow-put-fullscreenmode.md)      | Legt den Vollbildmodus fest.                                                                                                                  |
| [**\_Höhe ablegen**](cbasecontrolwindow-put-height.md)                       | Legt die aktuelle Fensterhöhe fest.                                                                                                             |
| [**\_Links ablegen**](cbasecontrolwindow-put-left.md)                           | Legt die linke Koordinate für das Fenster fest.                                                                                                    |
| [**\_messagedrain platzieren**](cbasecontrolwindow-put-messagedrain.md)           | Legt das Fenster für die Nachrichten Ableitung fest.                                                                                                              |
| [**\_Besitzer ablegen**](cbasecontrolwindow-put-owner.md)                         | Legt das übergeordnete Microsoft Win32-Fenster Handle fest.                                                                                              |
| [**\_oben platzieren**](cbasecontrolwindow-put-top.md)                             | Legt die Position für den oberen Rand des Fensters fest.                                                                                                |
| [**\_sichtbar machen**](cbasecontrolwindow-put-visible.md)                     | Blendet das Fenster aus oder ein.                                                                                                                  |
| [**\_Breite platzieren**](cbasecontrolwindow-put-width.md)                         | Legt die Breite des Fensters fest.                                                                                                               |
| [**\_Windows State platzieren**](cbasecontrolwindow-put-windowstate.md)             | Legt den Zustand des Fensters fest.                                                                                                               |
| [**\_Windows Style platzieren**](cbasecontrolwindow-put-windowstyle.md)             | Legt die Standardfenster Stile fest.                                                                                                            |
| [**\_Windows styleex ablegen**](cbasecontrolwindow-put-windowstyleex.md)         | Legt die erweiterten Fenster Stile fest.                                                                                                            |
| [**Setwindowvorder Grund**](cbasecontrolwindow-setwindowforeground.md)      | Legt das Fenster im Vordergrund fest.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Legt die Fensterposition fest.                                                                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 



