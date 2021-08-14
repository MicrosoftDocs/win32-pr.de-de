---
title: Drucken (Dialogfeld)
description: Im Dialogfeld Drucken können Benutzer Optionen für einen bestimmten Druckauftrag auswählen.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche,Common Dialog Box Library
- Benutzereingabe, Common Dialog Box Library
- Erfassen von Benutzereingaben, Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Dialogfeld Drucken
- Dialogfeld "Druckeinrichtung"
- Anpassen des Dialogfelds "Drucken"
- Vordefinierte Dialogfelder
- Dialogfelder, Drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afd8cfa31a83f664e859cd93acc9d28543b7ab00dcb8f130fdbac329cd1429e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720917"
---
# <a name="print-dialog-box"></a>Drucken (Dialogfeld)

Im Dialogfeld **Drucken** können Benutzer Optionen für einen bestimmten Druckauftrag auswählen. Der Benutzer kann z. B. den zu verwendende Drucker, den Bereich der zu druckten Seiten und die Anzahl der Kopien angeben.

Sie können die [**PrintDlgEx-Funktion**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) verwenden, um ein [Druckeigenschaftenblatt](print-property-sheet.md)anzuzeigen, das eine **Seite Allgemein** mit Steuerelementen enthält, die dem Dialogfeld **Drucken** ähneln. Das Eigenschaftenblatt kann auch zusätzliche anwendungsspezifische und treiberspezifische Eigenschaftenseiten enthalten, die auf die Seite **Allgemein** folgen.

Sie erstellen ein Dialogfeld **Drucken** und zeigen es an, indem Sie eine [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) initialisieren und die Struktur an die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) übergeben.

Die folgende Abbildung zeigt ein typisches Dialogfeld **Drucken.**

![Dialogfeld "Drucken"](images/printdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **TRUE** zurück und verwendet die [**PRINTDLG-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlga) um Informationen zur Auswahl des Benutzers zurückzugeben. Beispielsweise geben die Member **hDevMode** und **hDevNames** in der Regel globale Speicherhandles für - und [**DEVNAMES-Strukturen**](/windows/win32/api/commdlg/ns-commdlg-devnames) zurück. Sie können die Informationen in diesen Strukturen verwenden, um einen Gerätekontext oder einen Informationskontext für den ausgewählten Drucker zu erstellen.

Wenn der Benutzer das Dialogfeld **Drucken** abbricht oder ein Fehler auftritt, gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **FALSE** zurück. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**CommDlgExtendedError-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) verwenden, um den erweiterten Fehlerwert abzurufen.

Das Dialogfeld **Drucken** enthält **eine** Gruppe von Optionsfeldern, die angeben, ob der Benutzer alle Seiten, einen Seitenbereich oder nur den ausgewählten Text drucken möchte. Vor dem Aufruf von [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))können Sie eines der **Flags PD \_ ALLPAGES,** **PD \_ SELECTION** oder **PD \_ PAGENUMS** festlegen, um anzugeben, welche Schaltfläche anfänglich ausgewählt wird. Wenn **PrintDlg** **TRUE** zurückgibt, legt die Funktion eines dieser Flags fest, um die Auswahl des Benutzers anzugeben. Wenn **PD \_ PAGENUMS** festgelegt ist, enthalten die **Elemente nFromPage** und **nToPage** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) die vom Benutzer angegebenen Start- und Endseiten. Um das Optionsfeld **Pages** und die zugehörigen **From-** und To edit-Steuerelemente **zu** deaktivieren, legen Sie das **PD \_ NOPAGENUMS-Flag** fest. Um das Optionsfeld **Auswahl** zu deaktivieren, legen Sie das **PD \_ NOSELECTION-Flag** fest.

Das Dialogfeld enthält ein Bearbeitungssteuerelement, in das der Benutzer die Anzahl der zu druckbaren Kopien eingeben kann. Wenn der **hDevMode-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) ungleich **NULL** ist, gibt der **dmCopies-Member** der -Struktur den Anfangswert für dieses Bearbeitungssteuerelement an. Wenn **hDevMode** **NULL** ist, gibt der **nCopies-Member** der **PRINTDLG-Struktur** den Anfangswert an. Wenn [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) zurückgegeben wird, gibt **nCopies** in der Regel die Anzahl der vom Benutzer angegebenen Kopien an. Wenn Sie jedoch beim Erstellen des Dialogfelds das **FLAG PD \_ USEDEVMODECOPIESANDCOLLATE** festlegen, wird **nCopies** bei der Rückgabe immer auf 1 festgelegt, und das **element dmCopies** von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) gibt die Anzahl der zu druckenden Kopien an.

Das **Kontrollkästchen Sortieren** gibt an, ob der Benutzer die Seiten sortieren möchte, wenn mehrere Kopien gedruckt werden. Das **PD \_ COLLATE-Flag** wird festgelegt, wenn das **Kontrollkästchen Sortieren** aktiviert ist. Wenn Ihre Anwendung nicht mehrere Kopien oder simulierte Sortierungen unterstützt, legen Sie das **FLAG PD \_ USEDEVMODECOPIESANDCOLLATE** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) fest. Dadurch werden das Kontrollkästchen **Sortieren** und das Bearbeitungssteuerelement **Anzahl von Kopien** deaktiviert, es sei denn, der Druckertreiber unterstützt mehrere Kopien und Sortierungen.

