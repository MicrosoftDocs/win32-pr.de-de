---
description: Die CDrawImage-Klasse ist eine Hilfsklasse, die das Zeichnen für einen Videorendererfilter verwaltet.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: CDrawImage-Klasse (Winutil.h)
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
ms.openlocfilehash: 951744cded927707ac0b39e562b4207acbecdd92420c91a2b130f0b493444b01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999554"
---
# <a name="cdrawimage-class"></a>CDrawImage-Klasse

Die `CDrawImage` -Klasse ist eine Hilfsklasse, die das Zeichnen für einen Videorendererfilter verwaltet. Alle Zeichnungsvorgänge werden mit GDI ausgeführt. Diese Klasse bietet keine Unterstützung für das Rendering mit DirectDraw. Die `CDrawImage` -Klasse erfordert, dass der besitzende Filter auch die [**CBaseWindow-Klasse**](cbasewindow.md) verwendet, die das Videofenster verwaltet. Der `CDrawImage` Konstruktor verwendet einen Zeiger auf das **CBaseWindow-Objekt.**

Das folgende Diagramm zeigt die bevorzugte Methode zur Verwendung dieser Klasse in einem benutzerdefinierten Videorendererfilter.

![Benutzerdefinierter Videorenderer mit cdrawimage](images/videorenderer.png)

Gehen Sie wie folgt vor, um diese Klasse zu verwenden:

-   Wenn die Pins eine Verbindung herstellen, rufen Sie die [**Methoden CDrawImage::NotifyMediaType**](cdrawimage-notifymediatype.md) und [**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md) auf.
-   Wenn sich der Medientyp ändert, rufen Sie **NotifyMediaType erneut** auf.
-   Rufen Sie vor dem Rendern [**CDrawImage::SetDrawContext auf.**](cdrawimage-setdrawcontext.md)
-   Rufen [**Sie CDrawImage::SetSourceRect**](cdrawimage-setsourcerect.md) auf, wenn sich das Quellrechteck ändert, und [**CDrawImage::SetTargetRect,**](cdrawimage-settargetrect.md) wenn sich das Zielrechteck ändert.
-   Verwalten Sie die Palette für palettierte Bilder, wie im folgenden Abschnitt zu Paletten beschrieben.

## <a name="allocators"></a>Allocators

Der im vorherigen Diagramm gezeigte Filter verwendet die benutzerdefinierte Zuweisungsklasse [**CImageAllocator.**](cimageallocator.md) Diese Zuweisung erstellt DIBs im freigegebenen Speicher mithilfe der **GDI-Funktion CreateDIBSection.** Die von der Zuweisung erstellten Beispiele sind [**CImageSample-Objekte.**](cimagesample.md)

Wenn der Filter die Zuweisung für die Verbindung besitzt, handelt es sich bei den Medienbeispielen garantiert um [**CImageSample-Objekte.**](cimagesample.md) In diesem Fall kann das **CDrawImage-Objekt** das Zeichnen mit **BitBlt oder** StretchBlt optimieren. Andernfalls muss die langsamere **SetDIBitsToDevice- oder** **StretchDIBits-Funktion verwendet** werden. Die schnellere Option wird durch die [**CDrawImage::FastRender-Methode**](cdrawimage-fastrender.md) implementiert, die langsamere Option durch die [**CDrawImage::SlowRender-Methode.**](cdrawimage-slowrender.md) (Trotz des Namens wird in **SlowRender** wahrscheinlich kein großer Leistungstreffer auftritt, insbesondere bei neuerer Hardware.)

## <a name="palettes"></a>Paletten

Wenn die [**FastRender-Methode**](cdrawimage-fastrender.md) zum Zeichnen verwendet wird und das Bild palettiert ist, muss der Filter die Palette wie folgt verwalten:

