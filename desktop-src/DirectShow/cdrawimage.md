---
description: Die cdrawimage-Klasse ist eine Hilfsklasse, die das Zeichnen für einen Videorenderer-Filter verwaltet.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: Cdrawimage-Klasse (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 001b91338b2956f663d777cbc9597fa2d9a478f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371558"
---
# <a name="cdrawimage-class"></a>Cdrawimage-Klasse

Die- `CDrawImage` Klasse ist eine Hilfsklasse, die das Zeichnen für einen Videorenderer-Filter verwaltet. Alle Zeichnungsvorgänge werden mit GDI ausgeführt. Diese Klasse bietet keine Unterstützung für das Rendering mit DirectDraw. Die- `CDrawImage` Klasse erfordert, dass der besitzende Filter auch die [**cbasewindow**](cbasewindow.md) -Klasse verwendet, die das Videofenster verwaltet. Der `CDrawImage` Konstruktor nimmt einen Zeiger auf das **cbasewindow** -Objekt an.

Das folgende Diagramm zeigt die bevorzugte Methode für die Verwendung dieser Klasse in einem benutzerdefinierten Videorendererfilter.

![benutzerdefinierter Videorenderer mit cdrawimage](images/videorenderer.png)

Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:

-   Wenn die Pins eine Verbindung herstellen, müssen Sie die [**cdrawimage:: notifymediatype**](cdrawimage-notifymediatype.md) -Methode und die [**cdrawimage:: notifyzucator**](cdrawimage-notifyallocator.md) -Methode abrufen.
-   Immer dann, wenn sich der Medientyp ändert, wird **notifymediatype** erneut aufgerufen.
-   Vor dem Auftreten eines Rendering muss [**cdrawimage:: setdrawcontext**](cdrawimage-setdrawcontext.md)aufgerufen werden.
-   Aufrufen von [**cdrawimage:: setsourcerect**](cdrawimage-setsourcerect.md) bei Änderung des Quell Rechtecks und [**cdrawimage:: settargetrect**](cdrawimage-settargetrect.md) bei Änderung des Ziel Rechtecks.
-   Verwalten Sie die Palette für Paletten-Bilder, wie im Abschnitt zu den folgenden Abschnitten beschrieben.

## <a name="allocators"></a>Allocators

Der im vorherigen Diagramm gezeigte Filter verwendet eine benutzerdefinierte zuordnerklasse, [**cimagezuordcator**](cimageallocator.md). Diese Zuweisung erstellt mithilfe der GDI-Funktion " **inatedibsection** " Disb im gemeinsam genutzten Speicher. Die von der Zuweisung erstellten Beispiele sind [**cimagesample**](cimagesample.md) -Objekte.

Wenn der Filter die Zuweisung der Verbindung besitzt, werden die Medien Beispiele garantiert [**cimagesample**](cimagesample.md) -Objekte sein. In diesem Fall kann das **cdrawimage** -Objekt das Zeichnen mithilfe von **BitBLT** oder StretchBlt optimieren. Andernfalls muss die Funktion die langsamere Funktion **SetDIBitsToDevice** oder **StretchDIBits** verwenden. Die schnellere Option wird von der [**cdrawimage:: fastrauender**](cdrawimage-fastrender.md) -Methode implementiert, die langsamere Option durch die [**cdrawimage:: slowrendering**](cdrawimage-slowrender.md) -Methode. (Trotz des Namens wird Ihnen wahrscheinlich keine große Leistung in **slowrendering** angezeigt, insbesondere bei neueren Hardware.)

## <a name="palettes"></a>Paletten

Wenn die [**fastrinender**](cdrawimage-fastrender.md) -Methode zum Zeichnen verwendet wird und das Bild palettisiert ist, muss der Filter die Palette wie folgt verwalten:

-   Die [**cimagesample**](cimagesample.md) -Klasse enthält eine palettenversionsnummer, die in der [**dibdata**](dibdata.md) -Struktur gespeichert ist. Der Wert wird initialisiert, wenn die Zuweisung das Beispiel erstellt.
-   Die **cdrawimage** -Klasse enthält auch eine palettenversionsnummer, die bei der Erstellung initialisiert wird.
-   Wenn sich der Medientyp in ein neues Format ändert, wird [**cdrawimage:: incrementpaletteversion**](cdrawimage-incrementpaletteversion.md)aufgerufen. Diese Methode erhöht die palettenversionsnummer des **cdrawimage** -Objekts. Wenn der Filter die " [**cimagepalette**](cimagepalette.md) "-Klasse zum Verwalten der Paletteninformationen verwendet, können Sie einfach " [**cimagepalette::P reparepalette**](cimagepalette-preparepalette.md) " aufrufen, wenn sich der Medientyp ändert. Die **PreparePalette** -Methode erhöht die palettenversion nur, wenn dies erforderlich ist.
-   Die [**fastrauender**](cdrawimage-fastrender.md) -Methode vergleicht die **cdrawimage** -palettenversion mit der palettenversion des Beispiels. Wenn die Versionsnummer des Beispiels hinter der **cdrawimage** -Versionsnummer liegt, ruft die **fastrauender** -Methode [**cdrawimage:: updatecolourtable**](cdrawimage-updatecolourtable.md)auf. Die **updatecolourtable** -Methode legt die Farbtabelle im Gerätekontext mithilfe der GDI-Funktion **setdibcolortable** fest. Außerdem wird die palettenversion im Beispiel auf die aktuelle Versionsnummer aktualisiert.
-   Wenn die PIN erneut eine Verbindung herstellt, sollte der Filter [**cdrawimage:: resetpaletteversion**](cdrawimage-resetpaletteversion.md) aufrufen, um die palettenversion zurückzusetzen. Beim erneuten Herstellen der PIN werden alle Beispiele von der Zuweisung erneut zugeordnet.



| Geschützte Member-Variablen                                            | BESCHREIBUNG                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bstretch**](cdrawimage-m-bstretch.md)                          | Gibt an, ob das Video Bild gestreckt werden muss, damit es an das Zielfenster angepasst wird.                                              |
| [**m \_ busingimagezuweisung**](cdrawimage-m-busingimageallocator.md)  | Gibt an, ob die Zuweisung der Pin-Verbindung ein **cimagezuordcator** -Objekt ist.                                         |
| [**m \_ endsample**](cdrawimage-m-endsample.md)                        | Gibt die Endzeit des neuesten Beispiels an.                                                                              |
| [**m \_ hdc**](cdrawimage-m-hdc.md)                                    | Handle für den Gerätekontext des besitzenden Fensters.                                                                              |
| [**m \_ memorydc**](cdrawimage-m-memorydc.md)                          | Handle für den Speichergeräte Kontext des besitzenden Fensters.                                                                       |
| [**m \_ paletteversion**](cdrawimage-m-paletteversion.md)              | Wird verwendet, um zu verfolgen, wann die Palette geändert wird                                                                                         |
| [**m \_ pbasewindow**](cdrawimage-m-pbasewindow.md)                    | Zeiger auf das besitzende **cbasewindow** -Objekt.                                                                                   |
| [**m \_ pmediatype**](cdrawimage-m-pmediatype.md)                      | Zeiger auf den aktuellen Medientyp.                                                                                              |
| [**Mio. \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | Gibt das Quell Rechteck für das Zeichnen an.                                                                                     |
| [**m \_ startsample**](cdrawimage-m-startsample.md)                    | Gibt die Startzeit des neuesten Beispiels an.                                                                             |
| [**m \_ targetrect**](cdrawimage-m-targetrect.md)                      | Gibt das Ziel Rechteck für das Zeichnen an.                                                                                     |
| Geschützte Methoden                                                     | BESCHREIBUNG                                                                                                                     |
| [**Display Sample Times**](cdrawimage-displaysampletimes.md)           | Zeichnet die Zeitstempel eines Medien Beispiels oberhalb des Video Bilds.                                                              |
| [**Fastrauender**](cdrawimage-fastrender.md)                           | Zeichnet das Video Bild mithilfe der Funktionen **BitBLT** oder **StretchBlt** .                                                         |
| [**Setstretchmode**](cdrawimage-setstretchmode.md)                   | Berechnet, ob das Video Bild gestreckt werden muss.                                                                           |
| [**Slowrendering**](cdrawimage-slowrender.md)                           | Zeichnet das Video Bild mithilfe der Funktionen **SetDIBitsToDevice** oder **StretchDIBits** .                                           |
| [**Updatecolourtable**](cdrawimage-updatecolourtable.md)             | Aktualisiert die Farbtabelle mit einer neuen Palette.                                                                                     |
| Öffentliche Methoden                                                        | BESCHREIBUNG                                                                                                                     |
| [**Cdrawimage**](cdrawimage-cdrawimage.md)                           | Konstruktormethode.                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | Zeichnet einen Videoframe im Videofenster.                                                                                        |
| [**Drawvideoimagehere**](cdrawimage-drawvideoimagehere.md)           | Zeichnet ein Bild aus einem Medien Beispiel in einen angegebenen Gerätekontext.                                                               |
| [**Getpaletteversion**](cdrawimage-getpaletteversion.md)             | Ruft die palettenversion ab.                                                                                                  |
| [**Getsourcerect**](cdrawimage-getsourcerect.md)                     | Ruft das aktuelle Quell Rechteck ab.                                                                                         |
| [**Gettargetrect**](cdrawimage-gettargetrect.md)                     | Ruft das aktuelle Ziel Rechteck ab.                                                                                    |
| [**Incrementpaletteversion**](cdrawimage-incrementpaletteversion.md) | Inkremente der palettenversion.                                                                                                 |
| [**Notifyzukator**](cdrawimage-notifyallocator.md)                 | Informiert das-Objekt darüber, `CDrawImage` ob die Zuweisung für die Verbindung ein **cimagezuordcator** -Objekt ist.                       |
| [**Notifyenddraw**](cdrawimage-notifyenddraw.md)                     | Wird nicht unterstützt.                                                                                                                  |
| [**Notifymediatype**](cdrawimage-notifymediatype.md)                 | Benachrichtigt das-Objekt über den aktuellen Medientyp.                                                                                  |
| [**Notifystartdraw**](cdrawimage-notifystartdraw.md)                 | Wird nicht unterstützt.                                                                                                                  |
| [**Resetpaletteversion**](cdrawimage-resetpaletteversion.md)         | Setzt die palettenversion zurück.                                                                                                     |
| [**Scalesourcerect**](cdrawimage-scalesourcerect.md)                 | Skaliert ein angegebenes Quell Rechteck, wenn ein Unterschied zwischen der nativen Videogröße und dem Medientyp Format vorliegt. Virtu. |
| [**Setdrawcontext**](cdrawimage-setdrawcontext.md)                   | Legt die für das Zeichnen verwendeten Geräte Kontexte fest.                                                                                      |
| [**Setsourcerect**](cdrawimage-setsourcerect.md)                     | Legt das Quell Rechteck fest.                                                                                                      |
| [**Settargetrect**](cdrawimage-settargetrect.md)                     | Legt das Ziel Rechteck fest.                                                                                                      |
| [**Usingimagezuordcator**](cdrawimage-usingimageallocator.md)         | Gibt an, ob die aktuelle Zuweisung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




