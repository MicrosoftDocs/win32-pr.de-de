---
description: 'Onlinehilfe kann in einer Vielzahl von Formen verfügbar sein, von detaillierten konzeptionellen Informationen bis zu schnellen Definitionen. Dieses Thema enthält folgende Abschnitte:'
title: Behandeln von Onlinehilfen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: caf576d723b27e1c81bb715ea04743740930b5bb257f03eb3ca0a9ab697affd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223682"
---
# <a name="handling-online-help"></a>Behandeln von Onlinehilfen

Onlinehilfe kann in einer Vielzahl von Formen verfügbar sein, von detaillierten konzeptionellen Informationen bis zu schnellen Definitionen. Dieses Thema enthält folgende Abschnitte:

-   [Informationen zur Hilfe](#about-help)
    -   [Hilfeanfragen](#help-requests)
    -   [Hilfeanzeige und Windows Hilfe](#help-display-and-windows-help)
-   [Verwenden der Hilfe](#using-help)
    -   [Bereitstellen von Hilfe in einem Dialogfeld](#providing-help-in-a-dialog-box)
    -   [Festlegen der Darstellung eines sekundären Hilfefensters](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Informationen zur Hilfe

Ein wichtiges Element einer benutzerfreundlichen Anwendung ist in der Onlinehilfe sofort verfügbar. Windows stellt Funktionen und Meldungen zur Verfügung, die bei Verwendung in Verbindung mit der Windows Help-Anwendung die Implementierung von Onlinehilfe in Ihrer Anwendung einfach machen. In dieser Übersicht werden die Elemente von Windows, die Onlinehilfe unterstützen. Es wird beschrieben, wie Sie diese Elemente verwenden, um Benutzern eine Möglichkeit zu geben, Hilfe an sich zu fordern. Außerdem wird erläutert, wie Sie die Windows-Hilfeanwendung verwenden, um Hilfe anzuzeigen.

### <a name="help-requests"></a>Hilfeanfragen

Die Windows-basierten Anwendungen stellen Onlinehilfeinformationen in einer Vielzahl von Formen bereit, von konzeptioneller Hilfe, die den Zweck der Funktionen einer Anwendung erläutert, bis hin zu Popuphilfe, die schnelle Definitionen einzelner Elemente in der Benutzeroberfläche der Anwendung bietet. Sie verwenden Funktionen und Nachrichten, um Benutzern eine Vielzahl von Möglichkeiten zum Anfordern des Zugriffs auf diese Informationen zu bieten. In den folgenden Abschnitten werden diese Hilfeanfragen beschrieben.

### <a name="help-menu"></a>Menü "Hilfe"

Die meisten Anwendungen bieten Benutzerzugriff auf Hilfeinformationen, indem sie ein **Hilfemenü** in das Hauptfenster einplanen. Wenn der Benutzer ein Element  aus einem Hilfemenü auswählt, empfängt die entsprechende Fensterprozedur eine [**WM \_ COMMAND-Meldung,**](../menurc/wm-command.md) die das ausgewählte Element identifiziert. Die Anwendung antwortet, indem die entsprechenden Hilfeinformationen angezeigt werden, z. B. eine Liste von Hilfethemen, ein Index oder eine Einführung in die Anwendung.

### <a name="help-from-the-keyboard"></a>Hilfe über die Tastatur

Windows ermöglicht dem Benutzer den Zugriff auf Hilfeinformationen über die Tastatur, indem die Anwendung benachrichtigt wird, wenn der Benutzer die F1-Taste drückt. Das System sendet eine [**WM \_ HELP-Nachricht**](wm-help.md) an das Fenster, das den Tastaturfokus hatte, als der Benutzer die Taste gedrückt hat. Wenn das Fenster ein untergeordnetes Fenster ist (z. B. ein Steuerelement in einem Dialogfeld), übergibt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Nachricht an das übergeordnete Fenster. Wenn ein Menü aktiv ist, wenn F1 gedrückt wird, sendet das System die Nachricht an das Fenster, das dem Menü zugeordnet ist. Die Anwendung reagiert, indem Hilfeinformationen angezeigt werden, die dem Fenster, Steuerelement oder Menü zugeordnet sind, das den Fokus besitzt oder aktiv ist. Wenn der Benutzer beispielsweise ein Steuerelement in einem Dialogfeld auswählt und F1 drückt, zeigt die Anwendung Hilfeinformationen für dieses Steuerelement an.

Der *lParam-Parameter* von [**WM \_ HELP**](wm-help.md) ist ein Zeiger auf eine [**HELPINFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-helpinfo) die ausführliche Informationen zu dem Element enthält, für das Hilfe angefordert wird. Sie verwenden diese Informationen, um das anzuzeigende Hilfethema zu bestimmen. Die **HELPINFO-Struktur** enthält auch die Koordinaten des Mauscursors zu dem Zeitpunkt, zu dem der Benutzer die Taste gedrückt hat. Anhand dieser Informationen können Sie Hilfe basierend auf der Position des Mauszeigers bereitstellen.

### <a name="help-from-the-mouse"></a>Hilfe mit der Maus

Windows bietet dem Benutzer Zugriff auf Hilfeinformationen mit der Maus, indem die Anwendung benachrichtigt wird, wenn der Benutzer auf die rechte Maustaste klickt oder nach dem Klicken auf die Frageschaltfläche (?) auf ein Fenster, Steuerelement oder Menü klickt. Die Anwendung antwortet, indem hilfeinformationen angezeigt werden, die dem angegebenen Fenster, Steuerelement oder Menü zugeordnet sind.

Das System sendet eine [**WM \_ CONTEXTMENU-Nachricht,**](../menurc/wm-contextmenu.md) wenn der Benutzer mit der rechten Maustaste klickt. Das Fenster, auf das geklickt wurde, empfängt die Meldung. Wenn das Fenster ein untergeordnetes Fenster ist, z. B. ein -Steuerelement, übergibt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Nachricht an das übergeordnete Fenster. Die **WM \_ CONTEXTMENU-Meldung** gibt die Koordinaten des Mauszeigers an. Die x-Koordinate befindet sich im niedrigwertigen Wort des *lParam-Parameters,* und die y-Koordinate befindet sich im hochwertigen Wort. Wenn der Benutzer auf ein Steuerelement geklickt hat, ist der *wParam-Parameter* das Handle für das Steuerelement, das den Klick empfangen hat.

Das System sendet eine [**WM \_ HELP-Nachricht,**](wm-help.md) wenn der Benutzer auf ein Element in einem Fenster klickt, nachdem er auf die Schaltfläche Frage (?) geklickt hat, die in der Titelleiste des Fensters angezeigt wird. Sie können einer Titelleiste eine Frage-Schaltfläche hinzufügen, indem Sie beim Erstellen des Fensters in der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) den **WS \_ EX \_ CONTEXTHELP-Stil** angeben. Der *lParam-Parameter* von **WM \_ HELP** ist ein Zeiger auf eine [**HELPINFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-helpinfo) die ausführliche Informationen über das Element enthält, für das Hilfe angefordert wird, einschließlich der Koordinaten des Mauszeigers zu dem Zeitpunkt, zu dem der Benutzer auf die Maustaste geklickt hat.

Die Schaltfläche Frage wird nur für die Verwendung in Dialogfeldern empfohlen. In der Vergangenheit haben Anwendungen Benutzerzugriff auf Hilfeinformationen zu  einem Dialogfeld bereitgestellt, indem sie eine Schaltfläche Hilfe im Dialogfeld bereitstellen. Diese Methode wird nicht mehr empfohlen. Verwenden Sie stattdessen die Schaltfläche Frage.

### <a name="help-display-and-windows-help"></a>Hilfeanzeige und Windows Hilfe

Sobald eine Anwendung eine Hilfeanfrage erhält, sollte sie die entsprechenden Hilfeinformationen anzeigen. Da die Windows-Hilfeanwendung eine konsistente Benutzeroberfläche bietet, wird empfohlen, dass Anwendungen anstelle anderer Methoden Windows Hilfe verwenden. Um Windows Hilfe an die Anzeige von Hilfeinformationen zu richten, verwendet eine Anwendung die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) und gibt Details an, z. B. die anzuzeigenden Informationen und die Form des Fensters, in dem sie angezeigt werden sollen. In den folgenden Abschnitten wird erläutert, wie **Sie WinHelp verwenden,** um Hilfeinformationen anzuzeigen.

### <a name="help-files"></a>Hilfedateien

Um Hilfeinformationen anzeigen zu können, müssen Sie beim Aufrufen der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) eine Hilfedatei angeben. Die Hilfedatei muss das format Windows Hilfedatei (.hlp) und mindestens ein Thema enthalten. Jedes Thema ist eine unterschiedliche Informationseinheit, z. B. eine konzeptionelle Beschreibung, eine Reihe von Anweisungen, ein Bild, eine Glossardefinition und so weiter. Themen müssen eindeutig identifiziert werden, damit Windows Hilfe sie finden kann, wenn sie angefordert werden. Intern verwendet Windows Hilfe Themenbezeichner, um Themen zu suchen, aber Anwendungen verwenden meistens Kontextbezeichner (eindeutige ganzzahlige Werte), um die anzuzeigenden Themen anzugeben. Der Autor der Hilfedatei muss Den Themenbezeichnern im MAP-Abschnitt der Projektdatei, die zum Erstellen der Hilfedatei verwendet wird, explizit \[ \] Kontextbezeichner zuordnen.

Wenn Sie eine Hilfedatei angeben, aber keinen Pfad angeben, sucht [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) im Hilfeverzeichnis oder in einem durch die PATH-Umgebungsvariablen angegebenen Verzeichnis nach der Hilfedatei. Darüber hinaus kann **WinHelp** eine Hilfedatei finden, deren Name im folgenden Registrierungsspeicherort aufgeführt ist:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Um die Registrierung nutzen zu können, müssen Sie einen Wertnamen erstellen, der denselben Namen wie Ihre Hilfedatei hat. Der diesem Namen zugewiesene Wert muss das Verzeichnis sein, in dem sich die Hilfedatei befindet.

Wenn [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) die angegebenen Hilfedatei nicht finden kann, wird ein Dialogfeld angezeigt, in dem der Benutzer den Speicherort der Hilfedatei angeben kann. Da **WinHelp** die Speicherortinformationen in der Registrierung speichert, wird nicht erneut nach dem Speicherort der gleichen Hilfedatei gefragt.

Weitere Informationen zum Erstellen und Erstellen einer Hilfedatei finden Sie in der Dokumentation zu Ihren Entwicklungstools.

### <a name="starting-windows-help"></a>Starten Windows Hilfe

Im folgenden Beispiel wird die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) verwendet, um die Windows Help-Anwendung zu starten und die Hilfedatei im Thema Inhalt zu öffnen.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



Im nächsten Beispiel wird die Benutzerhilfedatei geöffnet, die Datei nach dem Thema durchsucht, das einer Schlüsselwortzeichenfolge zugeordnet ist, und anschließend wird das Thema angezeigt.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Dialogfeld "Hilfethemen"

Sie können das Dialogfeld **Hilfethemen** anzeigen, indem Sie die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) mit dem **Befehl HELP \_ FINDER** aufrufen. Mithilfe **des Dialogfelds** Hilfethemen kann der Benutzer die anzuzeigenden Themen auswählen, indem er die Titel der Themen, die den Themen zugeordneten Schlüsselwörter oder die Wörter und Ausdrücke in den Themen ankn.) Anwendungen zeigen dieses Dialogfeld in der Regel an, wenn der Benutzer im Menü Hilfe einen Befehl auswählt, z. B. Hilfethemen. Eine Anwendung kann dieses Dialogfeld auch anzeigen, wenn der Benutzer die Taste drückt, wenn kein bestimmtes Fenster, Steuerelement oder Menü in der Anwendung den Fokus besitzt oder aktiv ist.

