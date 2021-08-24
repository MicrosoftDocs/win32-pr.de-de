---
title: Erstellen von Assistenten
description: Ein Assistent ist ein Eigenschaftenblatttyp, der eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu führen.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4254b448c719e3e1397fceadfcdc28475eaeae588f6f1eb0f0168cea07327d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655824"
---
# <a name="how-to-create-wizards"></a>Erstellen von Assistenten

Ein Assistent ist ein Eigenschaftenblatttyp, der eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu führen.

Assistenten sind einer der Schlüssel zur Vereinfachung der Benutzerfreundlichkeit. Sie ermöglichen es Ihnen, einen komplexen Vorgang wie die Konfiguration einer Anwendung zu übernehmen und in eine Reihe einfacher Schritte aufzugliedern. An jedem Punkt des Prozesses können Sie eine Erläuterung der benötigten Informationen bereitstellen und Steuerelemente anzeigen, die es dem Benutzer ermöglichen, Eine Auswahl zu treffen und Text einzugeben.

Ein Assistent ist tatsächlich ein Eigenschaftenblatttyp. Ein Eigenschaftenblatt ist im Wesentlichen ein Container für eine Auflistung von *Seiten,* wobei jede Seite ein separates Dialogfeld ist. Während reguläre Eigenschaftenblätter es dem Benutzer ermöglichen, jederzeit auf eine beliebige Seite zuzugreifen, zeigen Assistenten Seiten nacheinander an. Anstelle von Registerkarten werden Schaltflächen verwendet, um vorwärts und rückwärts zu navigieren. Die Reihenfolge, in der Seiten angezeigt werden, wird von der Anwendung gesteuert und kann basierend auf Benutzereingaben geändert werden.

Es gibt zwei Hauptstile des Assistenten: den älteren Wizard97-Stil und den in Windows Vista eingeführten Style Style VonIer. Abbildungen finden Sie unter [Informationen zu Eigenschaftenblättern.](property-sheets.md) (Ein dritter Stil, der nur die PSH \_ verwendet WIZARD- oder PSH \_ WIZARD \_ LITE-Flag, stellt eine einfache Sequenz von Eigenschaftenblättern ohne Header oder Wasserzeichen dar.)

> [!Note]  
> Ein "Wasserzeichen" im Kontext von Assistenten ist eine Bitmap, die am linken Rand einiger Seiten angezeigt wird.

 

Bei den meisten Erläuterungen in diesem Dokument wird davon ausgegangen, dass Sie einen Assistenten für ein System mit [Version 5.80](common-control-versions.md) oder höher der allgemeinen Steuerelemente implementieren. Wenn Sie versuchen, den Wizard97-Stil mit früheren Versionen der allgemeinen Steuerelemente zu verwenden, wird die Anwendung möglicherweise kompiliert, aber nicht ordnungsgemäß angezeigt. Eine Erläuterung zum Erstellen eines Assistenten97-kompatiblen Assistenten auf früheren Systemen finden Sie unter Abwärtskompatible Assistenten weiter unten in diesem Thema.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="wizard-implementation"></a>Assistentenimplementierungen

Das Implementieren eines Assistenten ähnelt der Implementierung eines regulären Eigenschaftenblatts. Auf der grundlegendsten Ebene geht es darum, eines der folgenden Flags oder Kombinationen von Flags in der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) festzulegen, die das Eigenschaftenblatt definiert.



| Flag                           | Style                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_PSH-ASSISTENT                    | Ein einfacher Assistent ohne Header oder Bitmaps.                                                                                                           |
| PSH \_ WIZARD \_ LITE              | Ähnlich wie beim \_ PSH-ASSISTENTEN mit einigen geringfügigen Unterschieden in der Darstellung, z. B. wird der Unterteiler über den Schaltflächen auf die vollständige Breite des Fensters festgelegt. |
| \_PSH-ASSISTENT97                  | Assistent97 mit (optionalen) Headern, Headerbitmaps und Wasserzeichen.                                                                            |
| \_PSH-ASSISTENT \| \_ PSH- UND PSH-ASSISTENT | Ein Assistent für Einen Assistenten. Assistenten verwenden keine Wasserzeichen oder Headerbitmaps. Sie erfordern das Singlethread-Apartmentmodell (STA).                         |



 

