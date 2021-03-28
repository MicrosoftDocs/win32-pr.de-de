---
description: 'Die Online Hilfe kann in einer Vielzahl von Formularen stehen, von detaillierten konzeptionellen Informationen bis hin zu schnell Definitionen. Dieses Thema enthält folgende Abschnitte:'
title: Behandeln der Online Hilfe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f1c125df135068c2eee37cb33a8a9d2b281b1f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994695"
---
# <a name="handling-online-help"></a>Behandeln der Online Hilfe

Die Online Hilfe kann in einer Vielzahl von Formularen stehen, von detaillierten konzeptionellen Informationen bis hin zu schnell Definitionen. Dieses Thema enthält folgende Abschnitte:

-   [Informationen zur Hilfe](#about-help)
    -   [Hilfeanfragen](#help-requests)
    -   [Hilfe Anzeige und Windows-Hilfe](#help-display-and-windows-help)
-   [Verwenden der Hilfe](#using-help)
    -   [Bereitstellen von Hilfe in einem Dialog Feld](#providing-help-in-a-dialog-box)
    -   [Festlegen des Erscheinungs Bilds eines sekundären Hilfe Fensters](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Informationen zur Hilfe

Ein wichtiges Element einer benutzerfreundlichen Anwendung ist in der Online Hilfe verfügbar. Windows stellt Funktionen und Meldungen bereit, die bei der Verwendung in Verbindung mit der Windows-Hilfe Anwendung es Ihnen ermöglichen, die Online Hilfe in Ihrer Anwendung zu implementieren. In dieser Übersicht werden die Elemente von Windows erläutert, die die Online Hilfe unterstützen. Es wird beschrieben, wie diese Elemente verwendet werden, um Benutzern das Anfordern von Hilfe zu ermöglichen, und es wird erläutert, wie die Windows-Hilfe Anwendung verwendet wird, um die Hilfe anzuzeigen.

### <a name="help-requests"></a>Hilfeanfragen

Die meisten Windows-basierten Anwendungen bieten Online Hilfe Informationen in einer Vielzahl von Formularen. Sie reichen von der konzeptionellen Hilfe aus, in der der Zweck der Funktionen einer Anwendung erläutert wird, um eine Popup Hilfe zu erhalten, die schnelle Definitionen einzelner Elemente in der Benutzeroberfläche der Anwendung bereitstellt. Mithilfe von Funktionen und Nachrichten können Sie Benutzern verschiedene Möglichkeiten zum Anfordern des Zugriffs auf diese Informationen zur Verfügung stellen. In den folgenden Abschnitten werden diese Hilfeanfragen beschrieben.

### <a name="help-menu"></a>Menü "Hilfe"

Die meisten Anwendungen bieten Benutzern Zugriff auf Hilfe Informationen, indem  Sie im Hauptfenster ein Hilfemenü einschließen. Wenn der Benutzer ein Element aus einem **Hilfemenü** auswählt, empfängt die entsprechende Fenster Prozedur eine WM- [**\_ Befehls**](../menurc/wm-command.md) Meldung, mit der das ausgewählte Element identifiziert wird. Die Anwendung antwortet, indem die entsprechenden Hilfe Informationen angezeigt werden, wie z. b. eine Liste der Hilfe Themen, ein Index oder eine Einführung in die Anwendung.

### <a name="help-from-the-keyboard"></a>Hilfe von der Tastatur

Windows ermöglicht Benutzern den Zugriff auf Informationen von der Tastatur, indem die Anwendung benachrichtigt wird, wenn der Benutzer die F1-Taste drückt. Das System sendet eine [**WM- \_ Hilfe**](wm-help.md) Meldung an das Fenster mit dem Tastaturfokus, wenn der Benutzer die Taste gedrückt hat. Wenn das Fenster ein untergeordnetes Fenster ist (z. b. ein Steuerelement in einem Dialogfeld), übergibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Nachricht an das übergeordnete Fenster. Wenn ein Menü aktiv ist, wenn F1 gedrückt wird, sendet das System die Meldung an das Fenster, das dem Menü zugeordnet ist. Die Anwendung antwortet, indem Hilfe Informationen angezeigt werden, die dem Fenster, der Steuerung oder dem Menü zugeordnet sind, das bzw. das den Fokus besitzt oder aktiv ist. Wenn der Benutzer z. b. ein Steuerelement in einem Dialogfeld auswählt und F1 drückt, zeigt die Anwendung Hilfe Informationen für dieses Steuerelement an.

Der *LPARAM* -Parameter der [**WM- \_ Hilfe**](wm-help.md) ist ein Zeiger auf eine [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die ausführliche Informationen über das Element enthält, für das die Hilfe angefordert wird. Anhand dieser Informationen können Sie das anzuzeigende Hilfethema ermitteln. Die **helpinfo** -Struktur enthält auch die Koordinaten des Mauszeigers zu dem Zeitpunkt, zu dem der Benutzer die Taste gedrückt hat. Sie können diese Informationen verwenden, um Hilfe basierend auf der Position des Mauszeigers bereitzustellen.

### <a name="help-from-the-mouse"></a>Hilfe von der Maus

Windows ermöglicht dem Benutzer den Zugriff auf Hilfe Informationen durch den Benutzer, indem er die Anwendung benachrichtigt, wenn der Benutzer mit der rechten Maustaste klickt oder auf ein Fenster, ein Steuerelement oder ein Menü klickt, nachdem er auf die Schaltfläche Frage (?) geklickt hat. Die Anwendung antwortet, indem Hilfe Informationen angezeigt werden, die dem angegebenen Fenster, Steuerelement oder Menü zugeordnet sind.

Das System sendet eine [**WM- \_ ContextMenu**](../menurc/wm-contextmenu.md) -Meldung, wenn der Benutzer mit der rechten Maustaste klickt. Das Fenster, auf das geklickt wurde, empfängt die Meldung. Wenn das Fenster ein untergeordnetes Fenster ist, z. b. ein-Steuerelement, übergibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Nachricht an das übergeordnete Fenster. Die " **WM \_ ContextMenu** "-Meldung gibt die Koordinaten des Mauszeigers an. Die x-Koordinate befindet sich in einem nieder wertigen Wort des *LPARAM* -Parameters, und die y-Koordinate befindet sich im hohen Bestell Wort. Wenn der Benutzer auf ein Steuerelement geklickt hat, ist der *wParam* -Parameter das Handle für das Steuerelement, das den Klick erhalten hat.

Das System sendet eine [**WM- \_ Hilfe**](wm-help.md) Nachricht, wenn der Benutzer auf ein Element in einem Fenster klickt, nachdem er auf die Schaltfläche "Frage (?)" geklickt hat, die in der Titelleiste des Fensters angezeigt wird. Sie können einer Titelleiste eine Frage Schaltfläche hinzufügen, indem Sie beim Erstellen des Fensters den Stil " **WS \_ Ex \_ CONTEXTHELP** " in [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion" angeben. Der *LPARAM* -Parameter der **WM- \_ Hilfe** ist ein Zeiger auf eine [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die ausführliche Informationen über das Element enthält, für das die Hilfe angefordert wird, einschließlich der Koordinaten des Mauszeigers zu dem Zeitpunkt, zu dem der Benutzer auf die Maustaste geklickt hat.

Die Frage Schaltfläche wird nur für die Verwendung in Dialogfeldern empfohlen. In der Vergangenheit haben Anwendungen Benutzer Zugriff auf Hilfe Informationen zu einem Dialogfeld bereitgestellt, indem Sie im Dialogfeld eine Schaltfläche " **Hilfe** " bereitstellen. Diese Methode wird nicht mehr empfohlen. Verwenden Sie stattdessen die Frage Schaltfläche.

### <a name="help-display-and-windows-help"></a>Hilfe Anzeige und Windows-Hilfe

Sobald eine Anwendung eine Hilfe Anforderung erhält, sollte Sie die entsprechenden Hilfe Informationen anzeigen. Da die Windows-Hilfe Anwendung eine konsistente Benutzeroberfläche bereitstellt, wird empfohlen, dass Anwendungen anstelle anderer Methoden die Windows-Hilfe verwenden. Um die Windows-Hilfe zum Anzeigen von Hilfe Informationen weiterzuleiten, verwendet eine Anwendung die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion und gibt Details wie z. b. die anzuzeigenden Informationen und die Form des Fensters an, in dem Sie angezeigt werden soll. In den folgenden Abschnitten wird erläutert, wie Sie mit **WinHelp** Hilfe Informationen anzeigen können.

### <a name="help-files"></a>Hilfedateien

Wenn Sie Hilfe Informationen anzeigen möchten, müssen Sie beim Aufrufen der [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion eine Hilfedatei angeben. Die Hilfedatei muss das Windows-Hilfedatei Format (. hlp) und mindestens ein Thema enthalten. Jedes Thema ist eine eindeutige Informationseinheit, z. b. eine konzeptionelle Beschreibung, eine Reihe von Anweisungen, ein Bild, eine Glossar Definition usw. Die Themen müssen eindeutig identifiziert werden, damit Sie von der Windows-Hilfe gefunden werden können, wenn Sie angefordert werden. Intern verwendet die Windows-Hilfe Themen Bezeichner, um nach Themen zu suchen, aber Anwendungen verwenden häufig Kontext Bezeichner (eindeutige ganzzahlige Werte), um die anzuzeigenden Themen anzugeben. Der Autor der Hilfedatei muss den Themen bezeichgern im \[ Karten \] Abschnitt der Projektdatei, die zum Erstellen der Hilfedatei verwendet wird, explizit Kontext Bezeichner zuordnen.

Wenn Sie eine Hilfedatei angeben, aber keinen Pfad angeben, sucht [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) nach der Hilfedatei im Hilfe Verzeichnis oder in einem Verzeichnis, das in der PATH-Umgebungsvariablen angegeben ist. Außerdem kann **WinHelp** eine Hilfedatei finden, deren Name im folgenden Registrierungs Speicherort aufgeführt ist:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Um die Registrierung zu nutzen, müssen Sie einen Wertnamen erstellen, der den gleichen Namen wie die Hilfedatei hat. Der diesem Namen zugewiesene Wert muss das Verzeichnis sein, in dem sich die Hilfedatei befindet.

Wenn die angegebene Hilfedatei von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) nicht gefunden werden kann, wird ein Dialogfeld angezeigt, in dem der Benutzer den Speicherort der Hilfedatei angeben kann. Da **WinHelp** die Speicherort Informationen in der Registrierung speichert, wird der Speicherort der gleichen Hilfedatei nicht erneut angefordert.

Weitere Informationen zum Erstellen und Erstellen einer Hilfedatei finden Sie in der Dokumentation, die mit ihren Entwicklungs Tools bereitgestellt wird.

### <a name="starting-windows-help"></a>Starten der Windows-Hilfe

Im folgenden Beispiel wird die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion verwendet, um die Windows-Hilfe Anwendung zu starten und die Hilfedatei für Ihr Inhalts Thema zu öffnen.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



Im nächsten Beispiel wird die Benutzerhilfe Datei geöffnet, die Datei nach dem Thema durchsucht, das einer Schlüsselwort Zeichenfolge zugeordnet ist, und anschließend wird das Thema angezeigt.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Hilfe Themen (Dialogfeld)

Sie können das Dialogfeld **Hilfe Themen** anzeigen, indem Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion mit dem Befehl **Help \_ Finder** aufrufen. Im Dialogfeld **Hilfe Themen** können Benutzer die anzuzeigenden Themen auswählen, indem Sie die Titel der Themen, die den Themen zugeordneten Schlüsselwörter oder die Wörter und Ausdrücke in den Themen anzeigen. Anwendungen zeigen dieses Dialogfeld in der Regel an, wenn der Benutzer im Menü Hilfe einen Befehl (z. b. Hilfe Themen) auswählt. In einer Anwendung kann dieses Dialogfeld auch angezeigt werden, wenn der Benutzer die Taste drückt, wenn kein bestimmtes Fenster, Steuerelement oder Menü in der Anwendung den Fokus hat oder aktiv ist.

In der Vergangenheit haben Anwendungen die **Hilfe \_ Inhalte** und **Hilfe \_ Index** Befehle mit der [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion verwendet, um das Inhalts Thema und den Schlüsselwort Index der Hilfedatei anzuzeigen. Diese Befehle werden nicht mehr empfohlen. Verwenden Sie stattdessen den **Help \_ Finder** -Befehl.

### <a name="information-topics"></a>Informationsthemen

Sie können ein bestimmtes Thema anzeigen, indem Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion mit dem Hilfe \_ Kontext Befehl aufrufen und den Kontext Bezeichner für das Thema angeben. Anwendungen verwenden den Hilfekontext-Befehl in der Regel als \_ Reaktion auf Benutzer Anforderungen für Themen, die konzeptionelle Informationen oder eine Verfahrenshilfe enthalten, anstelle von Informationen zu einem bestimmten Steuerelement oder Menü. In solchen Fällen wird der Benutzer möglicherweise weiterhin in der Hilfedatei nach verwandten Informationen suchen, bevor er zur Anwendung zurückkehrt.

Der Hilfe \_ Kontext Befehl ruft eine reguläre Instanz der Windows-Hilfe auf und ermöglicht dem Benutzer das Auffinden weiterer Themen in der Hilfedatei. In der Regel wird das Haupt Hilfefenster angezeigt, das eine Titelleiste, ein Systemmenü, eine Schaltfläche zum minimieren und maximieren, ein Hauptmenü, eine optionale Navigationsleiste, einen Größen Anpassungsrahmen und einen Client Bereich enthält. Der Text des ausgewählten Themas wird im Client Bereich angezeigt, und der Benutzer kann über die Hilfedatei durch die Verwendung von "Hot Links" oder Navigations Schaltflächen im Hauptfenster navigieren. Die reguläre Instanz der Windows-Hilfe kann auch verwendet werden, um die Hilfe in einem oder mehreren sekundären Fenstern anstelle des Hauptfensters anzuzeigen.

### <a name="pop-up-topics"></a>Popup Themen

Sie können ein Popup Thema anzeigen, das Informationen für ein bestimmtes Steuerelement oder Menü enthält, indem Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion mit dem Hilfe- \_ WM-Hilfe- \_ oder Help \_ ContextMenu-Befehl aufrufen. Diese Befehle zeigen ein Thema in einem Popup Fenster in der Nähe des entsprechenden Steuer Elements oder Menüs an. Damit der Benutzer sofort zur Arbeit in der Anwendung zurückkehren kann, wird das Popup Fenster zerstört, sobald der Benutzer eine Taste drückt oder mit der linken Maustaste klickt.

Sie verwenden den Help \_ WM Help- \_ Befehl bei der Verarbeitung von [**WM- \_ Hilfe**](wm-help.md) Nachrichten für Steuerelement Fenster. Da die meisten Steuerelemente die **WM- \_ Hilfe** Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben, verarbeitet die entsprechende Dialogfeld Prozedur (oder übergeordnete Fenster Prozedur) diese Nachricht. Anstatt einen bestimmten Kontext Bezeichner anzugeben, muss die Dialogfeld Prozedur ein Array von Steuerelement-und kontextbezeichnerpaaren an [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergeben, zusammen mit dem Steuerelement handle, das im **hitemhandle** -Member der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur angegeben ist, die mit der **WM- \_ Hilfe** Nachricht übergeben wird. Die-Funktion bestimmt den Bezeichner des Steuer Elements, für das die **WM- \_ Hilfe** Nachricht generiert wurde, und verwendet den passenden Kontext Bezeichner, um das entsprechende Thema anzuzeigen.

\_Beim Verarbeiten von [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) -Nachrichten verwenden Sie den Befehl "Hilfe" ContextMenu. Da die meisten Steuerelemente die **WM- \_ ContextMenu** -Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben, verarbeitet die entsprechende Dialogfeld Prozedur (oder übergeordnete Fenster Prozedur) diese Nachricht. Die Prozedur gibt ein Array von Steuerelement-und kontextbezeichnerpaaren an. Außerdem wird das Handle im *wParam* -Parameter beim Aufrufen von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) angegeben, sodass die Funktion den entsprechenden Kontext Bezeichner aus dem Array auswählen und das entsprechende Thema anzeigen kann. Im Gegensatz zum Help \_ WM \_ Help-Befehl \_ zeigt Help ContextMenu zuerst **den Befehl What es this?** in einem Menü an. Wenn der Benutzer den Befehl auswählt, zeigt **WinHelp** das Thema an. Andernfalls wird die Anforderung abgebrochen.

Sie können Popup Themen auch anzeigen, indem Sie den Hilfe \_ contextpopup-Befehl verwenden und einen Kontext Bezeichner des Themas angeben. Dieser Befehl ähnelt dem Hilfe \_ Kontext Befehl, ruft jedoch die Popup Instanz der Windows-Hilfe auf, die von Help \_ WM \_ Help und Help \_ ContextMenu verwendet wird. Anwendungen können diesen Befehl als Antwort auf die [**WM- \_ Hilfe**](wm-help.md) Nachrichten verwenden, um Hilfe für Menüs und für Fenster anzuzeigen, die keine Steuerelemente in einem Dialogfeld sind. Damit dieser Befehl am effektivsten verwendet werden kann, sollte die Anwendung diesen Menüs und Fenstern Kontext Bezeichner zuweisen.

Sie können jedem Fenster oder Menü in der Anwendung einen Kontext Bezeichner zuweisen. Wenn eine [**WM- \_ Hilfe**](wm-help.md) Meldung generiert wird, enthält das System den Kontext Bezeichner in der [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die an das übergeordnete Fenster in der **WM- \_ Hilfe** Nachricht weitergeleitet wird. Das übergeordnete Fenster kann dann den Kontext Bezeichner an [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) übergeben, um das angeforderte Hilfethema anzuzeigen.

Mithilfe der [**setwindowcontexthelpid**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) -Funktion können Sie einem Fenster oder Steuerelement einen Kontext Bezeichner zuweisen und die [**setmenucontexthelpid**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) -Funktion verwenden, um einem Menü einen Kontext Bezeichner zuzuweisen. Sie können den Kontext Bezeichner für ein Fenster oder Menü mithilfe der [**getwindowcontexthelpid**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) -Funktion oder der [**getmenucontexthelpid**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) -Funktion abrufen.

### <a name="keyword-searches"></a>Schlüsselwort Suche

Sie können es Benutzern ermöglichen, Themen zu suchen und anzuzeigen, indem Sie den Themen in der Hilfedatei Schlüsselwörter zuweisen. Ein Schlüsselwort ist einfach eine Zeichenfolge, die einem oder mehreren Themen zugeordnet ist. Windows Help sammelt alle Schlüsselwörter in einer Hilfedatei, platziert Sie in einer Tabelle und zeigt Sie in der Index Liste des Dialog Felds **Hilfe Themen** an. Wenn der Benutzer ein Schlüsselwort auswählt, zeigt die Windows-Hilfe das zugehörige Hilfethema an oder zeigt eine Liste der Themen an, aus denen der Benutzer auswählen kann, wenn dem Schlüsselwort mehr als ein Thema zugeordnet ist.

In einer Anwendung können Sie mithilfe der Funktion "Hilfe" \_ , "Hilfe \_ partialkey" oder "Help \_ multikey" mit der Funktion " [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) " Hilfe Themen suchen und anzeigen, die auf ganzzahligen oder partiellen Schlüsselwörtern basieren. Sie geben den Befehl, die Schlüsselwort Zeichenfolge, die Hilfedatei und das Handle für das Besitzer Fenster an. In allen Fällen zeigt **WinHelp** das entsprechende Thema an, wenn eine einzelne Übereinstimmung gefunden wird. Wenn mehrere Übereinstimmungen gefunden werden, zeigt die Funktion das Dialogfeld gefundene Themen an, und der Benutzer kann auswählen, welches Thema Sie anzeigen möchten. Wenn keine Entsprechung gefunden wird, zeigt **WinHelp** entweder die Index Liste (für Hilfe \_ Schlüssel und Hilfe \_ partialkey) an oder zeigt eine Fehlermeldung an (für Hilfe- \_ Multikey).

Die Anwendung kann in einem einzelnen [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Befehl nach mehreren Schlüsselwörtern suchen, indem Sie die Schlüsselwörter durch Semikolons trennt. (Das Suchen nach mehreren Schlüsselwörtern wird nicht für Hilfedateien unterstützt, die für Windows Version 3 erstellt wurden. *x*) Sie kann auch über mehrere Hilfedateien hinweg nach Schlüsselwörtern suchen, wenn die angegebene Hilfedatei über eine Inhalts Datei (. CNT) verfügt, die die Befehle Index oder: Link enthält. Mit dem \_ Befehl Hilfe Key sucht **WinHelp** in allen durch diese Befehle angegebenen Dateien nach Schlüsselwörtern. Mit den Befehlen "Help \_ multikey" und "Help \_ partialkey" durchsucht die Funktion alle Dateien, mit Ausnahme derjenigen, die durch: Link Befehle angegeben werden.

Standardmäßig erkennt Windows Help nur die Schlüsselwort Tabelle, die durch das K Fußnote-Zeichen in der Hilfe Quelldatei identifiziert wird. Sie können die Windows-Hilfe weiterleiten, um zusätzliche Schlüsselwort Tabellen zu erstellen, indem Sie in der Hilfe Quelldatei ein anderes fußnotiz Zeichen als K mit der Schlüsselwort Definition hinzufügen. (Das fußnotiz Zeichen A ist jedoch reserviert.) Sie müssen alle zusätzlichen Schlüsselwort Tabellen definieren, indem Sie bei der \[ \] Erstellung der Hilfedatei im Abschnitt "Optionen" der Projektdatei eine multikey-Anweisung verwenden.

Eine Anwendung kann den Befehl Hilfe \_ SetIndex mit der [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion verwenden, um die Windows-Hilfe anzuweisen, eine andere Schlüsselwort Tabelle als K in der Index Liste anzuzeigen. Um die Windows-Hilfe zum Suchen nach einem Schlüsselwort in einer alternativen Schlüsselwort Tabelle zu verwenden, kann eine Anwendung den Help \_ multikey-Befehl verwenden. Sie geben das Schlüsselwort und die Schlüsselwort Tabelle in einer [**multikeyhelp**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) -Struktur an, die Sie an **WinHelp** übergeben.

Wenn [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ein Thema anzeigt, wird es in dem Fenster angezeigt, das durch den ">"-Fußnote für das Thema angegeben wird, und zwar im Fenster, das durch den Befehl: base in der Inhalts Datei oder im Hauptfenster angegeben wird. Wenn das Hauptfenster beim Abrufen von **WinHelp** bereits für eine andere Hilfedatei geöffnet ist, blendet die Funktion das Hauptfenster beim Suchen aus. Wenn Sie in diesem Fall sowohl die **gefundenen Themen** als auch die Dialogfelder der **Hilfe Themen** abbrechen, wird das Hauptfenster geschlossen.

### <a name="secondary-help-windows"></a>Sekundäre Hilfefenster

Das Hauptfenster der Windows-Hilfe Anwendung wird als primäres Fenster bezeichnet. In der Windows-Hilfe können auch Hilfe Themen in einem sekundären Fenster angezeigt werden. Im Gegensatz zum primären Hilfefenster enthält ein sekundäres Fenster keine Menüleiste. Sie können eine Navigationsleiste in ein sekundäres Fenster einschließen, und Sie können der Leiste Schaltflächen hinzufügen. Sie können auch festlegen, dass die Windows-Hilfe automatisch die Höhe des sekundären Fensters anpasst, um das Thema zu berücksichtigen.

Sie müssen sekundäre Fenster im Windows- \[ \] Abschnitt der Hilfeprojekt Datei definieren, indem Sie den Namen und optional die anfängliche Größe und Position jedes Fensters angeben. Sie können die Windows-Hilfe Anwendung zum Anzeigen eines Themas in einem sekundären Fenster leiten, indem Sie eine Spitze Klammer (>) und den Namen, den Sie für das sekundäre Fenster definiert haben, an den Namen der Hilfedatei anfügen. Die resultierende Zeichenfolge wird dann an die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion weitergeleitet.

Eine Anwendung kann die Größe und Position eines primären oder sekundären Fensters ändern, indem Sie die Adresse einer [**helpwininfo**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) -Struktur und den Hilfe- \_ setwinpos-Befehl in einem Aufrufen von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)angibt. **Helpwininfo** gibt den Namen des Fensters und seine neue Größe und Position an.

### <a name="training-card-help"></a>Hilfe zu Schulungs Karten

Mithilfe der Hilfe zu Schulungs Karten kann eine Anwendung eine Sequenz von Anweisungen anzeigen, die den Benutzer durch die Schritte einer Aufgabe führt. Eine Schulungs Karte besteht in der Regel aus Text, in dem ein bestimmter Schritt und Schaltflächen erläutert werden, die mit TCard-Makros verknüpft sind. Dadurch kann der Benutzer der Anwendung mitteilen, was Sie als nächstes tun möchten. Schulungs Karten können nur in sekundären Fenstern angezeigt werden und dürfen keine heißen Links zu anderen Themen in der Hilfedatei enthalten.

Eine Anwendung initiiert die Trainingskarten Instanz der Windows-Hilfe, indem Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion aufruft und den Help \_ TCard-Befehl in Verbindung mit einem anderen Befehl, z. b. dem Hilfe Kontext, angibt \_ . Wenn der Benutzer anschließend auf eine Schaltfläche in der Trainings Karte klickt, auf einen Hotspot klickt, der dem TCard-Makro zugewiesen ist, oder die Schulungs Karte schließt, benachrichtigt die Windows-Hilfe die Anwendung, indem er eine [**WM- \_ TCard**](wm-tcard.md) -Nachricht sendet. Der *wParam* -Parameter identifiziert die Schaltfläche oder die Benutzeraktion, und der *LPARAM* -Parameter enthält zusätzliche Daten. die Bedeutung von hängt vom Wert von *wParam* ab.

### <a name="canceling-help"></a>Abbrechen der Hilfe

Die Windows-Hilfe erfordert, dass die Hilfe von einer Anwendung explizit abgebrochen wird, damit alle Ressourcen freigegeben werden können, die zum Nachverfolgen der Anwendung und ihrer Hilfedateien verwendet werden. Die Anwendung kann dies jederzeit erreichen, indem Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion aufrufen und den Befehl "Hilfe beenden" angeben \_ . Beachten Sie, dass dies für die Popup Instanz der Windows-Hilfe nicht zutrifft. Eine Anwendung sollte nicht versuchen, eine Popup Instanz zu schließen.

Wenn eine Anwendung [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)aufruft, muss Sie die Hilfe abbrechen, bevor das Hauptfenster geschlossen wird (z. b. als Antwort auf die WM-Lösch \_ Nachricht in der Hauptfenster Prozedur). Eine Anwendung muss **WinHelp** nur einmal anrufen, um die Hilfe abzubrechen, unabhängig davon, wie viele Hilfedateien Sie geöffnet hat. Die Windows-Hilfe wird weiterhin ausgeführt, bis alle Anwendungen oder DLLs die Hilfe abgebrochen haben.

Um die Trainingskarten Instanz der Windows-Hilfe zu schließen, müssen Sie \_ \_ beim Aufrufen von [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)sowohl die Help TCard-als auch die help quit-Befehle angeben. Die Trainingskarten Instanz der Windows-Hilfe muss von einer Anwendung nicht abgebrochen werden, wenn der Benutzer Sie zuerst abbricht. In der Windows-Hilfe wird eine Anwendung benachrichtigt, wenn der Benutzer die Trainingskarten Instanz abbricht, indem die [**WM- \_ TCard**](wm-tcard.md) -Nachricht mit dem *wParam* -Parameter auf idclose gesendet wird.

## <a name="using-help"></a>Verwenden der Hilfe

In diesem Abschnitt wird gezeigt, wie die kontextbezogene Hilfe für ein Dialogfeld bereitgestellt wird und wie die Darstellung eines sekundären Hilfe Fensters festgelegt wird.

-   [Bereitstellen von Hilfe in einem Dialog Feld](#providing-help-in-a-dialog-box)
-   [Festlegen des Erscheinungs Bilds eines sekundären Hilfe Fensters](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Bereitstellen von Hilfe in einem Dialog Feld

Um kontextbezogene Hilfe in einem Dialogfeld bereitzustellen, müssen Sie ein Array erstellen, das aus Paaren von **DWORD** -Werten besteht. Der erste Wert in jedem Paar ist der Bezeichner eines Steuer Elements im Dialogfeld, und der zweite Wert ist der Kontext Bezeichner des Hilfe Themas für das Steuerelement. Das Array sollte ein Bezeichner Paar für jedes Steuerelement im Dialogfeld enthalten.

In der Dialogfeld Prozedur müssen die Nachrichten [**WM \_ Help**](wm-help.md) und [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) verarbeitet werden. Die Dialogfeld Prozedur empfängt die **WM- \_ Hilfe** , wenn der Benutzer die Taste und das **WM- \_ Kontextmenü** drückt, wenn der Benutzer mit der rechten Maustaste klickt.

Der *LPARAM* -Parameter der [**WM- \_ Hilfe**](wm-help.md) enthält die Adresse einer [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur. Der **hitemhandle** -Member dieser Struktur identifiziert das Steuerelement, für das der Benutzerhilfe angefordert hat. Sie müssen dieses Handle zusammen mit dem [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Help- \_ WM \_ -Befehl, dem Namen der Hilfedatei und einem Zeiger auf das Array von Bezeichners an die WinHelp-Funktion übergeben. Die **WinHelp** -Funktion durchsucht das Array nach dem Steuerelement Bezeichner des angegebenen Steuer Elements und ruft dann den entsprechenden Hilfe Kontext Bezeichner ab. Als nächstes übergibt die Funktion den Hilfe Kontext Bezeichner an die Windows-Hilfe, die das entsprechende Thema findet und in einem Popup Fenster anzeigt. Wenn das Steuerelement den Bezeichner-1 aufweist, sucht das System nach dem nächsten Steuerelement, das ein Tabstopp ist, und verwendet dann seinen Bezeichner, um den Hilfe Kontext Bezeichner zu suchen. Aus diesem Grund ist es wichtig, dass Sie statischen Text vor Steuerelementen in einer Ressourcen Datei platzieren.

Wenn Sie die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion aufrufen, ähnelt die Verarbeitung von [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) der Verarbeitung der [**WM- \_ Hilfe**](wm-help.md) mit diesen beiden Ausnahmen:

-   Sie übergeben den *wParam* -Parameter aus dem [**WM- \_ Kontextmenü**](../menurc/wm-contextmenu.md), bei dem es sich um das Handle für das Steuerelement handelt, das die Nachricht gesendet hat.
-   Sie geben den **Hilfe \_ Kontextmenü** Befehl anstelle der **Hilfe \_ WM- \_ Hilfe** an.

Der **\_ Kontextmenü** Befehl bewirkt, dass die Windows-Hilfe ein Menü anzeigt, bevor das Hilfethema angezeigt wird. Das Menü ist System definiert. Dadurch kann der Benutzer die Hilfe für das Steuerelement anzeigen oder das Dialogfeld **Hilfe Themen** anzeigen.

Im folgenden Beispiel wird gezeigt, wie die kontextbezogene Hilfe in einem Dialogfeld implementiert wird.


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



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Festlegen des Erscheinungs Bilds eines sekundären Hilfe Fensters

Eine Anwendung kann die Größe, Position und Anzeige des Zustands eines sekundären Hilfe Fensters festlegen, indem der \_ Befehl Hilfe setwinpos und die Adresse einer [**helpwininfo**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) -Struktur an die [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion übergeben werden. Die Member von **helpwininfo** geben den Namen des zu ändernden Fensters und die neue Größe, Position und Anzeige des Fensters an.

Im folgenden Beispiel wird das Aussehen eines sekundären Fensters mit dem Namen "WND \_ Menu" festgelegt. Der Name muss im \[ Windows- \] Abschnitt der Hilfeprojekt Datei definiert werden.


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



 

 