In der Vergangenheit haben Anwendungen die Befehle **HELP \_ CONTENTS** und **HELP \_ INDEX** mit der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) verwendet, um das Inhaltsthema und den Schlüsselwortindex der Hilfedatei anzuzeigen. Diese Befehle werden nicht mehr empfohlen. Verwenden Sie **stattdessen den Befehl HELP \_ FINDER.**

### <a name="information-topics"></a>Informationsthemen

Sie können ein bestimmtes Thema anzeigen, indem Sie die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) mit dem BEFEHL HELP CONTEXT aufrufen und den \_ Kontextbezeichner für das Thema angeben. Anwendungen verwenden in der Regel den HELP CONTEXT-Befehl als Reaktion auf Benutzeranforderungen für Themen, die konzeptionelle Informationen oder prozedurale Hilfe enthalten, und nicht auf Informationen zu einem bestimmten \_ Steuerelement oder Menü. In solchen Fällen kann der Benutzer die Hilfedatei weiter durchsuchen, um nach verwandten Informationen zu suchen, bevor er zur Anwendung zurückkehrt.

Der HELP CONTEXT-Befehl ruft eine reguläre Instanz von Windows Hilfe auf, sodass der Benutzer andere Themen \_ in der Hilfedatei finden kann. In der Regel wird das Hauptfenster Hilfe angezeigt, das eine Titelleiste, ein Systemmenü, Schaltflächen zum Minimieren und Maximieren, ein Hauptmenü, eine optionale Navigationsleiste, einen Größenrahmen und einen Clientbereich enthält. Der Text des ausgewählten Themas wird im Clientbereich angezeigt, und der Benutzer kann mithilfe von hot-Links oder Navigationsschaltflächen im Hauptfenster durch die Hilfedatei navigieren. Die reguläre Instanz der Windows Hilfe kann auch verwendet werden, um Hilfe in einem oder in mindestens einem sekundären Fenster anstelle des Hauptfensters anzuzeigen.

