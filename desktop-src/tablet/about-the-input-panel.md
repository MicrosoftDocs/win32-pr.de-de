---
description: Ab Version 1.0 des Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) bietet der Tablet PC-Eingabebereich auf Systemebene einen universellen Mechanismus zum Ausführen von Texteingaben auf der Windows-Plattform, obwohl er keinen programmgesteuerten Zugriff bietet. Das PenInputPanel-Objekt des Tablet PC SDK, Version 1.5, integriert Texteingabetools in Anwendungen.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Informationen zum Eingabebereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844410"
---
# <a name="about-the-input-panel"></a>Informationen zum Eingabebereich

\[[**PenInputPanel**](peninputpanel-class.md) wurde durch [**TextInput ersetzt.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) Weitere Informationen finden Sie unter [Programmieren des Texteingabebereichs.](programming-the-text-input-panel.md)\]

Ab Version 1.0 des Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) bietet der Tablet PC-Eingabebereich auf Systemebene einen universellen Mechanismus zum Ausführen von Texteingaben auf der Windows-Plattform, obwohl er keinen programmgesteuerten Zugriff bietet. Das [**PenInputPanel-Objekt**](peninputpanel-class.md) des Tablet PC SDK, Version 1.5, integriert Texteingabetools in Anwendungen.

Die folgende Grafik zeigt den Stifteingabebereich, der über dem Beispiel für das [Formular für automatische Ansprüche angezeigt](auto-claims-form-sample.md) wird.

![Stifteingabebereich, der im Beispielbeispiel für das Formular für automatische Ansprüche angezeigt wird](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) ist praktisch für Anwendungsentwickler. Es ist nicht notwendig, Steuerelemente in vorhandenen Formularen zu ersetzen. Sie können **PenInputPanel-Objekte** einfach an vorhandene Steuerelemente anfügen, die Texteingaben empfangen, und sie können beginnen, Eingaben vom **PenInputPanel-Objekt zu** empfangen.

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) übernimmt die Einstellungen aus dem Eingabebereich für die folgenden Eigenschaften:

-   Layout
-   Breite der Ink-Daten
-   Erkennungs-Timeout
-   Feldgröße, Sendemodus und andere Einstellungen für ostasiatische Boxeingaben

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) bietet keinen Zugriff auf die zugrunde liegende Ink-Datei. Verwenden Sie das Steuerelement [InkPicture, um die InkPicture-Datei](inkpicture-control-reference.md) zu erhalten.

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) stellt eine benutzeroberfläche bereit, die von Endbenutzern Ihrer Anwendungen leicht gefunden werden kann. Sie wird automatisch aktiviert, wenn der Benutzer mithilfe des Tablettstifts auf ein Fenster mit einem **PenInputPanel-Objekt** tippt. Der Stifteingabebereich wird automatisch angezeigt, wenn das System ein CursorButtonUp-Ereignis für das Fenster erkennt, an das das **PenInputPanel-Objekt** angefügt ist. Die automatische Aktivierung kann deaktiviert werden, indem die [**AutoShow-Eigenschaft**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) auf **FALSE festgelegt wird.**

Der Stifteingabebereich wird bei Mausereignissen nicht automatisch angezeigt. Stiftereignisse werden bei Verwendung von Terminaldiensten in Mausereignisse konvertiert. Das [**PenInputPanel-Objekt**](peninputpanel-class.md) funktioniert nicht über eine Terminaldiensteverbindung.

## <a name="pen-input-panel-input-modes"></a>Eingabemodi des Stifteingabebereichs

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) ermöglicht entweder Tastaturfunktionen oder Handschrifteingaben mit zusätzlichen Tastaturen, die die Eingabe unterstützen. Die Benutzeroberfläche für den Stifteingabebereich umfasst Folgendes:

-   Schreibblock
-   Schreibpad für ostasiatische Sprachen
-   QuickKeys-Tastaturen
-   Tastatur an Ort und Stelle

Die Verfügbarkeit des Schreibpads im Vergleich zum Schreibpad für ostasiatische Sprachen hängt von der Standardeinstellung des Benutzer-Locale im Betriebssystem ab.

### <a name="writing-pad"></a>Schreibblock

Das Schreibpad ähnelt der vertrauten Benutzeroberfläche des Eingabebereichs.

Das Schreibpad erfasst Handschrift vom Endbenutzer. Die grundlegende Benutzeroberfläche enthält eine einzelne Schreibzeile, in der der Benutzer Text mit einem digitalen Stift schreiben kann. Wenn der Benutzer mit dem Schreiben fertig ist und entweder auf die Schaltfläche Senden tippt oder auf ein Timeout wartet, wird die Handschrift an die Erkennenden gesendet.

Ink wird erkannt, nachdem seit dem Sammeln des letzten Ink-Strichs ein angegebener Zeitraum verstrichen ist. Wenn das Timeout auftritt, wird ink von der Auflistungsoberfläche entfernt, und die Erkennung erfolgt. Der erkannte Text wird dann in das Steuerelement eingefügt, an das das [**PenInputPanel-Objekt**](peninputpanel-class.md) angefügt ist.

### <a name="east-asian-multibox-pad"></a>Ostasiatisches Multiboxpad

Die ostasiatische Version des Stifteingabebereichs zeigt eine Multibox-Schnittstelle für die Eingabe von asiatisch-zeichen an. Sie bietet Alternativen und ähnelt der Benutzeroberfläche des Eingabebereichs. Benutzer können falsch korrigierte Zeichen korrigieren, indem sie auf ein Schreibfeld tippen und das richtige Zeichen aus einer Liste von Alternativen in der Leiste oben im Stifteingabebereich auswählen. Filterschaltflächen stehen zur Verfügung, um die Liste der Erkennungs alternativer Zeichen auf bestimmte Zeichentypen wie Symbole zu verengen.

