---
description: Ab Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK), Version 1,0, bietet der System-Level Tablet PC Input Panel einen universellen Mechanismus zum Ausführen von Texteingaben auf der Windows-Plattform, obwohl dieser keinen programmgesteuerten Zugriff bietet. Das Tablet PC SDK, Version 1,5, "tzinputpanel"-Objekt integriert Texteingabe Tools in Anwendungen.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Informationen zum Eingabebereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db733e49e49d428b5ff8072a1315787d9fafd25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393245"
---
# <a name="about-the-input-panel"></a>Informationen zum Eingabebereich

\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)ersetzt. Weitere Informationen finden Sie unter [Programmieren des Text Eingabe Panels](programming-the-text-input-panel.md).\]

Ab Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK), Version 1,0, bietet der System-Level Tablet PC Input Panel einen universellen Mechanismus zum Ausführen von Texteingaben auf der Windows-Plattform, obwohl dieser keinen programmgesteuerten Zugriff bietet. Das Tablet PC SDK, Version 1,5, " [**tzinputpanel**](peninputpanel-class.md) "-Objekt integriert Texteingabe Tools in Anwendungen.

In der folgenden Abbildung wird der Stift Eingabebereich angezeigt, der über dem Beispiel " [Auto Claims Form Sample](auto-claims-form-sample.md) " angezeigt wird.

![Stift Eingabebereich wird über automatisches Anspruchsformular Beispiel Beispiel angezeigt](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Das [**Objekt**](peninputpanel-class.md) "" "" "" "ist für Anwendungsentwickler praktisch. Es ist nicht erforderlich, Steuerelemente für vorhandene Formulare zu ersetzen. Sie können an vorhandene Steuerelemente, die Texteingaben empfangen, einfach " **cuinputpanel** "-Objekte anfügen, und Sie können damit beginnen, Eingaben **aus dem "** "-Objekt "" ""

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " übernimmt die Einstellungen aus dem Eingabe Panel für die folgenden Eigenschaften:

-   Layout
-   Frei Handstärke
-   Erkennungs Timeout
-   Feldgröße, Sendemodus und andere Einstellungen, die speziell für die ostasiatische einfügende Eingabe gelten

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " bietet keinen Zugriff auf die zugrunde liegende frei Hand Eingabe. Um frei Hand Eingaben zu erhalten, verwenden Sie das [InkPicture](inkpicture-control-reference.md) -Steuerelement.

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " stellt eine direkte Benutzeroberfläche (User Interface, UI) bereit, die von Endbenutzern Ihrer Anwendungen problemlos erkannt werden kann. Sie wird automatisch aktiviert, wenn der Benutzer auf ein Fenster mit einem **PenInputPanel** -Objekt tippt, das den Tablettstift verwendet. Der Stift Eingabebereich wird automatisch angezeigt, wenn das System ein Cursor Button up-Ereignis für das Fenster erkennt, an das das **PenInputPanel** -Objekt angefügt wird. Die automatische Aktivierung kann deaktiviert werden, indem die [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) -Eigenschaft auf **false** festgelegt wird.

Der Stift Eingabe Panel wird bei Mausereignissen nicht automatisch angezeigt. Pen-Ereignisse werden bei der Verwendung von Terminal Diensten in Mausereignisse konvertiert. Das Objekt " [**pinputpanel**](peninputpanel-class.md) " funktioniert nicht über eine Terminal Dienste-Verbindung.

## <a name="pen-input-panel-input-modes"></a>Eingabemodi für Stift Eingabebereich

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " ermöglicht die Tastatur-oder Handschrift Eingabe mit zusätzlichen normalen zur Unterstützung der Eingabe. Die Benutzeroberfläche zum Stift Eingabe Panel umfasst Folgendes:

-   Schreiben von Pad
-   Schreiben von Pad für ostasiatische Sprachen
-   QuickKeys-normalen
-   Direkte Tastatur

Die Verfügbarkeit des Schreib Bereichs im Vergleich zum Schreibvorgang für ostasiatische Sprachen hängt von der Standardeinstellung für das Gebiets Schema des Benutzers im Betriebssystem ab.

### <a name="writing-pad"></a>Schreiben von Pad

Der Schreibbereich ähnelt der vertrauten Benutzeroberfläche des Eingabe Panels.

Das Schreiben von Pad sammelt Handschrift vom Endbenutzer. Die grundlegende Benutzeroberfläche enthält eine einzelne Schreib Zeile, in der der Benutzer Text mit einem digitalen Stift schreiben kann. Wenn der Benutzer das Schreiben beendet und entweder auf die Schaltfläche "Senden" tippt oder darauf wartet, dass ein Timeout auftritt, wird die Handschrift an die Erkennung gesendet.

Frei Hand Eingaben werden erkannt, nachdem eine angegebene Zeitspanne seit dem Zeitpunkt der letzten Erfassung des frei Hand Strichs verstrichen ist. Wenn das Timeout auftritt, wird die frei Hand Eingabe aus der Auflistungs Oberfläche entfernt und die Erkennung erfolgt. Der erkannte Text wird dann in das Steuerelement eingefügt, an das das Objekt " [**tzinputpanel**](peninputpanel-class.md) " angefügt wird.

### <a name="east-asian-multibox-pad"></a>Ostasiatische Multibox-Pad

Die ostasiatische Version des Stift Eingabe Panels zeigt eine Multibox-Schnittstelle für die Eingabe asiatischer Zeichen an. Es stellt Alternativen bereit und ähnelt der Benutzeroberfläche des Eingabe Panels. Benutzer können falsch erkannte Zeichen korrigieren, indem Sie auf ein Schreib Feld tippen und das richtige Zeichen aus einer Liste von Alternativen in der Leiste oben im Stift Eingabe Panel auswählen. Filter Schaltflächen sind verfügbar, um die Liste der Erkennungs Alternativen auf angegebene Zeichen Typen, z. b. Symbole, einzugrenzen.

Die koreanischen und japanischen Versionen des Schreib Rasters verfügen zusätzlich zu den kleinen Tastenkombinationen, die für alle sprach Skins gemeinsam sind.

Um lateinische Zeichen im Schreib-Pad für ostasiatische Sprachen zu erhalten, legen Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) " fest, um die Genauigkeit der lateinischen Zeichenerkennung zu erhöhen. Legen Sie den **Digit** -Member des [**Faktoid**](factoid-constants.md) -Objekts für numerische Zeichen oder den **OneChar** -Member des **Faktoid** -Objekts für alphabetische und numerische Zeichen fest.

