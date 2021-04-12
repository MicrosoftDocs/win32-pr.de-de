---
description: Die cbasecontrolvideo-Klasse implementiert die ibasicvideo-Schnittstelle und steuert die Videoeigenschaften eines generischen Videofensters. Im Allgemeinen ist ein cbasecontrolvideo-Objekt ein Videorenderer, der Video in einem Fenster auf der Anzeige zeichnet.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: Cbasecontrolvideo-Klasse
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
ms.openlocfilehash: e2e5962eb9d175bfbbeadd149a547f0d36fbf49f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482211"
---
# <a name="cbasecontrolvideo-class"></a>Cbasecontrolvideo-Klasse

![cbasecontrolvideo-Klassenhierarchie](images/wctrl02.png)

Die **cbasecontrolvideo** -Klasse implementiert die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle und steuert die Videoeigenschaften eines generischen Videofensters. Im Allgemeinen ist ein **cbasecontrolvideo** -Objekt ein Videorenderer, der Video in einem Fenster auf der Anzeige zeichnet.

Viele **cbasecontrolvideo** -Member-Funktionen erfordern nur, dass der Videorenderer mit einem Filter Diagramm verbunden ist. Wenn keine Verbindung besteht, geben die Element Funktionen **VFW \_ E \_ nicht \_ verbunden** zurück. Eigenschaften, die für einen Videorenderer festgelegt werden, werden zwischen aufeinander folgenden Verbindungen und Trennungen beibehalten. Alle Anwendungen sollten sicherstellen, dass die renderereigenschaften zurückgesetzt werden, bevor eine Präsentation gestartet wird.

Wenn Sie mit Videoarbeiten, kann die Anwendung einen Teil des Videos auswählen, der verwendet werden soll. Dieser Teil ist das Quell Rechteck, das vom **cbasecontrolvideo** -Objekt gesteuert wird. **Cbasecontrolvideo** ermöglicht der Anwendung das Festlegen und Abrufen des Quell Rechtecks. Alle Rechtecke, die von **cbasecontrolvideo** verwendet werden, verwenden die Werte Width und Height anstelle von Rechten und unteren Werten. Wenn kein Quell Rechteck festgelegt wurde, geben die Eigenschaften des Quell Rechtecks die vollständige, Native Videogröße zurück.



