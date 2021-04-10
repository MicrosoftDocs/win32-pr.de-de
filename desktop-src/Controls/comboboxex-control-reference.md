---
title: ComboBoxEx-Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit ComboBoxEx-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a926ccf2f9f5b5bb68e040731d6b9d8e37ee8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961367"
---
# <a name="comboboxex-control"></a>ComboBoxEx-Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit ComboBoxEx-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                | Inhalte                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md) | ComboBoxEx-Steuerelemente sind Kombinations Feld-Steuerelemente, die native Unterstützung für Element Bilder bereitstellen.<br/> |
| [Verwenden von ComboBoxEx-Steuerelementen](using-comboboxex.md)    | Dieser Abschnitt enthält Beispielcode und Informationen zur Verwendung von ComboBoxEx-Steuerelementen.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                                   | Inhalte                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DeleteItem**](cbem-deleteitem.md)             | Entfernt ein Element aus einem ComboBoxEx-Steuerelement. <br/>                                                                                                                                                     |
| [**CBEM \_ getcombocontrol**](cbem-getcombocontrol.md)   | Ruft das Handle für das untergeordnete Kombinations Feld-Steuerelement ab. <br/>                                                                                                                                                |
| [**CBEM \_ geteditcontrol**](cbem-geteditcontrol.md)     | Ruft das Handle für den Bearbeitungs Steuerelement Teil eines ComboBoxEx-Steuer Elements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den [**CBS- \_ Dropdown**](combo-box-styles.md) Stil festgelegt ist. <br/> |
| [**CBEM \_ GetExtendedStyle**](cbem-getextendedstyle.md) | Ruft die erweiterten Stile ab, die für ein ComboBoxEx-Steuerelement verwendet werden. <br/>                                                                                                                             |
| [**CBEM \_ GetImageList**](cbem-getimagelist.md)         | Ruft das Handle für eine Bildliste ab, die einem ComboBoxEx-Steuerelement zugewiesen ist. <br/>                                                                                                                             |
| [**CBEM- \_ GetItem**](cbem-getitem.md)                   | Ruft Element Informationen für ein bestimmtes ComboBoxEx-Element ab.<br/>                                                                                                                                              |
| [**CBEM \_ getunicodeformat**](cbem-getunicodeformat.md) | Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. <br/>                                                                                                                                        |
| [**CBEM \_ haseditchanged**](cbem-haseditchanged.md)     | Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungs Steuer Elements geändert hat.<br/>                                                                                                                  |
| [**CBEM \_ InsertItem**](cbem-insertitem.md)             | Fügt ein neues Element in einem ComboBoxEx-Steuerelement ein. <br/>                                                                                                                                                    |
| [**CBEM- \_ killcombofocus**](cbem-killcombofocus.md)     | Diese Meldung ist nicht implementiert. <br/>                                                                                                                                                               |
| [**CBEM \_ setcombofocus**](cbem-setcombofocus.md)       | Diese Meldung ist nicht implementiert. <br/>                                                                                                                                                               |
| [**CBEM- \_ textendedstyle**](cbem-setextendedstyle.md) | Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuer Elements fest. <br/>                                                                                                                                              |
| [**CBEM \_ SetImageList**](cbem-setimagelist.md)         | Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest. <br/>                                                                                                                                                   |
| [**CBEM \_ -Element**](cbem-setitem.md)                   | Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest. <br/>                                                                                                                                       |
| [**CBEM- \_ Code Format**](cbem-setunicodeformat.md) | Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen. <br/>      |
| [**CBEM \_ SetWindowTheme**](cbem-setwindowtheme.md)     | Legt den visuellen Stil eines ComboBoxEx-Steuer Elements fest.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                      | Inhalte                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cben \_ BeginEdit](cben-beginedit.md)                      | Wird gesendet, wenn der Benutzer die Dropdown Liste aktiviert oder in das Bearbeitungsfeld des Steuer Elements klickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                    |
| [cben \_ DeleteItem](cben-deleteitem.md)                    | Wird gesendet, wenn ein Element gelöscht wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                                     |
| [cben \_ dragbegin](cben-dragbegin.md)                      | Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsbereich des Steuer Elements angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                  |
| [cben \_ EndEdit](cben-endedit.md)                          | Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungs Felds abgeschlossen hat oder ein Element aus der Dropdown Liste des Steuer Elements ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                             |
| [cben \_ getdispinfo](cben-getdispinfo.md)                  | Wird gesendet, um Anzeigeinformationen zu einem Rückruf Element abzurufen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                             |
| [cben \_ InsertItem](cben-insertitem.md)                    | Wird gesendet, wenn ein neues Element in das Steuerelement eingefügt wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/>                                                                                                  |
| [NM \_ setcursor (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuer Elements, dass das-Steuerelement den Cursor als Antwort auf eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht festlegt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |



 

### <a name="structures"></a>Strukturen



| Thema                                    | Inhalte                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Enthält Informationen zu einem Element in einem ComboBoxEx-Steuerelement.<br/>                                                                                                                       |
| [**Nmcbedragbegin**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Enthält Informationen, die mit dem [cben \_ dragbegin](cben-dragbegin.md) -Benachrichtigungs Code verwendet werden. <br/>                                                                                      |
| [**Nmcbeendedit**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Enthält Informationen zum Abschluss eines Bearbeitungsvorgangs innerhalb eines ComboBoxEx-Steuer Elements. Diese Struktur wird mit dem [cben \_ EndEdit](cben-endedit.md) -Benachrichtigungs Code verwendet. <br/> |
| [**Nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Enthält Informationen, die speziell für ComboBoxEx-Elemente zur Verwendung mit Benachrichtigungs Codes gelten. <br/>                                                                                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                                        | Inhalte                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Erweiterte Stile des ComboBoxEx-Steuer Elements](comboboxex-control-extended-styles.md) | Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten Standardformate für Kombinations Feld-Steuerelemente.<br/> |



 

 

