---
description: Die CBaseControlVideo-Klasse implementiert die IBasicVideo-Schnittstelle und steuert die Videoeigenschaften eines generischen Videofensters. Im Allgemeinen ist ein CBaseControlVideo-Objekt ein Videorenderer, der Videos in ein Fenster auf der Anzeige zeichnet.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: CBaseControlVideo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d8e6f7c881cc62f9124a58cb168bb3b2123d5f8e3c99b1d86b6aed0f87e2aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697944"
---
# <a name="cbasecontrolvideo-class"></a>CBaseControlVideo-Klasse

![cbasecontrolvideo-Klassenhierarchie](images/wctrl02.png)

Die **CBaseControlVideo-Klasse** implementiert die [**IBasicVideo-Schnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) und steuert die Videoeigenschaften eines generischen Videofensters. Im Allgemeinen ist ein **CBaseControlVideo-Objekt** ein Videorenderer, der Videos in ein Fenster auf der Anzeige zeichnet.

Viele **CBaseControlVideo-Memberfunktionen** erfordern nur, dass der Videorenderer mit einem Filterdiagramm verbunden ist. Wenn keine Verbindung besteht, geben Memberfunktionen **VFW \_ E NOT CONNECTED \_ \_ zurück.** Für einen Videorenderer festgelegte Eigenschaften bleiben zwischen aufeinander folgenden Verbindungen und Trennungen erhalten. Alle Anwendungen sollten sicherstellen, dass sie die Renderereigenschaften zurücksetzen, bevor sie eine Präsentation starten.

Bei der Arbeit mit Videos kann die Anwendung einen Teil des Videos auswählen, der verwendet werden soll. Dieser Teil ist das Quellrechteck, das das **CBaseControlVideo-Objekt** steuert. **Mit CBaseControlVideo** kann Ihre Anwendung das Quellrechteck festlegen und abrufen. Alle Rechtecke, die **CBaseControlVideo** verwendet, verwenden Werte für Breite und Höhe anstelle von rechten und unteren Werten. Wenn kein Quellrechteck festgelegt wurde, geben die Eigenschaften des Quellrechtecks die vollständige native Videogröße zurück.



| Geschützte Datenmember                                                                   | Beschreibung                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Zeiger auf einen besitzenden Medienfilter.                                                              |
| m \_ pInterfaceLock                                                                        | Extern definierter kritischer Abschnitt.                                                            |
| m \_ pPin                                                                                  | Steuerung der Medientypen für die Verbindung.                                                      |
| Elementfunktionen                                                                         | Beschreibung                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Erstellt ein **CBaseControlVideo-Objekt.**                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Erstellt eine Speicherkopie eines Videobilds.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Ruft Informationen zur Videobildgröße ab.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Legt den Pin fest, mit dem dieses Objekt synchronisiert werden soll.                                         |
| Überschreibbare Memberfunktionen                                                             | Beschreibung                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Bestimmt, ob ein Quellrechteck gültig ist.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Bestimmt, ob ein Zielrechteck gültig ist.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Ruft das aktuelle Quellvideorechteck (rein virtuell) ab.                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Gibt das aktuelle Bild in einem Speicherpuffer (rein virtuell) zurück.                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Ruft das aktuelle Zielvideorechteck (rein virtuell) ab.                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Ruft die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ab, die das Videoformat enthält. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Bestimmt, ob der Renderer das Standardquellenrechteck (rein virtuell) verwendet.                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Bestimmt, ob der Renderer das Standardzielrechteck (rein virtuell) verwendet.                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Wird aufgerufen, wenn sich das Quell- oder Zielrechteck ändert.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Übergibt EC \_ VIDEO SIZE CHANGED an die \_ \_ Anwendung.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Legt das Standard-Quellvideorechteck (rein virtuell) fest.                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Legt das Standardzielvideorechteck (rein virtuell) fest.                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Legt das aktuelle Quellvideorechteck (rein virtuell) fest.                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Legt das aktuelle Zielrechteck (rein virtuell) fest.                                               |
| IBasicVideo-Methoden                                                                      | Beschreibung                                                                                     |
| [**get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Ruft eine ungefähre durchschnittliche Zeit pro Frame ab.                                                |
| [**Get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Ruft eine ungefähre Bitfehlerrate ab.                                                        |
| [**Get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)                                    | Ruft eine ungefähre Bitrate für das Video ab.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Ruft ein Speicherrendering des aktuellen Bilds ab.                                              |
| [**get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Ruft die Höhe des aktuellen Zielrechtecks ab.                                           |
| [**get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Ruft die linke Koordinate des aktuellen Zielrechtecks ab.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Ruft die aktuelle Zielposition ab.                                                     |
| [**Get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Ruft die obere Koordinate des aktuellen Zielrechtecks ab.                                   |
| [**Get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Ruft die Breite des aktuellen Zielrechtecks ab.                                            |
| [**get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Ruft die Höhe des aktuellen Quellrechtecks ab.                                                |
| [**get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Ruft die linke Koordinate des aktuellen Quellrechtecks ab.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Ruft die aktuelle Quellposition ab.                                                          |
| [**Get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Ruft die obere Koordinate des aktuellen Quellrechtecks ab.                                        |
| [**Get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Ruft die Breite des aktuellen Quellrechtecks ab.                                                 |
| [**Get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Ruft die Höhe des nativen Videos ab.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Ruft einen Bereich von Paletteneinträgen für das Video ab.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Ruft die Breite und Höhe des nativen Videos ab.                                             |
| [**get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Ruft die systemeigene Videobreite ab.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Bestimmt, ob der Renderer das Standardzielfenster verwendet.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Bestimmt, ob der Renderer das Standardquellfenster verwendet.                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Legt die Höhe des Zielrechtecks fest.                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Legt die linke Koordinate des Zielrechtecks fest.                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Legt die oberste Koordinate des Zielrechtecks fest.                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Legt die Breite des Zielrechtecks fest.                                                         |
| [**\_put SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Legt die Höhe des Quellrechtecks fest.                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Legt die linke Koordinate des Quellrechtecks fest.                                                    |
| [**put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Legt die oberste Koordinate des Quellrechtecks fest.                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Legt die Breite des Quellrechtecks fest.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Legt die Standardzielposition erneut fest.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Legt die Standardquellposition erneut fest.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Legt die Zielrechteckposition fest.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Legt die Position des Quellrechtecks fest.                                                             |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 