### <a name="pop-up-topics"></a>Popupthemen

Sie können ein Popupthema anzeigen, das Informationen zu einem bestimmten Steuerelement oder Menü enthält, indem Sie die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) mit dem Befehl HELP WM HELP oder \_ HELP \_ \_ CONTEXTMENU aufrufen. Diese Befehle zeigen ein Thema in einem Popupfenster in der Nähe des entsprechenden Steuerelements oder Menüs an. Damit der Benutzer sofort zur Arbeit in der Anwendung zurückkehren kann, wird das Popupfenster zerstört, sobald der Benutzer eine Taste drückt oder auf die linke Maustaste klickt.

Sie verwenden den Help \_ WM \_ HELP-Befehl, wenn Sie [**WM \_ HELP-Meldungen**](wm-help.md) für Steuerungsfenster verarbeiten. Da die meisten Steuerelemente die **WM \_ HELP-Nachricht** an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, verarbeitet die entsprechende Dialogfeldprozedur (oder übergeordnete Fensterprozedur) diese Meldung. Anstatt einen bestimmten Kontextbezeichner anzugeben, muss die Dialogfeldprozedur ein Array von Steuerelement- und Kontextbezeichnerpaaren an [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergeben, zusammen mit dem Steuerelementhandle, das im **hItemHandle-Element** der [**HELPINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-helpinfo) angegeben ist, das mit der **WM \_ HELP-Nachricht** übergeben wird. Die -Funktion bestimmt den Bezeichner des Steuerelements, für das die **WM \_ HELP-Nachricht** generiert wurde, und verwendet den übereinstimmenden Kontextbezeichner, um das entsprechende Thema anzuzeigen.

Sie verwenden den Befehl HELP \_ CONTEXTMENU, wenn Sie [**WM \_ CONTEXTMENU-Nachrichten**](../menurc/wm-contextmenu.md) verarbeiten. Da die meisten Steuerelemente die **WM \_ CONTEXTMENU-Nachricht** an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, verarbeitet die entsprechende Dialogfeldprozedur (oder übergeordnete Fensterprozedur) diese Meldung. Die Prozedur gibt ein Array von Steuerelement- und Kontextbezeichnerpaaren an. außerdem wird das Handle im *wParam-Parameter* beim Aufrufen von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) angegeben, damit die Funktion den entsprechenden Kontextbezeichner aus dem Array auswählen und das entsprechende Thema anzeigen kann. Im Gegensatz zum \_ HELP WM \_ HELP-Befehl zeigt HELP \_ CONTEXTMENU zuerst einen What **es This?-Befehl** in einem Menü an. Wenn der Benutzer den Befehl ausgibt, zeigt **WinHelp** das Thema an. Andernfalls wird die Anforderung abgebrochen.

