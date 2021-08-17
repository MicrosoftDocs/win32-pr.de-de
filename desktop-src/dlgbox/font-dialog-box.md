---
title: Dialogfeld 'Schriftart'
description: Im Dialogfeld Schriftart können Benutzer Attribute für eine logische Schriftart auswählen, z. B. Schriftfamilie und zugeordneter Schriftschnitt, Punktgröße, Effekte (Unterstrichen, Ausstrich und Textfarbe) und ein Skript (oder Zeichensatz).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche,Common Dialog Box Library
- Benutzereingabe, Common Dialog Box Library
- Erfassen von Benutzereingaben, Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Schriftart (Dialogfeld)
- Dialogfeld "Schriftart anpassen"
- Flags, Dialogfeld "Schriftart"
- Initialisierungsflags
- Vordefinierte Dialogfelder
- Dialogfelder, Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8544fcb60e499a360f60d1701863a11138d3f16fb06a770a9a2763800d908e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785889"
---
# <a name="font-dialog-box"></a>Dialogfeld 'Schriftart'

Im Dialogfeld **Schriftart** können Benutzer Attribute für eine logische Schriftart auswählen, z. B. Schriftfamilie und zugeordneter Schriftschnitt, Punktgröße, Effekte (Unterstrichen, Ausstrich und Textfarbe) und ein Skript (oder Zeichensatz).

Sie erstellen und zeigen ein Dialogfeld **Schriftart** an, indem Sie eine [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) initialisieren und die Struktur an die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) übergeben.

Der folgende Screenshot zeigt ein typisches Dialogfeld **Schriftart.**

![Screenshot des Dialogfelds "Schriftart"](images/fontdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **TRUE** zurück und legt die Informationen zur Auswahl des Benutzers in der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) fest.

Wenn der Benutzer das Dialogfeld **Schriftart** abbricht oder ein Fehler auftritt, gibt [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **FALSE** zurück, und der Inhalt der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) ist nicht definiert. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**CommDlgExtendedError-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) verwenden, um den erweiterten Fehlerwert abzurufen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Initialisierungsflags des Dialogfelds "Schriftart"](#font-dialog-box-initialization-flags)
-   [Anpassen des Schriftartdialogfelds für frühere Versionen von Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Anpassen des Schriftartdialogfelds in Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Initialisierungsflags des Dialogfelds "Schriftart"

Vor dem Aufrufen von [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)muss der **Flags-Member** der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) **CF \_ SCREENFONTS,** **CF \_ PRINTERFONTS** oder **CF \_ BOTH** angeben, um anzugeben, ob das Dialogfeld Bildschirmschriftarten, Druckerschriftarten oder beides auflisten soll. Wenn Sie **CF \_ PRINTERFONTS** oder **CF \_ BOTH** angeben, muss der **hDC-Member** der **CHOOSEFONT-Struktur** ein Handle für einen Gerätekontext für den Drucker angeben.

Wenn das **Flag CF \_ PRINTERFONTS** oder **CF \_ BOTH** festgelegt ist, wird die Bezeichnung für die Beschreibung des Schriftarttyps am unteren Rand des Dialogfelds **Schriftart** angezeigt.

Ab Windows 7 werden die Flags **CF \_ PRINTERFONTS,** **CF \_ SCREENFONTS,** **CF \_ BOTH** und **CF \_ WYSIWYG** nicht mehr von der [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) für die Schriftartenumeration verwendet. Sie sind in Windows 7 veraltet. Das **CF \_ PRINTERFONTS-Flag** behält jedoch eine Funktion bei: , um die Bezeichnung für die Beschreibung des Schriftarttyps am unteren Rand des Dialogfelds **Schriftart** anzuzeigen.

Sie können den **Flags-Member** verwenden, um einige der Steuerelemente des Dialogfelds **Schriftart** zu aktivieren oder zu deaktivieren, und Sie können den **Flags-Member** in Verbindung mit anderen [**CHOOSEFONT-Membern**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwenden, um die Anfangswerte einiger Steuerelemente zu steuern.

**So zeigen Sie die Steuerelemente an, die es dem Benutzer ermöglichen, die Optionen "Strikeout", "Underline" und "Color" auszuwählen:**

-   Legen Sie das **CF \_ EFFECTS-Flag** fest. Sie können den **rgbColors-Member** der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwenden, um eine anfängliche Schriftfarbe anzugeben.

**So geben Sie die Anfangswerte für die Dialogfelder Schriftart, Schriftschnitt, Schriftgrad, Größe, Ausstrich und Unterstreichung an:**

1.  So geben Sie die Anfangswerte für die Dialogfelder Schriftart, Schriftschnitt, Schriftgrad, Größe, Ausstrich und Unterstreichung an:
2.  Legen Sie das **FLAG CF \_ INITTOLOGFONTSTRUCT** im **Flags-Member** zusammen mit Membern der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) fest, auf die das **lpLogFont** zeigt, um die Anfangswerte für die Schriftartattribute anzugeben.
3.  Sie können auch die Flags **CF \_ NOFACESEL,** **CF \_ NOSTYLESEL** und **CF \_ NOSIZESEL** verwenden, um zu verhindern, dass das Dialogfeld **Schriftart** Anfangswerte für die entsprechenden Steuerelemente anzeigt. Dies ist nützlich, wenn Sie mit einer Auswahl von Text arbeiten, der über mehr als eine Schriftart, einen Stil oder eine Punktgröße verfügt. Diese Werte werden auch in **Flags** festgelegt, wenn [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) zurückgegeben wird, wenn der Benutzer keinen entsprechenden Wert ausgewählt hat.

**So initialisieren Sie das Schriftschnitt-Steuerelement mit einem angegebenen Formatnamen**

-   Legen Sie das **CF \_ USESTYLE-Flag** fest, und verwenden Sie den **lpszStyle-Member,** um den Stilnamen anzugeben.

> [!Note]  
> Um Ihre Anwendung zu globalisieren, geben Sie den Stil mithilfe der **Member lfWeight** und **lfItalic** der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) an, auf die **lpLogFont** zeigt. Der Formatname kann sich abhängig von der Sprache der Systembenutzerschnittstelle ändern.

 