Das grundlegende Verfahren zum Implementieren eines Assistenten lautet wie folgt:

1.  Erstellen Sie für jede Seite eine Dialogfeldvorlage.
2.  Definieren Sie die Seiten, indem Sie eine [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) für jede Seite erstellen. Diese Struktur definiert die Seite und enthält Zeiger auf die Dialogfeldvorlage und alle Bitmaps oder andere Ressourcen.
3.  Übergeben Sie die im vorherigen Schritt erstellte [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) an die [**CreatePropertySheetPage-Funktion,**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) um das HPROPSHEETPAGE-Handle der Seite zu erstellen.
4.  Definieren Sie den Assistenten, indem Sie dafür eine [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) erstellen.
5.  Übergeben Sie die [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) an die [**PropertySheet-Funktion,**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) um den Assistenten anzuzeigen.
6.  Implementieren Sie Dialogfeldverfahren für jede Seite, um Benachrichtigungsmeldungen von den Steuerelementen der Seite und den Schaltflächen des Assistenten zu verarbeiten und andere Windows Messaging zu verarbeiten.

### <a name="create-the-dialog-box-templates"></a>Erstellen der Dialogfeldvorlagen

Es gibt zwei grundlegende Arten von Assistentenseiten: außen und innen. Äußere Seiten sind die Einführungs- (Willkommens-) und Vervollständigungsseiten. Alle anderen sind innere Seiten.

**Vorlagen für das Dialogfeld "Außenseite"**

Das grundlegende Layout der Einführungs- und Vervollständigungsseiten ist identisch. Die folgende Abbildung zeigt eine Assistenten97-Beispieleinführungsseite mit einem Platzhalter-Wasserzeichen.

![Screenshot einer Assistentenseite mit einer Grafik auf der linken Seite, Titel und Text auf der rechten Seite und den Schaltflächen "Zurück", "Weiter" und "Abbrechen" am unteren Rand](images/wiz97exterior.png)

Für die äußeren Seiten von Wizard97 ist die Dialogfeldvorlage 317 x 193 Dialogeinheiten. Er füllt den gesamten Assistenten mit Ausnahme der Beschriftung und des Bands am unteren Rand aus, das die Schaltflächen **Zurück,** **Weiter** und **Abbrechen** enthält. Die linke Seite der Vorlage, die für eine "Wasserzeichen"-Bitmap reserviert ist, sollte keine Steuerelemente enthalten. Das Wasserzeichen wird in der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) des Assistenten angegeben und automatisch der Seite hinzugefügt. Beim Entwerfen der Ressourcenvorlage müssen Sie Speicherplatz dafür zulassen.

Beachten Sie beim Erstellen der Wasserzeichenbitmap, dass das Dialogfeld möglicherweise größer wird, wenn der Benutzer z. B. eine große Systemschriftart ausgibt. Verschiedene Sprachen weisen in der Regel auch unterschiedliche Schriftartmetriken auf. Wenn die Seite wächst, wird der für das Wasserzeichen reservierte Bereich proportional größer. Sie können jedoch weder die Wasserzeichenbitmap ändern, noch wird die Bitmap gestreckt, um den größeren Bereich zu füllen. Stattdessen wird die Bitmap in ihrer ursprünglichen Größe im oberen linken Teil des reservierten Bereichs gelassen. Der Teil des größeren reservierten Bereichs, der nicht durch das Wasserzeichen abgedeckt ist, wird automatisch mit der Farbe des oberen linken Pixels der Bitmap gefüllt.

Wenn Sie über Wasserzeichenbitmaps unterschiedlicher Größe für verschiedene Schriftartmetriken verfügen müssen, sind zwei mögliche Lösungen möglich:

-   Abrufen der Schriftartmetriken vor dem Erstellen des Assistenten und Angeben einer geeigneten Wasserzeichenbitmap.
-   Geben Sie beim Erstellen des Assistenten keine Wasserzeichenbitmap an. Wizard97 lässt den Wasserzeichenbereich leer. Zeichnen Sie dann eine entsprechend dimensionierte Bitmap auf dem für das Wasserzeichen reservierten Bereich.

Sie können Steuerelemente im Bereich rechts neben dem Wasserzeichen wie bei einem regulären Dialogfeld platzieren. Die Hintergrundfarbe dieses Bereichs wird vom System bestimmt und erfordert keine Aktion. In der Regel werden in diesem Bereich zwei statische Steuerelemente angezeigt. Die obere enthält den Titel und verwendet eine große fett formatierte Schriftart (12 Punkt Verdana Bold für Wizard97). Die andere , die für erläuternden Text vorgesehen ist, verwendet die Standardschriftart des Dialogfelds.

Der Hauptunterschied zwischen den Einführungs- und Vervollständigungsseiten sind die Assistentenschaltflächen und der Text in den statischen Steuerelementen. Einführungsseiten verfügen normalerweise über die **Schaltflächen Weiter** und **Zurück,** wobei nur die Schaltfläche **Weiter** aktiviert ist. Auf Vervollständigungsseiten ist die Schaltfläche **Zurück** aktiviert, und die Schaltfläche **Weiter** wird durch die Schaltfläche **Fertig stellen** ersetzt.

> [!Note]  
> In Den Assistenten wird die Schaltfläche **Zurück** durch eine Pfeilschaltfläche in der Beschriftungsleiste ersetzt.

 

Sie können den Text auf der Schaltfläche **Fertig stellen** ändern, indem Sie dem Assistenten eine [**PSM \_ SETFINISHTEXT-Nachricht**](psm-setfinishtext.md) senden. Standardmäßig enthält die Schaltfläche **Fertig stellen** keine Tastaturbeschleunigung. Um eine Tastaturbeschleunigung zu definieren, fügen Sie ein ampersand in die Textzeichenfolge ein, die Sie an PSM \_ SETFINISHTEXT übergeben. Beispielsweise definiert "&Finish" "F" als Tastaturbeschleunigung.

**Vorlagen für das Dialogfeld "Innere Seite"**

Innere Seiten haben eine etwas andere Darstellung als äußere Seiten. Die folgende Abbildung zeigt eine Assistenten97-Beispielseite mit einer Platzhalterheaderbitmap.

![Screenshot einer Assistentenseite mit Titel- und Untertiteltext und einer Grafik oben, Text in der Mitte und Schaltflächen unten](images/wiz97interior.png)

Der Headerbereich am oberen Rand der Seite wird vom Eigenschaftenblatt behandelt, sodass er nicht in der Vorlage enthalten ist. Der Inhalt des Headers wird in der [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) der Seite und in der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) des Assistenten angegeben. Da die innere Seite zwischen der Kopfzeile und den Schaltflächen passen muss, ist die Dialogfeldvorlage Wizard97 317 x 143 Dialogeinheiten, etwas kleiner als die Vorlage für äußere Seiten.

Die folgende Abbildung zeigt einen Assistenten, der aus derselben Vorlage erstellt wurde.

