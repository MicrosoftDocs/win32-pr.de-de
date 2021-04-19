---
description: Die cbasewindow-Klasse ist eine Basisklasse für die Verwaltung von Fenstern.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Cbasewindow-Klasse (winutil. h)
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
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370869"
---
# <a name="cbasewindow-class"></a>Cbasewindow-Klasse

Die- `CBaseWindow` Klasse ist eine Basisklasse für die Verwaltung von Windows. Videorenderer können diese Klasse zum Erstellen von Video Fenstern verwenden. Um diese Klasse zu verwenden, erstellen Sie eine abgeleitete Klasse, die von erbt `CBaseWindow` . In der abgeleiteten Klasse:

-   Implementieren Sie die reine virtuelle Methode [**cbasewindow:: getclasswindowstyles**](cbasewindow-getclasswindowstyles.md), mit der die Fenster Stile definiert werden.
-   Überschreiben Sie die [**cbasewindow:: onreceivemess**](cbasewindow-onreceivemessage.md) -Methode, die Fenster Meldungen verarbeitet.
-   Implementieren Sie einen debugtor, der die [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) -Methode aufruft.

Bevor Sie eine Instanz der abgeleiteten Klasse verwenden, können Sie die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode aufzurufen.



| Geschützte Member-Variablen                                           | BESCHREIBUNG                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ HINSTANCE**](cbasewindow-m-hinstance.md)                      | Handle für die Modul Instanz.                                                 |
| [**m- \_ HWND**](cbasewindow-m-hwnd.md)                                | Handle für das Fenster des Objekts.                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | Handle für den Gerätekontext des Fensters.                                         |
| [**m \_ Breite**](cbasewindow-m-width.md)                              | Breite des Client Bereichs in Pixel.                                           |
| [**m \_ Höhe**](cbasewindow-m-height.md)                            | Die Höhe des Client Bereichs in Pixel.                                          |
| [**m- \_ bactivated**](cbasewindow-m-bactivated.md)                    | Flag, das angibt, ob das Fenster aktiviert wurde.                     |
| [**m \_ pclassname**](cbasewindow-m-pclassname.md)                    | Statische Zeichenfolge, die den Namen der Fenster Klasse enthält.                      |
| [**m \_ classstyles**](cbasewindow-m-classstyles.md)                  | Klassen Stile für das Fenster.                                                   |
| [**m \_ windowstyles**](cbasewindow-m-windowstyles.md)                | Fenster Stile für das Fenster.                                                  |
| [**m \_ windowstylesex**](cbasewindow-m-windowstylesex.md)            | Erweiterte Fenster Stile für das Fenster.                                         |
| [**m \_ showstagemess Age**](cbasewindow-m-showstagemessage.md)        | Private Nachricht, die das Fenster in den Vordergrund bringt.                      |
| [**m \_ showstagetop**](cbasewindow-m-showstagetop.md)                | Eine private Nachricht, die den Fenster Stil auf WS \_ Ex \_ TopMost festlegt.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Private Nachricht, die die Palette erkennt.                                     |
| [**m \_ memorydc**](cbasewindow-m-memorydc.md)                        | Handle für den Kontext des Speichergeräts.                                           |
| [**m \_ hpalette**](cbasewindow-m-hpalette.md)                        | Handle für die Palette des Fensters.                                                |
| [**m \_ bnorealize**](cbasewindow-m-bnorealize.md)                    | Flag, das angibt, ob das Fenster seine Palette erkennen soll.             |
| [**m \_ bbackground**](cbasewindow-m-bbackground.md)                  | Flag, das angibt, ob die Palette eine Hintergrund Palette sein soll.        |
| [**m wird durch \_ brealisieren**](cbasewindow-m-brealizing.md)                    | Flag, das angibt, ob eine neue Palette realisiert wird.                   |
| [**m \_ windowlock**](cbasewindow-m-windowlock.md)                    | Kritischer Abschnitt, um den Zugriff auf das Objekt zu serialisieren.                           |
| [**m \_ bdogetdc**](cbasewindow-m-bdogetdc.md)                        | Flag, das angibt, ob der Gerätekontext abgerufen werden soll.                    |
| [**m \_ bdopostto Destroy**](cbasewindow-m-bdoposttodestroy.md)        | Flag, das angibt, ob das Fenster seine Zerstörungs Nachricht postet oder sendet. |
| Geschützte Methoden                                                    | BESCHREIBUNG                                                                    |
| [**Onpalettechange**](cbasewindow-onpalettechange.md)               | Verarbeitet palettenänderungs Meldungen. Virtu.                                      |
| Öffentliche Methoden                                                       | BESCHREIBUNG                                                                    |
| [**Cbasewindow**](cbasewindow-cbasewindow.md)                       | Konstruktormethode.                                                            |
| [**Donewithwindow**](cbasewindow-donewithwindow.md)                 | Zerstört das Fenster. Virtu.                                                  |
| [**Preparewindow**](cbasewindow-preparewindow.md)                   | Erstellt das Fenster. Virtu.                                                   |
| [**Inactivatewindow**](cbasewindow-inactivatewindow.md)             | Deaktiviert das Fenster. Virtu.                                               |
| [**Activatewindow**](cbasewindow-activatewindow.md)                 | Passt die Größe des Fensters gemäß den Anforderungen der abgeleiteten Klasse an. Virtu.  |
| [**OnSize speziell gehandhabt**](cbasewindow-onsize.md)                                 | Verarbeitet Nachrichten der WM- \_ Größe. Virtu.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Behandelt WM- \_ Schließen-Nachrichten. Virtu.                                           |
| [**Getdefaultrect**](cbasewindow-getdefaultrect.md)                 | Ruft die Standardgröße des Client Bereichs ab. Virtu.                        |
| [**Nicht initialisiererfenster**](cbasewindow-uninitialisewindow.md)         | Gibt die Fenster Ressourcen frei. Virtu.                                      |
| [**Initialisiererfenster**](cbasewindow-initialisewindow.md)             | Initialisiert das Fenster. Virtu.                                               |
| [**Completeconnect**](cbasewindow-completeconnect.md)               | Benachrichtigt das Fenster, dass die Eingabe-PIN des Renderers verbunden wurde.          |
| [**Dokreatewindow**](cbasewindow-docreatewindow.md)                 | Erstellt das Fenster.                                                            |
| [**Performancealignwindow**](cbasewindow-performancealignwindow.md) | Richtet das Fenster an eine **DWORD** -Grenze aus, um eine maximale Leistung zu erzielen.            |
| [**Doshowwindow**](cbasewindow-doshowwindow.md)                     | Legt den Anzeige Zustand des Fensters fest.                                                  |
| [**Pinsel Fenster**](cbasewindow-paintwindow.md)                       | Bewirkt, dass das Fenster neu gezeichnet wird.                                             |
| [**Dosetwindowvorder Grund**](cbasewindow-dosetwindowforeground.md)   | Bringt das Fenster in den Vordergrund.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Installiert eine Palette für das Fenster. Virtu.                                    |
| [**"" Festlegen**](cbasewindow-setrealize.md)                         | Gibt an, ob im Fenster Paletten realisiert werden.                                |
| [**Dorealilpalette**](cbasewindow-dorealisepalette.md)             | Erkennt die aktuelle Palette des Fensters. Virtu.                                |
| [**Possiblyeatmessage**](cbasewindow-possiblyeatmessage.md)         | Ermöglicht einer abgeleiteten Klasse das Weiterleiten von Nachrichten an ein anderes Fenster. Virtu.        |
| [**Getwindowwidth**](cbasewindow-getwindowwidth.md)                 | Ruft die aktuelle Breite des Fensters ab.                                     |
| [**Getwindowheight**](cbasewindow-getwindowheight.md)               | Ruft die aktuelle Höhe des Fensters ab.                                    |
| [**Getwindowhwnd**](cbasewindow-getwindowhwnd.md)                   | Ruft ein Handle für das Fenster ab.                                              |
| [**Getmemoryhdc**](cbasewindow-getmemoryhdc.md)                     | Ruft ein Handle für den Speichergeräte Kontext ab.                               |
| [**Getwindowhdc**](cbasewindow-getwindowhdc.md)                     | Ruft ein Handle für den Gerätekontext des Fensters ab.                             |
| [**Onreceivemess**](cbasewindow-onreceivemessage.md)             | Verarbeitet Fenster Meldungen. Virtu.                                              |
| [**Unsetpalette**](cbasewindow-unsetpalette.md)                     | Löscht die aktuelle Palette des Fensters und stellt die Standardsystem Palette wieder her.  |
| Reine virtuelle Methoden                                                 | BESCHREIBUNG                                                                    |
| [**Getclasswindowstyles**](cbasewindow-getclasswindowstyles.md)     | Ruft die Klassen Stile und Fenster Stile des Fensters ab.                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