Sie können Popupthemen auch anzeigen, indem Sie den Befehl HELP \_ CONTEXTPOPUP verwenden und einen Kontextbezeichner des Themas angeben. Dieser Befehl ähnelt dem Befehl HELP CONTEXT, ruft jedoch die Popupinstanz von Windows Hilfe auf, die \_ von HELP WM HELP und HELP \_ \_ \_ CONTEXTMENU verwendet wird. Anwendungen können diesen Befehl als Reaktion auf [**WM \_ HELP-Meldungen**](wm-help.md) verwenden, um Hilfe für Menüs und Fenster anzuzeigen, die keine Steuerelemente in einem Dialogfeld sind. Um diesen Befehl am effektivsten zu verwenden, sollte die Anwendung diesen Menüs und Fenstern Kontextbezeichner zuweisen.

Sie können einem beliebigen Fenster oder Menü in der Anwendung einen Kontextbezeichner zuweisen. Wenn eine [**WM \_ HELP-Nachricht**](wm-help.md) generiert wird, enthält das System den Kontextbezeichner in der [**HELPINFO-Struktur,**](/windows/win32/api/winuser/ns-winuser-helpinfo) der in der **\_ WM-HILFE-Nachricht** an das übergeordnete Fenster übergeben wird. Das übergeordnete Fenster kann dann den Kontextbezeichner an [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergeben, um das angeforderte Hilfethema anzuzeigen.

Sie verwenden die [**SetWindowContextHelpId-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) um einem Fenster oder Steuerelement einen Kontextbezeichner zuzuweisen, und die [**SetMenuContextHelpId-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) um einem Menü einen Kontextbezeichner zuzuweisen. Sie können den Kontextbezeichner für ein Fenster oder Menü abrufen, indem Sie die Funktion [**GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) oder [**GetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) verwenden.

### <a name="keyword-searches"></a>Schlüsselwortsuchen

Sie können dem Benutzer ermöglichen, Themen zu suchen und anzuzeigen, indem Sie Themen in der Hilfedatei Schlüsselwörter zuweisen. Ein Schlüsselwort ist einfach eine Zeichenfolge, die einem oder mehreren Themen zugeordnet ist. Windows Die Hilfe erfasst alle Schlüsselwörter in einer Hilfedatei, platziert sie in einer Tabelle und zeigt sie in der Indexliste des Dialogfelds **Hilfethemen** an. Wenn der Benutzer ein Schlüsselwort auswählt, zeigt Windows Hilfe das zugehörige Hilfethema an, oder wenn dem Schlüsselwort mehr als ein Thema zugeordnet ist, wird eine Liste von Themen angezeigt, aus denen der Benutzer auswählen kann.

In einer Anwendung können Sie den Befehl HELP \_ KEY, HELP \_ PARTIALKEY oder HELP \_ MULTIKEY mit der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) verwenden, um Hilfethemen basierend auf ganzen oder partiellen Schlüsselwörtern zu suchen und anzuzeigen. Sie geben den Befehl, die Schlüsselwortzeichenfolge, die Hilfedatei und das Handle für das Besitzerfenster an. Wenn eine einzelne Übereinstimmung gefunden wird, zeigt **WinHelp** in allen Fällen das entsprechende Thema an. Wenn mehrere Übereinstimmungen gefunden werden, zeigt die Funktion das Dialogfeld Themen gefunden an, und der Benutzer kann auswählen, welches Thema angezeigt werden soll. Wenn keine Übereinstimmung gefunden wird, zeigt **WinHelp** entweder die Indexliste (für HELP \_ KEY und HELP \_ PARTIALKEY) oder eine Fehlermeldung (für HELP \_ MULTIKEY) an.