![Screenshot, der sich vom vorherigen unterscheidet, indem oben ein Titelbereich und unten nur die Schaltflächen next und cancel angezeigt werden](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definieren der Assistentenseiten

Nachdem Sie die Dialogfeldvorlagen und zugehörigen Ressourcen wie Bitmaps und Zeichenfolgentabellen erstellt haben, können Sie die Eigenschaftenblattseiten erstellen. Die Prozedur ähnelt der für Standardeigenschaftenblätter. Füllen Sie zunächst die entsprechenden Member einer [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) aus. (Einige Member sind assistentenspezifisch.) Rufen Sie dann die [**CreatePropertySheetPage-Funktion**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) auf, um das HPROPSHEETPAGE-Handle der Seite zu erstellen.

Die folgenden assistentenbezogenen Flags können im **dwFlags-Member** der [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) festgelegt werden.



| Flag                   | Beschreibung                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | Legen Sie dieses Flag für äußere Seiten im Assistenten97 fest. Der Header wird nicht angezeigt, und es kann ein Wasserzeichen angezeigt werden.                                |
| PSP \_ USEHEADERTITLE    | Legen Sie dieses Flag für innere Seiten fest, um einen Titel im Headerbereich von Wizard97 oder im oberen Bereich des Clientbereichs eines Assistenten zu setzen. |
| PSP \_ USEHEADERSUBTITLE | Legen Sie dieses Flag für innere Seiten fest, um in Wizard97 einen Untertitel in den Headerbereich zu setzen.                                                  |



 

Wenn Sie PSP \_ USEHEADERTITLE oder PSP \_ USEHEADERSUBTITLE festgelegt haben, weisen Sie den Titel- und Untertiteltext den **PszHeaderTitle-** bzw. **pszHeaderSubtitle-Membern** zu. Wenn Sie Textzeichenfolgen Membern der [**PROPSHEETPAGE-**](pss-propsheetpage.md) und [**PROPSHEETHEADER-Strukturen**](pss-propsheetheader.md) zuweisen, können Sie entweder einen Zeichenfolgenzeiger zuweisen oder das **MAKEINTRESOURCE-Makro** verwenden, um einen Wert aus einer Zeichenfolgenressource zuzuweisen. Die Zeichenfolgenressource wird aus dem Modul geladen, das im **hInstance-Element** der **PROPSHEETHEADER-Struktur** des Assistenten angegeben ist.

Wenn Sie [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) aufrufen, um eine Seite zu erstellen, weisen Sie das Ergebnis einem Element eines Arrays von HPROPSHEETPAGE-Handles zu. Dieses Array wird beim Erstellen des Eigenschaftenblatts verwendet. Der Arrayindex des Handles einer Seite bestimmt die Standardreihenfolge, in der sie angezeigt wird. Nachdem Sie das HPROPSHEETPAGE-Handle einer Seite erstellt haben, können Sie dieselbe [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) wiederverwenden, um die nächste Seite zu erstellen, indem Sie den relevanten Membern neue Werte zuweisen.

Eine alternative Möglichkeit zum Erstellen von Seiten besteht darin, separate [**PROPSHEETPAGE-Strukturen**](pss-propsheetpage.md) für jede Seite zu verwenden und ein Array von Strukturen zu erstellen. Dieses Array wird anstelle eines Arrays von HPROPSHEETPAGE-Handles verwendet, wenn das Eigenschaftenblatt erstellt wird. Durch die Verwendung separater **PROPSHEETPAGE-Strukturen** entfällt die Notwendigkeit, [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) aufzurufen, aber es wird mehr Arbeitsspeicher verwendet. Andernfalls gibt es keinen signifikanten Unterschied zwischen den beiden Ansätzen.

Im folgenden Beispiel wird eine innere Wizard97-Seite durch Zuweisen von Werten zu einer [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) definiert. In diesem Beispiel werden Titel, Untertitel und Dialogfeldvorlage der Seite durch ihre Ressourcen-IDs identifiziert. Die [**CreatePropertySheetPage-Funktion**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) wird dann aufgerufen, um das HPROPSHEETPAGE-Handle der Seite zu erstellen. Da es sich um die zweite seite handelt, die angezeigt wird, wird das Handle dem Array von Handles *(ahpsp)* mit einem Index von 1 zugewiesen.


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>Benutzerdefinierte Seitendaten

Wenn Sie eine Seite erstellen, können Sie ihr benutzerdefinierte Daten zuweisen, indem Sie den **lParam-Member** der [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) verwenden, in der Regel durch Zuweisen eines Zeigers auf eine benutzerdefinierte Struktur.

Wenn die Seite zum ersten Mal ausgewählt wird, empfängt ihre Dialogfeldprozedur eine [**WM \_ INITDIALOG-Meldung.**](/windows/desktop/dlgbox/wm-initdialog) Der *lParam-Wert* der Nachricht verweist auf eine Kopie der [**PROPSHEETPAGE-Struktur**](pss-propsheetpage.md) der Seite, aus der Sie die benutzerdefinierten Daten abrufen können. Sie können diese Daten dann zur Verwendung in nachfolgenden Nachrichten speichern, indem [**Sie SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) mit GWL \_ USERDATA als Indexparameter verwenden. Mehrere Seiten können einen Zeiger auf dieselben Daten haben, und alle Änderungen an den Daten, die von einer Seite vorgenommen werden, stehen den anderen Seiten in ihren Dialogfeldprozessen zur Verfügung.

### <a name="define-the-wizard-property-sheet"></a>Definieren des Eigenschaftenblatts des Assistenten

Wie bei normalen Eigenschaftenblättern definieren Sie das Eigenschaftenblatt des Assistenten, indem Sie Elemente einer [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) ausfüllen. Mit dieser Struktur können Sie die Seiten, aus denen der Assistent bestehen, und die Standardreihenfolge, in der sie angezeigt werden, zusammen mit mehreren zugehörigen Parametern angeben. Anschließend starten Sie den Assistenten, indem Sie die [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) aufrufen.

Im Stil Wizard97 wird der **pszCaption-Member** der [**PROPSHEETHEADER-Struktur**](pss-propsheetheader.md) ignoriert. Stattdessen zeigt der Assistent die Beschriftung an, die in der Dialogfeldvorlage der aktuellen Seite angegeben ist. Wenn in der Vorlage keine Beschriftung vorhanden ist, wird die Beschriftung von der vorherigen Seite angezeigt. Um die gleiche Beschriftung auf allen Seiten anzuzeigen, geben Sie daher die Beschriftung in der Vorlage für die Einführungsseite an.

Im Stil des Assistenten wird die Beschriftung des Dialogfelds aus **pszCaption** übernommen.

Wenn Sie ein Array von HPROPSHEETPAGE-Handles für Ihre Seiten erstellt haben, weisen Sie das Array dem **phpage-Member** zu. Wenn Sie stattdessen ein Array von [**PROPSHEETPAGE-Strukturen**](pss-propsheetpage.md) erstellt haben, weisen Sie das Array dem **ppsp-Member** zu, und legen Sie das PSH \_ PROPSHEETPAGE-Flag im **dwFlags-Member** fest.

Im folgenden Beispiel werden *psh*, einer [**PROPSHEETHEADER-Struktur,**](pss-propsheetheader.md) Werte zugewiesen und die [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) aufgerufen, um den Assistenten zu starten. Der Assistent im Stil von Wizard97 verfügt über Wasserzeichen- und Headergrafiken, die durch ihre Ressourcen-IDs angegeben werden. Das *ahpsp-Array* enthält alle HPROPSHEETPAGE-Handles und definiert die Standardreihenfolge, in der sie angezeigt werden.


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>Die Dialogfeldprozedur

Jede Seite des Assistenten benötigt eine Dialogfeldprozedur, um Windows Nachrichten zu verarbeiten, insbesondere Benachrichtigungen von den Steuerelementen und dem Assistenten. Die drei Meldungen, die fast alle Assistenten verarbeiten müssen, sind [**WM \_ INITDIALOG,**](/windows/desktop/dlgbox/wm-initdialog) [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)und [**WM \_ NOTIFY.**](wm-notify.md)

Die [**WM \_ NOTIFY-Meldung**](wm-notify.md) wird empfangen, bevor die Seite angezeigt wird und wenn auf eine der Schaltflächen des Assistenten geklickt wird. Der *lParam-Parameter* der Nachricht ist ein Zeiger auf eine [**NMHDR-Headerstruktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr) Die ID der Benachrichtigung ist im **Codemember** der Struktur enthalten. Die vier Benachrichtigungen, die die meisten Assistenten behandeln müssen, lauten wie folgt.



| Code                                | BESCHREIBUNG                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ SETACTIVE](psn-setactive.md) | Wird gesendet, bevor die Seite angezeigt wird.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Wird gesendet, wenn auf die Schaltfläche **Zurück** geklickt wird.   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Wird gesendet, wenn auf die Schaltfläche **Weiter** geklickt wird.   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Wird gesendet, wenn auf die Schaltfläche **Fertig stellen** geklickt wird. |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Behandeln von WM \_ INITDIALOG und WM \_ DESTROY