**So zeigen Sie die Schaltfläche Anwenden an**

-   Legen Sie das **CF \_ APPLY-Flag** fest, und stellen Sie eine Hookprozedur bereit, um [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) für die Schaltfläche **Anwenden** zu verarbeiten. Die Hookprozedur kann die [**WM \_ CHOOSEFONT \_ GETLOGFONT-Nachricht**](wm-choosefont-getlogfont.md) an das Dialogfeld senden, um die Adresse der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) abzurufen, die die aktuelle Auswahl für die Schriftart enthält.

**So zeigen Sie die Schaltfläche "Hilfe" an**

-   Legen Sie das **CF \_ SHOWHELP-Flag** fest. Das **hwndOwner-Element** muss das Fenster identifizieren, um die registrierte [**HELPMSGSTRING-Meldung**](helpmsgstring.md) zu erhalten, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.

**So beschränken Sie die im Dialogfeld angezeigten Schriftarten**

-   Legen Sie eine beliebige Kombination der Flags **CF \_ TTONLY,** **CF \_ FIXEDPITCHONLY,** **CF \_ NOVECTORFONTS,** **CF \_ NOVERTFONTS,** **CF \_ SCALABLEONLY** und **CF \_ WYSIWYG** fest. Sie können auch die verfügbaren Stile einschränken, die im Dialogfeld für einige Schriftarten angezeigt werden, indem Sie den **CF \_ NOSIMULATIONS-Wert** verwenden.

Ab Windows 7 wird die Liste der im Dialogfeld angezeigten Schriftarten basierend auf den angezeigten Schriftarten des Benutzers eingeschränkt. Um die Einschränkung zu entfernen, legen Sie das **FLAG CF \_ INACTIVEFONTS** fest.

**So schränken Sie die Schriftartnamen, Stile und Punktgrößen ein, die der Benutzer angeben kann**

1.  Legen Sie das **CF \_ FORCEFONTEXIST-Flag** fest, um den Benutzer darauf zu beschränken, nur gültige Schriftartnamen, Stile und Punktgrößen anzugeben, die im Dialogfeld aufgeführt sind.
2.  Legen Sie das **FLAG CF \_ LIMITSIZE** fest, um den Benutzer auf die Angabe von Punktgrößen in dem Bereich zu beschränken, der von den **Membern nSizeMin** und **nSizeMax** angegeben wird.

**So beschränken oder deaktivieren Sie das Kombinationsfeld Skripts**

-   Legen Sie das **CF \_ NOSCRIPTSEL-Flag** fest, um das **Kombinationsfeld Skripts** zu deaktivieren, oder legen Sie das **CF \_ SELECTSCRIPT-Flag** fest, um die Auswahl im **Kombinationsfeld Skripts** auf einen angegebenen Zeichensatz zu beschränken.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Anpassen des Dialogfelds "Schriftart" in früheren Versionen von Windows

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld **Schriftart** bereitstellen, wenn Sie beispielsweise zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwendet Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld Schriftart bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Font.dlg angegebene Standardvorlage ändern. Die Steuerelementbezeichner, die in der Standardvorlage des Dialogfelds Schriftart verwendet werden, werden in der Datei Dlgs.h definiert.
2.  Verwenden Sie die [**CHOOSEFONT-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **FLAG CF \_ ENABLETEMPLATE** im **Flags-Member** fest. Verwenden Sie die Member **hInstance** und **lpTemplateName** der Struktur, um den Modul- und Ressourcennamen zu identifizieren.
    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **FLAG CF \_ ENABLETEMPLATEHANDLE** fest. Verwenden Sie den **Member hInstance,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**CFHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) für das Dialogfeld **Schriftart** bereitstellen. Die Hookprozedur kann Nachrichten verarbeiten, die an das Dialogfeld gesendet werden, und Nachrichten an das Dialogfeld senden. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hookprozedur zum Verarbeiten von Eingaben für Ihre Steuerelemente bereitstellen.

