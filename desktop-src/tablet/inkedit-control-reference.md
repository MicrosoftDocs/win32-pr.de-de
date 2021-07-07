---
description: Mit dem InkEdit-Steuerelement können Sie Ink-, Ink- und Ink-Daten erfassen und als Text anzeigen.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: InkEdit-Steuerelementreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe2aad6b7d8b536f2ede35fd93bd19840e69fc
ms.sourcegitcommit: f8f06d7ad2ff6599e90b0493b355e0c1811d898f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113369312"
---
# <a name="inkedit-control-reference"></a>InkEdit-Steuerelementreferenz

Mit dem InkEdit-Steuerelement können Sie Ink-, Ink- und Ink-Daten erfassen und als Text anzeigen. Mit diesem Steuerelement können Sie intelligente Formulare aktivieren, wodurch die Genauigkeit der Texteingabe verbessert wird.

Dieses Steuerelement ist eine Obermenge des [**RichEdit-Steuerelements.**](/windows/desktop/api/richole/nn-richole-iricheditole) Es erweitert das **RichEdit-Steuerelement** um die Möglichkeit, Ink zu erfassen, zu erkennen und anzuzeigen.

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Das Erstellen des InkEdit-Steuerelements hinter einem transparenten Steuerelement (z. B. eine GroupBox mit dem WS EX TRANSPARENT-Eigenschaftensatz) verhindert, dass \_ \_ InkEdit InkEdit sammelt.

## <a name="members"></a>Member



| Enumeration                                            | Beschreibung                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Definiert Werte, die angeben, ob das Steuerelement flach oder 3D angezeigt wird.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Definiert Werte, die angeben, ob das Steuerelement über einen Rahmen verfügt.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Definiert Werte, die das Interesse an einer Reihe anwendungsspezifischer Gesten festlegen.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Definiert Werte, die angeben, ob eine Auswahl als Ink oder Text angezeigt wird.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Definiert Werte, die angeben, ob sich das InkEdit-Steuerelement im Leerlauf befindet, Ink sammelt oder Ink erkennt.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Definiert Werte, die angeben, wie Ink in das InkEdit-Steuerelement eingefügt wird.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Definiert Werte, die die Sammlungsmoduseinstellungen für gezeichnete Ink-Ob-Ink-Sammlungen deaktiviert, Ink-Sammlungen oder Ink- und Gestensammlungen angeben.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Definiert Werte, die angeben, welche Maustaste gedrückt wurde.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Definiert Werte, die den Typ des angezeigten Mauszeigers angeben.<br/>                                                                                             |
| [**Mousebutton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Definiert Werte, die angeben, welche Maustaste gedrückt wurde.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Definiert Werte, die angeben, wie die Bildlaufleisten eines InkEdit-Steuerelements auf dem Bildschirm angezeigt werden.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Definiert Werte, die die Ausrichtung des Absatzes relativ zu den Rändern des InkEdit-Steuerelements angeben.<br/>                                                      |



 



| Ereignisbenachrichtigungsmeldung                                   | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [\_IECN-STRICH](inkedit-messages--win32-only-.md)            | Diese Meldung wird über eine WM \_ NOTIFY-Nachricht gesendet, wenn ein Strich abgeschlossen ist (nur Win32).<br/>  |
| [\_IECN-GESTE](inkedit-messages--win32-only-.md)           | Diese Meldung wird über eine WM \_ NOTIFY-Nachricht gesendet, wenn eine Geste abgeschlossen ist (nur Win32).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Diese Meldung wird über eine WM NOTIFY-Nachricht gesendet, wenn eine Erkennung \_ auftritt (nur Win32).<br/>     |



 



| Ereignis                                                  | BESCHREIBUNG                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Veränderung**](inkedit-change.md)                       | Tritt ein, wenn sich der Inhalt des Steuerelements oder eines Eigenschaftswerts ändert.<br/>                                                                                                              |
| [**klicken**](inkedit-click.md)                         | Tritt beim Klicken auf das Steuerelement ein.<br/>                                                                                                                                              |
| [**Dblclick**](inkedit-dblclick.md)                   | Tritt beim Doppelklicken auf das Steuerelement ein.<br/>                                                                                                                                       |
| [**Geste**](inkedit-gesture.md)                     | Tritt ein, wenn eine Anwendungsgeste erkannt wird.<br/>                                                                                                                                |
| [**Keydown**](inkedit-keydown.md)                     | Tritt ein, wenn der Benutzer eine Taste drückt, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                          |
| [**Keypress**](inkedit-keypress.md)                   | Tritt ein, wenn eine Taste gedrückt wird, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                                |
| [**Keyup**](inkedit-keyup.md)                         | Tritt ein, wenn eine Taste freigegeben wird, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                               |
| [**Mousedown**](inkedit-mousedown.md)                 | Tritt ein, wenn sich der Mauszeiger über dem InkEdit-Steuerelement befindet und eine Maustaste gedrückt wird.<br/>                                                                                         |
| [**Mousemove**](inkedit-mousemove.md)                 | Tritt ein, wenn der Mauszeiger über das InkEdit-Steuerelement bewegt wird.<br/>                                                                                                                 |
| [**Mouseup**](inkedit-mouseup.md)                     | Tritt ein, wenn sich der Mauszeiger über dem InkEdit-Steuerelement befindet und eine Maustaste losgelassen wird.<br/>                                                                                        |
| [**Recognitionresult**](inkedit-recognitionresult.md) | Tritt ein, wenn das InkEdit-Steuerelement ergebnisse manuell aus einem Aufruf der [**Recognize-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) oder automatisch nach dem Ausgelösten des Erkennungs-Timeouts abruft.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Tritt ein, wenn sich die Auswahl der InkEdit-Steuerelements ändert.<br/>                                                                                                             |
| [**Takt**](inkedit-stroke.md)                       | Tritt ein, wenn der Benutzer ein neues [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) für ein [**beliebiges IInkTablet-Objekt zeichnet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)<br/>                                                 |



 



