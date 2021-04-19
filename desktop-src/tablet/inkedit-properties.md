---
description: Dieser Abschnitt enthält die Eigenschaften, die zum InkEdit-Steuerelement gehören.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: InkEdit-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360609"
---
# <a name="inkedit-properties"></a>InkEdit-Eigenschaften

Dieser Abschnitt enthält die Eigenschaften, die zum InkEdit-Steuerelement gehören.



| Eigenschaft                                                 | BESCHREIBUNG                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Darstellung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ruft einen Wert ab, der bestimmt, ob das [InkEdit](inkedit-control-reference.md) -Steuerelement flach oder 3D angezeigt wird, oder legt diesen fest.<br/>                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ruft die Hintergrundfarbe für das [InkEdit](inkedit-control-reference.md) -Steuerelement ab oder legt diese fest.<br/>                                                                                                 |
| [**Rahmenart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ruft einen Wert ab, der bestimmt, ob das [InkEdit](inkedit-control-reference.md) -Steuerelement einen Rahmen hat, oder legt ihn fest<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ruft einen Wert ab, der bestimmt, ob Bild Lauf leisten im [InkEdit](inkedit-control-reference.md) -Steuerelement deaktiviert sind, oder legt diesen fest.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ruft die Zeichnungs Attribute für frei Hand Eingaben ab, die auf dem [InkEdit](inkedit-control-reference.md) -Steuerelement noch gezeichnet werden sollen, oder legt diese fest.<br/>                                                                |
| [**Aktiviert**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ruft einen Wert ab, der bestimmt, ob das [InkEdit](inkedit-control-reference.md) -Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.<br/>                                                     |
| [**Faktoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Dient zum Abrufen oder Festlegen der [Faktoid](factoid-constants.md) -Konstante, die ein [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt verwendet, um die Suche nach dem Erkennungs Ergebnis einzuschränken.<br/>                  |
| [**Raster**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ruft die Schriftart des Texts ab, der vom [InkEdit](inkedit-control-reference.md) -Steuerelement angezeigt wird, oder legt diese fest.<br/>                                                                                       |
| [**HWND**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ruft das Fenster Handle ab, an das das [**InkDisp**](inkdisp-class.md) -Steuerelement gebunden ist.<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie frei Hand Eingaben in das [InkEdit](inkedit-control-reference.md) -Steuerelement eingefügt werden.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die frei Hand Auflistung deaktiviert ist, frei Hand Eingaben gesammelt oder frei Hand Eingaben und Gesten gesammelt werden<br/>                                                                |
| [**Gesperrt**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ruft einen Wert ab, der angibt, ob das [InkEdit](inkedit-control-reference.md) -Steuerelement schreibgeschützt ist oder nicht, oder legt diesen fest.<br/>                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ruft einen Wert ab, der angibt, ob ein [InkEdit](inkedit-control-reference.md) -Steuerelement eine maximale Anzahl von Zeichen enthalten kann, oder legt diesen fest. wenn dies der Fall ist, wird die maximale Anzahl von Zeichen<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.<br/>                                                                                                                                                 |
| [**Mouum Zeiger**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Dient zum Abrufen oder Festlegen eines Werts, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich der Mauszeiger über einem bestimmten Teil des [InkEdit](inkedit-control-reference.md) -Steuer Elements befindet<br/>                |
| [**Mehrzeiligen**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ruft einen Wert ab, der angibt, ob es sich um ein mehrzeilige [InkEdit](inkedit-control-reference.md) -Steuerelement handelt.<br/>                                                                           |
| [**Erkennungs Timeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ruft die Zeitspanne (in Millisekunden) zwischen dem letzten erfassten [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt und dem Anfang der Texterkennung ab oder legt diese fest.<br/>                         |
| [**Erkennung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ruft das für die Erkennung zu verwendende [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt ab oder legt es fest.<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ruft den Typ der Scrollleisten ab, die im [InkEdit](inkedit-control-reference.md) -Steuerelement angezeigt werden, oder legt ihn fest.<br/>                                                                                   |
| [**Selalignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ruft die Ausrichtung ab, die auf die aktuelle Auswahl oder Einfügemarke angewendet werden soll (nur Laufzeit), oder legt diese fest.<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im [InkEdit](inkedit-control-reference.md) -Steuerelement fett formatiert ist (nur Laufzeit).<br/>                  |
| [**Selcharoffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ruft ab oder legt fest, ob Text im [InkEdit](inkedit-control-reference.md) -Steuerelement in der Baseline, als superskript oder als Index (nur Laufzeit) angezeigt wird.<br/>                             |
| [**Selcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ruft die Textfarbe der aktuellen Textauswahl oder Einfügemarke ab oder legt Sie fest (nur Lauf Zeit).<br/>                                                                                               |
| [**Selfontname**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ruft den Schriftart Namen des ausgewählten Texts innerhalb des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab oder legt ihn fest (nur Laufzeit).<br/>                                                                |
| [**Selfontsize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ruft den Schrift Grad des ausgewählten Texts innerhalb des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab oder legt ihn fest (nur Laufzeit).<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ruft das Array der eingebetteten [**InkDisp**](inkdisp-class.md) -Objekte (sofern als frei Hand Eingabe angezeigt) ab, die die aktuelle Auswahl enthält, oder legt dieses fest.<br/>                                                      |
| [**Selinksdisplaymode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ruft einen Wert ab oder legt einen Wert fest, mit dem die Darstellung der Auswahl zwischen frei Hand Eingaben und Text aktiviert werden kann.<br/>                                                                                             |
| [**Selitalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im [InkEdit](inkedit-control-reference.md) -Steuerelement kursiv formatiert ist (nur Laufzeit).<br/>                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ruft die Anzahl der Zeichen ab, die im [InkEdit](inkedit-control-reference.md) -Steuerelement ausgewählt werden (nur Laufzeit), oder legt diese fest.<br/>                                                            |
| [**Selrtf**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ruft den derzeit ausgewählten RTF (Rich Text Format)-formatierten Text im [InkEdit](inkedit-control-reference.md) -Steuerelement ab oder legt ihn fest (nur Laufzeit).<br/>                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ruft den Anfangspunkt des Texts ab, der im Textfeld (nur Laufzeit) ausgewählt ist, oder legt diesen fest.<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ruft den markierten Text innerhalb des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab oder legt ihn fest (nur Lauf Zeit).<br/>                                                                                 |
| [**Selunter Streichung**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Schriftart Stil des aktuell ausgewählten Texts im [InkEdit](inkedit-control-reference.md) -Steuerelement unterstrichen ist (nur Laufzeit).<br/>            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ruft einen Wert ab, der angibt, ob sich das [InkEdit](inkedit-control-reference.md) -Steuerelement im Leerlauf befindet, frei Hand Eingaben sammelt oder frei Hand Eingaben erkennt (nur Laufzeit).<br/>                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ruft den aktuellen Text im Textfeld ab oder legt diesen fest.<br/>                                                                                                                                              |
| [**Textrtf**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ruft den Text des [InkEdit](inkedit-control-reference.md) -Steuer Elements ab, einschließlich aller RTF-Codes, oder legt diesen fest.<br/>                                                                                     |
| [**Usemoueinforinput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ruft einen Wert ab, der angibt, ob die Maus als Eingabegerät verwendet werden kann, oder legt diesen fest.<br/>                                                                                                       |



 

 

 




