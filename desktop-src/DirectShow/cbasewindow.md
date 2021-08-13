---
description: Die CBaseWindow-Klasse ist eine Basisklasse zum Verwalten von Fenstern.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: CBaseWindow-Klasse (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d2a3004343df7846d4bf600690bc6a1e45b46111f91828c7de31219a751308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657193"
---
# <a name="cbasewindow-class"></a>CBaseWindow-Klasse

Die `CBaseWindow` -Klasse ist eine Basisklasse zum Verwalten von Fenstern. Videorenderer können diese Klasse verwenden, um Videofenster zu erstellen. Um diese Klasse zu verwenden, erstellen Sie eine abgeleitete Klasse, die von `CBaseWindow` erbt. In der abgeleiteten Klasse:

-   Implementieren Sie die reine virtuelle [**Methode CBaseWindow::GetClassWindowStyles,**](cbasewindow-getclasswindowstyles.md)die die Fensterstile definiert.
-   Überschreiben Sie [**die CBaseWindow::OnReceiveMessage-Methode,**](cbasewindow-onreceivemessage.md) die Fenstermeldungen verarbeitet.
-   Implementieren Sie einen Destruktor, der die [**CBaseWindow::D oneWithWindow-Methode**](cbasewindow-donewithwindow.md) aufruft.

Rufen Sie vor der Verwendung einer Instanz der abgeleiteten Klasse die [**CBaseWindow::P repareWindow-Methode**](cbasewindow-preparewindow.md) auf.



| Geschützte Membervariablen                                           | BESCHREIBUNG                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ hInstance**](cbasewindow-m-hinstance.md)                      | Handle für die Modulinstanz.                                                 |
| [**m \_ hwnd**](cbasewindow-m-hwnd.md)                                | Handle für das Fenster des Objekts.                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | Handle für den Gerätekontext des Fensters.                                         |
| [**m \_ Width**](cbasewindow-m-width.md)                              | Breite des Clientbereichs in Pixel.                                           |
| [**m \_ Höhe**](cbasewindow-m-height.md)                            | Höhe des Clientbereichs in Pixel.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Flag, das angibt, ob das Fenster aktiviert wurde.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Statische Zeichenfolge, die den Namen der Fensterklasse enthält.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Klassenstile für das Fenster.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Fensterstile für das Fenster.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Erweiterte Fensterstile für das Fenster.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Private Nachricht, die das Fenster in den Vordergrund bringt.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Private Nachricht, die den Fensterstil auf WS \_ EX TOPMOST (WS EX \_ TOPMOST) setzt.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Private Nachricht, die die Palette realisiert.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Handle für den Speichergerätekontext.                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | Handle für die Palette des Fensters.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Flag, das angibt, ob das Fenster seine Palette realisieren soll.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Flag, das angibt, ob die Palette eine Hintergrundpalette sein soll.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Flag, das angibt, ob eine neue Palette realisiert wird.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Kritischer Abschnitt, um den Zugriff auf das Objekt zu serialisieren.                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Flag, das angibt, ob der Gerätekontext abgerufen werden soll.                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Flag, das angibt, ob das Fenster seine Zerstörungsmeldung sendet oder sendet. |
| Geschützte Methoden                                                    | BESCHREIBUNG                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Verarbeitet Palettenänderungsmeldungen. Virtuellen.                                      |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Konstruktormethode.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Zerstört das Fenster. Virtuellen.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Erstellt das Fenster. Virtuellen.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Deaktiviert das Fenster. Virtuellen.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Größe des Fensters gemäß den Anforderungen der abgeleiteten Klasse. Virtuellen.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Verarbeitet WM \_ SIZE-Nachrichten. Virtuellen.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Verarbeitet WM \_ CLOSE-Meldungen. Virtuellen.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Ruft die Standardgröße des Clientbereichs ab. Virtuellen.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Gibt die Ressourcen des Fensters frei. Virtuellen.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Initialisiert das Fenster. Virtuellen.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Benachrichtigt das Fenster, dass der Eingabepin des Renderers verbunden wurde.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Erstellt das Fenster.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Richtet das Fenster an einer **DWORD-Grenze** aus, um maximale Leistung zu erzielen.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Legt den Showzustand des Fensters fest.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Bewirkt, dass das Fenster neu gepaint wird.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Bringt das Fenster in den Vordergrund.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Installiert eine Palette für das Fenster. Virtuellen.                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | Gibt an, ob das Fenster Paletten erkennt.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Erkennt die aktuelle Palette des Fensters. Virtuellen.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Ermöglicht es einer abgeleiteten Klasse, Nachrichten an ein anderes Fenster weiter zu senden. Virtuellen.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Ruft die aktuelle Breite des Fensters ab.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Ruft die aktuelle Höhe des Fensters ab.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Ruft ein Handle für das Fenster ab.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Ruft ein Handle für den Speichergerätekontext ab.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Ruft ein Handle für den Gerätekontext des Fensters ab.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Verarbeitet Fenstermeldungen. Virtuellen.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Löscht die aktuelle Palette des Fensters und stellt die Standardsystempalette wieder auf.  |
| Rein virtuelle Methoden                                                 | BESCHREIBUNG                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Ruft die Klassen- und Fensterstile des Fensters ab.                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




