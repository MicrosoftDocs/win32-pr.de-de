---
title: ComboBoxEx-Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit ComboBoxEx-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded6ff945424f63baaf0063ce5d8897f84883d5063989aa6c7a9fb1a4f76a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413463"
---
# <a name="comboboxex-control"></a>ComboBoxEx-Steuerelement

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit ComboBoxEx-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                                | Inhalte                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md) | ComboBoxEx-Steuerelemente sind Kombinationsfeld-Steuerelemente, die native Unterstützung für Elementbilder bereitstellen.<br/> |
| [Verwenden von ComboBoxEx-Steuerelementen](using-comboboxex.md)    | Dieser Abschnitt enthält Beispielcode und Informationen zur Verwendung von ComboBoxEx-Steuerelementen.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                                   | Inhalte                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Entfernt ein Element aus einem ComboBoxEx-Steuerelement. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Ruft das Handle für das untergeordnete Kombinationsfeld-Steuerelement ab. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Ruft das Handle für den Bearbeitungssteuerteil eines ComboBoxEx-Steuerelements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den [**CBS-DROPDOWN-Stil \_ festgelegt**](combo-box-styles.md) ist. <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | Ruft die erweiterten Stile ab, die für ein ComboBoxEx-Steuerelement verwendet werden. <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | Ruft das Handle für eine Bildliste ab, die einem ComboBoxEx-Steuerelement zugewiesen ist. <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | Ruft Elementinformationen für ein bestimmtes ComboBoxEx-Element ab.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Ruft das Unicode-Zeichenformatflag für das Steuerelement ab. <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungssteuerfelds geändert hat.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Fügt ein neues Element in ein ComboBoxEx-Steuerelement ein. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Diese Meldung ist nicht implementiert. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Diese Meldung ist nicht implementiert. <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuerelements fest. <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Legt das UNICODE-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Legt den visuellen Stil eines ComboBoxEx-Steuerelements fest.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                      | Inhalte                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Wird gesendet, wenn der Benutzer die Dropdownliste aktiviert oder auf das Bearbeitungsfeld des Steuerelements klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Wird gesendet, wenn ein Element gelöscht wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsteil des Steuerelements angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungsfelds abgeschlossen hat oder ein Element aus der Dropdownliste des Steuerelements ausgewählt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | Wird gesendet, um Anzeigeinformationen zu einem Rückrufelement abzurufen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Wird gesendet, wenn ein neues Element in das -Steuerelement eingefügt wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuerelements, dass das -Steuerelement den Cursor als Reaktion auf eine [**WM \_ SETCURSOR-Meldung anordnt.**](/windows/desktop/menurc/wm-setcursor) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |



 

### <a name="structures"></a>Strukturen



| Thema                                    | Inhalte                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Enthält Informationen zu einem Element in einem ComboBoxEx-Steuerelement.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Enthält Informationen, die mit dem [CBEN \_ DRAGBEGIN-Benachrichtigungscode](cben-dragbegin.md) verwendet werden. <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Enthält Informationen zum Abschluss eines Bearbeitungsvorgang innerhalb eines ComboBoxEx-Steuerelements. Diese Struktur wird mit dem [CBEN \_ ENDEDIT-Benachrichtigungscode](cben-endedit.md) verwendet. <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Enthält Spezifische Informationen zu ComboBoxEx-Elementen zur Verwendung mit Benachrichtigungscodes. <br/>                                                                                               |



 

### <a name="constants"></a>Konstanten



| Thema                                                                        | Inhalte                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Erweiterte Stile des ComboBoxEx-Steuerelements](comboboxex-control-extended-styles.md) | Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standarden Kombinationsfeld-Steuerelementstile.<br/> |



 

 