Das Kontrollkästchen **In Datei drucken** gibt an, ob der Benutzer die Ausgabe an eine Datei und nicht an einen Drucker senden möchte. Sie können das **PD \_ PRINTTOFILE-Flag** festlegen, damit das Kontrollkästchen anfänglich aktiviert ist. Um das Kontrollkästchen auszublenden, legen Sie das **FLAG PD \_ HIDEPRINTTOFILE** fest. Legen Sie das **PD \_ DISABLEPRINTTOFILE-Flag** fest, um es zu deaktivieren. Wenn der Benutzer die Option **In Datei drucken** auswählt, legt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) das **PD \_ PRINTTOFILE-Flag** fest und gibt "FILE:" an dem Offset zurück, der durch den **wOutputOffset-Member** der [**DEVNAMES-Struktur**](/windows/win32/api/commdlg/ns-commdlg-devnames) angegeben wird. Wenn Sie die Funktion aufrufen, um den Druckvorgang zu starten, geben Sie diese FILE:-Zeichenfolge im **lpszOutput-Member** der -Struktur an. Die Angabe dieser Zeichenfolge bewirkt, dass das Drucksubsystem den Benutzer nach dem Namen der Ausgabedatei abfragt.

Standardmäßig zeigt das Dialogfeld **Drucken** anfänglich Informationen zum aktuellen Standarddrucker an. Um Informationen für einen anderen installierten Drucker anzuzeigen, initialisieren Sie eine - und eine [**DEVNAMES-Struktur**](/windows/win32/api/commdlg/ns-commdlg-devnames) und weisen den **Membern hDevMode** und **hDevNames** das globale Speicherhandle der -Struktur zu. Der Gerätename, den Sie im **dmDeviceName-Element** der [**DEVMODE-Struktur**](/windows/win32/api/wingdi/ns-wingdi-devmodea) und im **wDriverOffset-Element** der **DEVNAMES-Struktur** angeben, muss ein Druckergerät identifizieren, das auch im \[ Abschnitt Geräte der \] Win.ini-Datei aufgeführt ist. Wenn das Gerät nicht aufgeführt ist, gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) einen Fehler zurück.

Sie können [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) anweisen, einen Gerätekontext oder Informationskontext für den Drucker zu erstellen, indem Sie das **FLAG PD \_ RETURNDC** oder **PD \_ RETURNIC** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) festlegen. Die Funktion gibt ein Handle für den Gerätekontext oder den Informationskontext im **hDC-Member** zurück. Wenn Sie das **PD \_ RETURNDC-Flag** verwenden, können Sie den Gerätekontext verwenden, um die Ausgabe für den Drucker zu generieren.

Um Informationen zum Standarddrucker abzurufen, ohne das Dialogfeld **Drucken** anzuzeigen, legen Sie das **PD \_ RETURNDEFAULT-Flag** fest. In diesem Fall gibt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) sofort zurück, nachdem die **Member hDevMode** und **hDevNames** auf Handles für Strukturen festgelegt wurden, die die Informationen enthalten.

Standardmäßig zeigt [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Meldungsfelder an, wenn Fehler auftreten. Die Funktion zeigt beispielsweise eine Fehlermeldung an, wenn keine Drucker installiert sind. Um zu verhindern, dass die Funktion diese Warnmeldungen anzeigt, legen Sie das **FLAG PD \_ NOWARNING** fest.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Anpassen des Dialogfelds "Drucken"](#customizing-the-print-dialog-box)
-   [Druckeinrichtung (Dialogfeld)](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Anpassen des Dialogfelds "Drucken"

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld **Drucken** bereitstellen, z. B. wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) verwendet Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld **Drucken** bereit:

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Prnsetup.dlg angegebene Standardvorlage ändern. Die in der Standardvorlage des **Dialogfelds Drucken** verwendeten Steuerelementbezeichner werden in der Datei Dlgs.h definiert.
2.  Verwenden Sie die [**PRINTDLG-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlga) um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **FLAG PD \_ ENABLEPRINTTEMPLATE** im **Flags-Member** fest. Verwenden Sie die Member **hInstance** und **lpPrintTemplateName** der Struktur, um den Modul- und Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **FLAG PD \_ ENABLEPRINTTEMPLATEHANDLE** fest. Verwenden Sie den **hPrintTemplate-Member,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**PrintHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) für das Dialogfeld **Drucken** bereitstellen. Die Hookprozedur kann Nachrichten verarbeiten, die an das Dialogfeld gesendet werden. Sie kann auch Nachrichten an das Dialogfeld senden. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hookprozedur zum Verarbeiten von Eingaben für Ihre Steuerelemente bereitstellen.

So aktivieren Sie eine Hookprozedur für das Dialogfeld **Drucken:**

1.  Legen Sie das **PD \_ ENABLEPRINTHOOK-Flag** im **Flags-Member** der [**PRINTDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-printdlga) fest.
2.  Geben Sie die Adresse der Hookprozedur im **Member lpfnPrintHook** an.

Nach der Verarbeitung der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sendet die Dialogfeldprozedur eine **WM \_ INITDIALOG-Nachricht** an die Hookprozedur. Der *lParam-Parameter* dieser Nachricht ist ein Zeiger auf die [**PRINTDLG-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-printdlga) die zum Initialisieren des Dialogfelds verwendet wird.

## <a name="print-setup-dialog-box"></a>Druckeinrichtung (Dialogfeld)

Sie können ein Dialogfeld **Druckeinrichtung** erstellen und anzeigen, indem Sie das **PD \_ PRINTSETUP-Flag** in einem Aufruf der [**PrintDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) festlegen. Das Dialogfeld **Druckeinrichtung** wurde jedoch durch das Dialogfeld **Seiteneinrichtung** ersetzt und sollte nicht in neuen Anwendungen verwendet werden.

Die folgenden Flags gelten nur für das Dialogfeld **Druckeinrichtung:**

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 