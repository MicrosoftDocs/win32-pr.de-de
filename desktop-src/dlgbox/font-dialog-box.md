---
title: Dialogfeld 'Schriftart'
description: Im Dialogfeld Schriftart können Benutzerattribute für eine logische Schriftart auswählen, z. b. Schriftfamilie und zugehörige Schriftart, Größe, Punktgröße, Effekte (unterstrichen, durchgestrichen und Textfarbe) und ein Skript (oder Zeichensatz).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, allgemeine Dialog Feld Bibliothek
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Schriftart (Dialogfeld)
- Dialogfeld "Schriftart anpassen"
- Flags, Dialogfeld "Schriftart"
- Initialisierungsflags
- vordefinierte Dialogfelder
- Dialogfelder, Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039543"
---
# <a name="font-dialog-box"></a>Dialogfeld 'Schriftart'

Im Dialogfeld **Schriftart** können Benutzerattribute für eine logische Schriftart auswählen, z. b. Schriftfamilie und zugehörige Schriftart, Größe, Punktgröße, Effekte (unterstrichen, durchgestrichen und Textfarbe) und ein Skript (oder Zeichensatz).

Sie erstellen und zeigen ein **Schriftart** Dialogfeld an, indem Sie eine [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) initialisieren und die Struktur an die Funktion " [**choosetfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) " übergeben.

Der folgende Screenshot zeigt ein typisches Dialogfeld für die **Schriftart** .

