---
description: Mit dem InkEdit-Steuerelement können Sie frei Hand Eingaben erfassen, frei Hand Eingaben erkennen und frei Hand Eingaben als Text anzeigen.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Referenz zum InkEdit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53edfdc6a72a7792c60a6c7c7bf0e38ffc5e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050447"
---
# <a name="inkedit-control-reference"></a>Referenz zum InkEdit-Steuerelement

Mit dem InkEdit-Steuerelement können Sie frei Hand Eingaben erfassen, frei Hand Eingaben erkennen und frei Hand Eingaben als Text anzeigen. Mit diesem Steuerelement können Sie intelligente Formulare aktivieren, wodurch die Genauigkeit von Texteingaben verbessert wird.

Dieses Steuerelement ist eine übergeordnete Gruppe des [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) -Steuer Elements. Es erweitert das **RichEdit** -Steuerelement mit der Fähigkeit, frei Hand Eingaben zu erfassen, zu erkennen und anzuzeigen.

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Wenn Sie das InkEdit-Steuerelement hinter einem transparenten Steuerelement erstellen (z. b. ein GroupBox-Element mit dem \_ \_ transparenten Eigenschaften Satz von WS-Ex), wird verhindert, dass InkEdit frei

## <a name="members"></a>Member



| Enumeration                                            | Beschreibung                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aussehen von anceconstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Definiert Werte, die angeben, ob das Steuerelement flach oder 3D angezeigt wird.<br/>                                                                                            |
| [**Borderstyleconstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Definiert Werte, die angeben, ob das Steuerelement über einen Rahmen verfügt.<br/>                                                                                                   |
| [**Inkapplicationgeste**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Definiert Werte, die das Interesse an einem Satz von anwendungsspezifischen Gesten festlegen.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Definiert Werte, die angeben, ob eine Auswahl als frei Hand oder Text angezeigt wird.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Definiert Werte, die angeben, ob das InkEdit-Steuerelement im Leerlauf ist, frei Hand Eingaben sammelt oder frei Hand Eingaben erkennt.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Definiert Werte, die angeben, wie Ink in das InkEdit-Steuerelement eingefügt wird.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Definiert Werte, die die auflistungsmoduseinstellungen für gezeichnete frei Hand Eingaben angeben: gibt an, ob die frei Hand Auflistung deaktiviert ist, frei Hand Eingaben gesammelt werden oder frei Hand Eingaben<br/> |
| [**Inkmoueinschaltfläche**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Definiert Werte, die angeben, welche Maustaste gedrückt wurde.<br/>                                                                                                     |
| [**Inkmousekunden-Zeiger**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Definiert Werte, die den Typ des Mauszeigers angeben, der angezeigt wird.<br/>                                                                                             |
| [**MoU. Button**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Definiert Werte, die angeben, welche Maustaste gedrückt wurde.<br/>                                                                                                     |
| [**Scrollbarskonstanten**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Definiert Werte, die angeben, wie die Bild Lauf leisten eines InkEdit-Steuer Elements auf dem Bildschirm angezeigt werden.<br/>                                                                     |
| [**Selalignmentconstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Definiert Werte, die die Ausrichtung des Absatzes relativ zu den Rändern des InkEdit-Steuer Elements angeben.<br/>                                                      |



 



| Ereignis Benachrichtigungs Meldung                                   | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [IECN- \_ Strich](inkedit-messages--win32-only-.md)            | Diese Meldung wird durch eine WM- \_ Benachrichtigungs Meldung gesendet, wenn ein Strich abgeschlossen ist (nur Win32).<br/>  |
| [IECN- \_ Geste](inkedit-messages--win32-only-.md)           | Diese Meldung wird durch eine WM- \_ Benachrichtigungs Meldung gesendet, wenn eine Geste abgeschlossen ist (nur Win32).<br/> |
| [IECN- \_ Erkennungs Ergebnis](inkedit-messages--win32-only-.md) | Diese Meldung wird durch eine WM- \_ Benachrichtigungs Meldung gesendet, wenn eine Erkennung erfolgt (nur Win32).<br/>     |



 



| Ereignis                                                  | BESCHREIBUNG                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klima**](inkedit-change.md)                       | Tritt auf, wenn sich der Inhalt des Steuer Elements oder ein Eigenschafts Wert ändert.<br/>                                                                                                              |
| [**Sie**](inkedit-click.md)                         | Tritt beim Klicken auf das Steuerelement ein.<br/>                                                                                                                                              |
| [**DblClick**](inkedit-dblclick.md)                   | Tritt beim Doppelklicken auf das Steuerelement ein.<br/>                                                                                                                                       |
| [**Geste**](inkedit-gesture.md)                     | Tritt auf, wenn eine Anwendungs Geste erkannt wird.<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | Tritt ein, wenn der Benutzer eine Taste drückt, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                          |
| [**KeyPress**](inkedit-keypress.md)                   | Tritt auf, wenn eine Taste gedrückt wird, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | Tritt auf, wenn eine Taste losgelassen wird, während das InkEdit-Steuerelement den Fokus besitzt.<br/>                                                                                                               |
| [**MouseDown**](inkedit-mousedown.md)                 | Tritt ein, wenn sich der Mauszeiger über dem InkEdit-Steuerelement befindet und eine Maustaste gedrückt wird.<br/>                                                                                         |
| [**MouseMove**](inkedit-mousemove.md)                 | Tritt ein, wenn der Mauszeiger über das InkEdit-Steuerelement bewegt wird.<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | Tritt ein, wenn sich der Mauszeiger über dem InkEdit-Steuerelement befindet und eine Maustaste losgelassen wird.<br/>                                                                                        |
| [**Erkennungs Ergebnis**](inkedit-recognitionresult.md) | Tritt auf, wenn das InkEdit-Steuerelement Ergebnisse manuell von einem Rückruf der Erkennungsmethode oder automatisch nach dem [**Auslösen des Erkennungs**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) Timeouts abruft.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Tritt auf, wenn sich die Auswahl von frei Hand Eingaben im InkEdit-Steuerelement ändert.<br/>                                                                                                             |
| [**Stellung**](inkedit-stroke.md)                       | Tritt auf, wenn der Benutzer ein neues [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt für ein beliebiges [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt zeichnet.<br/>                                                 |



 



| Nachricht erhalten/festlegen                                               | BESCHREIBUNG                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EM \_ getinkmode](inkedit-messages--win32-only-.md)           | Ruft den Freihand-Modus des Steuer Elements ab (nur Win32).<br/>                                                                                                                       |
| [EM- \_ abkmode](inkedit-messages--win32-only-.md)           | Legt den Freihand-Modus des Steuer Elements fest (nur Win32).<br/>                                                                                                                       |
| [EM \_ getinkinsertmode](inkedit-messages--win32-only-.md)     | Ruft den Einfügemodus des-Steuer Elements ab (nur Win32).<br/>                                                                                                             |
| [EM- \_ Objekt Modus](inkedit-messages--win32-only-.md)     | Legt den Einfügemodus des-Steuer Elements fest (nur Win32).<br/>                                                                                                             |
| [EM \_ getdrawattr](inkedit-messages--win32-only-.md)          | Ruft die aktuellen Zeichnungs Attribute des Steuer Elements ab (nur Win32).<br/>                                                                                                     |
| [EM \_ setdrawattr](inkedit-messages--win32-only-.md)          | Legt die Zeichnungs Attribute fest, die für die zukünftige Ink-Auflistung verwendet werden sollen (nur Win32).<br/>                                                                                           |
| [EM \_ getrecotimeout](inkedit-messages--win32-only-.md)       | Ruft das Erkennungs Timeout für das-Steuerelement ab (nur Win32).<br/>                                                                                                           |
| [EM- \_ Start Timeout](inkedit-messages--win32-only-.md)       | Legt das Erkennungs Timeout für das-Steuerelement fest (nur Win32).<br/>                                                                                                           |
| [EM \_ GetGestureStatus](inkedit-messages--win32-only-.md)     | Ruft den Gesten Status für das-Steuerelement ab (nur Win32).<br/>                                                                                                                |
| [EM \_ SetGestureStatus](inkedit-messages--win32-only-.md)     | Legt den Gesten Status für das-Steuerelement fest (nur Win32).<br/>                                                                                                                |
| [EM \_ getrecognizer](inkedit-messages--win32-only-.md)        | Ruft die Erkennungsfunktion ab, die vom-Steuerelement verwendet wird (nur Win32).<br/>                                                                                                              |
| [EM-Ziel \_ Erkennungs Modul](inkedit-messages--win32-only-.md)        | Legt die Erkennung fest, die vom-Steuerelement verwendet wird (nur Win32).<br/>                                                                                                              |
| [EM \_ getfaktoid](inkedit-messages--win32-only-.md)           | Ruft das für die Erkennung zu verwendende Faktoid ab (nur Win32).<br/>                                                                                                                |
| [EM \_ setfaktiod](inkedit-messages--win32-only-.md)           | Legt das für die Erkennung zu verwendende Faktoid fest (nur Win32).<br/>                                                                                                                |
| [EM \_ getselink](inkedit-messages--win32-only-.md)            | Ruft die frei Hand Eingaben in der Auswahl ab (nur Win32).<br/>                                                                                                                          |
| [EM \_ setselink](inkedit-messages--win32-only-.md)            | Legt die frei Hand Eingaben in der Auswahl fest (nur Win32).<br/>                                                                                                                          |
| [EM \_ getselinkdisplaymode](inkedit-messages--win32-only-.md) | Gibt die aktuelle Darstellung der frei Hand Eingaben im ausgewählten Bereich zurück, indem einer der Werte der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration (nur Win32) verwendet wird.<br/> |
| [EM \_ setselinkdisplaymode](inkedit-messages--win32-only-.md) | Legt die Darstellung der frei Hand Eingaben im ausgewählten Bereich fest, indem einer der Werte der [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) -Enumeration (nur Win32) verwendet wird.<br/>            |
| [EM \_ GetStatus](inkedit-messages--win32-only-.md)            | Ruft den Status des Steuer Elements ab (nur Win32).<br/>                                                                                                                         |
| [EM \_ erkennen](inkedit-messages--win32-only-.md)            | Erzwingt die Erkennung (nur Win32).<br/>                                                                                                                                     |
| [EM \_ getmouseicon](inkedit-messages--win32-only-.md)         | Ruft das Maus Symbol ab (nur Win32).<br/>                                                                                                                                    |
| [EM * \_ tmouseicon](inkedit-messages--win32-only-.md)         | Legt das Maus Symbol fest (nur Win32).<br/>                                                                                                                                    |
| [EM \_ getmoucpointer](inkedit-messages--win32-only-.md)      | Ruft den Mauszeiger ab (nur Win32).<br/>                                                                                                                                 |
| [EM \_ -Timeout](inkedit-messages--win32-only-.md)      | Legt nur den Mauszeiger Win32 fest).<br/>                                                                                                                                  |
| [EM \_ getusemouseforinput](inkedit-messages--win32-only-.md)  | Ruft den Zustand ab, der unabhängig davon behandelt wird, ob Maus Eingaben wie pen Input (nur Win32) behandelt werden.<br/>                                                                                        |
| [EM \_ setusemouseforinput](inkedit-messages--win32-only-.md)  | Legt den Status fest, der angibt, ob Maus Eingaben wie Stift Eingaben behandelt werden (nur Win32).<br/>                                                                                        |



 



| Methode                                               | BESCHREIBUNG                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Ruft das Interesse des InkEdit-Steuer Elements in einem bekannten Satz von Gesten ab.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Gibt an, dass eine Erkennung erfolgen soll.<br/>                             |
| [**Aktualisieren**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Bewirkt, dass das Steuerelement neu gezeichnet wird.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Legt das Interesse des InkEdit-Steuer Elements in einem bekannten Satz von Gesten fest.<br/> |



 



| Eigenschaft                                                 | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Darstellung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement flach oder 3D angezeigt wird, oder legt diesen fest.<br/>                                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ruft die Hintergrundfarbe für das InkEdit-Steuerelement ab oder legt diese fest.<br/>                                                                                                                 |
| [**Rahmenart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement einen Rahmen hat, oder legt ihn fest<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ruft einen Wert ab, der bestimmt, ob Bild Lauf leisten im InkEdit-Steuerelement deaktiviert sind, oder legt diesen fest.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ruft die Zeichnungs Attribute für frei Hand Eingaben ab, die auf dem InkEdit-Steuerelement noch gezeichnet werden sollen, oder legt diese fest.<br/>                                                                                |
| [**Aktiviert**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ruft einen Wert ab, der bestimmt, ob das InkEdit-Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.<br/>                                                                     |
| [**Faktoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Dient zum Abrufen oder Festlegen der [Faktoid](factoid-constants.md) -Konstante, die ein [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt verwendet, um die Suche nach dem Erkennungs Ergebnis einzuschränken.<br/> |
| [**Raster**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ruft die Schriftart des Texts ab, der vom InkEdit-Steuerelement angezeigt wird, oder legt diese fest.<br/>                                                                                                       |
| [**HWND**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ruft das Fenster Handle ab, an das das [**InkDisp**](inkdisp-class.md) -Steuerelement gebunden ist.<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie frei Hand Eingaben in das InkEdit-Steuerelement eingefügt werden.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die frei Hand Auflistung deaktiviert ist, frei Hand Eingaben gesammelt oder frei Hand Eingaben und Gesten gesammelt werden<br/>                                               |
| [**Gesperrt**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ruft einen Wert ab, der angibt, ob das InkEdit-Steuerelement schreibgeschützt ist oder nicht, oder legt diesen fest.<br/>                                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ruft einen Wert ab, der angibt, ob ein InkEdit-Steuerelement eine maximale Anzahl von Zeichen enthalten kann, oder legt diesen fest. wenn dies der Fall ist, wird die maximale Anzahl von Zeichen<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.<br/>                                                                                                                                |
| [**Mouum Zeiger**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Dient zum Abrufen oder Festlegen eines Werts, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich der Mauszeiger über einem bestimmten Teil des InkEdit-Steuer Elements befindet<br/>                                |
| [**Mehrzeiligen**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ruft einen Wert ab, der angibt, ob es sich um ein mehrzeilige InkEdit-Steuerelement handelt.<br/>                                                                                           |
| [**Erkennungs Timeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ruft die Zeitspanne (in Millisekunden) zwischen dem letzten erfassten [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt und dem Anfang der Texterkennung ab oder legt diese fest.<br/>        |
| [**Erkennung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ruft das für die Erkennung zu verwendende [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt ab oder legt es fest.<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ruft den Typ der Scrollleisten ab, die im InkEdit-Steuerelement angezeigt werden, oder legt ihn fest.<br/>                                                                                                   |
| [**Selalignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ruft die Ausrichtung ab, die auf die aktuelle Auswahl oder Einfügemarke angewendet werden soll (nur Laufzeit), oder legt diese fest.<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im InkEdit-Steuerelement fett formatiert ist (nur Laufzeit).<br/>                                  |
| [**Selcharoffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ruft ab oder legt fest, ob Text im InkEdit-Steuerelement in der Baseline, als superskript oder als Index (nur Laufzeit) angezeigt wird.<br/>                                             |
| [**Selcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ruft die Textfarbe der aktuellen Textauswahl oder Einfügemarke ab oder legt Sie fest (nur Lauf Zeit).<br/>                                                                              |
| [**Selfontname**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ruft den Schriftart Namen des ausgewählten Texts innerhalb des InkEdit-Steuer Elements ab oder legt ihn fest (nur Laufzeit).<br/>                                                                                |
| [**Selfontsize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ruft den Schrift Grad des ausgewählten Texts innerhalb des InkEdit-Steuer Elements ab oder legt ihn fest (nur Laufzeit).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ruft das Array der eingebetteten [**InkDisp**](inkdisp-class.md) -Objekte (sofern als frei Hand Eingabe angezeigt) ab, die die aktuelle Auswahl enthält, oder legt dieses fest.<br/>                                     |
| [**Selinksdisplaymode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ruft einen Wert ab oder legt einen Wert fest, mit dem die Darstellung der Auswahl zwischen frei Hand Eingaben und Text aktiviert werden kann.<br/>                                                                            |
| [**Selitalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im InkEdit-Steuerelement kursiv formatiert ist (nur Laufzeit).<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ruft die Anzahl der Zeichen ab, die im InkEdit-Steuerelement ausgewählt werden (nur Laufzeit), oder legt diese fest.<br/>                                                                            |
| [**Selrtf**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ruft den derzeit ausgewählten RTF (Rich Text Format)-formatierten Text im InkEdit-Steuerelement ab oder legt ihn fest (nur Laufzeit).<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ruft den Anfangspunkt des Texts ab, der im Textfeld (nur Laufzeit) ausgewählt ist, oder legt diesen fest.<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ruft den markierten Text innerhalb des InkEdit-Steuer Elements ab oder legt ihn fest (nur Lauf Zeit).<br/>                                                                                                 |
| [**Selunter Streichung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im InkEdit-Steuerelement unterstrichen ist (nur Laufzeit).<br/>                            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ruft einen Wert ab, der angibt, ob sich das InkEdit-Steuerelement im Leerlauf befindet, frei Hand Eingaben sammelt oder frei Hand Eingaben erkennt (nur Laufzeit).<br/>                                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ruft den aktuellen Text im Textfeld ab oder legt diesen fest.<br/>                                                                                                                             |
| [**Textrtf**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ruft den Text des InkEdit-Steuer Elements ab, einschließlich aller RTF-Codes, oder legt diesen fest.<br/>                                                                                                     |
| [**Usemoueinforinput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ruft einen Wert ab, der angibt, ob die Maus als Eingabegerät verwendet werden kann, oder legt diesen fest.<br/>                                                                                      |



 



| Struktur                                                                    | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IEC \_ strokeinfo**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Enthält Informationen zu einem [**Stroke**](inkedit-stroke.md) -Ereignis (nur Win32).<br/> |
| [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Enthält Informationen über eine bestimmte Geste (nur Win32).<br/>                       |
| [**IEC- \_ erkentionresultinfo**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Enthält Informationen zu einem Erkennungs Ergebnis (nur Win32).<br/>                     |



 

## <a name="com-implementation"></a>COM-Implementierung

Dieses Objekt implementiert die **iinkedit** -com-Schnittstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[InkPicture-Steuerelement Verweis](inkpicture-control-reference.md)
</dt> <dt>

[**Inkrecognizercontext-Klasse**](inkrecognizercontext-class.md)
</dt> </dl>

 