| Geschützte Datenmember                                                                   | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Zeiger auf einen besitzenden Medienfilter.                                                              |
| m \_ pinterfakelock                                                                        | Extern definierter kritischer Abschnitt.                                                            |
| m \_ ppin                                                                                  | Steuerung der Medientypen für die Verbindung.                                                      |
| Elementfunktionen                                                                         | BESCHREIBUNG                                                                                     |
| [**Cbasecontrolvideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Erstellt ein **cbasecontrolvideo** -Objekt.                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Erstellt eine Speicher Kopie eines Video Bilds.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Ruft Informationen zur Video Bild Größe ab.                                                         |
| [**Setcontrolvideopin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Legt die PIN fest, mit der dieses Objekt synchronisiert werden soll.                                         |
| Über schreibbare Member-Funktionen                                                             | BESCHREIBUNG                                                                                     |
| [**Checksourcerect**](cbasecontrolvideo-checksourcerect.md)                             | Bestimmt, ob ein Quell Rechteck gültig ist.                                                      |
| [**Checktargetrect**](cbasecontrolvideo-checktargetrect.md)                             | Bestimmt, ob ein Ziel Rechteck gültig ist.                                                      |
| [**Getsourcerect**](cbasecontrolvideo-getsourcerect.md)                                 | Ruft das aktuelle Quellvideo Rechteck (rein virtuell) ab.                                    |
| [**Getstaticimage**](cbasecontrolvideo-getstaticimage.md)                               | Gibt das aktuelle Bild in einem Speicherpuffer (rein virtuell) zurück.                                    |
| [**Gettargetrect**](cbasecontrolvideo-gettargetrect.md)                                 | Ruft das aktuelle Ziel Video Rechteck (rein virtuell) ab.                                    |
| [**Getvideoformat**](cbasecontrolvideo-getvideoformat.md)                               | Ruft die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur ab, die das Videoformat enthält. |
| [**Isdefaultsourcerect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Bestimmt, ob der Renderer das standardmäßige Quell Rechteck verwendet (rein virtuell).                |
| [**Isdefaulttargetrect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Bestimmt, ob der Renderer das standardmäßige Ziel Rechteck verwendet (rein virtuell).                |
| [**Onupdaterectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Wird aufgerufen, wenn das Quell-oder Ziel Rechteck geändert wird.                                             |
| [**Onvideosizechange**](cbasecontrolvideo-onvideosizechange.md)                         | Übergibt \_ \_ die Größe des EC-Videos \_ an die Anwendung.                                             |
| [**Setdefaultsourcerect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Legt das standardmäßige Quellvideo Rechteck (rein virtuell) fest.                                         |
| [**Setdefaulttargetrect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Legt das standardmäßige Ziel Video Rechteck (rein virtuell) fest.                                         |
| [**Setsourcerect**](cbasecontrolvideo-setsourcerect.md)                                 | Legt das aktuelle Quellvideo Rechteck (rein virtuell) fest.                                         |
| [**Settargetrect**](cbasecontrolvideo-settargetrect.md)                                 | Legt das aktuelle Ziel Rechteck (rein virtuell) fest.                                               |
| Ibasicvideo-Methoden                                                                      | BESCHREIBUNG                                                                                     |
| [**\_avgtimeperframe abrufen**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Ruft eine ungefähre durchschnittliche Zeit pro Frame ab.                                                |
| [**\_biterrorrate erhalten**](cbasecontrolvideo-get-biterrorrate.md)                          | Ruft eine ungefähre Bitfehlerrate ab.                                                        |
| [**get- \_ Bitrate**](cbasecontrolvideo-get-bitrate.md)                                    | Ruft eine ungefähre Bitrate für das Video ab.                                                |
| [**Gettimestimage**](cbasecontrolvideo-getcurrentimage.md)                             | Ruft ein Speicher Rendering des aktuellen Bilds ab.                                              |
| [**\_destinationheight erhalten**](cbasecontrolvideo-get-destinationheight.md)                | Ruft die Höhe des aktuellen Ziel Rechtecks ab.                                           |
| [**\_destinationleft erhalten**](cbasecontrolvideo-get-destinationleft.md)                    | Ruft die linke Koordinate des aktuellen Ziel Rechtecks ab.                                  |
| [**Getdestinationposition**](cbasecontrolvideo-getdestinationposition.md)               | Ruft die aktuelle Zielposition ab.                                                     |
| [**\_destinationtop erhalten**](cbasecontrolvideo-get-destinationtop.md)                      | Ruft die obere Koordinate des aktuellen Ziel Rechtecks ab.                                   |
| [**\_destinationwidth erhalten**](cbasecontrolvideo-get-destinationwidth.md)                  | Ruft die Breite des aktuellen Ziel Rechtecks ab.                                            |
| [**\_sourceHeight erhalten**](cbasecontrolvideo-get-sourceheight.md)                          | Ruft die Höhe des aktuellen Quell Rechtecks ab.                                                |
| [**\_sourceLeft erhalten**](cbasecontrolvideo-get-sourceleft.md)                              | Ruft die linke Koordinate des aktuellen Quell Rechtecks ab.                                       |
| [**Getsourceposition**](cbasecontrolvideo-getsourceposition.md)                         | Ruft die aktuelle Quell Position ab.                                                          |
| [**\_sourceTop erhalten**](cbasecontrolvideo-get-sourcetop.md)                                | Ruft die obere Koordinate des aktuellen Quell Rechtecks ab.                                        |
| [**\_sourceWidth erhalten**](cbasecontrolvideo-get-sourcewidth.md)                            | Ruft die Breite des aktuellen Quell Rechtecks ab.                                                 |
| [**Holen Sie sich \_ videoheight**](cbasecontrolvideo-get-videoheight.md)                            | Ruft die Größe des nativen Videos ab.                                                              |
| [**Getvideopaletteentries**](cbasecontrolvideo-getvideopaletteentries.md)               | Ruft einen Bereich von paletteneinträgen für das Video ab.                                             |
| [**Getvideosize**](cbasecontrolvideo-getvideosize.md)                                   | Ruft die Breite und Höhe des systemeigenen Videos ab.                                             |
| [**\_Video Breite erhalten**](cbasecontrolvideo-get-videowidth.md)                              | Ruft die systemeigene Video Breite ab.                                                               |
| [**Isusingdefaultdestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Bestimmt, ob der Renderer das Standardziel Fenster verwendet.                             |
| [**Isusingdefaultsource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Bestimmt, ob der Renderer das standardmäßige Quell Code Fenster verwendet.                                  |
| [**\_destinationheight platzieren**](cbasecontrolvideo-put-destinationheight.md)                | Legt die Höhe des Ziel Rechtecks fest.                                                        |
| [**\_destinationleft platzieren**](cbasecontrolvideo-put-destinationleft.md)                    | Legt die linke Koordinate des Ziel Rechtecks fest.                                               |
| [**\_destinationtop platzieren**](cbasecontrolvideo-put-destinationtop.md)                      | Legt die obere Koordinate des Ziel Rechtecks fest.                                                |
| [**\_destinationwidth platzieren**](cbasecontrolvideo-put-destinationwidth.md)                  | Legt die Breite des Ziel Rechtecks fest.                                                         |
| [**\_sourceHeight platzieren**](cbasecontrolvideo-put-sourceheight.md)                          | Legt die Höhe des Quell Rechtecks fest.                                                             |
| [**\_sourceLeft einfügen**](cbasecontrolvideo-put-sourceleft.md)                              | Legt die linke Koordinate des Quell Rechtecks fest.                                                    |
| [**\_sourceTop platzieren**](cbasecontrolvideo-put-sourcetop.md)                                | Legt die obere Koordinate des Quell Rechtecks fest.                                                     |
| [**\_sourceWidth platzieren**](cbasecontrolvideo-put-sourcewidth.md)                            | Legt die Breite des Quell Rechtecks fest.                                                              |
| [**Setdefaultdestinationposition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Legt die Standardziel Position erneut fest.                                                    |
| [**Setdefaultsourceposition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Legt die Standard Quell Position erneut fest.                                                         |
| [**Setdestinationposition**](cbasecontrolvideo-setdestinationposition.md)               | Legt die Position des Ziel Rechtecks fest.                                                        |
| [**Setsourceposition**](cbasecontrolvideo-setsourceposition.md)                         | Legt die Position des Quell Rechtecks fest.                                                             |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 



