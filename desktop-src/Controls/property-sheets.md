---
title: Informationen über Eigenschaftenblätter
description: Ein Eigenschaftenblatt ist ein Fenster, in dem der Benutzer die Eigenschaften eines Elements anzeigen und bearbeiten kann.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5ed4299a0771d9f2b4df6f17929474c7f4868edf7bcaf1ade5baa7e572b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914704"
---
# <a name="about-property-sheets"></a>Informationen über Eigenschaftenblätter

Ein *Eigenschaftenblatt* ist ein Fenster, in dem der Benutzer die Eigenschaften eines Elements anzeigen und bearbeiten kann. Beispielsweise kann eine Tabellenkalkulationsanwendung ein Eigenschaftenblatt verwenden, damit der Benutzer die Schriftart- und Rahmeneigenschaften einer Zelle festlegen oder die Eigenschaften eines Geräts anzeigen und festlegen kann, z. B. ein Laufwerk, einen Drucker oder eine Maus.

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Grundlagen zu Eigenschaftenblättern](#property-sheet-basics)
-   [Dialogfelder "Eigenschaftenblatt"](#property-sheet-dialog-boxes)
-   [Seiten](#pages)
-   [Erstellen von Eigenschaftenblättern](#property-sheet-creation)
-   [Hinzufügen und Entfernen von Seiten](#adding-and-removing-pages)
-   [Titel und Seitenbezeichnungen des Eigenschaftenblatts](#property-sheet-title-and-page-labels)
-   [Seitenaktivierung](#page-activation)
-   [Hilfeschaltfläche](#help-button)
    -   [Entfernen der Hilfeschaltfläche "Beschriftungsleiste"](#removing-the-caption-bar-help-button)
-   [Schaltflächen "OK", "Abbrechen" und "Anwenden"](#ok-cancel-and-apply-buttons)
-   [Assistenten](#wizards)

## <a name="property-sheet-basics"></a>Grundlagen zu Eigenschaftenblättern

Um Eigenschaftenblätter in Ihrer Anwendung zu implementieren, schließen Sie die Headerdatei Prsht.h in Ihr Projekt ein. Prsht.h enthält alle Bezeichner, die mit Eigenschaftenblättern verwendet werden.

Ein Eigenschaftenblatt enthält ein oder mehrere überlappende untergeordnete Fenster, die als Seiten bezeichnet werden und jeweils Steuerelementfenster zum Festlegen einer Gruppe verwandter Eigenschaften enthalten. Beispielsweise kann eine Seite die Steuerelemente zum Festlegen der Schriftarteigenschaften eines Elements enthalten, einschließlich Typformat, Punktgröße, Farbe usw. Jede Seite verfügt über eine Registerkarte, die der Benutzer auswählen kann, um die Seite in den Vordergrund des Eigenschaftenblatts zu bringen. Beispielsweise zeigt die Date-Time Systemsteuerungsanwendung das folgende Eigenschaftenblatt an.

![Screenshot eines Eigenschaftenblatts mit zwei Registerkarten, von denen eine eine Uhr und ein monatliches Kalendersteuerelement anzeigt](images/propsheet1.png)

Ein Standardeigenschaftenblatt mit mehreren Seiten im Registerkartenbereich ermöglicht dem Benutzer zufälligen Zugriff auf alle Eigenschaften. Wenn es besser ist, Eigenschaften nacheinander festzulegen, können Sie einen [Assistenten](#wizards)verwenden.

## <a name="property-sheet-dialog-boxes"></a>Dialogfelder "Eigenschaftenblatt"

Ein Eigenschaftenblatt und die darin enthaltenen Seiten sind eigentlich Dialogfelder. Das Eigenschaftenblatt ist ein systemdefiniertes Dialogfeld, das die Seiten verwaltet und einen gemeinsamen Container für sie bereitstellt. Ein Eigenschaftenblattdialogfeld kann modal oder moduslos sein. Sie enthält einen Rahmen, eine Titelleiste und vier Schaltflächen: **OK,** **Abbrechen,** **Anwenden** und (optional) **Hilfe**. Die Dialogfeldprozesen für die Seiten erhalten Benachrichtigungscodes in Form von [**WM \_ NOTIFY-Meldungen,**](wm-notify.md) wenn der Benutzer auf die Schaltflächen klickt.

> [!NOTE]  
> Nicht alle Informationen in diesem Abschnitt gelten für Assistenten, die ein etwas anderes Aussehen und Verhalten aufweisen. Assistenten verfügen beispielsweise über einen anderen Satz von Schaltflächen und keine Registerkarten. Weitere Informationen finden Sie unter [Erstellen von Assistenten.](wizards.md)

Jede Seite in einem Eigenschaftenblatt ist ein anwendungsdefiniertes, modusloses Dialogfeld, das die Steuerelementfenster verwaltet, die zum Anzeigen und Bearbeiten der Eigenschaften eines Elements verwendet werden. Sie stellen die Dialogfeldvorlage bereit, die zum Erstellen der einzelnen Seiten verwendet wird, sowie die Dialogfeldprozedur, die die Steuerelemente verwaltet und die Eigenschaften des entsprechenden Elements festlegt.

Ein Eigenschaftenblatt sendet Benachrichtigungscodes an die Dialogfeldprozedur für eine Seite, wenn die Seite die Aktivierung erhält oder verliert und der Benutzer auf die Schaltfläche **OK,** **Abbrechen,** **Anwenden** oder **Hilfe** klickt. Die Benachrichtigungen werden in Form von [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) gesendet. Der *lParam-Parameter* ist die Adresse einer [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die das Fensterhandle für das Eigenschaftenblattdialogfeld enthält.

Einige Benachrichtigungscodes erfordern, dass eine Seite entweder **TRUE** oder **FALSE** als Antwort auf die [**WM \_ NOTIFY-Nachricht**](wm-notify.md) zurückgibt. Zu diesem Zweck muss die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) verwenden, um den **\_ DWL-MSGRESULT-Wert** für das Seitendialogfeld entweder auf **TRUE** oder **FALSE** festzulegen.

## <a name="pages"></a>Seiten

Ein Eigenschaftenblatt muss mindestens eine Seite enthalten, darf jedoch nicht mehr als den Wert von **MAXPROPPAGES** enthalten, wie in den Windows Headerdateien definiert. Jede Seite verfügt über einen nullbasierten Index, den das Eigenschaftenblatt entsprechend der Reihenfolge zuweist, in der die Seite dem Eigenschaftenblatt hinzugefügt wird. Die Indizes werden in Nachrichten verwendet, die Sie an das Eigenschaftenblatt senden.

Eine Eigenschaftenseite kann ein geschachteltes Dialogfeld enthalten. Andernfalls müssen Sie den [**WS \_ EX \_ CONTROLPARENT-Stil**](/windows/desktop/winmsg/extended-window-styles) für das Dialogfeld der obersten Ebene einschließen und die [**IsDialogMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) mit dem Handle für das übergeordnete Dialogfeld aufrufen. Dadurch wird sichergestellt, dass der Benutzer Mnemonik und die Navigationsschlüssel des Dialogfelds verwenden kann, um den Fokus auf Steuerelemente im geschachtelten Dialogfeld zu verschieben.

Jede Seite verfügt über ein entsprechendes Symbol und eine entsprechende Bezeichnung. Das Eigenschaftenblatt erstellt eine Registerkarte für jede Seite und zeigt das Symbol und die Bezeichnung auf der Registerkarte an. Von allen Eigenschaftenblattseiten wird erwartet, dass sie eine nichtbold-Schriftart verwenden. Um sicherzustellen, dass die Schriftart nicht fett formatiert ist, geben Sie den **DS \_ 3DLOOK-Stil** in der Dialogfeldvorlage an.

Die Dialogfeldprozedur für eine Seite darf die [**EndDialog-Funktion**](/windows/desktop/api/winuser/nf-winuser-enddialog) nicht aufrufen. Dadurch wird das gesamte Eigenschaftenblatt zerstört, nicht nur die Seite.

Die Mindestgröße für eine Eigenschaftenblattseite beträgt 212 Dialogeinheiten horizontal und 114 Dialogeinheiten vertikal. Wenn ein Seitendialogfeld kleiner ist, wird die Seite vergrößert, bis sie die Mindestgröße erreicht. Die Headerdatei Prsht.h enthält drei Empfohlene Größen für Eigenschaftenblattseiten, wie in der folgenden Tabelle dargestellt.

|  Size                |   BESCHREIBUNG                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Breite einer kleinen Eigenschaftenblattseite in Dialogeinheiten.         |
| **PROP \_ SM \_ CYDLG**  | Höhe einer kleinen Eigenschaftenblattseite in Dialogeinheiten.        |
| **PROP \_ MEDI \_ CXDLG** | Breite einer Eigenschaftenblattseite mittlerer Größe in Dialogeinheiten.  |
| **PROP \_ MEDI \_ CYDLG** | Höhe einer Eigenschaftenblattseite mittlerer Größe in Dialogeinheiten. |
| **PROP \_ LG \_ CXDLG**  | Breite einer großen Eigenschaftenblattseite in Dialogeinheiten.         |
| **PROP \_ LG \_ CYDLG**  | Höhe einer großen Eigenschaftenblattseite in Dialogeinheiten.        |

Die Verwendung dieser empfohlenen Größen trägt dazu bei, die visuelle Konsistenz zwischen Ihrer Anwendung und anderen Microsoft Windows-Anwendungen sicherzustellen.

Im Microsoft Visual Studio Ressourcen-Editor können Sie im Dialogfeld **Ressource hinzufügen** eine Seite mit der entsprechenden Größe erstellen. Erweitern Sie den Knoten Dialog, und wählen Sie **IDD \_ PROPPAGE \_ LARGE**, **IDD \_ PROPPAGE \_ MEDIUM** oder **IDD \_ PROPPAGE \_ SMALL** aus.

Das Eigenschaftenblatt wird automatisch so angepasst, dass es die größte Seite aufnehmen kann.

## <a name="property-sheet-creation"></a>Erstellen von Eigenschaftenblättern

Vor dem Erstellen eines Eigenschaftenblatts müssen Sie eine oder mehrere Seiten definieren. Dies umfasst das Auffüllen einer [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) mit Informationen zur Seite ( Symbol, Bezeichnung, Dialogfeldvorlage, Dialogfeldprozedur usw.) und das anschließende Angeben der Adresse der Struktur in einem Aufruf der [**CreatePropertySheetPage-Funktion.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) Die Funktion gibt ein Handle für den HPROPSHEETPAGE-Typ zurück, der die Seite eindeutig identifiziert.

Um ein Eigenschaftenblatt zu erstellen, geben Sie die Adresse einer [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) in einem Aufruf der [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) an. Die -Struktur definiert das Symbol und den Titel für das Eigenschaftenblatt und enthält auch die Adresse eines Arrays von HPROPSHEETPAGE-Handles, die Sie mit [**createPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)abrufen. Wenn **PropertySheet** das Eigenschaftenblatt erstellt, enthält es die im Array identifizierten Seiten. Die Seiten werden im Eigenschaftenblatt in der reihenfolge angezeigt, in der sie im Array enthalten sind.

Eine weitere Möglichkeit zum Zuweisen von Seiten zu einem Eigenschaftenblatt besteht darin, ein Array von [**PROPSHEETPAGE-Strukturen**](pss-propsheetpage.md) anstelle eines Arrays von **HPROPSHEETPAGE-Handles** anzugeben. In diesem Fall erstellt [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) Handles für die Seiten, bevor sie dem Eigenschaftenblatt hinzugefügt werden.

Wenn eine Seite erstellt wird, empfängt die zugehörige Dialogfeldprozedur eine [**\_ WM-INITDIALOG-Meldung.**](/windows/desktop/dlgbox/wm-initdialog) Der *lParam-Parameter* der Nachricht ist ein Zeiger auf eine Kopie der [**PROPSHEETPAGE-Struktur,**](pss-propsheetpage.md) die beim Erstellen der Seite definiert wird. Insbesondere beim Erstellen einer Seite kann der **lParam-Member** der Struktur verwendet werden, um anwendungsdefinierte Informationen an die Dialogfeldprozedur zu übergeben. Mit Ausnahme des **lParam-Elements** muss diese Struktur als schreibgeschützt behandelt werden. Das Ändern anderer Änderungen als **lParam** hat unvorhersehbare Folgen.

Wenn das System anschließend eine Kopie der [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) der Seite an Ihre Anwendung übergibt, verwendet es den gleichen Zeiger. Alle Änderungen an der Struktur werden übergeben. Da das **lParam-Element** vom System ignoriert wird, kann es geändert werden, um Informationen an andere Teile der Anwendung zu senden. Sie können beispielsweise **lParam** verwenden, um Informationen an die [*Rückruffunktion PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) der Seite zu übergeben.

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) legt automatisch die Größe und Anfangsposition eines Eigenschaftenblatts fest. Die Position basiert auf der Position des Besitzerfensters, und die Größe basiert auf der größten Seite, die beim Erstellen des Eigenschaftenblatts im Seitenarray angegeben wurde. Wenn die Seiten mit der Breite der vier Schaltflächen am unteren Rand des Eigenschaftenblatts übereinstimmen sollen, legen Sie die Breite der breitesten Seite auf 190 Dialogeinheiten fest.

Die Größe eines Eigenschaftenblatts wird anhand der *Breiten-* und *Höheneigenschaften* der Dialogfeldvorlage in der Ressourcendatei berechnet. Weitere Informationen finden Sie unter [**DIALOG-Ressource**](/windows/desktop/menurc/dialog-resource) oder [**DIALOGEX-Ressource.**](/windows/desktop/menurc/dialogex-resource) Beachten Sie jedoch, dass die Dimensionen aus Kompatibilitätsgründen relativ zur MS Shell Dlg-Schriftart und nicht zur von der Seite verwendeten Schriftart berechnet werden. Wenn Sie eine Seite entwerfen, die eine andere Schriftart verwendet, kann einer der folgenden Vorschläge verwendet werden.

-   Passen Sie die Abmessungen der Dialogvorlage an, um den Größenunterschied zwischen der MS Shell Dlg-Schriftart und der Schriftart zu kompensieren, die die Seite tatsächlich verwendet. Wenn Sie z. B. eine Schriftart auswählen, die doppelt so breit ist wie MS Shell Dlg, legen Sie die Width-Eigenschaft der Dialogvorlage auf das Doppelte der normalen Verwendung fest.
-   Verwenden Sie eine [**DIALOGEX-Vorlage,**](/windows/desktop/menurc/dialogex-resource) und legen Sie den **Dialogstil DS \_ SHELLFONT** fest. In diesem Fall interpretiert der Eigenschaftenblatt-Manager die Dialogvorlagendimensionen relativ zur Schriftart, die von der Dialogvorlage verwendet wird.

## <a name="adding-and-removing-pages"></a>Hinzufügen und Entfernen von Seiten

Nach dem Erstellen eines Eigenschaftenblatts kann eine Anwendung eine Seite am Ende der vorhandenen Seiten hinzufügen, indem sie eine [**PSM \_ ADDPAGE-Nachricht**](psm-addpage.md) sendet. Um eine Seite zwischen vorhandenen Seiten einfügen zu können, senden Sie eine [**PropSheet \_ InsertPage-Meldung.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) Beachten Sie, dass sich die Größe des Eigenschaftenblatts nicht ändern kann, nachdem es erstellt wurde. Alle hinzugefügten oder eingefügten Seiten dürfen nicht größer als die größte Seite sein, die derzeit im Eigenschaftenblatt enthalten ist. Um eine Seite zu entfernen, senden Sie eine [**PSM \_ REMOVEPAGE-Nachricht.**](psm-removepage.md)

Wenn Sie eine Seite definieren, können Sie die Adresse einer [*PropSheetPageProc-Rückruffunktion*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) angeben, die das Eigenschaftenblatt beim Erstellen oder Entfernen der Seite aufruft. Die *Verwendung von PropSheetPageProc* bietet Ihnen die Möglichkeit, Initialisierungs- und Bereinigungsvorgänge für einzelne Seiten durchzuführen.

> [!NOTE]  
> Eine Reihe von Meldungen und ein Funktionsaufruf treten auf, während das Eigenschaftenblatt die Liste der Seiten manipuliert. Während diese Aktion stattfindet, führt der Versuch, die Liste der Seiten zu ändern, zu unvorhersehbaren Ergebnissen. Fügen Sie in Ihrer Implementierung von [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)oder bei der Verarbeitung der folgenden Benachrichtigungen und -Meldungen keine Seiten hinzu, fügen Sie sie ein oder Windows entfernen.
>
> -   [PSN \_ APPLY](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [PSN \_ RESET](psn-reset.md)
> -   [PSN \_ SETACTIVE](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)

Wenn die Notwendigkeit besteht, eine Eigenschaftenblattseite zu ändern, während Sie eine dieser Nachrichten behandeln, oder wenn [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) in Betrieb ist, veröffentlichen Sie eine private Windows Nachricht. Ihre Anwendung erhält diese Meldung erst, nachdem der Eigenschaftenblatt-Manager seine Aufgaben abgeschlossen hat. An diesem Punkt ist es sicher, die Liste der Seiten zu ändern.

Wenn ein Eigenschaftenblatt zerstört wird, werden automatisch alle Seiten zerstört, die ihm hinzugefügt wurden. Die Seiten werden in umgekehrter Reihenfolge von der im Array angegebenen zerstört, die zum Erstellen der Seiten verwendet wird. Verwenden Sie die [**DestroyPropertySheetPage-Funktion,**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) um eine Seite zu zerstören, die von der [**CreatePropertySheetPage-Funktion**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) erstellt, aber nicht dem Eigenschaftenblatt hinzugefügt wurde.

## <a name="property-sheet-title-and-page-labels"></a>Eigenschaftenblatttitel und Seitenbezeichnungen

Sie geben den Titel eines Eigenschaftenblatts in der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) an, die zum Erstellen des Eigenschaftenblatts verwendet wird. Wenn **das dwFlags-Member** den **PSH \_ PROPTITLE-Wert** enthält, fügt das Eigenschaftenblatt je nach Version das Suffix "Properties" oder das Präfix "Properties for" hinzu. Sie können den Titel ändern, nachdem ein Eigenschaftenblatt erstellt wurde, indem Sie die [**MELDUNG PSM \_ SETTITLE**](psm-settitle.md) verwenden. In einem Assistenten kann diese Meldung verwendet werden, um den Titel einer inneren Seite dynamisch zu ändern.

Standardmäßig verwendet ein Eigenschaftenblatt die in der Dialogfeldvorlage angegebene Namenszeichenfolge als Bezeichnung für eine Seite. Sie können die Namenszeichenfolge überschreiben, indem Sie den **PSP \_ USETITLE-Wert** in das **dwFlags-Member** der [**PROPSHEETPAGE-Struktur,**](pss-propsheetpage.md) die die Seite definiert, hinzufügen. Wenn **PSP \_ USETITLE angegeben** wird, muss das **pszTitle-Member** die Adresse der Bezeichnungszeichenfolge für die Seite enthalten.

## <a name="page-activation"></a>Seitenaktivierung

Ein Eigenschaftenblatt kann nur eine aktive Seite gleichzeitig haben. Die Seite mit der Aktivierung befindet sich im Vordergrund des überlappenden Stapels von Seiten. Der Benutzer aktiviert eine Seite, indem er seine Registerkarte auswählt. eine Anwendung aktiviert eine Seite mithilfe der [**PSM \_ SETCURSEL-Meldung.**](psm-setcursel.md)

Das Eigenschaftenblatt sendet den [PSN \_ KILLACTIVE-Benachrichtigungscode](psn-killactive.md) an die Seite, die die Aktivierung verlieren wird. Als Antwort muss die Seite alle Änderungen überprüfen, die der Benutzer an der Seite vorgenommen hat. Wenn die Seite zusätzliche Benutzereingaben erfordert, bevor die Aktivierung verloren geht, verwenden Sie die [**SetWindowLong-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) um den **DWL \_ MSGRESULT-Wert** der Seite auf **TRUE zu setzen.** Außerdem muss auf der Seite ein Meldungsfeld angezeigt werden, das das Problem beschreibt und die empfohlene Aktion enthält. Legen **Sie DWL \_ MSGRESULT auf** FALSE **fest,** wenn es in Ordnung ist, die Aktivierung zu verlieren.

Bevor die Seite angezeigt wird, auf der die Aktivierung aktiviert wird, sendet das Eigenschaftenblatt den [PSN SETACTIVE-Benachrichtigungscode \_ ](psn-setactive.md) an die Seite. Die Seite muss reagieren, indem sie ihre Steuerfenster initialisiert.

## <a name="help-button"></a>Schaltfläche "Hilfe"

Eigenschaftenblätter können zwei Hilfeschaltflächen anzeigen: eine Hilfeschaltfläche für Eigenschaftenblätter, die am unteren Rand des Frames neben den Schaltflächen **OK** Anwenden abbrechen angezeigt wird, und eine Standard-Beschriftungsleistenschaltfläche, die kontextsensitive Hilfe /  /  bietet.

Die Hilfeschaltfläche des Eigenschaftenblatts ist optional und kann seite für Seite aktiviert werden. So zeigen Sie die Hilfeschaltfläche des Eigenschaftenblatts für eine oder mehrere Seiten an:

-   Legen Sie **das PSH \_ HASHELP-Flag** im **dwFlags-Member** der [**PROPSHEETHEADER-Struktur des Eigenschaftenblatts**](pss-propsheetheader.md) fest.
-   Legen Sie für jede Seite, auf der eine Hilfeschaltfläche angezeigt wird, das **PSP \_ HASHELP-Flag** im **dwFlags-Member** der [**PROPSHEETPAGE-Struktur der Seite**](pss-propsheetpage.md) fest.

Wenn der Benutzer auf die Schaltfläche Hilfe klickt, erhält die aktive Seite einen [PSN \_ HELP-Benachrichtigungscode.](psn-help.md) Die Seite muss antworten, indem Hilfeinformationen angezeigt werden, in der Regel durch Aufrufen der [**WinHelp-Funktion.**](/windows/desktop/api/winuser/nf-winuser-winhelpa)

### <a name="removing-the-caption-bar-help-button"></a>Entfernen der Hilfeschaltfläche der Beschriftungsleiste

Die Hilfeschaltfläche der Beschriftungsleiste wird standardmäßig angezeigt, sodass kontextorientierte Hilfe immer für die Schaltflächen OK/Abbrechen/Übernehmen verfügbar ist. Diese Schaltfläche kann jedoch bei Bedarf entfernt werden. So entfernen Sie die Hilfeschaltfläche der Beschriftungsleiste eines Eigenschaftenblatts:

-   Für Versionen der allgemeinen Steuerelemente vor [Version 5.80](common-control-versions.md)müssen Sie eine [**Rückruffunktion für Eigenschaftenblätter implementieren.**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)
-   Für [Version 5.80](common-control-versions.md) und höher der allgemeinen Steuerelemente können Sie einfach das PSH \_ NOCONTEXTHELP-Flag im **dwFlags-Element** der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) des Eigenschaftenblatts festlegen. Wenn Sie jedoch Abwärtskompatibilität mit früheren allgemeinen Steuerelementversionen benötigen, müssen Sie die Rückruffunktion implementieren.

So implementieren Sie eine Rückruffunktion für Eigenschaftenblätter, die die Hilfeschaltfläche der Beschriftungsleiste entfernt:

-   Legen Sie **das PSH \_ USECALLBACK-Flag** im **dwFlags-Member** der [**PROPSHEETHEADER-Struktur des Eigenschaftenblatts**](pss-propsheetheader.md) fest.
-   Legen Sie den **pfnCallBack-Member** der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) auf die Rückruffunktion fest.
-   Implementieren Sie die Rückruffunktion. Wenn diese Funktion die **PSCB \_ PRECREATE-Nachricht** empfängt, erhält sie auch einen Zeiger auf die Dialogfeldvorlage des Eigenschaftenblatts. Entfernen Sie den **DS \_ CONTEXTHELP-Stil** aus dieser Vorlage.

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

Wenn die [**DLGTEMPLATEEX-Struktur**](/windows/desktop/dlgbox/dlgtemplateex) nicht definiert ist, schließen Sie die folgende Deklaration ein:

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

## <a name="ok-cancel-and-apply-buttons"></a>Schaltflächen "OK", "Abbrechen" und "Anwenden"

Die **Schaltflächen OK** **und Anwenden** sind ähnlich. beides leitet die Seiten eines Eigenschaftenblatts an, um die vom Benutzer vorgenommenen Eigenschaftsänderungen zu überprüfen und anzuwenden. Der einzige Unterschied ist, dass das Klicken auf die **Schaltfläche OK** bewirkt, dass das Eigenschaftenblatt zerstört wird, nachdem die Änderungen angewendet wurden.

Wenn der Benutzer auf  die Schaltfläche **OK** oder Übernehmen klickt, sendet das Eigenschaftenblatt eine [PSN \_ KILLACTIVE-Benachrichtigung](psn-killactive.md) an die aktive Seite, um die Änderungen des Benutzers zu überprüfen. Wenn die Änderungen gültig sind, muss die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) aufrufen, bei der der **DWL \_ MSGRESULT-Wert** auf **FALSE festgelegt ist.** Wenn die Änderungen des Benutzers ungültig sind, muss die Seite **DWL \_ MSGRESULT** auf **TRUE** festlegen und ein Dialogfeld anzeigen, in dem der Benutzer über das Problem informiert wird. Die Seite bleibt aktiv, bis **DWL \_ MSGRESULT** als Reaktion auf eine PSN KILLACTIVE-Nachricht auf **FALSE** \_ festgelegt wird.

Nachdem eine Seite auf eine [ \_ PSN-KILLACTIVE-Benachrichtigung](psn-killactive.md) reagiert hat, indem **DWL \_ MSGRESULT** auf **FALSE** festgelegt wurde, sendet das Eigenschaftenblatt eine [PSN \_ APPLY-Benachrichtigung](psn-apply.md) an jede Seite. Wenn eine Seite diese Benachrichtigung empfängt, muss sie die neuen Eigenschaften auf das entsprechende Element anwenden. Um dem Eigenschaftenblatt anzugeben, dass die Änderungen für die Seite gültig sind, rufen Sie [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, während **DWL \_ MSGRESULT** auf **PSNRET \_ NOERROR festgelegt ist.** Wenn die Änderungen für die Seite ungültig sind, geben Sie einen Fehler zurück. Dadurch wird verhindert, dass das Eigenschaftenblatt zerstört wird, und der Fokus wird entweder auf die Seite, die die PSN APPLY-Benachrichtigung empfangen hat, oder auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche Anwenden \_ gedrückt wurde.  Um einen Fehler zurückgibt und anzugeben, welche Seite den Fokus erhält, legen **Sie DWL \_ MSGRESULT** auf einen der folgenden Werte fest.

-   **PSNRET \_ UNGÜLTIG.** Das Eigenschaftenblatt wird nicht zerstört, und der Fokus wird auf diese Seite zurückgegeben.
-   **PSNRET \_ UNGÜLTIGE \_ NOCHANGEPAGE.** Das Eigenschaftenblatt wird nicht zerstört, und der Fokus wird auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche gedrückt wurde.

Eine Anwendung kann die [**PSM \_ APPLY-Nachricht**](psm-apply.md) verwenden, um die Auswahl der Schaltfläche **Anwenden zu** simulieren.

Die **Schaltfläche** Anwenden wird anfänglich deaktiviert, wenn eine Seite aktiv wird. Dies bedeutet, dass noch keine Eigenschaftsänderungen angewendet werden müssen. Wenn die Seite Eingaben über eines ihrer Steuerelemente empfängt, die angeben, dass der Benutzer eine Eigenschaft bearbeitet hat, muss die Seite die [**PSM \_ CHANGED-Nachricht**](psm-changed.md) an das Eigenschaftenblatt senden. Die Meldung bewirkt, dass das Eigenschaftenblatt die Schaltfläche **Anwenden** aktiviert. Wenn der Benutzer anschließend  auf  die Schaltfläche Anwenden oder Abbrechen klickt, muss die Seite ihre Steuerelemente erneut initialisieren und dann die [**PSM \_ UNCHANGED-Meldung**](psm-unchanged.md) senden, um die Schaltfläche Anwenden erneut **zu** deaktivieren.

Manchmal **führt die** Schaltfläche Anwenden dazu, dass eine Seite eine Änderung an einem Eigenschaftenblatt vor sich hat, und die Änderung kann nicht rückgängig gemacht werden. In diesem Fall muss die Seite die [**\_ PSM-Nachricht CANCELTOCLOSE**](psm-canceltoclose.md) an das Eigenschaftenblatt senden. Die Meldung bewirkt, dass das Eigenschaftenblatt den Text der **Schaltfläche OK** in "Schließen" ändert, was bedeutet, dass die angewendeten Änderungen nicht abgebrochen werden können.

Manchmal nimmt eine Seite eine Änderung an der Systemkonfiguration vor, Windows neu gestartet oder das System neu gestartet werden muss, bevor die Änderung wirksam werden kann. Nachdem eine solche Änderung durchgeführt wurde, muss eine Seite entweder die [**PSM \_ RESTARTWINDOWS-**](psm-restartwindows.md) oder [**PSM \_ REBOOTSYSTEM-Nachricht**](psm-rebootsystem.md) an das Eigenschaftenblatt senden. Diese Meldungen bewirken, dass die [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) den **\_ ID-Wert PSRESTARTWINDOWS** oder **die ID \_ PSREBOOTSYSTEM** zurücksendet, nachdem das Eigenschaftenblatt zerstört wurde.

Wenn ein Benutzer  auf die Schaltfläche Abbrechen klickt, sendet das Eigenschaftenblatt den [PSN RESET-Benachrichtigungscode \_ ](psn-reset.md) an alle Seiten und gibt an, dass das Eigenschaftenblatt zerstört werden soll. Eine Seite muss die Benachrichtigung verwenden, um Bereinigungsvorgänge durchzuführen.

## <a name="wizards"></a>Assistenten

Ein Assistent ist eine besondere Art von Eigenschaftenblatt. Assistenten sind so konzipiert, dass Seiten nacheinander in einer Sequenz angezeigt werden, die von der Anwendung gesteuert wird. Anstatt aus einer Gruppe von Seiten auszuwählen, indem sie auf eine Registerkarte klicken, navigieren Benutzer nacheinander vorwärts und rückwärts durch die Sequenz, indem sie auf Schaltflächen klicken. Der folgende Screenshot zeigt beispielsweise die Willkommensseite des Assistenten zum Hinzufügen von Hardware:

![Screenshot der Willkommensseite eines Assistenten](images/wizard97.png)

Der folgende Screenshot zeigt die erste Seite eines Assistenten für Assistenten, den neuen Stil, der in Windows Vista eingeführt wurde.

![Screenshot der ersten Seite eines Assistenten](images/wizardaero.png)

Eine [vollständige Erörterung der Assistenten](wizards.md) finden Sie unter Erstellen von Assistenten.