**So aktivieren Sie eine Hookprozedur für das Dialogfeld Schriftart**

1.  Legen Sie das **FLAG CF \_ ENABLEHOOK** im **Flags-Member** der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) fest.
2.  Geben Sie die Adresse der Hookprozedur im **lpfnHook-Member** an.

Nach der Verarbeitung der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sendet die Dialogfeldprozedur eine **WM \_ INITDIALOG-Nachricht** an die Hookprozedur. Der *lParam-Parameter* dieser Meldung ist ein Zeiger auf die [**CHOOSEFONT-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) die zum Initialisieren des Dialogfelds verwendet wird.

Die Hookprozedur kann die [**MELDUNGEN WM \_ CHOOSEFONT \_ GETLOGFONT,**](wm-choosefont-getlogfont.md) [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)und [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) an das Dialogfeld senden, um die aktuellen Werte und Flags des Dialogfelds abzurufen und festzulegen.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Anpassen des Dialogfelds "Schriftart" in Windows 7

Der folgende Screenshot zeigt ein typisches Dialogfeld **Schriftart** in Windows 7.

![Screenshot des Schriftartfelds "Dialob"](images/fontdialogboxwin7.png)

In früheren Windows Versionen enthält die Vorlagendatei font.dlg eine ChooseFont-Standardvorlage. Die Vorlagendatei font.dlg in Windows 7 enthält zwei Standardvorlagen: die Standardvorlage aus früheren Windows-Versionen und die neue Windows 7 ChooseFont-Vorlage. Wenn Sie das Dialogfeld **Schriftart** in Windows 7 anpassen, müssen Sie daher die folgenden Probleme berücksichtigen.

1.  Verwenden Sie die neue Vorlage, wenn Sie benutzerdefinierte Vorlagen für Anwendungen erstellen, die auf Windows 7 ausgeführt werden. Diese neue Vorlage enthält ein Linksteuerelement, auf das der Benutzer klicken kann, um das Fenster **Schriftarten Systemsteuerung** zu starten, wie im folgenden Screenshot gezeigt.

    ![Screenshot der Schriftart-Systemsteuerung in Windows 7](images/fontcontrolpanelforwin7.png)

2.  Um dieses Linksteuerelement verwenden zu können, muss Ihre aufrufende Anwendung die COMCTL32.DLL Version 6 oder höher verwenden. Andernfalls gibt die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) einen Fehler zurück, wenn sie versucht, das Linksteuerelement in Ihrer benutzerdefinierten Vorlage zu erstellen. Kompilieren Sie die aufrufende Anwendung mit COMCTL32.DLL Version 6.0, um zu ermitteln, ob dieses Steuerelement aktiviert ist. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen mit allgemeinen Steuerelementen.](/previous-versions//ms649781(v=vs.85))
3.  Wenn Ihre Anwendung COMCTL32.DLL Version 5.0 oder früher verwendet, müssen Sie folgende Schritte ausführen, wenn Sie eine benutzerdefinierte Vorlage erstellen:

    -   Geben Sie das Steuerelement als **PUSHBUTTON** an. Das Steuerelement, das zum Starten des **Systemsteuerung Schriftarten** verwendet wird, wird als Schaltfläche und nicht als Link angezeigt.
    -   Ersetzen Sie den folgenden Text in der Datei font.dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        mit folgendem Text:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Um sicherzustellen, dass Ihre Anwendung eine benutzerdefinierte Vorlage verwendet, müssen Sie eine benutzerdefinierte Vorlage mit dem **FLAG CF \_ ENABLETEMPLATE** angeben, eine benutzerdefinierte Vorlage basierend auf der chooseFont-Vorlage Windows 7 erstellen und optional eine Hookprozedur aktivieren.

        Wenn Sie eine Hookprozedur aktivieren, ohne eine benutzerdefinierte Vorlage zu erstellen, wird die ChooseFont-Standardvorlage für frühere Windows Versionen geladen.

> [!Note]  
> Sie müssen den **Steuerelementtyp CONTROL** oder **PUSHBUTTON** in der neuen Vorlage angeben, abhängig von der Version von COMMCTL.DLL, mit der Ihre Anwendung kompiliert wird. Beachten Sie auch, dass Windows 7 spezifische Features, z. B. DIE ANZEIGE VON SCHRIFTARTLISTEN und erweiterten Familien, nicht verfügbar sind, wenn Ihre Anwendungen in früheren Versionen des Windows Betriebssystems ausgeführt werden.

 

 

 