![Screenshot mit dem Dialogfeld "Schriftart"](images/fontdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt die [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion **true** zurück und legt die Informationen zur Auswahl des Benutzers in der [**selecsefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur fest.

Wenn der Benutzer das Dialogfeld " **Schriftart** " abbricht oder ein Fehler auftritt, gibt " [**Choice Font**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) " den Wert " **false** " zurück, und der Inhalt der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur ist nicht definiert. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**kommdlgextendecoderror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion verwenden, um den erweiterten Fehlerwert abzurufen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Dialog Feld-Initialisierungsflags für Schriftart](#font-dialog-box-initialization-flags)
-   [Anpassen des Dialog Felds "Schriftart" unter früheren Versionen von Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Anpassen des Dialog Felds "Schriftart" unter Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Dialog Feld-Initialisierungsflags für Schriftart

Vor dem Aufruf der [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)muss **der Flags** -Member [**der chooonfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur **CF \_ screenfonts**, **CF \_ Printerfonts** oder **CF \_ both** angeben, um anzugeben, ob das Dialogfeld Bildschirm Schriftarten, Drucker Schriftarten oder beides auflisten soll. Wenn Sie **CF \_ Printerfonts** oder **CF \_ both** angeben, muss der **hdc** -Member der **chootarfont** -Struktur ein Handle für einen Gerätekontext für den Drucker angeben.

Wenn das Flag **CF \_ Printerfonts** oder **CF \_ both** festgelegt ist, wird die Bezeichnung Schriftart Type Description am unteren Rand des Dialog Felds **Schriftart** angezeigt.

Ab Windows 7 werden die Flags **"CF \_ Printerfonts**", "CF **\_ screenfonts**", " **CF \_ both**" und " **CF \_ WYSIWYG** " nicht mehr von der " [**choosetfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) "-Funktion für die Schriftart Enumeration verwendet. Sie sind in Windows 7 veraltet. Allerdings behält das **CF \_ Printerfonts** -Flag eine Funktion bei: zum Anzeigen der Bezeichnung Schriftart Typbeschreibung unten im Dialogfeld **Schriftart** .

Sie können das **Flags** -Element verwenden, um einige der **Schriftart** Dialogfeld-Steuerelemente zu aktivieren oder zu deaktivieren, und Sie können den **Flags** -Member zusammen mit anderen Member der [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwenden, um die Anfangswerte einiger Steuerelemente zu steuern.

**So zeigen Sie die Steuerelemente an, die es dem Benutzer ermöglichen, Optionen für das stricken, unterstreichen und die Farbe auszuwählen:**

-   Legen Sie das **CF \_ Effects** -Flag fest. Sie können den **rgbcolors** -Member der [**chooonfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur verwenden, um eine anfängliche Schriftfarbe anzugeben.

**So geben Sie die Anfangswerte für die Dialogfeld-Steuerelemente Schriftart, Schriftart Stil, Größe, Strich und Unterstreichung an:**

1.  So geben Sie die Anfangswerte für die Dialogfeld-Steuerelemente Schriftart, Schriftart Stil, Größe, Strich und Unterstreichung an:
2.  Legen Sie **das \_ CF inittologfontstruct** -Flag im **Flags** -Member zusammen mit Membern der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur fest, auf die von **lplogfont** verwiesen wird, um die Anfangswerte für die Schriftart Attribute anzugeben.
3.  Sie können auch die **CF noanesel \_**, **CF \_ nostylesel** und **CF \_ nosizesel** Flags verwenden, um zu verhindern, dass das Dialogfeld **Schriftart** anfängliche Werte für die entsprechenden Steuerelemente anzeigt. Dies ist hilfreich, wenn Sie mit einer Auswahl von Text arbeiten, der mehr als eine Schriftart, einen Stil oder eine Punktgröße aufweist. Diese Werte werden auch in **Flags** festgelegt, wenn [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) zurückgibt, wenn der Benutzer keinen entsprechenden Wert ausgewählt hat.

**So initialisieren Sie das Steuerelement Schriftart Stil mit einem angegebenen Stilnamen**

-   Legen Sie das **CF \_ usestyle** -Flag fest, und verwenden Sie den **lpszstyle** -Member, um den Formatvorlagen Namen anzugeben.

> [!Note]  
> Zum Globalisieren der Anwendung geben Sie den Stil mithilfe der **lfWeight** -und **lfitalic** -Elemente der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur an, auf die von **lplogfont** verwiesen wird. Der Stilname kann sich abhängig von der Sprache der Systembenutzer Oberfläche ändern.

 

**Anzeigen der Schaltfläche "anwenden"**

-   Legen Sie das Flag zum **\_ Anwenden von CF** fest, und stellen Sie eine Hook-Prozedur zum Verarbeiten von [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachrichten **für die Schalt** Fläche Die Hook-Prozedur kann die [**WM- \_ Auswahl Schriftart \_ getlogfont**](wm-choosefont-getlogfont.md) an das Dialogfeld senden, um die Adresse der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur abzurufen, die die aktuelle Auswahl für die Schriftart enthält.

**Anzeigen der Schaltfläche "Hilfe"**

-   Legen Sie das **CF \_ ShowHelp** -Flag fest. Das **hwndOwner** -Mitglied muss das Fenster identifizieren, um die registrierte [**helpmsgstring**](helpmsgstring.md) -Meldung zu erhalten, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.

**So schränken Sie die im Dialogfeld angezeigten Schriftarten ein**

-   Legen Sie eine beliebige Kombination der Flags **CF \_ ttonly**, **CF \_ FixedPitchOnly**, **CF \_ novector Fonts**, **CF \_ novertfonts**, **CF \_ scalableonly** und **CF \_ WYSIWYG** fest. Sie können auch die verfügbaren Stile einschränken, die im Dialogfeld für einige Schriftarten angezeigt werden, indem Sie den Wert **CF \_ nosimulationen** verwenden.

Ab Windows 7 wird die im Dialogfeld angezeigte Liste der Schriftarten auf der Grundlage der angezeigten Schriftarten des Benutzers eingeschränkt. Um die Einschränkung zu entfernen, legen Sie das **CF \_ inactivefonts** -Flag fest.

**So schränken Sie die Namen, Stile und Punktgrößen der Schriftart ein, die der Benutzer angeben kann**

1.  Legen Sie das **CF \_ forcefontexist** -Flag fest, um den Benutzer so einzuschränken, dass nur gültige Schriftart Namen, Stile und Punktgrößen angegeben werden, die im Dialogfeld aufgelistet sind.
2.  Legen Sie das Flag "Flag **\_ limitsize** " fest, um den Benutzer auf die Angabe von Punktgrößen in dem Bereich zu beschränken, der durch die Member **nsizemin** und **nsizemax** angegeben wird

**So beschränken oder deaktivieren Sie das Kombinations Feld "Skripts"**

-   Legen Sie das Flag **CF \_ noscriptsel** fest, um das Kombinations Feld **Skripts** zu deaktivieren, oder legen Sie das Flag **CF \_ selectScript** fest, um die Auswahl im Kombinations Feld **Skripts** auf einen angegebenen Zeichensatz zu beschränken.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Anpassen des Dialog Felds "Schriftart" unter früheren Versionen von Windows

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld **Schriftart** angeben, z. b. Wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwendet die benutzerdefinierte Vorlage anstelle der Standardvorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld "Schriftart" bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Schriftart. DLG angegebene Standardvorlage ändern. Die in der Standard Schriftart-Dialogfeld Vorlage verwendeten Steuerelement-IDs werden in der Datei "Dlgs. h" definiert.
2.  Verwenden Sie die [**chooonfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur, um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **CF \_ ENABLETEMPLATE** -Flag im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.
    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das Flag " **CF \_ enabletemplatehandle** " fest. Verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur für das Dialogfeld " **Schriftart** " bereitstellen. Die Hook-Prozedur kann Nachrichten verarbeiten, die an das Dialogfeld gesendet werden, und Meldungen an das Dialogfeld senden. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hook-Prozedur bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten.

**So aktivieren Sie eine Hook-Prozedur für das Dialogfeld "Schriftart"**

1.  Legen Sie das **CF \_ ENABLEHOOK** -Flag im **Flags** -Member der [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnhook** -Member an.

Nach der Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung sendet die Dialogfeld Prozedur eine " **WM \_ InitDialog** "-Meldung an die Hook-Prozedur. Der *LPARAM* -Parameter dieser Nachricht ist ein Zeiger auf die [**ausgewählter Font**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur, die verwendet wird, um das Dialogfeld zu initialisieren.

Die Hook-Prozedur kann die Nachrichten [**WM \_ choosefont \_ getlogfont**](wm-choosefont-getlogfont.md), [**WM \_ choosefont \_ setlogfont**](wm-choosefont-setlogfont.md)und [**WM \_ choosefont \_ setFlags**](wm-choosefont-setflags.md) an das Dialogfeld senden, um die aktuellen Werte und Flags des Dialog Felds zu erhalten und festzulegen.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Anpassen des Dialog Felds "Schriftart" unter Windows 7

Der folgende Screenshot zeigt ein typisches Dialogfeld **Schriftart** in Windows 7.

![Screenshot mit dem Schriftart-dialob-Feld](images/fontdialogboxwin7.png)

In früheren Windows-Versionen enthält die Template-Datei der Schriftart. DLG eine Standardvorlage für die Auswahl Schriftart. Die Vorlagen Datei "Font. Dlg" unter Windows 7 enthält zwei Standardvorlagen: die Standardvorlage aus früheren Windows-Versionen und die neue Windows 7-Auswahl Schriftart Vorlage. Wenn Sie das Dialogfeld **Schriftart** unter Windows 7 anpassen, müssen Sie daher die folgenden Punkte beachten.

1.  Verwenden Sie die neue Vorlage, wenn Sie benutzerdefinierte Vorlagen für Anwendungen erstellen, die unter Windows 7 ausgeführt werden. Diese neue Vorlage enthält ein Link Steuerelement, auf das der Benutzer klicken kann, um das Fenster " **Schriftarten-Systemsteuerung** " zu starten, wie im folgenden Screenshot gezeigt.

    ![Screenshot der Schriftart-Systemsteuerung in Windows 7](images/fontcontrolpanelforwin7.png)

2.  Um dieses Link Steuerelement zu verwenden, muss die aufrufende Anwendung die COMCTL32.DLL Version 6 oder höher verwenden. Andernfalls gibt die [**choosetfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion einen Fehler zurück, wenn versucht wird, das Link-Steuerelement in der benutzerdefinierten Vorlage zu erstellen. Um zu ermitteln, ob dieses Steuerelement aktiviert ist, kompilieren Sie die aufrufenden Anwendung mit COMCTL32.DLL Version 6,0. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen mit allgemeinen Steuerelementen](/previous-versions//ms649781(v=vs.85)).
3.  Wenn Ihre Anwendung COMCTL32.DLL Version 5,0 oder früher verwendet, müssen Sie Folgendes tun, wenn Sie eine benutzerdefinierte Vorlage erstellen:

    -   Legen Sie das Steuerelement als **PUSHBUTTON** fest. Das Steuerelement, das zum Starten der **Schriftarten-Systemsteuerung** verwendet wird, wird als Schaltfläche und nicht als Link angezeigt.
    -   Ersetzen Sie den folgenden Text in der Schriftart. DLG:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        mit folgendem Text:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Um sicherzustellen, dass Ihre Anwendung eine benutzerdefinierte Vorlage verwendet, müssen Sie eine benutzerdefinierte Vorlage mit dem **CF \_ ENABLETEMPLATE** -Flag angeben, eine benutzerdefinierte Vorlage erstellen, die auf der Windows 7-Auswahl Schriftart basiert, und dann optional eine Hook-Prozedur aktivieren.

        Wenn Sie eine Hook-Prozedur aktivieren, ohne eine benutzerdefinierte Vorlage zu erstellen, wird die Standardvorlage für die Auswahl Schriftart für frühere Windows-Versionen geladen.

> [!Note]  
> Abhängig von der Version von COMMCTL.DLL, für die die Anwendung kompiliert wird, müssen Sie **den Steuerelement-oder** **PUSHBUTTON** -Steuerelement-Typ in der neuen Vorlage angeben. Beachten Sie außerdem, dass bestimmte Features von Windows 7, wie z. b. die WYSIWYG-Anzeige von Schriftart Listen und erweiterten Familien, nicht verfügbar sind, wenn Ihre Anwendungen unter früheren Versionen des Windows-Betriebssystems ausgeführt werden.

 

 

 