Wenn eine Seite zum ersten Mal angezeigt wird, empfängt die zugehörige Dialogfeldprozedur eine [**\_ WM-INITDIALOG-Meldung.**](/windows/desktop/dlgbox/wm-initdialog) Durch die Behandlung dieser Meldung kann der Assistent alle erforderlichen Initialisierungsaufgaben ausführen, z. B. das Speichern benutzerdefinierter Daten oder das Festlegen von Schriftarten.

Wenn das Eigenschaftenblatt zerstört wird, erhalten Sie eine [**WM \_ DESTROY-Nachricht.**](/windows/desktop/winmsg/wm-destroy) Der Assistent wird automatisch vom System zerstört, aber durch die Behandlung dieser Meldung können Sie alle erforderlichen Bereinigungen durchführen.

### <a name="handle-psn_setactive"></a>Behandeln von PSN \_ SETACTIVE

Der [PSN SETACTIVE-Benachrichtigungscode \_ ](psn-setactive.md) wird jedes Mal gesendet, wenn eine Seite sichtbar gemacht wird. Beim ersten Aufruf einer Seite folgt PSN \_ SETACTIVE der [**\_ WM-INITDIALOG-Meldung.**](/windows/desktop/dlgbox/wm-initdialog) Wenn die Seite anschließend erneut angezeigt wird, erhält sie nur eine PSN \_ SETACTIVE-Benachrichtigung. Diese Benachrichtigung wird normalerweise verarbeitet, um Daten für die Seite zu initialisieren und die entsprechenden Schaltflächen zu aktivieren.