Ihre Anwendung kann in einem einzelnen Aufruf von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) nach mehreren Schlüsselwörtern suchen, indem sie die Schlüsselwörter durch Semikolons trennt. (Die Suche nach mehreren Schlüsselwörtern wird für Hilfedateien, die für Windows Version 3 erstellt wurden, nicht unterstützt. *x*) Sie kann auch in mehreren Hilfedateien nach Schlüsselwörtern suchen, wenn die angegebene Hilfedatei über eine Inhaltsdatei (.cnt) verfügt, die :Index- oder :Link-Befehle enthält. Mit dem Befehl HELP \_ KEY sucht **WinHelp** in allen Dateien, die von diesen Befehlen angegeben werden, nach Schlüsselwörtern. Mit den Befehlen HELP \_ MULTIKEY und HELP \_ PARTIALKEY durchsucht die Funktion alle Dateien mit Ausnahme der durch :Link-Befehle angegebenen Dateien.

Standardmäßig erkennt Windows Hilfe nur die Schlüsselworttabelle, die durch das Fußnotenzeichen K in der Hilfequelldatei identifiziert wird. Sie können Windows Hilfe anweisen, zusätzliche Schlüsselworttabellen zu erstellen, indem Sie in der Hilfequelldatei ein anderes Fußnotenzeichen als K mit der Schlüsselwortdefinition hinzufügen. (Das Fußnotenzeichen A ist jedoch reserviert.) Sie müssen alle zusätzlichen Schlüsselworttabellen definieren, indem Sie multikey-Anweisungen im \[ Abschnitt OPTIONS \] der Projektdatei verwenden, wenn Sie die Hilfedatei erstellen.