| Get/Set message                                               | BESCHREIBUNG                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EM \_ GETINKMODE](inkedit-messages--win32-only-.md)           | Ruft den Ink-Modus des Steuerelements ab (nur Win32).<br/>                                                                                                                       |
| [EM \_ SETINKMODE](inkedit-messages--win32-only-.md)           | Legt den Ink-Modus des Steuerelements fest (nur Win32).<br/>                                                                                                                       |
| [EM \_ GETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Ruft den Ink-Einfügemodus des Steuerelements ab (nur Win32).<br/>                                                                                                             |
| [EM \_ SETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Legt den Einfügemodus für die Ink-Datei des Steuerelements fest (nur Win32).<br/>                                                                                                             |
| [EM \_ GETDRAWATTR](inkedit-messages--win32-only-.md)          | Ruft die aktuellen Zeichnungsattribute des Steuerelements ab (nur Win32).<br/>                                                                                                     |
| [EM \_ SETDRAWATTR](inkedit-messages--win32-only-.md)          | Legt die Zeichnungsattribute fest, die für zukünftige Ink-Sammlungen verwendet werden sollen (nur Win32).<br/>                                                                                           |
| [EM \_ GETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Ruft das Erkennungs-Timeout für das Steuerelement ab (nur Win32).<br/>                                                                                                           |
| [EM \_ SETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Legt das Erkennungs-Timeout für das Steuerelement fest (nur Win32).<br/>                                                                                                           |
| [EM \_ GETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Ruft den Gestenstatus für das Steuerelement ab (nur Win32).<br/>                                                                                                                |
| [EM \_ SETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Legt den Gestenstatus für das Steuerelement fest (nur Win32).<br/>                                                                                                                |
| [EM \_ GETRECOGNIZER](inkedit-messages--win32-only-.md)        | Ruft die vom -Steuerelement verwendete Erkannten ab (nur Win32).<br/>                                                                                                              |
| [EM \_ SETRECOGNIZER](inkedit-messages--win32-only-.md)        | Legt die vom Steuerelement verwendete -Erkennen fest (nur Win32).<br/>                                                                                                              |
| [EM \_ GETFACTOID](inkedit-messages--win32-only-.md)           | Ruft das Factoid ab, das für die Erkennung verwendet werden soll (nur Win32).<br/>                                                                                                                |
| [EM \_ SETFACTIOD](inkedit-messages--win32-only-.md)           | Legt das Factoid fest, das für die Erkennung verwendet werden soll (nur Win32).<br/>                                                                                                                |
| [EM \_ GETSELINK](inkedit-messages--win32-only-.md)            | Ruft die Ink-Datei in der Auswahl ab (nur Win32).<br/>                                                                                                                          |
| [EM \_ SETSELINK](inkedit-messages--win32-only-.md)            | Legt die Ink-Datei in der Auswahl fest (nur Win32).<br/>                                                                                                                          |
| [EM \_ GETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Gibt die aktuelle Darstellung der Ink-Funktion im ausgewählten Bereich zurück, indem einer der Werte der [**InkDisplayMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) verwendet wird (nur Win32).<br/> |
| [EM \_ SETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Legt die Darstellung der Ink-Eigenschaft im ausgewählten Bereich mithilfe eines der Werte der [**InkDisplayMode-Enumeration**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) fest (nur Win32).<br/>            |
| [EM \_ GETSTATUS](inkedit-messages--win32-only-.md)            | Ruft den Status des Steuerelements ab (nur Win32).<br/>                                                                                                                         |
| [EM \_ RECOGNIZE](inkedit-messages--win32-only-.md)            | Erzwingt die Erkennung (nur Win32).<br/>                                                                                                                                     |
| [EM \_ GETMOUSEICON](inkedit-messages--win32-only-.md)         | Ruft das Maussymbol ab (nur Win32).<br/>                                                                                                                                    |
| [EM \_ SETMOUSEICON](inkedit-messages--win32-only-.md)         | Legt das Maussymbol fest (nur Win32).<br/>                                                                                                                                    |
| [EM \_ GETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Ruft den Mauszeiger ab (nur Win32).<br/>                                                                                                                                 |
| [EM \_ SETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Legt nur den Mauszeiger Win32 fest.<br/>                                                                                                                                  |
| [EM \_ GETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Ruft den Status ab, ob Mauseingaben wie Stifteingaben behandelt werden (nur Win32).<br/>                                                                                        |
| [EM \_ SETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Legt den Status fest, ob Mauseingaben wie Stifteingaben behandelt werden (nur Win32).<br/>                                                                                        |



 



| Methode                                               | BESCHREIBUNG                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Ruft das Interesse des InkEdit-Steuerelements in einem bekannten Satz von Gesten ab.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Gibt an, dass die Erkennung erfolgen soll.<br/>                             |
| [**Aktualisieren**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Bewirkt, dass das Steuerelement neu gezeichnet wird.<br/>                                        |
| [**Setgesturestatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Legt das Interesse des InkEdit-Steuerelements in einem bekannten Satz von Gesten fest.<br/> |



 



| Eigenschaft                                                 | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Darstellung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement flach oder 3D angezeigt wird, oder legt diesen fest.<br/>                                                                                      |
| [**Backcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ruft die Hintergrundfarbe für das InkEdit-Steuerelement ab oder legt diese fest.<br/>                                                                                                                 |
| [**Rahmenart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement über einen Rahmen verfügt, oder legt diesen fest.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ruft einen Wert ab, der bestimmt, ob Bildlaufleisten im InkEdit-Steuerelement deaktiviert sind, oder legt diesen fest.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ruft die Zeichnungsattribute für inkEdit zu zeichnende InkEdit-Steuerelement ab oder legt diese fest.<br/>                                                                                |
| [**Aktiviert**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement auf vom Benutzer generierte Ereignisse reagieren kann, oder legt diesen fest.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Ruft die [Factoid-Konstante ab,](factoid-constants.md) mit der ein [**IInkRecognizer-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) die Suche nach dem Erkennungsergebnis einschränkt, oder legt diese fest.<br/> |
| [**Schriftart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ruft die Schriftart des Texts ab, der vom InkEdit-Steuerelement angezeigt wird, oder legt diese fest.<br/>                                                                                                       |
| [**Hwnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ruft das Fensterhandler ab, an das [**das InkDisp-Steuerelement**](inkdisp-class.md) gebunden ist.<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ruft einen Wert ab, der angibt, wie InkEdit als Text oder als InkEdit-Steuerelement eingefügt wird, oder legt diesen fest.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Ink-Auflistung deaktiviert, die Ink-Sammlung oder die Ink- und Gesten gesammelt werden.<br/>                                               |
| [**Locked**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ruft einen Wert ab, der angibt, ob das InkEdit-Steuerelement schreibgeschützt ist, oder legt diesen fest.<br/>                                                                                       |
| [**Maxlength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ruft einen Wert ab, der angibt, ob ein InkEdit-Steuerelement eine maximale Anzahl von Zeichen enthalten kann, oder legt ihn fest und gibt in diesem Beispiel die maximale Anzahl von Zeichen an.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ruft das aktuelle benutzerdefinierte Maussymbol ab oder legt es fest.<br/>                                                                                                                                |
| [**Mousepointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Ruft einen Wert ab, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des InkEdit-Steuerelements befindet, oder legt diesen fest.<br/>                                |
| [**Mehrzeiligen**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ruft einen Wert ab, der angibt, ob es sich um ein mehrline-InkEdit-Steuerelement handelt, oder legt diesen fest.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ruft die Zeitdauer zwischen dem letzten erfassten [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) und dem Beginn der Texterkennung in Millisekunden ab oder legt diese fest.<br/>        |
| [**Erkennungsmodul**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ruft das [**IInkRecognizer-Objekt ab, das**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) für die Erkennung verwendet werden soll, oder legt es fest.<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ruft den Typ der Scrollleisten ab, die im InkEdit-Steuerelement angezeigt werden, oder legt diesen fest.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ruft die Ausrichtung ab, die auf die aktuelle Auswahl oder Einfügemarke angewendet werden soll (nur Laufzeit), oder legt diese fest.<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ruft einen Wert ab, der angibt, ob der Schriftschnitt des aktuell ausgewählten Texts im InkEdit-Steuerelement fett formatiert ist (nur Laufzeit), oder legt diesen fest.<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ruft ab oder legt fest, ob Text im InkEdit-Steuerelement in der Baseline, als Hochskript oder als Inskript (nur Laufzeit) angezeigt wird.<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ruft die Textfarbe der aktuellen Textauswahl oder Einfügemarke (nur Laufzeit) ab oder legt diese fest.<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ruft den Schriftartnamen des ausgewählten Texts im InkEdit-Steuerelement ab oder legt den Schriftartnamen fest (nur Zur Laufzeit).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ruft den Schriftgrad des ausgewählten Texts im InkEdit-Steuerelement ab oder legt den Schriftgrad fest (nur Laufzeit).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ruft das Array eingebetteter [**InkDisp-Objekte**](inkdisp-class.md) ab (wenn es als Ink angezeigt wird), das die aktuelle Auswahl enthält, oder legt dieses fest.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ruft einen Wert ab, der die Darstellung der Auswahl zwischen Ink und Text ermöglicht, oder legt diesen fest.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ruft einen Wert ab, der angibt, ob der Schriftschnitt des aktuell ausgewählten Texts im InkEdit-Steuerelement italisch ist (nur Laufzeit), oder legt diesen fest.<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ruft die Anzahl der Zeichen ab, die im InkEdit-Steuerelement ausgewählt sind (nur Laufzeit), oder legt diese fest.<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ruft den aktuell ausgewählten RTF-formatierten Text (Rich Text Format) im InkEdit-Steuerelement ab (nur Laufzeit), oder legt den Text fest.<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ruft den Anfangspunkt des Texts ab, der im Textfeld ausgewählt ist (nur Laufzeit), oder legt diesen fest.<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ruft den ausgewählten Text im InkEdit-Steuerelement ab (nur Laufzeit), oder legt den text fest.<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ruft einen Wert ab, der angibt, ob der Schriftschnitt des aktuell ausgewählten Texts im InkEdit-Steuerelement unterstrichen ist (nur Laufzeit), oder legt diesen fest.<br/>                            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ruft einen Wert ab, der angibt, ob sich das InkEdit-Steuerelement im Leerlauf befindet, Ink-Daten sammelt oder Ink erkennt (nur Laufzeit).<br/>                                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ruft den aktuellen Text im Textfeld ab oder legt diesen fest.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ruft den Text des InkEdit-Steuerelements einschließlich aller RTF-Codes ab oder legt den Text fest.<br/>                                                                                                     |
| [**Usemouseforinput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ruft einen Wert ab, der angibt, ob die Maus als Eingabegerät verwendet werden kann, oder legt diesen fest.<br/>                                                                                      |

| Struktur                                                                    | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Enthält Informationen zu einem [**Stroke-Ereignis**](inkedit-stroke.md) (nur Win32).<br/> |
| [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Enthält Informationen zu einer bestimmten Geste (nur Win32).<br/>                       |
| [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Enthält Informationen zu einem Erkennungsergebnis (nur Win32).<br/>                     |

## <a name="com-implementation"></a>COM-Implementierung

Dieses Objekt implementiert die [IInkEdit-COM-Schnittstelle.](/windows/win32/api/inked/nn-inked-iinkedit)

## <a name="related-topics"></a>Zugehörige Themen

- [**InkOverlay-Klasse**](inkoverlay-class.md), 
- [InkPicture-Steuerelementreferenz](inkpicture-control-reference.md)
- [**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md)