-   Die [**CImageSample-Klasse**](cimagesample.md) enthält eine Palettenversionsnummer, die in der [**DIBDATA-Struktur gespeichert**](dibdata.md) ist. Der Wert wird initialisiert, wenn die Zuweisung das Beispiel erstellt.
-   Die **CDrawImage-Klasse** enthält auch eine Palettenversionsnummer, die bei der Erstellung initialisiert wird.
-   Wenn sich der Medientyp in ein neues palettiertes Format ändert, rufen Sie [**CDrawImage::IncrementPaletteVersion auf.**](cdrawimage-incrementpaletteversion.md) Diese Methode erhöht die Versionsnummer der Palette des **CDrawImage-Objekts.** Wenn der Filter die [**CImagePalette-Klasse**](cimagepalette.md) zum Verwalten der Paletteninformationen verwendet, können Sie einfach [**CImagePalette::P reparePalette**](cimagepalette-preparepalette.md) aufrufen, wenn sich der Medientyp ändert. Die **PreparePalette-Methode** erhöht die Palettenversion nur bei Bedarf.
-   Die [**FastRender-Methode**](cdrawimage-fastrender.md) vergleicht die **Version der CDrawImage-Palette** mit der Palettenversion des Beispiels. Wenn die Versionsnummer des Beispiels hinter der **CDrawImage-Versionsnummer** liegt, ruft die **FastRender-Methode** [**CDrawImage::UpdateColourTable auf.**](cdrawimage-updatecolourtable.md) Die **UpdateColourTable-Methode** legt die Farbtabelle im Gerätekontext mithilfe der **GDI-Funktion SetDIBColorTable** fest. Außerdem wird die Palettenversion im Beispiel auf die aktuelle Versionsnummer aktualisiert.
-   Wenn die Verbindung mit dem Pin wiederhergestellt wird, sollte der Filter [**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) aufrufen, um die Palettenversion zurückzusetzen. Bei der erneuten Verbindung mit pin ordnet die Zuweisung alle Stichproben neu zu.



| Geschützte Membervariablen                                            | BESCHREIBUNG                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bStretch**](cdrawimage-m-bstretch.md)                          | Gibt an, ob das Videobild gestreckt werden muss, damit es in das Zielfenster passt.                                              |
| [**m \_ bUsingImageAllocator**](cdrawimage-m-busingimageallocator.md)  | Gibt an, ob die Zuweisung für die Pinverbindung ein **CImageAllocator-Objekt** ist.                                         |
| [**m \_ EndSample**](cdrawimage-m-endsample.md)                        | Gibt die Stoppzeit des letzten Beispiels an.                                                                              |
| [**m \_ hdc**](cdrawimage-m-hdc.md)                                    | Handle für den Gerätekontext des besitzenden Fensters.                                                                              |
| [**m \_ MemoryDC**](cdrawimage-m-memorydc.md)                          | Handle für den Speichergerätekontext des besitzenden Fensters.                                                                       |
| [**m \_ PaletteVersion**](cdrawimage-m-paletteversion.md)              | Wird verwendet, um zu verfolgen, wann sich die Palette ändert.                                                                                         |
| [**m \_ pBaseWindow**](cdrawimage-m-pbasewindow.md)                    | Zeiger auf das besitzende **CBaseWindow-Objekt.**                                                                                   |
| [**m \_ pMediaType**](cdrawimage-m-pmediatype.md)                      | Zeiger auf den aktuellen Medientyp.                                                                                              |
| [**m \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | Gibt das Quellrechteck für das Zeichnen an.                                                                                     |
| [**m \_ StartSample**](cdrawimage-m-startsample.md)                    | Gibt die Startzeit des letzten Beispiels an.                                                                             |
| [**m \_ TargetRect**](cdrawimage-m-targetrect.md)                      | Gibt das Zielrechteck für das Zeichnen an.                                                                                     |
| Geschützte Methoden                                                     | BESCHREIBUNG                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Zeichnet die Zeitstempel eines Medienbeispiels auf dem Videobild.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Zeichnet das Videobild mithilfe der **Funktionen BitBlt** oder **StretchBlt.**                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | Berechnet, ob das Videobild gestreckt werden muss.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Zeichnet das Videobild mithilfe der **Funktionen SetDIBitsToDevice** oder **StretchDIBits.**                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Aktualisiert die Farbtabelle mit einer neuen Palette.                                                                                     |
| Öffentliche Methoden                                                        | BESCHREIBUNG                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Konstruktormethode.                                                                                                             |
| [**Drawimage**](cdrawimage-drawimage.md)                             | Zeichnet einen Videoframe im Videofenster.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Zeichnet ein Bild aus einem Medienbeispiel in einen angegebenen Gerätekontext.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Ruft die Palettenversion ab.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Ruft das aktuelle Quellrechteck ab.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Ruft das aktuelle Zielrechteck ab.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Erhöht die Palettenversion.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informiert das `CDrawImage` -Objekt, ob die Zuweisung für die Verbindung ein **CImageAllocator-Objekt** ist.                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | Wird nicht unterstützt.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Benachrichtigt das -Objekt über den aktuellen Medientyp.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | Wird nicht unterstützt.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Setzt die Palettenversion zurück.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Skaliert ein angegebenes Quellrechteck, wenn ein Unterschied zwischen der nativen Videogröße und dem Medientypformat besteht. Virtuellen. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Legt die gerätekontexte fest, die zum Zeichnen verwendet werden.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Legt das Quellrechteck fest.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Legt das Zielrechteck fest.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Gibt an, ob die aktuelle Zuweisung ein [**CImageAllocator-Objekt**](cimageallocator.md) ist.                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




