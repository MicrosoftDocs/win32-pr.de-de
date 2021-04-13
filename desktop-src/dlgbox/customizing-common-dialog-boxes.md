---
title: Anpassen von allgemeinen Dialog Feldern
description: In diesem Thema wird erläutert, wie allgemeine Dialogfelder verwendet werden.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Allgemeine Dialog Feld Bibliothek, anpassen
- Allgemeine Dialogfelder, anpassen
- Anpassen von allgemeinen Dialogfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7eaa71c4f6fc6aa038ef150eb53935f6b3ec280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390908"
---
# <a name="customizing-common-dialog-boxes"></a>Anpassen von allgemeinen Dialog Feldern

Sie können die Standard Dialogfelder in ihrer Standardform verwenden, oder Sie können Sie anpassen. Aus Sicht des Benutzers ist der Hauptvorteil des allgemeinen Dialog Felds die konsistente Darstellung und Funktionalität von Anwendung zu Anwendung. Daher ist es wichtig, dass Sie ein gängiges Dialogfeld nur dann anpassen, wenn es für eine Anwendung unbedingt erforderlich ist. Andernfalls gehen die konsistente Darstellung und die einfache Programmierschnittstelle verloren. Die entsprechenden Anpassungen behalten so viele der ursprünglichen Steuerelemente wie möglich bei. Das Erhöhen der Größe des Dialog Felds oder das Hinzufügen neuer Steuerelemente im Bereich, der bereits im Dialogfeld verfügbar ist, ist eine geeignete Anpassung. Das Ausblenden von ursprünglichen Steuerelementen oder das andere Ändern der beabsichtigten Funktionalität der ursprünglichen Steuerelemente ist eine weniger geeignete Anpassung.

In diesem Abschnitt werden die folgenden Methoden zum Anpassen eines allgemeinen Dialog Felds erläutert:

-   [Benutzerdefinierte Vorlagen](#custom-templates)
-   [Hook-Prozeduren für allgemeine Dialog Felder](#hook-procedures-for-common-dialog-boxes)
-   [Allgemeine Dialog Meldungen](#common-dialog-messages)
-   [Hilfe Unterstützung](#help-support)
    -   [Kontextbezogene Hilfe](#context-sensitive-help)
    -   [Schaltfläche "Hilfe"](#the-help-button)

## <a name="custom-templates"></a>Benutzerdefinierte Vorlagen

Allgemeine Dialogfelder verfügen über Standardvorlagen, die die Anzahl, den Typ und die Position der Standard Steuerelemente im Dialogfeld definieren. Sie können eine benutzerdefinierte Vorlage definieren, um Benutzern den Zugriff auf zusätzliche Steuerelemente zu gestatten, die für Ihre Anwendung eindeutig sind.

Für alle Standard Dialogfelder außer den Dialogfeldern Explorer-Style **Öffnen** und **Speichern** unter Ändern Sie die Standardvorlage, um eine benutzerdefinierte Vorlage zu erstellen, die die Standardvorlage ersetzt. Die benutzerdefinierte Vorlage definiert den Typ und die Position der Standard Steuerelemente sowie alle zusätzlichen Steuerelemente.

Wenn Sie eine benutzerdefinierte Dialogfeld Vorlage erstellen, indem Sie die Standard Dialogfeld Vorlage ändern, stellen Sie sicher, dass die Bezeichner für alle hinzugefügten Steuerelemente eindeutig sind und nicht mit den bezeichnerelementen der Standard Steuerelemente in Konflikt stehen. In der folgenden Tabelle werden der Name der Standardvorlagen Datei und der Includedatei für jeden der allgemeinen Dialogfeld Typen aufgelistet.



| Dialog Feldtyp               | Vorlagendatei | Includedatei |
|-------------------------------|---------------|--------------|
| **Farbe**                     | Color. DLG     | Colordlg. h   |
| **Suchen**                      | FindText. DLG  | Dlgs. h       |
| **Schriftart**                      | Schriftart. DLG      | Dlgs. h       |
| **Öffnen** (Mehrfachauswahl) | FileOpen. DLG  | Dlgs. h       |
| **Öffnen** (einfache Auswahl)   | FileOpen. DLG  | Dlgs. h       |
| **Seite einrichten**                | Prnsetup. DLG  | Dlgs. h       |
| **Drucken**                     | Prnsetup. DLG  | Dlgs. h       |
| **Druck Setup** (veraltet)    | Prnsetup. DLG  | Dlgs. h       |
| **Replace**                   | FindText. DLG  | Dlgs. h       |



 

Um eine benutzerdefinierte Vorlage zu aktivieren, müssen Sie ein Flag im **Flags** -Member der entsprechenden Struktur für das Dialogfeld festlegen. Wenn die Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie ein **ENABLETEMPLATE** -Flag im **Flags** -Element fest, und verwenden Sie die Member **HINSTANCE** und **lptemplatename** der Struktur, um das Modul und den Ressourcennamen zu identifizieren. Wenn sich die Vorlage bereits im Arbeitsspeicher befindet, legen Sie ein **enabletemplatehandle** -Flag im **Flags** -Member fest, und verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

In den meisten Fällen müssen Sie auch eine Hook-Prozedur aktivieren, damit das Dialogfeld Eingaben für die zusätzlichen Steuerelemente in der benutzerdefinierten Vorlage unterstützt und verarbeitet.

Die Standardvorlagen für die Dialogfelder **Öffnen** und **Speichern** unter im Explorer sind nicht für die Änderung verfügbar. Stattdessen definiert die benutzerdefinierte Vorlage ein untergeordnetes Dialogfeld, das nur die Elemente enthält, die dem Standard Dialogfeld hinzugefügt werden sollen. Die benutzerdefinierte Vorlage kann auch ein statisches Steuerelement definieren, das den Speicherort des Clusters der Standard Steuerelemente im untergeordneten Dialogfeld angibt. Weitere Informationen finden Sie unter [benutzerdefinierte Vorlagen im Explorer-Stil](open-and-save-as-dialog-boxes.md).

## <a name="hook-procedures-for-common-dialog-boxes"></a>Hook-Prozeduren für allgemeine Dialog Felder

Sie können für jedes der Standard Dialogfelder eine Hook-Prozedur aktivieren, mit der Nachrichten aus der Standard Dialogfeld Prozedur verarbeitet werden. Es gibt zwei allgemeine Arten von gängigen Dialogfeld-Hook-Prozeduren:

-   Die Standard-Hook-Prozedur wird mit den meisten gängigen Dialogfeldern verwendet.
-   Die in den Dialogfeldern " **Öffnen** " und " **Speichern** unter" unterstützte Hook-Prozedur im Explorer-Stil

Wenn Sie eine standardhook-Prozedur für eines der allgemeinen Dialogfelder bereitstellen, verarbeitet die Standard Dialogfeld-Prozedur die zugehörigen Nachrichten wie folgt.



| `Message`                                 | Verarbeitung                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ InitDialog**](wm-initdialog.md) | Die Standard Dialogfeld Prozedur verarbeitet die Nachricht vor der Übergabe an die Hook-Prozedur. Der *LPARAM* -Parameter der Nachricht ist ein Zeiger auf die Initialisierungs Struktur, die beim Erstellen des Dialog Felds angegeben wurde. |
| Alle anderen Nachrichten                      | Die Hook-Prozedur empfängt zuerst die Nachricht. Der Rückgabewert der Hook-Prozedur bestimmt dann, ob die Nachricht von der Standard Dialogfeld Prozedur verarbeitet oder ignoriert wird.                                     |



 

Im Dialogfeld Explorer-Stil **Öffnen** und **Speichern** unter empfängt die Hook-Prozedur keine Nachrichten, die für die Standard Steuerelemente im Dialogfeld vorgesehen sind. Stattdessen empfängt er Benachrichtigungs Meldungen aus dem Dialogfeld und Meldungen für alle zusätzlichen Steuerelemente, die Sie in einer benutzerdefinierten Vorlage definiert haben. Weitere Informationen finden Sie unter [Hook-Prozeduren im Explorer-Stil](open-and-save-as-dialog-boxes.md).

Um eine Hook-Prozedur zu aktivieren, legen Sie einen **ENABLEHOOK** -Wert im **Flags** -Member der entsprechenden Struktur für das Dialogfeld fest. Wenn ein **ENABLEHOOK** -Flag festgelegt ist, muss ein **lpfnhook** -Member der-Struktur die Adresse der Hook-Prozedur angeben.

In der folgenden Tabelle wird der Typ der Hook-Prozedur angezeigt, die für jedes der allgemeinen Dialogfelder bereitgestellt werden soll.



| Dialog Feldtyp                          | Hook-Prozedur                                      |
|------------------------------------------|-----------------------------------------------------|
| **Farbe**                                | [*Cchookproc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Suchen** oder **ersetzen**                  | [*Frhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Schriftart**                                 | [*Cfhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Öffnen** oder **Speichern** unter (Explorer-Stil) | [*Ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Öffnen** oder **Speichern** unter (Alter Stil)      | [*Ofnhuokprocoldstyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Drucken**                                | [*Printhookproc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Seite einrichten**                           | [*Page-tuphook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Im Dialogfeld **Seite einrichten** können Sie auch eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur angeben. Dies ist eine besondere Hook-Prozedur, mit der Sie die Darstellung der Beispielseite anpassen können, die im Dialogfeld **Seite einrichten** angezeigt wird.

> [!Note]  
> Das Dialogfeld **Druck Setup** wurde durch das Dialogfeld **Seite einrichten** abgelöst. Anwendungen sollten das Dialogfeld **Seite einrichten** verwenden. Aus Kompatibilitätsgründen unterstützt die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion jedoch weiterhin die Anzeige des Dialog Felds **Druck Setup** . Sie können eine [*setuphookproc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) -Prozedur für das **Druck Installations** Dialogfeld bereitstellen.

 

## <a name="common-dialog-messages"></a>Allgemeine Dialog Meldungen

Allgemeine Dialogfelder verwenden Sie Meldungen, um die Fenster Prozedur oder die Hook-Prozedur zu benachrichtigen, wenn bestimmte Ereignisse auftreten. Außerdem gibt es Nachrichten, die Sie an ein gemeinsames Dialogfeld senden können, um Informationen abzurufen oder um das Verhalten oder die Darstellung des Dialog Felds zu steuern. In diesem Abschnitt werden die allgemeinen Dialog Meldungen beschrieben, die von der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion registriert werden, Meldungen, die vom Dialogfeld **Schriftart** und **Seite einrichten** verwendet werden, und Meldungen, die von den Dialogfeldern im Explorer-Format **Öffnen** und **Speichern** unter verwendet werden.

Die allgemeine Dialog Feld Bibliothek definiert einen Satz von Meldungs Zeichenfolgen. Sie können eine Konstante, die einer dieser Meldungs Zeichenfolgen zugeordnet ist, an [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) übergeben, um eine Nachrichten-ID zu erhalten. Anschließend können Sie den Bezeichner verwenden, um Nachrichten zu erkennen und zu verarbeiten, die über ein gemeinsames Dialogfeld gesendet wurden, oder um Nachrichten an ein gemeinsames Dialogfeld zu senden. In der folgenden Tabelle werden die Nachrichten Konstanten und deren Verwendung beschrieben.



| -Konstanten                               | Zweck                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Colorokstring**](colorokstring.md) | Ein **Farb** Dialogfeld sendet diese Meldung an die Hook-Prozedur, wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche **OK** klickt. Die Hook-Prozedur kann die Farbe akzeptieren oder ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.                                                                                                                                                                                             |
| [**Fileokstring**](fileokstring.md)   | Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet diese Nachricht an die Hook-Prozedur, wenn der Benutzer einen Dateinamen auswählt und auf die Schaltfläche **OK** klickt. Die Hook-Prozedur kann den Dateinamen akzeptieren oder ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt. In Dialogfeldern zum **Öffnen** und **Speichern unter im** Explorer-Format wurde diese Meldung durch die [**CDN \_ FileOk**](cdn-fileok.md) -Benachrichtigungs Meldung abgelöst.<br/> |
| [**Findmsgstring**](findmsgstring.md) | Mit dem Dialogfeld **Suchen** oder **ersetzen** wird diese Meldung an die Fenster Prozedur des übergeordneten Fensters gesendet, wenn der Benutzer auf die **suchen weiter**, **ersetzen** oder **Alle ersetzen** klickt oder das Dialogfeld schließt. Der *LPARAM* -Parameter der Nachricht ist ein Zeiger auf eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, die die Eingabe des Benutzers enthält.                                                                               |
| [**Helpmsgstring**](helpmsgstring.md) | Alle allgemeinen Dialogfelder senden diese Meldung an die Fenster Prozedur ihres übergeordneten Fensters, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt. In Dialogfeldern zum **Öffnen** und **Speichern unter im** Explorer-Stil wurde diese Meldung durch die [**CDN- \_ Hilfe**](cdn-help.md) -Benachrichtigungs Meldung abgelöst.<br/>                                                                                                                    |
| [**Lbselchstring**](lbselchstring.md) | Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet diese Nachricht an die Hook-Prozedur, wenn der Benutzer die Auswahl im Listenfeld **Dateiname** ändert. In Dialogfeldern zum **Öffnen** und **Speichern unter im** Explorer-Stil wurde diese Meldung durch die CDN-Benachrichtigungs Meldung " [**\_ selChange**](cdn-selchange.md) " abgelöst.<br/>                                                                                           |
| [**"Sstrgbstring"**](setrgbstring.md)   | Eine Hook-Prozedur kann diese Nachricht an ein **Farb** Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.                                                                                                                                                                                                                                                                                                                   |
| [**Sharevistring**](sharevistring.md) | Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet diese Nachricht an die Hook-Prozedur, wenn eine Freigabe Verletzung für die ausgewählte Datei auftritt, wenn der Benutzer auf die Schaltfläche **OK** klickt. In Dialogfeldern zum **Öffnen** und **Speichern unter im** Explorer-Stil wurde diese Meldung durch die [**CDN \_ shareverletzungs**](cdn-shareviolation.md) -Benachrichtigungs Meldung ersetzt.<br/>                                                        |



 

In einigen gängigen Dialogfeldern werden andere Fenster Meldungen gesendet und empfangen. Die Hook-Prozedur für ein Dialogfeld **Schriftart** kann beliebige der **WM- \_ Auswahl Schriftart \_ \*** an das Dialogfeld **Schriftart** senden. Weitere Informationen finden Sie unter [Dialog Feld "Schriftart](font-dialog-box.md)". Im Dialogfeld **Seite einrichten** werden die **WM \_ - \_ \* PSD** -Meldungen gesendet, wenn Sie eine [*pagepainthook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur aktiviert haben. Weitere Informationen finden Sie unter [Dialog Feld "Seite einrichten](page-setup-dialog-box.md)".

Die Dialogfelder "Explorer-Format **Öffnen** " und " **Speichern** unter" unterstützen eine Reihe vordefinierter Nachrichten. Dazu zählen Benachrichtigungs Meldungen, die in Form einer [**WM \_**](../controls/wm-notify.md) -Benachrichtigungs Meldung an Ihre Hook-Prozedur gesendet werden, sowie Nachrichten, die von ihrer Hook-Prozedur an das Dialogfeld gesendet werden können. Eine umfassende Liste dieser Meldungen finden Sie unter [Hook-Prozeduren im Explorer-Stil](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Hilfe Unterstützung

Standard Dialogfelder bieten kontextabhängige Hilfe für die Standard Steuerelemente des Dialog Felds. Sie können eine **Hilfe** Schaltfläche anzeigen und Nachrichten verarbeiten, die generiert werden, wenn der Benutzer auf die Schaltfläche klickt, um zusätzliche Hilfe für ein Dialogfeld zu erhalten. Die Schaltfläche **Hilfe** ist eine Ergänzung zur standardmäßigen kontextbezogenen Hilfe. Die Schaltfläche " **Hilfe** " ist nützlich, um den allgemeinen Zweck des Dialog Felds zu beschreiben, das für Ihre Anwendung gilt.

-   [Kontextbezogene Hilfe](#context-sensitive-help)
-   [Schaltfläche "Hilfe"](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive Hilfe

Alle allgemeinen Dialogfelder bieten kontextabhängige Hilfe für die Standard Steuerelemente des Dialog Felds. Der Benutzer kann die Hilfe für einzelne Steuerelemente mit einer der folgenden Methoden anzeigen:

-   Auswählen des Steuer Elements und drücken der F1-Taste.
-   Klicken Sie auf die **?** -Schaltfläche in der Titelleiste, und klicken Sie anschließend auf ein-Steuerelement.
-   Klicken Sie mit der rechten Maustaste auf ein Steuerelement.

Wenn Sie ein Dialogfeld durch Hinzufügen neuer Steuerelemente anpassen, müssen Sie die Hilfe Unterstützung für diese Steuerelemente auch erweitern, indem Sie Anforderungen für die Hook-Prozedur verarbeiten. Die Hook-Prozedur empfängt die folgenden Meldungen, wenn der Benutzer die Hilfe anfordert.



| Benutzeraktion                                                           | `Message`                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Klicken Sie mit der rechten Maustaste auf ein Steuerelement.                          | [**WM- \_ ContextMenu**](/windows/desktop/menurc/wm-contextmenu) |
| Die F1-Taste wurde gedrückt.                                                   | [**WM- \_ Hilfe**](../shell/wm-help.md)               |
| Geklickt **?** auf der Titelleiste, und klicken Sie dann auf ein-Steuerelement. | [**WM- \_ Hilfe**](../shell/wm-help.md)               |



 

Sie sollten diese Nachrichten für die Steuerelemente verarbeiten, die Sie hinzugefügt haben, aber die Standard Dialogfeld Prozedur verarbeitet die Nachrichten für die Standard Steuerelemente. Weitere Informationen zum Verarbeiten dieser Nachrichten finden Sie in der [Hilfe](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85)).

### <a name="the-help-button"></a>Schaltfläche "Hilfe"

Sie können eine **Hilfe** Schaltfläche in einem der allgemeinen Dialogfelder anzeigen, indem Sie einen **ShowHelp** -Wert im **Flags** -Member der Initialisierungs Struktur für das Dialogfeld festlegen. Wenn Sie die Schaltfläche " **Hilfe** " anzeigen, müssen Sie die Anforderung des Benutzers verarbeiten. Die Verarbeitung kann entweder in einer der Fenster Prozeduren der Anwendung oder in einer Hook-Prozedur für das Dialogfeld durchgeführt werden. In der Regel verarbeiten Sie die Anforderung der Hilfe, indem Sie die [**WinHelp**](/windows/win32/api/winuser/nf-winuser-winhelpa) -Funktion aufrufen.

Zum Verarbeiten von Hilfe Nachrichten in einer ihrer Fenster Prozeduren müssen Sie eine Nachrichten-ID für die durch den [**helpmsgstring**](helpmsgstring.md) -Wert definierte Zeichenfolge abrufen und das Fenster zum Empfangen von Nachrichten identifizieren. Um die Nachrichten-ID zu erhalten, geben Sie **helpmsgstring** als Parameter in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion an. Wenn Sie das Dialogfeld erstellen, verwenden Sie das **hwndOwner** -Element der Dialogfeld Initialisierungs Struktur, um das Fenster zu identifizieren, das die Nachrichten empfangen soll. Die Dialogfeld Prozedur sendet die Nachricht an die Fenster Prozedur, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.

Zum Verarbeiten von Hilfe Nachrichten in einer Hook-Prozedur sollten Sie die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht verarbeiten. Die Hook-Prozedur bietet Hilfe, wenn der *wParam* -Parameter dieser Meldung anzeigt, dass der Benutzer auf die Schaltfläche " **Hilfe** " geklickt hat. Der Bezeichner der **Hilfe** Schaltfläche ist die **pshHelp** -Konstante, die in der Datei "Dlgs. h" definiert ist.

Die Hook-Prozeduren für die Dialogfelder zum **Öffnen** und **Speichern** unter im Explorer-Stil empfangen keine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen für die Schaltfläche " **Hilfe** ". Stattdessen sendet das Dialogfeld eine [**CDN- \_ Hilfe**](cdn-help.md) Benachrichtigungs Meldung an die Hook-Prozedur, wenn auf die Schaltfläche **Hilfe** geklickt wird.

 