Eine Anwendung kann den Befehl HELP \_ SETINDEX mit der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) verwenden, um Windows Hilfe anweisen, eine andere Schlüsselworttabelle als K in der Indexliste anzuzeigen. Um Windows Hilfe anweisen zu können, nach einem Schlüsselwort in einer alternativen Schlüsselworttabelle zu suchen, kann eine Anwendung den \_ HELP MULTIKEY-Befehl verwenden. Sie geben das Schlüsselwort und die Schlüsselworttabelle in einer [**MULTIKEYHELP-Struktur**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) an, die Sie an **WinHelp** übergeben.

Wenn [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ein Thema anzeigt, wird es in dem Fenster angezeigt, das durch die Fußnote ">" für das Thema angegeben wird, im Fenster, das durch den Befehl :Base in der Inhaltsdatei oder im Hauptfenster angegeben wird. Wenn das Hauptfenster bereits für eine andere Hilfedatei geöffnet ist, wenn Sie **WinHelp** aufrufen, blendet die Funktion das Hauptfenster während der Suche aus. In diesem Fall wird das Hauptfenster durch Das Abbrechen der Dialogfelder **"Themen gefunden"** und **"Hilfethemen"** geschlossen.

### <a name="secondary-help-windows"></a>Sekundäre Hilfefenster

Das Hauptfenster der Windows-Hilfeanwendung wird als primäres Fenster bezeichnet. Windows Hilfe kann auch Hilfethemen in einem sekundären Fenster anzeigen. Im Gegensatz zum primären Hilfefenster enthält ein sekundäres Fenster keine Menüleiste. Sie können eine Navigationsleiste in ein sekundäres Fenster einschließen und der Leiste Schaltflächen hinzufügen. Sie können auch festlegen, dass Windows Hilfe automatisch die Höhe des sekundären Fensters anpasst, um das Thema aufzunehmen.

Sie müssen sekundäre Fenster im \[ \] Windows-Abschnitt ihrer Hilfeprojektdatei definieren und dabei den Namen und optional die Anfangsgröße und Position der einzelnen Fenster bereitstellen. Sie können die Windows Hilfeanwendung anweisen, ein Thema in einem sekundären Fenster anzuzeigen, indem Sie eine spitze Klammer (>) und den Namen, den Sie für das sekundäre Fenster definiert haben, an den Namen der Hilfedatei anfügen. Die resultierende Zeichenfolge wird dann an die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergeben.

Eine Anwendung kann die Größe und Position eines primären oder sekundären Fensters ändern, indem sie die Adresse einer [**HELPWININFO-Struktur**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) und den \_ HELP SETWINPOS-Befehl in einem Aufruf von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)angibt. **HELPWININFO** gibt den Namen des Fensters und seine neue Größe und Position an.