Standardmäßig zeigt der Assistent die Schaltflächen **Zurück,** **Weiter** und **Abbrechen** an, wobei alle Schaltflächen aktiviert sind. Um eine Schaltfläche zu deaktivieren oder **Fertig stellen** anstelle von **Weiter** anzuzeigen, müssen Sie eine [**PSM \_ SETWIZBUTTONS-Nachricht**](psm-setwizbuttons.md) senden. Nachdem diese Nachricht gesendet wurde, wird der Zustand der Schaltflächen beibehalten, bis sie von einer anderen **PSM \_ SETWIZBUTTONS-Nachricht** geändert wird, auch wenn eine neue Seite ausgewählt ist. In der Regel senden alle [PSN \_ SETACTIVE-Handler](psn-setactive.md) diese Meldung, um sicherzustellen, dass jede Seite den richtigen Schaltflächenzustand auf hat.

Sie können den Schaltflächenzustand mit dieser Meldung jederzeit ändern. Beispielsweise kann es sein, dass die Schaltfläche **Weiter** anfänglich deaktiviert werden soll. Nachdem ein Benutzer alle erforderlichen Informationen eingegeben hat, können Sie eine weitere [**PSM \_ SETWIZBUTTONS-Nachricht**](psm-setwizbuttons.md) senden, um die Schaltfläche **Weiter** zu aktivieren und den Benutzer zur nächsten Seite zu bringen.

Das folgende Codefragment verwendet das [**\_ PropSheet-Makro SetWizButtons,**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) um die Schaltflächen **Zurück** und **Weiter** auf einer inneren Seite zu aktivieren, bevor sie angezeigt werden.


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Behandeln von PSN \_ WIZNEXT, PSNWIZBACK und PSN \_ WIZFINISH