### <a name="quickkeys-keypads"></a>QuickKeys-Keypads

Der Stift Eingabe Panel bietet zwei kleine normalen zum Eingeben von Symbolen und Zahlen.

### <a name="in-place-keyboard"></a>Direkte Tastatur

Der Stift Eingabe Panel bietet einen Tastaturmodus für Situationen, in denen die Handschrifterkennung nicht ausreicht. Wenn Sie beispielsweise ein Kennwort oder eine Teilenummer eingeben, haben die Benutzer wahrscheinlich mehr Erfolg, wenn Sie die Tastatur für den Stift Eingabebereich verwenden, als dies beim Schreiben des Pads der Fall wäre. Dies liegt daran, dass es unwahrscheinlich ist, dass Kenn Wörter oder Teilenummern im Erkennungs Wörterbuch des Schreibvorgangs enthalten sind.

## <a name="recognizer-support"></a>Erkennungs Unterstützung

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " unterstützt Versand erkenungen für Windows XP Tablet PC Edition Version 1,0 und das Tablet PC SDK Version 1,5.

## <a name="automatic-positioning"></a>Automatische Positionierung

Standardmäßig wird der Stift Eingabebereich automatisch relativ zu dem Steuerelement positioniert, an das es angefügt ist. Das Steuerelement überschneidet sich nicht, es sei denn, für den Stift Eingabebereich und das Steuerelement ist nicht genügend Bildschirm vorhanden, oder der Entwickler legt die Position des Stift Eingabe Panels nicht explizit fest.

Automatisches Positionieren von Funktionen nur, wenn der Entwickler die Position nicht explizit mithilfe der Methode " [**muveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) " festgelegt hat. Zum Überschreiben der automatischen Positionierung ändern Sie die Werte der Eigenschaften [**oben**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) und [**Links**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in einem [**PanelMoving**](peninputpanel-panelmoving.md) -Ereignishandler.

Die Position des Stift Eingabe Panels wird durch die Ränder des Bildschirms eingeschränkt. Kein Rand des Stift Eingabe Bereichs kann von jedem Rahmen des Bildschirms über 0,25 Zoll liegen.

Standardmäßig wird der obere Rand des Stift Eingabe Bereichs am unteren Rand des Steuer Elements angezeigt, an das es angefügt ist, und wird vom-Steuerelement durch den Wert der [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) -Eigenschaft getrennt. Wenn unter dem Steuerelement nicht genügend Platz vorhanden ist, wird der untere Teil des Stift Eingabe Bereichs am oberen Rand des Steuer Elements angezeigt, an das es angefügt ist. es wird durch den Wert der **VerticalOffset** -Eigenschaft vom-Steuerelement getrennt. Wenn der Platz immer noch nicht ausreicht, wie bei einem voll Bild Bearbeitungs Steuerelement, überlappt der Stift Eingabebereich das Steuerelement.

Der Eingabebereich des linken Edge-Stifts wird am linken Rand des Steuer Elements angezeigt, an das es angefügt ist, und wird vom-Steuerelement durch den Wert der [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) -Eigenschaft getrennt, mit Ausnahme der vom Bildschirm begrenzten. Wenn die gewünschte Position den Stift Eingabebereich hinter den verfügbaren Bildschirm Begrenzungen platziert, nimmt der Stift Eingabe Panel die nächstmögliche horizontale Position an.

### <a name="forced-overlap"></a>Erzwungene Überschneidung

Manchmal ist es erforderlich, dass der Stift Eingabebereich das angefügte Steuerelement überlappt, wie bei einem voll Bild Bearbeitungs Steuerelement. In solchen Fällen wird die automatische Positionierung des Stift Eingabe Bereichs anhand der folgenden Regeln bestimmt:

-   Wenn sich die Einfügemarke in der oberen Hälfte des angefügten Steuer Elements befindet, befindet sich die vertikale Position des Stift Eingabe Bereichs am unteren Rand des Bildschirms, was möglicherweise über dem unteren Teil des Steuer Elements liegt.
-   Wenn sich die Einfügemarke in der unteren Hälfte des angefügten Steuer Elements befindet, befindet sich die vertikale Position des Stift Eingabe Bereichs am oberen Rand des Bildschirms und kann Sie möglicherweise über der oberen Hälfte des Steuer Elements platzieren.

### <a name="windowless-controls"></a>Fensterlose Steuerelemente

Wenn ein [**PenInputPanel**](peninputpanel-class.md) -Objekt an ein fensterloses Steuerelement angefügt ist, wird der Stift Eingabebereich relativ zum übergeordneten Element des fensterlosen Steuer Elements positioniert. Legen Sie die Eigenschaften [**oben**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) und [**Links**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in einem [**PanelMoving**](peninputpanel-panelmoving.md) -Ereignishandler fest, oder verwenden Sie die Methode " [**muveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) ", um den Stift Eingabebereich manuell zu positionieren.

 

 