Die koreanischen und japanischen Versionen des Schreibpads verfügen über einen Konvertierungsschlüssel zusätzlich zu den Mini-Quicktasten, die allen Sprachs skins gemeinsam sind.

Um lateinische Zeichen im Schreibpad für ostasiatische Sprachen zu erhalten, legen Sie die [**Factoid-Eigenschaft**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) fest, um die Genauigkeit der lateinischen Zeichenerkennung zu erhöhen. Legen Sie **das Digit-Member** des [**Factoid-Objekts**](factoid-constants.md) für numerische Zeichen oder das **OneChar-Member** des **Factoid-Objekts** für alphabetische und numerische Zeichen fest.

### <a name="quickkeys-keypads"></a>QuickKeys-Tastaturen

Der Stifteingabebereich bietet zwei kleine Tastaturen zum Eingeben von Symbolen und Zahlen.

### <a name="in-place-keyboard"></a>In-Place-Tastatur

Der Stifteingabebereich bietet einen Tastaturmodus für Situationen, in denen die Handschrifterkennung nicht ausreicht. Wenn Sie z. B. ein Kennwort oder eine Teilnummer eingeben, werden Benutzer wahrscheinlich mehr Erfolg bei der Verwendung der Tastatur des Stifteingabebereichs als beim Schreibpad haben. Dies liegt daran, dass Kennwörter oder Teilenummern wahrscheinlich nicht im Wörterbuch der Schreibauflage enthalten sind.

## <a name="recognizer-support"></a>Unterstützung für die Wiedererkennung

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) unterstützt die Windows XP Tablet PC Edition Version 1.0 und das Tablet PC SDK Version 1.5.

## <a name="automatic-positioning"></a>Automatische Positionierung

Standardmäßig wird der Stifteingabebereich automatisch relativ zum Steuerelement positioniert, an das er angefügt ist. Es überlappt das Steuerelement nicht, es sei denn, es ist nicht genügend Bildschirmfläche sowohl für den Stifteingabebereich als auch für das Steuerelement vorhanden, oder es sei denn, der Entwickler legt die Position des Stifteingabebereichs explizit fest.

Automatische Positionierungsfunktionen nur, wenn der Entwickler die Position nicht explizit mit der [**MoveTo-Methode festgelegt**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) hat. Um die automatische Positionierung zu überschreiben, ändern Sie die Werte der [**Eigenschaften Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) und [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in einem [**PanelMoving-Ereignishandler.**](peninputpanel-panelmoving.md)

Die Position des Stifteingabebereichs wird durch die Ränder des Bildschirms eingeschränkt. Kein Rand des Stifteingabebereichs kann näher als 0,25 Zoll von einem Rand des Bildschirms entfernt sein.

Standardmäßig wird der obere Rand des Stifteingabebereichs am unteren Rand des Steuerelements angezeigt, an das es angefügt ist, und durch den Wert der [**VerticalOffset-Eigenschaft**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) vom Steuerelement getrennt. Wenn unter dem Steuerelement nicht genügend Platz vorhanden ist, wird der untere Rand des Stifteingabebereichs am oberen Rand des Steuerelements angezeigt, an das es angefügt ist, und durch den Wert der **VerticalOffset-Eigenschaft** vom Steuerelement getrennt. Wenn immer noch nicht genügend Platz vorhanden ist, wie bei einem Vollbild-Bearbeitungssteuerfeld, überlappt der Stifteingabebereich das Steuerelement.

Der Eingabebereich des linken Randstifts wird am linken Rand des Steuerelements angezeigt, an das es angefügt ist, und wird durch den Wert der [**HorizontalOffset-Eigenschaft**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) vom Steuerelement getrennt, außer als durch den Bildschirm gebunden. Wenn die gewünschte Position den Stifteingabebereich über die verfügbaren Bildschirmgrenzen hinaus platziert, nimmt der Stifteingabebereich die nächste mögliche horizontale Position an.

### <a name="forced-overlap"></a>Erzwungene Überlappung

Manchmal ist es erforderlich, dass sich der Stifteingabebereich mit dem angefügten Steuerelement überschneidet, wie es bei einem Vollbildbearbeitungssteuerfeld der Fall ist. In solchen Fällen wird die automatische Positionierung des Stifteingabebereichs anhand der folgenden Regeln bestimmt:

-   Wenn sich die Einfügemarke in der oberen Hälfte des angefügten Steuerelements befindet, befindet sich die vertikale Position des Stifteingabebereichs am unteren Bildschirmrand und platziert sie möglicherweise über dem unteren Teil des Steuerelements.
-   Wenn sich die Einfügemarke in der unteren Hälfte des angefügten Steuerelements befindet, befindet sich die vertikale Position des Stifteingabebereichs am oberen Bildschirmrand und platziert sie möglicherweise über der oberen Hälfte des Steuerelements.

### <a name="windowless-controls"></a>Fensterlose Steuerelemente

Wenn ein [**PenInputPanel-Objekt**](peninputpanel-class.md) an ein fensterloses Steuerelement angefügt wird, wird der Stifteingabebereich relativ zum übergeordneten Element des fensterlosen Steuerelements positioniert. Legen Sie [**die Eigenschaften Oben**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) und [**Links**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in einem [**PanelMoving-Ereignishandler**](peninputpanel-panelmoving.md) fest, oder verwenden Sie die [**MoveTo-Methode,**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) um den Stifteingabebereich manuell zu positionieren.

 

 