Wenn sie auf die Schaltfläche **Weiter** oder **Zurück** klicken, erhalten Sie einen [PSN \_ WIZNEXT-](psn-wiznext.md) oder [PSN WIZBACK-Benachrichtigungscode. \_](psn-wizback.md) Standardmäßig wechselt der Assistent automatisch zur nächsten oder vorherigen Seite in der Reihenfolge, die beim Erstellen des Eigenschaftenblatts definiert wird. Ein häufiger Grund für die Behandlung dieser Benachrichtigungen besteht darin, zu verhindern, dass der Benutzer seitenwechselt, oder die Standardreihenfolge der Seite außer Kraft zu setzen.

Um zu verhindern, dass der Benutzer seitenwechselt, behandeln Sie die Schaltflächenbenachrichtigung, rufen Sie die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, wobei der \_ DWL-MSGRESULT-Wert auf –1 festgelegt ist, und geben **Sie TRUE** zurück. Beispiel:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Um die Standardreihenfolge zu überschreiben und zu einer bestimmten Seite zu wechseln, rufen [**Sie SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf, wobei der DWL-MSGRESULT-Wert \_ auf die Ressourcen-ID des Dialogfelds der Seite festgelegt ist, und geben **Sie TRUE** zurück. Beispiel:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Wenn Sie auf die Schaltfläche **Fertig stellen** oder **Abbrechen** klicken, erhalten Sie einen [PSN \_ WIZFINISH-](psn-wizfinish.md) bzw. [PSN RESET-Benachrichtigungscode. \_](psn-reset.md) Wenn auf eine dieser Schaltflächen geklickt wird, wird der Assistent automatisch vom System zerstört. Sie können diese Benachrichtigungen jedoch verarbeiten, wenn Sie Bereinigungsaufgaben ausführen müssen, bevor der Assistent zerstört wird. Um zu verhindern, dass der Assistent zerstört wird, wenn Sie eine PSN \_ WIZFINISH-Benachrichtigung erhalten, rufen Sie [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ MSGRESULT-Wert auf **TRUE** auf, und geben **Sie TRUE** zurück. Beispiel:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Abwärtskompatible Assistenten

Im vorherigen Abschnitt wird davon ausgegangen, dass Sie einen Assistenten für ein System mit [Version 5](common-control-versions.md) oder höher der allgemeinen Steuerelemente implementieren.

Wenn Sie einen Assistenten für Systeme mit früheren Versionen der allgemeinen Steuerelemente schreiben, sind viele der im vorherigen Abschnitt erläuterten Features nicht verfügbar. Eine Reihe von Membern der [**PROPSHEETHEADER-**](pss-propsheetheader.md) und [**PROPSHEETPAGE-Strukturen,**](pss-propsheetpage.md) die vom Wizard97-Stil verwendet werden, werden nur von allgemeinen Steuerelementen der Version 5 und höher unterstützt. Es ist jedoch weiterhin möglich, einen *abwärtskompatiblen* Assistenten zu implementieren, der der Darstellung des Assistenten97 ähnelt. Dazu müssen Sie Folgendes explizit implementieren:

-   Fügen Sie die Wasserzeichengrafik zur Dialogfeldvorlage für Ihre Einführungs- und Vervollständigungsseiten hinzu.
-   Stellen Sie alle Ihre Vorlagen in die gleiche Größe ein. Es gibt keinen separaten systemdefinierten Headerbereich für innere Seiten.
-   Erstellen Sie den Headerbereich der inneren Seite explizit für Ihre Vorlagen.
-   Verwenden Sie keine Headergrafik, da sie mit dem Titel oder Untertitel in Konflikt stehen kann, wenn sich die Größe des Assistenten ändert.

Weitere Informationen zu abwärtskompatiblen Assistenten finden Sie unter [Abwärtskompatibeler Assistent 97](/previous-versions//ms737910(v=vs.85)).

## <a name="remarks"></a>Hinweise

Eine vollständige Beschreibung der Entwurfsprobleme für Wizard97 finden Sie in der [Wizard97-Spezifikation](/previous-versions//ms738248(v=vs.85))an anderer Stelle im Windows SDK. Dieses Dokument enthält Richtlinien für z. B. die Dimensionen für die Dialogfelder, Bitmapdimensionen und Farben und die Platzierung von Steuerelementen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaftenblättern](using-property-sheets.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 