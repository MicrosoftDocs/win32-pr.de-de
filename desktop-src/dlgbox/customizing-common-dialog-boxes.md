---
title: Anpassen von allgemeinen Dialogfeldern
description: In diesem Thema wird erläutert, wie allgemeine Dialogfelder verwendet werden.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Allgemeine Dialogfeldbibliothek, Anpassen
- Allgemeine Dialogfelder, Anpassen
- Anpassen gängiger Dialogfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6272cbff88b7544ea945851f4f347cb43031b93ae08852bc139c7fb7ca6dd91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786120"
---
# <a name="customizing-common-dialog-boxes"></a>Anpassen von allgemeinen Dialogfeldern

Sie können die allgemeinen Dialogfelder in ihrer Standardform verwenden oder sie anpassen. Aus Sicht des Benutzers besteht der Hauptvorteil des allgemeinen Dialogfelds in der konsistenten Darstellung und Funktionalität von Anwendung zu Anwendung. Daher ist es wichtig, ein allgemeines Dialogfeld nur anzupassen, wenn es für eine Anwendung unbedingt erforderlich ist. Andernfalls gehen die konsistente Darstellung und die einfache Codierungsschnittstelle verloren. Geeignete Anpassungen lassen so viele der ursprünglichen Steuerelemente wie möglich erhalten. Das Erhöhen der Größe des Dialogfelds oder das Hinzufügen neuer Steuerelemente in dem bereich, der bereits im Dialogfeld verfügbar ist, ist eine geeignete Anpassung. Das Ausblenden ursprünglicher Steuerelemente oder eine anderweitige Änderung der beabsichtigten Funktionalität der ursprünglichen Steuerelemente ist eine weniger geeignete Anpassung.

In diesem Abschnitt werden die folgenden Methoden zum Anpassen eines allgemeinen Dialogfelds erläutert:

-   [Benutzerdefinierte Vorlagen](#custom-templates)
-   [Hook-Prozeduren für allgemeine Dialogfelder](#hook-procedures-for-common-dialog-boxes)
-   [Allgemeine Dialogmeldungen](#common-dialog-messages)
-   [Hilfesupport](#help-support)
    -   [Kontextorientierte Hilfe](#context-sensitive-help)
    -   [Schaltfläche "Hilfe"](#the-help-button)

## <a name="custom-templates"></a>Benutzerdefinierte Vorlagen

Allgemeine Dialogfelder verfügen über Standardvorlagen, die die Anzahl, den Typ und die Position der Standardsteuerelemente im Dialogfeld definieren. Sie können eine benutzerdefinierte Vorlage definieren, um Benutzern Zugriff auf zusätzliche Steuerelemente zu geben, die für Ihre Anwendung eindeutig sind.

Für alle gängigen Dialogfelder  mit  Ausnahme der Dialogfelder Öffnen und Speichern unter im Explorer-Stil ändern Sie die Standardvorlage, um eine benutzerdefinierte Vorlage zu erstellen, die die Standardvorlage ersetzt. Die benutzerdefinierte Vorlage definiert den Typ und die Position der Standardsteuerelemente sowie alle zusätzlichen Steuerelemente.

Wenn Sie eine benutzerdefinierte Dialogfeldvorlage erstellen, indem Sie die Standarddialogfeldvorlage ändern, stellen Sie sicher, dass die Bezeichner für alle hinzugefügten Steuerelemente eindeutig sind und nicht mit den Bezeichnern der Standardsteuerelemente in Konflikt stehen. In der folgenden Tabelle sind der Name der Standardvorlagendatei und die Includedatei für jeden der allgemeinen Dialogfeldtypen aufgeführt.



| Dialogfeldtyp               | Vorlagendatei | Includedatei |
|-------------------------------|---------------|--------------|
| **Farbe**                     | Color.dlg     | ColorDlg.h   |
| **Suchen**                      | Findtext.dlg  | Dlgs.h       |
| **Schriftart**                      | Font.dlg      | Dlgs.h       |
| **Öffnen** (Mehrfachauswahl) | Fileopen.dlg  | Dlgs.h       |
| **Öffnen** (Einzelauswahl)   | Fileopen.dlg  | Dlgs.h       |
| **Seiteneinrichtung**                | Prnsetup.dlg  | Dlgs.h       |
| **Drucken**                     | Prnsetup.dlg  | Dlgs.h       |
| **Drucksetup** (veraltet)    | Prnsetup.dlg  | Dlgs.h       |
| **Replace**                   | Findtext.dlg  | Dlgs.h       |



 

Um eine benutzerdefinierte Vorlage zu aktivieren, müssen Sie im **Flags-Member** der entsprechenden Struktur für das Dialogfeld ein Flag festlegen. Wenn die Vorlage eine Ressource in einer Anwendung oder Dynamic Link Library ist, legen Sie ein **ENABLETEMPLATE-Flag** im **Flags-Element** fest, und verwenden Sie die **Elemente hInstance** und **lpTemplateName** der Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn sich die Vorlage bereits im Arbeitsspeicher befindet, legen Sie ein **ENABLETEMPLATEHANDLE-Flag** im **Flags-Element** fest, und verwenden Sie den **hInstance-Member,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

In den meisten Fällen müssen Sie auch eine Hookprozedur für das Dialogfeld aktivieren, um Eingaben für die zusätzlichen Steuerelemente in Ihrer benutzerdefinierten Vorlage zu unterstützen und zu verarbeiten.

Für die Dialogfelder **Öffnen** und **Speichern unter** im Explorer-Stil sind die Standardvorlagen nicht zur Änderung verfügbar. Stattdessen definiert Ihre benutzerdefinierte Vorlage ein untergeordnetes Dialogfeld, das nur die Elemente enthält, die dem Standarddialogfeld hinzugefügt werden sollen. Die benutzerdefinierte Vorlage kann auch ein statisches Steuerelement definieren, das den Speicherort des Clusters von Standardsteuerelementen im untergeordneten Dialogfeld angibt. Weitere Informationen finden Sie unter [Benutzerdefinierte Vorlagen im Explorer-Stil.](open-and-save-as-dialog-boxes.md)

## <a name="hook-procedures-for-common-dialog-boxes"></a>Hook-Prozeduren für allgemeine Dialogfelder

Für jedes der allgemeinen Dialogfelder können Sie eine Hookprozedur aktivieren, um Nachrichten aus der Standarddialogfeldprozedur zu verarbeiten. Es gibt zwei allgemeine Typen allgemeiner Dialoghook-Prozeduren:

-   Die standardmäßige Hookprozedur, die mit den gängigsten Dialogfeldern verwendet wird
-   Hookprozedur im Explorer-Stil, die von den Dialogfeldern **Öffnen** **und Speichern unter** unterstützt wird

Wenn Sie eine Standardhookprozedur für eines der allgemeinen Dialogfelder bereitstellen, verarbeitet die Standarddialogfeldprozedur die Meldungen wie folgt.



| `Message`                                 | Verarbeitung                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](wm-initdialog.md) | Die Standardprozedur des Dialogfelds verarbeitet die Nachricht, bevor sie an die Hookprozedur übergeben wird. Der *lParam-Parameter der Nachricht* ist ein Zeiger auf die Initialisierungsstruktur, die beim Erstellen des Dialogs angegeben wurde. |
| Alle anderen Nachrichten                      | Die Hookprozedur empfängt zuerst die Meldung. Anschließend bestimmt der Rückgabewert der Hookprozedur, ob die Standarddialogprozedur die Nachricht verarbeitet oder ignoriert.                                     |



 

Für die Dialogfelder **Öffnen** und Speichern **unter** im Explorer-Stil werden von der Hookprozedur keine Nachrichten empfangen, die für die Standardsteuerelemente im Dialogfeld vorgesehen sind. Stattdessen empfängt sie Benachrichtigungsmeldungen aus dem Dialogfeld und Meldungen für alle zusätzlichen Steuerelemente, die Sie in einer benutzerdefinierten Vorlage definiert haben. Weitere Informationen finden Sie unter [Hook-Prozeduren im Explorer-Stil.](open-and-save-as-dialog-boxes.md)

Um eine Hookprozedur zu aktivieren, legen Sie einen **ENABLEHOOK-Wert** im **Flags-Member** der entsprechenden -Struktur für das Dialogfeld fest. Wenn ein **ENABLEHOOK-Flag** festgelegt ist, muss ein **lpfnHook-Member** der -Struktur die Adresse der Hookprozedur angeben.

Die folgende Tabelle zeigt den Typ der Hookprozedur, die für jedes der allgemeinen Dialogfelder angegeben werden soll.



| Dialogfeldtyp                          | Hookprozedur                                      |
|------------------------------------------|-----------------------------------------------------|
| **Farbe**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Suchen** oder **Ersetzen**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Schriftart**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Öffnen** oder **Speichern unter** (Explorer-Format) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Öffnen** oder **Speichern unter** (altes Format)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Drucken**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Seiteneinrichtung**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Im Dialogfeld **Seiteneinrichtung** können Sie auch eine [*PagePaintHook-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) angeben. Dies ist eine spezielle Hookprozedur, mit der Sie die Darstellung der Beispielseite anpassen können, die im Dialogfeld **Seiteneinrichtung** angezeigt wird.

> [!Note]  
> Das Dialogfeld **Druckeinrichtung** wurde durch das Dialogfeld **Seiteneinrichtung** ersetzt. Anwendungen sollten das Dialogfeld **Seiteneinrichtung** verwenden. Aus Kompatibilitätsgründen unterstützt die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) jedoch weiterhin die Anzeige des Dialogfelds **Druckeinrichtung.** Sie können eine [*SetupHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) für das Dialogfeld **Setup drucken** bereitstellen.

 

## <a name="common-dialog-messages"></a>Allgemeine Dialogfeldmeldungen

Allgemeine Dialogfelder verwenden Meldungen, um Ihre Fensterprozedur oder Hookprozedur zu benachrichtigen, wenn bestimmte Ereignisse auftreten. Darüber hinaus gibt es Nachrichten, die Sie an ein allgemeines Dialogfeld senden können, um Informationen abzurufen oder das Verhalten oder die Darstellung des Dialogfelds zu steuern. In diesem Abschnitt werden die allgemeinen Dialogfeldmeldungen beschrieben, die von der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) registriert werden, die vom Dialogfeld **Schriftart** und vom Dialogfeld **Seiteneinrichtung** verwendeten Meldungen sowie die Meldungen, die von den Dialogfeldern **Öffnen** und **Speichern unter** im Explorer-Stil verwendet werden.

Die Common Dialog Box Library definiert einen Satz von Meldungszeichenfolgen. Sie können eine Konstante, die einer dieser Nachrichtenzeichenfolgen zugeordnet ist, an [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) übergeben, um einen Nachrichtenbezeichner abzurufen. Anschließend können Sie den Bezeichner verwenden, um Nachrichten zu erkennen und zu verarbeiten, die von einem allgemeinen Dialogfeld gesendet werden, oder um Nachrichten an ein allgemeines Dialogfeld zu senden. Die folgende Tabelle zeigt die Nachrichtenkonstanten und beschreibt deren Verwendung.



| Contants                               | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Ein Dialogfeld **Farbe** sendet diese Meldung an die Hookprozedur, wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche **OK** klickt. Die Hookprozedur kann die Farbe akzeptieren oder ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Ein Dialogfeld **Öffnen** oder **Speichern unter** sendet diese Meldung an die Hookprozedur, wenn der Benutzer einen Dateinamen auswählt und auf die Schaltfläche **OK** klickt. Die Hookprozedur kann den Dateinamen akzeptieren oder ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt. In den Dialogfeldern **Öffnen** und **Speichern** unter im Explorer-Stil wurde diese Meldung durch die [**CDN FILEOK-Benachrichtigungsmeldung \_**](cdn-fileok.md) ersetzt.<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Ein Dialogfeld **Suchen** oder **Ersetzen** sendet diese Meldung an die Fensterprozedur des übergeordneten Fensters, wenn der Benutzer auf **"Weiter suchen",** **"Ersetzen"** oder **"Alle ersetzen"** klickt oder das Dialogfeld schließt. Der *lParam-Parameter* der Nachricht ist ein Zeiger auf eine [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) die die Eingabe des Benutzers enthält.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Alle gängigen Dialogfelder senden diese Meldung an die Fensterprozedur des übergeordneten Fensters, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt. In den Dialogfeldern **Öffnen** und **Speichern** unter im Explorer-Stil wurde diese Meldung durch die [**CDN HILFE-Benachrichtigungsmeldung \_**](cdn-help.md) ersetzt.<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Ein Dialogfeld **Öffnen** oder **Speichern unter** sendet diese Meldung an die Hookprozedur, wenn der Benutzer die Auswahl im Listenfeld **Dateiname** ändert. In den Dialogfeldern **Öffnen** und **Speichern unter** im Explorer-Stil wurde diese Meldung durch die [**CDN SELCHANGE-Benachrichtigungsmeldung \_**](cdn-selchange.md) ersetzt.<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Eine Hookprozedur kann diese Nachricht an ein Dialogfeld **Farbe** senden, um die aktuelle Farbauswahl festzulegen.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Ein Dialogfeld **Öffnen** oder **Speichern unter** sendet diese Meldung an die Hookprozedur, wenn eine Freigabeverletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt. In den Dialogfeldern **Öffnen** und **Speichern unter** im Explorer-Stil wurde diese Meldung durch die Benachrichtigungsmeldung [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md) ersetzt.<br/>                                                        |



 

Einige gängige Dialogfelder senden und empfangen andere Fenstermeldungen. Die Hookprozedur für **ein** Schriftartdialogfeld kann alle **WM \_ CHOOSEFONT \_ \* *_-Meldungen an das*** Dialogfeld _Font senden. Weitere Informationen finden Sie unter [Schriftartdialogfeld.](font-dialog-box.md) Im Dialogfeld **Seiteneinrichtung** werden die Meldungen **WM \_ PSD \_ \** _ gesendet, wenn Sie eine [_PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Hookprozedur aktiviert haben. Weitere Informationen finden Sie unter [Dialogfeld "Seiteneinrichtung".](page-setup-dialog-box.md)

Die Dialogfelder **Öffnen** und **Speichern unter** im Explorer-Stil unterstützen eine Reihe vordefinierter Nachrichten. Dazu gehören Benachrichtigungsmeldungen, die in Form einer [**WM \_ NOTIFY-Nachricht**](../controls/wm-notify.md) an Ihre Hookprozedur gesendet werden, und Nachrichten, die ihre Hookprozedur an das Dialogfeld senden kann. Eine vollständige Liste dieser Meldungen finden Sie unter Hookprozes im [Explorer-Stil.](open-and-save-as-dialog-boxes.md)

## <a name="help-support"></a>Hilfeunterstützung

Allgemeine Dialogfelder bieten kontextbezogene Hilfe für die Standardsteuerelemente des Dialogfelds. Um zusätzliche Hilfe für ein allgemeines Dialogfeld bereitzustellen, können Sie eine **Hilfeschaltfläche** anzeigen und Nachrichten verarbeiten, die generiert werden, wenn der Benutzer auf die Schaltfläche klickt. Die Schaltfläche **Hilfe** ist eine Ergänzung zur standardmäßigen kontextbezogenen Hilfe. Die Schaltfläche **Hilfe** ist nützlich, um den allgemeinen Zweck des Dialogfelds für Ihre Anwendung zu beschreiben.

-   [Kontextbezogene Hilfe](#context-sensitive-help)
-   [Schaltfläche "Hilfe"](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive-Hilfe

Alle gängigen Dialogfelder bieten kontextbezogene Hilfe für die Standardsteuerelemente des Dialogfelds. Der Benutzer kann hilfe für einzelne Steuerelemente mit einer der folgenden Methoden anzeigen:

-   Wählen Sie das Steuerelement aus, und drücken Sie F1.
-   Klicken Sie auf **?** -Schaltfläche in der Titelleiste und anschließendes Klicken auf ein Steuerelement.
-   Klicken sie mit der rechten Maustaste über ein Steuerelement.

Wenn Sie ein Dialogfeld anpassen, indem Sie neue Steuerelemente hinzufügen, müssen Sie auch die Hilfeunterstützung für diese Steuerelemente erweitern, indem Sie Anforderungen für Hilfe in der Hookprozedur verarbeiten. Die Hookprozedur empfängt die folgenden Nachrichten, wenn der Benutzer Hilfe anfordert.



| Benutzeraktion                                                           | `Message`                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Klicken Sie mit der rechten Maustaste auf ein Steuerelement.                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| Drücken Sie F1.                                                   | [**\_WM-HILFE**](../shell/wm-help.md)               |
| Klicken Sie auf **?** klicken Sie auf der Titelleiste auf ein Steuerelement. | [**\_WM-HILFE**](../shell/wm-help.md)               |



 

Sie sollten diese Nachrichten für die hinzugefügten Steuerelemente verarbeiten, aber lassen Sie die Standarddialogfeldprozedur die Meldungen für die Standardsteuerelemente verarbeiten. Weitere Informationen zum Verarbeiten dieser Nachrichten finden Sie unter [Hilfe.](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85))

### <a name="the-help-button"></a>Schaltfläche "Hilfe"

Sie können eine **Hilfeschaltfläche** in einem der allgemeinen Dialogfelder anzeigen, indem Sie einen **SHOWHELP-Wert** im Flags-Member der **Initialisierungsstruktur** für das Dialogfeld festlegen. Wenn Sie die Schaltfläche **Hilfe** anzeigen, müssen Sie die Hilfeanforderung des Benutzers verarbeiten. Die Verarbeitung kann entweder in einer der Fensterprozesen Ihrer Anwendung oder in einer Hookprozedur für das Dialogfeld erfolgen. In der Regel würden Sie die Hilfeanforderung verarbeiten, indem Sie die [**WinHelp-Funktion**](/windows/win32/api/winuser/nf-winuser-winhelpa) aufrufen.

Um Hilfenachrichten in einer Ihrer Fensterprozesuren zu verarbeiten, müssen Sie einen Meldungsbezeichner für die Zeichenfolge abrufen, die durch den [**HELPMSGSTRING-Wert**](helpmsgstring.md) definiert ist, und das Fenster identifizieren, das Nachrichten empfangen soll. Um den Nachrichtenbezeichner abzurufen, geben Sie **HELPMSGSTRING** als Parameter in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) an. Verwenden Sie beim Erstellen des Dialogfelds den **Member hwndOwner** der Initialisierungsstruktur des Dialogfelds, um das Fenster zu identifizieren, das die Nachrichten empfangen soll. Die Dialogfeldprozedur sendet die Meldung an die Fensterprozedur, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.

Um Hilfenachrichten in einer Hookprozedur zu verarbeiten, sollten Sie die [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) verarbeiten. Die Hookprozedur bietet Hilfe, wenn der *wParam-Parameter* dieser Meldung angibt, dass der Benutzer auf die Schaltfläche **Hilfe** geklickt hat. Der Bezeichner der **Schaltfläche Hilfe** ist die **pshHelp-Konstante,** die in der Datei Dlgs.h definiert ist.

Hookprozes für die Dialogfelder **Öffnen** und **Speichern unter** im Explorer-Stil erhalten keine [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) für die **Schaltfläche Hilfe.** Stattdessen sendet das Dialogfeld eine [**CDN HELP-Benachrichtigungsmeldung \_**](cdn-help.md) an die Hookprozedur, wenn auf die Schaltfläche **Hilfe** geklickt wird.

 