### <a name="training-card-help"></a>Hilfe zu Trainingskarten

Mithilfe der Trainingskartenhilfe kann eine Anwendung eine Abfolge von Anweisungen anzeigen, um den Benutzer durch die Schritte einer Aufgabe zu führen. Eine Trainingskarte besteht in der Regel aus Text, der einen bestimmten Schritt erläutert, und Schaltflächen, die TCard-Makros zugeordnet sind, sodass der Benutzer der Anwendung mitteilen kann, was als Nächstes zu tun ist. Trainingskarten können nur in sekundären Fenstern angezeigt werden und dürfen keine hot-Links zu anderen Themen in der Hilfedatei enthalten.

Eine Anwendung initiiert die Trainingskarteninstanz von Windows Help, indem sie die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) aufruft und den HELP \_ TCARD-Befehl in Kombination mit einem anderen Befehl wie HELP \_ CONTEXT angibt. Wenn der Benutzer anschließend auf eine Schaltfläche auf der Trainingskarte klickt, auf einen Dem TCard-Makro zugewiesenen Hotspots klickt oder die Trainingskarte schließt, benachrichtigt Windows Hilfe die Anwendung, indem eine [**\_ WM-TCARD-Nachricht**](wm-tcard.md) gesendet wird. Der *wParam-Parameter* identifiziert die Schaltfläche oder Benutzeraktion, und der *lParam-Parameter* enthält zusätzliche Daten, deren Bedeutung vom Wert von *wParam abhängt.*

### <a name="canceling-help"></a>Abbrechen der Hilfe

Windows Die Hilfe erfordert, dass eine Anwendung die Hilfe explizit abbricht, damit sie alle Ressourcen freigeben kann, die zum Nachverfolgen der Anwendung und ihrer Hilfedateien verwendet werden. Die Anwendung kann dies jederzeit tun, indem sie die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) aufruft und den \_ HELP QUIT-Befehl angibt. Beachten Sie, dass dies für die Popupinstanz von Windows Help nicht zutrifft. Eine Anwendung sollte nicht versuchen, eine Popupinstanz zu schließen.

