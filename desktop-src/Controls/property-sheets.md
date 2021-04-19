---
title: Informationen zu Eigenschaften Blättern
description: Ein Eigenschaften Blatt ist ein Fenster, das es dem Benutzer ermöglicht, die Eigenschaften eines Elements anzuzeigen und zu bearbeiten.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3256959b588e2109740033692c0c528889fc939f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106355249"
---
# <a name="about-property-sheets"></a>Informationen zu Eigenschaften Blättern

Ein Eigenschaften *Blatt* ist ein Fenster, das es dem Benutzer ermöglicht, die Eigenschaften eines Elements anzuzeigen und zu bearbeiten. Beispielsweise kann eine Tabellenkalkulationsanwendung mithilfe eines Eigenschaften Blatts die Schriftart-und Rahmen Eigenschaften einer Zelle festlegen oder die Eigenschaften eines Geräts anzeigen und festlegen, z. b. ein Laufwerk, einen Drucker oder eine Maus.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Grundlagen zu Eigenschaften Blättern](#property-sheet-basics)
-   [Dialog Felder für Eigenschaften Blätter](#property-sheet-dialog-boxes)
-   [Seiten](#pages)
-   [Erstellen eines Eigenschaften Blatts](#property-sheet-creation)
-   [Hinzufügen und Entfernen von Seiten](#adding-and-removing-pages)
-   [Titel und Seiten Bezeichnungen des Eigenschaften Blatts](#property-sheet-title-and-page-labels)
-   [Seiten Aktivierung](#page-activation)
-   [Hilfe Schaltfläche](#help-button)
    -   [Entfernen der Hilfe Schaltfläche für die Titelleiste](#removing-the-caption-bar-help-button)
-   [Schaltflächen OK, Abbrechen und anwenden](#ok-cancel-and-apply-buttons)
-   [Assistenten](#wizards)

## <a name="property-sheet-basics"></a>Grundlagen zu Eigenschaften Blättern

Um Eigenschaften Blätter in der Anwendung zu implementieren, fügen Sie die Header Datei prsht. h in das Projekt ein. Prsht. h enthält alle Bezeichner, die für Eigenschaften Blätter verwendet werden.

Ein Eigenschaften Blatt enthält ein oder mehrere überlappende untergeordnete Fenster mit dem Namen pages, die jeweils Steuer Fenster zum Festlegen einer Gruppe verwandter Eigenschaften enthalten. Beispielsweise kann eine Seite die Steuerelemente zum Festlegen der Schriftart Eigenschaften eines Elements enthalten, einschließlich typstil, Punktgröße, Farbe usw. Jede Seite verfügt über eine Registerkarte, auf die der Benutzer klicken kann, um die Seite in den Vordergrund des Eigenschaften Blatts zu verschieben. Beispielsweise wird in der System Steuerungsanwendung Date-Time das folgende Eigenschaften Blatt angezeigt.

![Screenshot eines Eigenschaften Blatts mit zwei Registerkarten, von denen eine Uhr und ein monatliches Kalender Steuerelement angezeigt wird](images/propsheet1.png)

Ein Standardeigenschaften Blatt mit mehreren Seiten im Registerkarten Format ermöglicht dem Benutzer den zufälligen Zugriff auf alle Eigenschaften. Wenn Sie für die Sequenzierung von Eigenschaften besser geeignet sind, können Sie einen [Assistenten](#wizards)verwenden.

## <a name="property-sheet-dialog-boxes"></a>Dialog Felder für Eigenschaften Blätter

Ein Eigenschaften Blatt und die darin enthaltenen Seiten sind tatsächlich Dialogfelder. Das Eigenschaften Blatt ist ein System definiertes Dialogfeld, das die Seiten verwaltet und einen gemeinsamen Container für Sie bereitstellt. Das Dialogfeld "Eigenschaften Blatt" kann modal oder nicht modelliert sein. Sie enthält einen Frame, eine Titelleiste und vier Schaltflächen: **OK**, **Abbrechen**, **anwenden** und (optional) **Hilfe**. Die Dialogfeld Prozeduren für die Seiten empfangen Benachrichtigungs Codes in Form von WM-Benachrichtigungs Meldungen, wenn der Benutzer auf die Schaltflächen klickt. [**\_**](wm-notify.md)

> [!NOTE]  
> Nicht alle Informationen in diesem Abschnitt gelten für Assistenten, die ein etwas anderes Aussehen und Verhalten aufweisen. Beispielsweise haben Assistenten einen anderen Satz von Schaltflächen und keine Registerkarten. Weitere Informationen finden Sie unter [Erstellen von Assistenten](wizards.md).

Jede Seite in einem Eigenschaften Blatt ist ein Anwendungs definiertes Dialogfeld, das die Steuerelement Fenster verwaltet, die zum Anzeigen und Bearbeiten der Eigenschaften eines Elements verwendet werden. Sie stellen die Dialogfeld Vorlage bereit, mit der die einzelnen Seiten erstellt werden, sowie die Dialogfeld Prozedur, mit der die Steuerelemente verwaltet werden, und legt die Eigenschaften des entsprechenden Elements fest.

Ein Eigenschaften Blatt sendet Benachrichtigungs Codes an die Dialogfeld Prozedur für eine Seite, wenn die Seite die Aktivierung erhält oder verliert und wenn der Benutzer auf die Schaltfläche **OK**, **Abbrechen**, **anwenden** oder **Hilfe** klickt. Die Benachrichtigungen werden in Form von WM- [**\_ Benachrichtigungs**](wm-notify.md) Nachrichten gesendet. Der *LPARAM* -Parameter ist die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die das Fenster Handle für das Eigenschaften Blatt-Dialogfeld enthält.

Einige Benachrichtigungs Codes erfordern, dass eine Seite in Reaktion auf die [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung entweder **true** oder **false** zurückgibt. Zu diesem Zweck muss die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion verwenden, um den **DWL- \_ msgresult** -Wert für das Seiten Dialogfeld auf " **true** " oder " **false**" festzulegen.

## <a name="pages"></a>Seiten

Ein Eigenschaften Blatt muss mindestens eine Seite enthalten, kann jedoch nicht mehr als den Wert von **maxproppages** enthalten, wie in den Windows-Header Dateien definiert. Jede Seite verfügt über einen NULL basierten Index, der vom Eigenschaften Blatt entsprechend der Reihenfolge zugewiesen wird, in der die Seite dem Eigenschaften Blatt hinzugefügt wird. Die Indizes werden in Nachrichten verwendet, die Sie an das Eigenschaften Blatt senden.

Eine Eigenschaften Seite kann ein Dialogfeld mit einem anderen Text enthalten. Wenn dies der Fall ist, müssen Sie den [**WS \_ Ex \_ controlparent**](/windows/desktop/winmsg/extended-window-styles) -Stil für das Dialogfeld der obersten Ebene einschließen und die [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) -Funktion mit dem Handle für das übergeordnete Dialogfeld aufrufen. Dadurch wird sichergestellt, dass der Benutzer mnetmonics und die Dialogfeld-Navigationstasten verwenden kann, um den Fokus auf die Steuerelemente im Dialogfeld für die Authentifizierung zu verschieben.

Jede Seite verfügt über ein entsprechendes Symbol und eine entsprechende Bezeichnung. Auf dem Eigenschaften Blatt wird eine Registerkarte für jede Seite erstellt, und das Symbol und die Bezeichnung werden auf der Registerkarte angezeigt. Es wird erwartet, dass auf allen Eigenschaften Blattseiten eine nicht fett formatierte Schriftart verwendet wird. Um sicherzustellen, dass die Schriftart nicht fett formatiert ist, geben Sie den **DS \_ 3dlook-** Stil in der Dialogfeld Vorlage an.

Die Dialogfeld Prozedur für eine Seite darf die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen. Dadurch wird das gesamte Eigenschaften Blatt, nicht nur die Seite, zerstört.

Die Mindestgröße für eine Eigenschaften Blattseite beträgt 212 Dialog Einheiten horizontal und 114 Dialog Einheiten vertikal. Wenn ein Seiten Dialogfeld kleiner als dieses ist, wird die Seite vergrößert, bis Sie der Mindestgröße entspricht. Die Header Datei "prsht. h" enthält drei Sätze von empfohlenen Größen für Eigenschaften Blattseiten, wie in der folgenden Tabelle dargestellt.

|  Size                |   BESCHREIBUNG                                                   |
|----------------------|-----------------------------------------------------------------|
| **Prop \_ SM \_ cxdlg**  | Breite (in Dialog Einheiten) einer kleinen Eigenschaften Blattseite.         |
| **Prop \_ SM \_ cydlg**  | Höhe in Dialogfeld Einheiten einer kleinen Eigenschaften Blattseite.        |
| **unterstützen von \_ Med \_ cxdlg** | Breite in Dialogfeld Einheiten einer Eigenschaften Blattseite mittlerer Größe.  |
| **Prop \_ Med \_ cydlg** | Höhe in Dialogfeld Einheiten einer Eigenschaften Blattseite mittlerer Größe. |
| **Prop \_ LG \_ cxdlg**  | Breite (in Dialog Einheiten) einer großen Eigenschaften Blattseite.         |
| **Prop \_ LG \_ cydlg**  | Höhe in Dialogfeld Einheiten einer großen Eigenschaften Blattseite.        |

Wenn Sie diese empfohlenen Größen verwenden, können Sie die visuelle Konsistenz zwischen Ihrer Anwendung und anderen Microsoft Windows-Anwendungen gewährleisten.

Im Ressourcen-Editor von Microsoft Visual Studio können Sie im Dialogfeld **Ressource hinzufügen** eine Seite mit der entsprechenden Größe erstellen. Erweitern Sie den Dialog Knoten, und wählen Sie **IDD \_ PropPage \_ Large**, **IDD \_ PropPage \_ Medium** oder **IDD \_ PropPage \_ Small** aus.

Das Eigenschaften Blatt wird automatisch angepasst, um der größten Seite Rechnung zu tragen.

## <a name="property-sheet-creation"></a>Erstellen eines Eigenschaften Blatts

Vor dem Erstellen eines Eigenschaften Blatts müssen Sie mindestens eine Seite definieren. Dies umfasst das Auffüllen einer [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur mit Informationen über die Seite – Symbol, Bezeichnung, Dialogfeld Vorlage, Dialogfeld Prozedur usw. – und die anschließende Angabe der Adresse der Struktur in einem Aufrufen der Funktion " [**deatepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ". Die-Funktion gibt ein Handle für den hpropsheetpage-Typ zurück, der die Seite eindeutig identifiziert.

Zum Erstellen eines Eigenschaften Blatts geben Sie die Adresse einer [**propsheederader**](pss-propsheetheader.md) -Struktur in einem Aufrufen der [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion an. Die-Struktur definiert das Symbol und den Titel für das Eigenschaften Blatt und enthält auch die Adresse eines Arrays von hpropsheetpage-Handles, das Sie mithilfe von " [**kreatepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)" abrufen. Wenn **PropertySheet** das Eigenschaften Blatt erstellt, enthält es die im Array identifizierten Seiten. Die Seiten werden im Eigenschaften Blatt in derselben Reihenfolge angezeigt, in der Sie im Array enthalten sind.

Eine andere Möglichkeit, Seiten einem Eigenschaften Blatt zuzuweisen, besteht darin, ein Array von [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen anstelle eines Arrays von **hpropsheetpage** -Handles anzugeben. In diesem Fall erstellt [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) Handles für die Seiten, bevor Sie dem Eigenschaften Blatt hinzugefügt werden.

Wenn eine Seite erstellt wird, erhält die zugehörige Dialogfeld Prozedur eine " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung. Der *LPARAM* -Parameter der Nachricht ist ein Zeiger auf eine Kopie der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur, die definiert wird, wenn die Seite erstellt wird. Insbesondere, wenn eine Seite erstellt wird, kann der **LPARAM** -Member der-Struktur verwendet werden, um Anwendungs definierte Informationen an die Dialogfeld Prozedur zu übergeben. Mit Ausnahme des **LPARAM** -Members muss diese Struktur als schreibgeschützt behandelt werden. Das Ändern anderer Elemente als **LPARAM** hat unvorhersehbare Konsequenzen.

Wenn das System anschließend eine Kopie der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur der Seite an Ihre Anwendung übergibt, wird derselbe Zeiger verwendet. Alle Änderungen an der Struktur werden zusammengefasst. Da das **LPARAM** -Element vom System ignoriert wird, kann es geändert werden, um Informationen an andere Teile der Anwendung zu senden. Sie können z. b. **LPARAM** verwenden, um Informationen an die [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion der Seite zu übergeben.

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) legt automatisch die Größe und die ursprüngliche Position eines Eigenschaften Blatts fest. Die Position basiert auf der Position des Besitzer Fensters, und die Größe basiert auf der größten Seite, die beim Erstellen des Eigenschaften Blatts im Seiten Array angegeben wurde. Wenn Sie möchten, dass die Seiten mit der Breite der vier Schaltflächen unten auf dem Eigenschaften Blatt identisch sind, legen Sie die Breite der breiteste Seite auf 190 Dialog Einheiten fest.

Die Größe eines Eigenschaften Blatts wird aus den Eigenschaften " *Width* " und " *height* " der Dialogfeld Vorlage in der Ressourcen Datei berechnet. Weitere Informationen finden Sie unter [**Dialog Feld Ressource**](/windows/desktop/menurc/dialog-resource) oder [**DIALOGEX-Ressource**](/windows/desktop/menurc/dialogex-resource) . Beachten Sie jedoch, dass die Dimensionen aus Kompatibilitätsgründen in Bezug auf die Schriftart der MS Shell Dlg anstelle der von der Seite verwendeten Schriftart berechnet werden. Wenn Sie eine Seite entwerfen, die eine andere Schriftart verwendet, können Sie einen der folgenden Vorschläge verwenden.

-   Passen Sie die Dimensionen der Dialogfeld Vorlage an, um den Unterschied in der Größe zwischen der MS Shell Dlg-Schriftart und der Schriftart, die von der Seite tatsächlich verwendet wird, auszugleichen. Wenn Sie z. b. eine Schriftart auswählen, die doppelt so breit ist wie die MS Shell Dlg, legen Sie die Width-Eigenschaft der Dialog Vorlage auf die doppelte normale Verwendung fest.
-   Verwenden Sie eine [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) -Vorlage, und legen Sie das Dialogfeld **DS \_ shellfont** fest. In diesem Fall interpretiert der Eigenschaften Blatt-Manager die Dialogfeld Vorlagen Dimensionen relativ zu der Schriftart, die von der Dialogfeld Vorlage verwendet wird.

## <a name="adding-and-removing-pages"></a>Hinzufügen und Entfernen von Seiten

Nach dem Erstellen eines Eigenschaften Blatts kann eine Anwendung eine Seite am Ende der vorhandenen Gruppe von Seiten hinzufügen, indem eine [**PSM- \_ addPage**](psm-addpage.md) -Nachricht gesendet wird. Um eine Seite zwischen vorhandenen Seiten einzufügen, senden Sie eine [**propsheet- \_ insertpage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) -Nachricht. Beachten Sie, dass die Größe des Eigenschaften Blatts nicht geändert werden kann, nachdem es erstellt wurde. Alle hinzugefügten oder eingefügten Seiten dürfen nicht größer als die größte Seite sein, die sich derzeit im Eigenschaften Blatt befinden. Um eine Seite zu entfernen, senden Sie eine [**PSM- \_ RemovePage**](psm-removepage.md) -Nachricht.

Wenn Sie eine Seite definieren, können Sie die Adresse einer [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Rückruffunktion angeben, die vom Eigenschaften Blatt beim Erstellen oder Entfernen der Seite aufgerufen wird. Durch die Verwendung von *PropSheetPageProc* haben Sie die Möglichkeit, Initialisierungs-und Bereinigungs Vorgänge für einzelne Seiten auszuführen.

> [!NOTE]  
> Eine Reihe von Nachrichten und ein Funktions aufruftritt auf, während das Eigenschaften Blatt die Liste der Seiten bearbeitet. Während diese Aktion ausgeführt wird, kann der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen führen. Fügen Sie in der Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)keine Seiten hinzu, fügen Sie Sie hinzu oder entfernen Sie Sie, oder behandeln Sie die folgenden Benachrichtigungen und Windows-Meldungen.
>
> -   [PSN- \_ Anwendung](psn-apply.md)
> -   [PSN- \_ killactive](psn-killactive.md)
> -   [PSN- \_ zurück Setzung](psn-reset.md)
> -   [PSN- \_ SETACTIVE](psn-setactive.md)
> -   [PSN- \_ witzback](psn-wizback.md)
> -   [PSN- \_ nächstes](psn-wiznext.md)
> -   [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)

Wenn die Notwendigkeit besteht, eine Eigenschaften Blattseite zu ändern, während Sie eine dieser Nachrichten verarbeiten, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, stellen Sie eine private Windows-Meldung bereit. Die Anwendung empfängt diese Nachricht erst, nachdem die Aufgaben des Eigenschaften Blatt-Managers abgeschlossen wurden. an diesem Punkt kann die Liste der Seiten sicher geändert werden.

Wenn ein Eigenschaften Blatt zerstört wird, werden automatisch alle Seiten zerstört, die dieser hinzugefügt wurden. Die Seiten werden in umgekehrter Reihenfolge aus dem-Array zerstört, das zum Erstellen der Seiten verwendet wird. Verwenden Sie die Funktion " [**destroypropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) ", um eine Seite zu zerstören, die [**von der Funktion**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) "" in der Funktion "Funktion" erstellt wurde, die jedoch nicht dem Eigenschaften Blatt hinzugefügt wurde.

## <a name="property-sheet-title-and-page-labels"></a>Titel und Seiten Bezeichnungen des Eigenschaften Blatts

Sie geben den Titel eines Eigenschaften Blatts in der [**propsheetheiader**](pss-propsheetheader.md) -Struktur an, die zum Erstellen des Eigenschaften Blatts verwendet wird. Wenn das **dwFlags** -Element den **PSH- \_ proptitle** -Wert enthält, fügt das Eigenschaften Blatt das Suffix "Properties" oder das Präfix "Properties for" (abhängig von der Version) hinzu. Sie können den Titel ändern, nachdem ein Eigenschaften Blatt mithilfe der [**PSM- \_ SetTitle**](psm-settitle.md) -Nachricht erstellt wurde. In einem Aero-Assistenten kann diese Meldung verwendet werden, um den Titel einer inneren Seite dynamisch zu ändern.

Standardmäßig verwendet ein Eigenschaften Blatt die namens Zeichenfolge, die in der Dialogfeld Vorlage als Bezeichnung für eine Seite angegeben ist. Sie können die namens Zeichenfolge überschreiben, indem Sie den Wert von " **PSP \_ usetitle** " in den **dwFlags** -Member der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur einschließen, die die Seite definiert. Bei Angabe von " **PSP \_ usetitle** " muss das **psztitle** -Element die Adresse der Bezeichnungs Zeichenfolge für die Seite enthalten.

## <a name="page-activation"></a>Seiten Aktivierung

Ein Eigenschaften Blatt kann jeweils nur eine aktive Seite enthalten. Die Seite, auf der sich die Aktivierung befindet, befindet sich im Vordergrund des überlappenden Stapel von Seiten. Der Benutzer aktiviert eine Seite durch Auswählen der Registerkarte. eine Anwendung aktiviert eine Seite mithilfe der [**PSM- \_ setcurrsel**](psm-setcursel.md) -Nachricht.

Das Eigenschaften Blatt sendet den Benachrichtigungs Code " [PSN \_ killactive](psn-killactive.md) " an die Seite, die die Aktivierung verliert. Als Antwort muss die Seite alle Änderungen überprüfen, die der Benutzer an der Seite vorgenommen hat. Wenn für die Seite vor dem Verlust der Aktivierung zusätzliche Benutzereingaben erforderlich sind, verwenden Sie die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion, um den **DWL- \_ msgresult** -Wert der Seite auf " **true**" festzulegen. Außerdem muss auf der Seite ein Meldungs Feld angezeigt werden, das das Problem beschreibt und die empfohlene Aktion bereitstellt. Legen Sie **DWL \_ msgresult** auf **false** fest, wenn es in Ordnung ist, die Aktivierung zu verlieren.

Bevor die Seite, die die Aktivierung erlangt, sichtbar ist, sendet das Eigenschaften Blatt den " [PSN \_ SETACTIVE](psn-setactive.md) "-Benachrichtigungs Code an die Seite. Die Seite muss durch initialisieren Ihrer Steuerelement Fenster Antworten.

## <a name="help-button"></a>Hilfe Schaltfläche

In Eigenschaften Blättern können zwei Hilfe Schaltflächen angezeigt werden: eine Hilfe Schaltfläche auf dem Eigenschaften Blatt, die unten im Frame angezeigt wird, neben den Schaltflächen **OK** / **Abbrechen** / **anwenden** und eine Standard-Titelleisten Schaltfläche, die kontextbezogene Hilfe bereitstellt.

Die Schaltfläche "Hilfe" des Eigenschaften Blatts ist optional und kann auf Seitenbasis aktiviert werden. So zeigen Sie die Eigenschaften Blatt Hilfe Schaltfläche für eine oder mehrere Seiten an:

-   Legen Sie das **PSH \_ HasHelp** -Flag im **dwFlags** -Member der [**propsheeder**](pss-propsheetheader.md) -Struktur des Eigenschaften Blatts fest.
-   Legen Sie für jede Seite, auf der eine Hilfe Schaltfläche angezeigt wird, das Flag " **PSP \_ HasHelp** " im **dwFlags** -Member der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur der Seite fest.

Wenn der Benutzer auf die Schaltfläche "Hilfe" klickt, empfängt die aktive Seite einen [PSN- \_ Hilfe](psn-help.md) -Benachrichtigungs Code. Die Seite muss Antworten, indem Hilfe Informationen angezeigt werden, in der Regel durch Aufrufen der [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) -Funktion.

### <a name="removing-the-caption-bar-help-button"></a>Entfernen der Hilfe Schaltfläche für die Titelleiste

Die Schaltfläche Hilfe Schaltfläche wird standardmäßig angezeigt, sodass die kontextbezogene Hilfe für die Schaltflächen OK/Abbrechen/anwenden immer verfügbar ist. Diese Schaltfläche kann jedoch ggf. entfernt werden. So entfernen Sie die Hilfe Schaltfläche der Beschriftungs Leiste eines Eigenschaften Blatts:

-   Für Versionen der allgemeinen Steuerelemente vor [Version 5,80](common-control-versions.md)müssen Sie eine [**Eigenschaften Blatt-Rückruffunktion**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)implementieren.
-   Bei [Version 5,80](common-control-versions.md) und höher der allgemeinen Steuerelemente können Sie einfach das PSH \_ nocontexthelp-Flag im **dwFlags** -Member der [**propsheeder**](pss-propsheetheader.md) -Struktur der Eigenschaften Seite festlegen. Wenn Sie jedoch eine Abwärtskompatibilität mit früheren allgemeinen Steuerelement Versionen benötigen, müssen Sie die Rückruffunktion implementieren.

So implementieren Sie eine Eigenschaften Blatt-Rückruffunktion, mit der die Schaltfläche "Titelleisten Hilfe" entfernt wird

-   Legen Sie das **PSH \_ usecallback** -Flag im **dwFlags** -Member der [**propsheeder**](pss-propsheetheader.md) -Struktur des Eigenschaften Blatts fest.
-   Legen Sie den **pfncallback** -Member der [**propsheevernader**](pss-propsheetheader.md) -Struktur so fest, dass er auf die Rückruffunktion verweist.
-   Implementieren Sie die Rückruffunktion. Wenn diese Funktion die **pscb \_ PreCreate** -Nachricht empfängt, wird auch ein Zeiger auf die Dialogfeld Vorlage des Eigenschaften Blatts angezeigt. Entfernen Sie **den \_ kontexthandator** aus dieser Vorlage.

Im folgenden Beispiel wird veranschaulicht, wie eine solche Rückruffunktion implementiert wird:

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

Wenn die [**dlgtemplateex**](/windows/desktop/dlgbox/dlgtemplateex) -Struktur nicht definiert ist, schließen Sie die folgende Deklaration ein:

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>Schaltflächen OK, Abbrechen und anwenden

Die Schaltflächen **OK** und **Apply** ähneln einander. beide Seiten leiten die Seiten eines Eigenschaften Blatts an, um die vom Benutzer vorgenommenen Eigenschaften Änderungen zu überprüfen und anzuwenden. Der einzige Unterschied besteht darin, dass das Klicken auf die Schaltfläche **OK** bewirkt, dass das Eigenschaften Blatt nach dem Anwenden der Änderungen zerstört wird.

Wenn der Benutzer auf **die Schaltfläche** **OK** oder übernehmen klickt, sendet das Eigenschaften Blatt eine [PSN- \_ killactive](psn-killactive.md) -Benachrichtigung an die aktive Seite und gibt dadurch die Möglichkeit, die Änderungen des Benutzers zu überprüfen. Wenn die Änderungen gültig sind, muss die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem **DWL-Wert " \_ msgresult** " aufrufen, der auf " **false**" festgelegt ist. Wenn die Änderungen des Benutzers nicht gültig sind, muss die **DWL \_ msgresult** auf der Seite auf **true** festgelegt werden, und es wird ein Dialogfeld angezeigt, in dem der Benutzer über das Problem informiert wird. Die Seite bleibt aktiv, bis **DWL \_ msgresult** als Antwort auf eine PSN-killactive-Nachricht auf **false** festgelegt ist \_ .

Nachdem eine Seite durch Festlegen von **DWL \_ msgresult** auf **false** auf eine [PSN- \_ killactive](psn-killactive.md) -Benachrichtigung reagiert hat, sendet das Eigenschaften Blatt eine PSN-Benachrichtigungs Benachrichtigung auf jede Seite. [ \_](psn-apply.md) Wenn eine Seite diese Benachrichtigung empfängt, muss Sie die neuen Eigenschaften auf das entsprechende Element anwenden. Um dem Eigenschaften Blatt mitzuteilen, dass die Änderungen für die Seite gültig sind, geben Sie [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit **DWL \_ msgresult** auf **psnret \_ noError** ein. Wenn die Änderungen für die Seite ungültig sind, wird ein Fehler zurückgegeben. Dadurch wird verhindert, dass das Eigenschaften Blatt zerstört wird, und es wird der Fokus entweder auf die Seite zurückgegeben, die die Benachrichtigung über das \_ Benachrichtigungs  Verhalten empfangen hat, oder auf die Seite, die beim Drücken der Schaltfläche " Wenn ein Fehler zurückgegeben werden soll, und geben Sie an, welche Seite den Fokus erhält, legen Sie **DWL \_ msgresult** auf einen der folgenden Werte fest.

-   **Psnret \_ Ungültig**. Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf diese Seite zurückgegeben.
-   **Psnret \_ Ungültige \_ nochangepage**. Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche gedrückt wurde.

Eine Anwendung kann die [**PSM-Nachricht \_ anwenden**](psm-apply.md) verwenden, um die Auswahl der Schaltfläche **anwenden** zu simulieren.

Die Schaltfläche **anwenden** ist anfänglich deaktiviert, wenn eine Seite aktiv wird. Dies deutet darauf hin, dass noch keine anzuwendenden Eigenschafts Änderungen vorhanden sind. Wenn die Seite Eingaben über eines der Steuerelemente empfängt, das angibt, dass der Benutzer eine Eigenschaft bearbeitet hat, muss die von der Seite [**\_ geänderte PSM**](psm-changed.md) -Nachricht an das Eigenschaften Blatt gesendet werden. Die Meldung bewirkt, dass auf dem Eigenschaften Blatt die Schaltfläche **anwenden** aktiviert wird. Wenn der Benutzer anschließend auf die Schaltfläche " **anwenden** " oder " **Abbrechen** " klickt, muss die Seite die zugehörigen Steuerelemente erneut initialisieren und dann die nicht geänderte [**PSM \_**](psm-unchanged.md) -Nachricht senden, um die Schaltfläche " **anwenden** "

Manchmal bewirkt die Schaltfläche **anwenden** , dass eine Seite eine Änderung an einem Eigenschaften Blatt vornimmt, und die Änderung kann nicht rückgängig gemacht werden. Wenn dies der Fall ist, muss die Seite die [**PSM \_ canceldeclose**](psm-canceltoclose.md) -Nachricht an das Eigenschaften Blatt senden. Die Meldung bewirkt, dass das Eigenschaften Blatt den Text der Schaltfläche **OK** in "Close" ändert, um anzugeben, dass die angewendeten Änderungen nicht abgebrochen werden können.

Manchmal nimmt eine Seite eine Änderung an der Systemkonfiguration vor, für die Windows neu gestartet oder das System neu gestartet werden muss, bevor die Änderung wirksam werden kann. Nachdem eine solche Änderung vorgenommen wurde, muss eine Seite entweder die [**PSM \_ restartwindows**](psm-restartwindows.md) -oder [**PSM \_ rebootsystem**](psm-rebootsystem.md) -Meldung an das Eigenschaften Blatt senden. Diese Nachrichten bewirken, dass die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion die **ID \_ psrestartwindows** oder die **ID \_ psrebootsystem** -Wert zurückgibt, nachdem das Eigenschaften Blatt zerstört wurde.

Wenn ein Benutzer auf die Schaltfläche **Abbrechen** klickt, sendet das Eigenschaften Blatt den Benachrichtigungs Code für die [PSN- \_ zurück](psn-reset.md) Setzung an alle Seiten, was darauf hinweist, dass das Eigenschaften Blatt zerstört werden soll. Eine Seite muss die Benachrichtigung verwenden, um Cleanupvorgänge auszuführen.

## <a name="wizards"></a>Assistenten

Ein Assistent ist ein spezieller Typ eines Eigenschaften Blatts. Assistenten sind so konzipiert, dass Seiten nacheinander in einer Sequenz angezeigt werden, die von der Anwendung gesteuert wird. Anstatt aus einer Gruppe von Seiten durch Klicken auf eine Registerkarte auszuwählen, navigieren die Benutzer nacheinander und rückwärts durch die Sequenz, indem Sie auf Schaltflächen klicken. Der folgende Screenshot zeigt z. b. die Willkommensseite des Assistenten zum Hinzufügen von Hardware:

![Screenshot der Willkommensseite eines Assistenten](images/wizard97.png)

Der folgende Screenshot zeigt die erste Seite eines Aero-Assistenten, den neuen Stil, der in Windows Vista eingeführt wurde.

![Screenshot der ersten Seite eines Aero-Assistenten](images/wizardaero.png)

Eine umfassende Erörterung der Assistenten finden Sie unter [Erstellen von Assistenten](wizards.md) .