Wenn eine Anwendung [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufruft, muss sie die Hilfe abbrechen, bevor sie ihr Hauptfenster schließt (z. B. als Reaktion auf die WM \_ DESTROY-Nachricht im Hauptfensterverfahren). Eine Anwendung muss **WinHelp** nur einmal aufrufen, um die Hilfe abzubrechen, unabhängig davon, wie viele Hilfedateien sie geöffnet hat. Windows Die Hilfe wird weiterhin ausgeführt, bis alle Anwendungen oder DLLs die Hilfe abgebrochen haben.

Um die Trainingskarteninstanz von Windows Help zu schließen, müssen Sie beim Aufrufen von WinHelp die Befehle HELP \_ TCARD und HELP \_ QUIT [](/windows/desktop/api/Winuser/nf-winuser-winhelpa)angeben. Eine Anwendung muss die Trainingskarteninstanz von Windows Hilfe nicht abbrechen, wenn der Benutzer sie zuerst abbricht. Windows Hilfe benachrichtigt eine Anwendung, wenn der Benutzer die Trainingskarteninstanz abbricht, indem die [**\_ WM-TCARD-Nachricht**](wm-tcard.md) mit dem *wParam-Parameter* auf IDCLOSE festgelegt wird.

## <a name="using-help"></a>Verwenden der Hilfe

In diesem Abschnitt erfahren Sie, wie Sie kontextbezogene Hilfe für ein Dialogfeld bereitstellen und die Darstellung eines sekundären Hilfefensters festlegen.

-   [Bereitstellen von Hilfe in einem Dialogfeld](#providing-help-in-a-dialog-box)
-   [Festlegen der Darstellung eines sekundären Hilfefensters](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Bereitstellen von Hilfe in einem Dialogfeld

Um kontextbezogene Hilfe in einem Dialogfeld bereitzustellen, müssen Sie ein Array erstellen, das aus Paaren von **DWORD-Werten** besteht. Der erste Wert in jedem Paar ist der Bezeichner eines Steuerelements im Dialogfeld, und der zweite ist der Kontextbezeichner des Hilfethemas für das Steuerelement. Das Array sollte ein Bezeichnerpaar für jedes Steuerelement im Dialogfeld enthalten.

Die Dialogfeldprozedur muss die [**\_ WM-HILFE-**](wm-help.md) und [**WM \_ CONTEXTMENU-Meldungen**](../menurc/wm-contextmenu.md) verarbeiten. Die Dialogfeldprozedur empfängt **\_ WM-HILFE,** wenn der Benutzer die TASTE drückt, und **WM \_ CONTEXTMENU,** wenn der Benutzer mit der rechten Maustaste klickt.

Der *lParam-Parameter* von [**WM \_ HELP**](wm-help.md) enthält die Adresse einer [**HELPINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-helpinfo) Der **hItemHandle-Member** dieser Struktur identifiziert das Steuerelement, für das der Benutzer Hilfe angefordert hat. Sie müssen dieses Handle [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) zusammen mit dem \_ HELP WM \_ HELP-Befehl, dem Namen Ihrer Hilfedatei und einem Zeiger auf das Array von Bezeichnern an die WinHelp-Funktion übergeben. Die **WinHelp-Funktion** durchsucht das Array nach dem Steuerelementbezeichner des angegebenen Steuerelements und ruft dann den entsprechenden Hilfekontextbezeichner ab. Als Nächstes übergibt die Funktion den Hilfekontextbezeichner an Windows Hilfe, die das entsprechende Thema sucht und in einem Popupfenster anzeigt. Wenn das Steuerelement über den Bezeichner -1 verfügt, sucht das System nach dem nächsten Steuerelement, bei dem es sich um einen Tabstopp handelt, und verwendet dann seinen Bezeichner, um den Hilfekontextbezeichner zu suchen. Aus diesem Grund ist es wichtig, dass Sie statischen Text vor Steuerelementen in einer Ressourcendatei platzieren.

Beim Aufrufen der [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ähnelt die Verarbeitung von [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) der Verarbeitung von [**WM \_ HELP**](wm-help.md) mit diesen beiden Ausnahmen:

-   Sie übergeben den *wParam-Parameter* von [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md), das das Handle an das Steuerelement darstellt, das die Nachricht gesendet hat.
-   Sie geben den **Befehl HELP \_ CONTEXTMENU** anstelle von **HELP WM HELP \_ \_ an.**

Der **Befehl HELP \_ CONTEXTMENU** bewirkt, dass Windows Hilfe ein Menü anzeigt, bevor das Hilfethema angezeigt wird. Das Menü ist systemdefiniert. Dadurch kann der Benutzer Hilfe für das Steuerelement oder das Dialogfeld **Hilfethemen** anzeigen.

Das folgende Beispiel zeigt, wie kontextbezogene Hilfe in einem Dialogfeld implementiert wird.


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Festlegen der Darstellung eines sekundären Hilfefensters

Eine Anwendung kann die Größe, Position und den Status eines sekundären Hilfefensters festlegen, indem sie den Befehl HELP \_ SETWINPOS und die Adresse einer [**HELPWININFO-Struktur**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) an die [**WinHelp-Funktion**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergibt. Die Member von **HELPWININFO** geben den Namen des fensters an, das geändert werden soll, sowie die neue Größe, Position und den Status des Fensters.

Im folgenden Beispiel wird die Darstellung eines sekundären Fensters mit dem Namen "wnd \_ menu" festgelegt. Der Name muss im \[ \] Windows-Abschnitt der Hilfeprojektdatei definiert werden.


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
