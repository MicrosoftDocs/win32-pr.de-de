---
title: Erstellen von Assistenten
description: Ein Assistent ist eine Art von Eigenschaften Blatt, das eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu leiten.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106363198"
---
# <a name="how-to-create-wizards"></a>Erstellen von Assistenten

Ein Assistent ist eine Art von Eigenschaften Blatt, das eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu leiten.

Assistenten sind einer der Schlüssel zum Vereinfachen der Benutzer Leistung. Sie ermöglichen es Ihnen, einen komplexen Vorgang auszuführen, z. b. die Konfiguration einer Anwendung, und Sie in eine Reihe einfacher Schritte zu unterbrechen. An jedem Punkt des Vorgangs können Sie eine Erläuterung dazu bereitstellen, was erforderlich ist, und Steuerelemente anzeigen, die es dem Benutzer ermöglichen, eine Auswahl vorzunehmen und Text einzugeben.

Ein Assistent ist tatsächlich ein Eigenschaftentyp. Bei einem Eigenschaften Blatt handelt es sich im Wesentlichen um einen Container für eine Auflistung von *Seiten*, wobei jede Seite ein separates Dialogfeld ist. Während reguläre Eigenschaften Blätter den Benutzer jederzeit jederzeit auf eine beliebige Seite zugreifen können, stellen die Assistenten Seiten nacheinander zur Verfügung. Anstelle von Registerkarten werden Schaltflächen verwendet, um vorwärts und rückwärts zu navigieren. Die Reihenfolge, in der Seiten angezeigt werden, wird von der Anwendung gesteuert und kann auf der Grundlage von Benutzereingaben geändert werden.

Es gibt zwei Hauptarten von Assistenten: der ältere Wizard97-Stil und der Aero-Stil, der in Windows Vista eingeführt wurde. Abbildungen finden Sie unter [Informationen zu Eigenschaften Blättern](property-sheets.md). (Ein Dritter Stil, nur mit dem PSH \_ Der Assistent oder das Flag "PSH \_ Wizard \_ Lite" zeigt eine einfache Sequenz von Eigenschaften Blättern ohne Header oder Wasserzeichen an.)

> [!Note]  
> Ein "Wasserzeichen" im Kontext von Assistenten ist eine Bitmap, die am linken Rand einiger Seiten angezeigt wird.

 

Die Diskussion in den meisten Fällen setzt voraus, dass Sie einen Assistenten für ein System mit [Version 5,80](common-control-versions.md) oder höher der allgemeinen Steuerelemente implementieren. Wenn Sie versuchen, den Wizard97-Stil mit früheren Versionen der allgemeinen Steuerelemente zu verwenden, kann Ihre Anwendung kompiliert werden, wird aber nicht ordnungsgemäß angezeigt. Eine Erläuterung zum Erstellen eines Wizard97-kompatiblen Assistenten auf früheren Systemen finden Sie unter abwärts kompatible Assistenten weiter unten in diesem Thema.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="wizard-implementation"></a>Implementierung des Assistenten

Das Implementieren eines Assistenten ähnelt dem Implementieren eines regulären Eigenschaften Blatts. Auf der grundlegendsten Ebene ist es wichtig, eines der folgenden Flags oder eine Kombination von Flags in der [**propsheeteader**](pss-propsheetheader.md) -Struktur festzulegen, die das Eigenschaften Blatt definiert.



| Flag                           | Stil                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| PSH- \_ Assistent                    | Ein einfacher Assistent ohne Header oder Bitmaps.                                                                                                           |
| PSH- \_ Assistent ( \_ Lite)              | Ähnlich wie bei einem PSH- \_ Assistenten mit einigen geringfügigen Unterschieden. beispielsweise wird der unter Teiler oberhalb der Schaltflächen auf die vollständige Breite des Fensters festgelegt. |
| PSH \_ WIZARD97                  | Ein Wizard97-Assistent mit (optionalen) Headern, Header Bitmaps und Wasserzeichen.                                                                            |
| PSH- \_ Assistent ( \| PSH-Assistent) \_ | Ein Aero-Assistent. Aero-Assistenten verwenden keine Wasserzeichen oder Header Bitmaps. Sie erfordern das STA-Modell (Single Thread-Apartment).                         |



 

Die grundlegende Vorgehensweise für die Implementierung eines Assistenten lautet wie folgt:

1.  Erstellen Sie eine Dialogfeld Vorlage für jede Seite.
2.  Definieren Sie die Seiten, indem Sie für jede Seite eine [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur erstellen. Diese Struktur definiert die Seite und enthält Zeiger auf die Dialogfeld Vorlage und alle Bitmaps oder andere Ressourcen.
3.  Übergeben Sie die [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur, die Sie im vorherigen Schritt erstellt haben, an [**die Funktion "**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) die Funktion" "von" ", um das hpropsheetpage-Handle der Seite zu erstellen.
4.  Definieren Sie den Assistenten, indem Sie dafür eine [**propsheetheiader**](pss-propsheetheader.md) -Struktur erstellen.
5.  Übergeben Sie die [**propsheethader**](pss-propsheetheader.md) -Struktur an die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion, um den Assistenten anzuzeigen.
6.  Implementieren Sie Dialogfeld Prozeduren für jede Seite, um Benachrichtigungs Meldungen aus den Steuerelementen der Seite und den Schaltflächen des Assistenten zu verarbeiten und andere Windows-Messaging zu verarbeiten.

### <a name="create-the-dialog-box-templates"></a>Erstellen der Dialog Feld Vorlagen

Es gibt zwei grundlegende Arten von Assistenten Seiten: Außen und innen. Externe Seiten sind die Einführungsseiten (Willkommen) und Abschluss Seiten. Alle anderen sind innere Seiten.

**Externe Seite (Dialog Feld Vorlagen)**

Das grundlegende Layout der Einführungs-und Abschluss Seiten ist identisch. Die folgende Abbildung zeigt eine Beispiel-Wizard97-Einführungsseite mit einem Platzhalter Wasserzeichen.

![Screenshot mit einer Assistenten Seite mit einer Grafik auf der linken Seite, Titel und TextText auf der rechten Seite, Schaltfläche "zurück", "weiter" und "Abbrechen" unten](images/wiz97exterior.png)

Für Wizard97-externe Seiten ist die Dialogfeld Vorlage 317x193 Dialog Einheiten. Es füllt den gesamten Assistenten mit Ausnahme der Beschriftung und des Bands im unteren Bereich, das die Schaltflächen **zurück**, **weiter** und **Abbrechen** enthält. Die linke Seite der Vorlage, die für eine "Wasserzeichen"-Bitmap reserviert ist, sollte keine Steuerelemente enthalten. Das Wasserzeichen ist in der [**propsheeder**](pss-propsheetheader.md) -Struktur des Assistenten angegeben und wird der Seite automatisch hinzugefügt. Beim Entwerfen der Ressourcen Vorlage müssen Sie Platz dafür zulassen.

Beachten Sie beim Erstellen der Wasserzeichen-Bitmap, dass das Dialogfeld die Größe vergrößern kann, wenn beispielsweise der Benutzer eine große System Schriftart auswählt. In unterschiedlichen Sprachen gibt es auch tendenziell verschiedene Schriftart Metriken. Wenn die Seite wächst, wird der für das Wasserzeichen reservierte Bereich proportional vergrößert. Allerdings können Sie die Wasserzeichen Bitmap nicht ändern, und die Bitmap ist nicht so gestreckt, dass der größere Bereich ausgefüllt wird. Stattdessen wird die ursprüngliche Größe der Bitmap im oberen linken Bereich des reservierten Bereichs belassen. Der Teil des größeren reservierten Bereichs, der nicht durch das Wasserzeichen abgedeckt wird, wird automatisch mit der Farbe des oberen linken Pixels der Bitmap aufgefüllt.

Wenn Sie unterschiedliche Wasserzeichen-Bitmaps für verschiedene Schriftart Metriken benötigen, sind zwei mögliche Lösungen:

-   Geben Sie die Schriftart Metrik vor dem Erstellen des Assistenten an, und geben Sie eine entsprechende Wasserzeichen-Bitmap an.
-   Geben Sie beim Erstellen des Assistenten keine Wasserzeichen-Bitmap an. Wizard97 lässt den Wasserzeichen Bereich leer. Zeichnen Sie dann eine Bitmap mit passender Größenanpassung in dem Bereich, der für das Wasserzeichen reserviert ist.

Sie können Steuerelemente im Bereich rechts neben dem Wasserzeichen platzieren, wie es bei einem regulären Dialogfeld der Fall wäre. Die Hintergrundfarbe dieses Bereichs wird durch das System bestimmt, und es ist keine Aktion erforderlich. In diesem Bereich fügen Sie in der Regel zwei statische Steuerelemente ein. Die obere enthält den Titel und verwendet eine große Fett Schrift (12 Punkte Verdana Bold für Wizard97). Der andere, der für erläuternden Text steht, verwendet die Standard Dialogfeld Schriftart.

Der Hauptunterschied zwischen der Einführungsseite und der Vervollständigungs Seite sind die Schaltflächen des Assistenten und der Text in den statischen Steuerelementen. Einführungsseiten verfügen normalerweise über eine Schaltfläche " **weiter** " und " **zurück** ", und nur die Schaltfläche " **weiter** " Auf den Abschluss Seiten wird die Schaltfläche " **zurück** " aktiviert, und die Schaltfläche **weiter** wird durch die Schaltfläche **Fertig** stellen ersetzt.

> [!Note]  
> In Aero-Assistenten wird die Schaltfläche " **zurück** " durch eine Pfeil Schaltfläche in der Titelleiste ersetzt.

 

Sie können den Text auf der Schaltfläche **Fertig** Stellen ändern, indem Sie dem Assistenten eine [**PSM \_ setfinishtext**](psm-setfinishtext.md) -Nachricht senden. Standardmäßig enthält die Schaltfläche **Fertig** stellen keine Tastatur Beschleunigung. Zum Definieren einer Zugriffstaste fügen Sie ein kaufmännisches und-Zeichen in die Text Zeichenfolge ein, die Sie an PSM \_ setfinishtext übergeben. Beispielsweise definiert "&Fertigstellen" "F" als Tastaturbeschleuniger.

**Dialog Feld Vorlagen für innere Seite**

Innere Seiten haben eine etwas andere Darstellung als externe Seiten. In der folgenden Abbildung wird eine Wizard97 innere Seite Sample mit einem Platzhalter-Header Bitmap dargestellt.

![Screenshot einer Assistenten Seite mit Titel und Untertitel Text und einer Grafik oben, Text in der Mitte und Schaltflächen unten](images/wiz97interior.png)

Der Header Bereich am oberen Rand der Seite wird vom Eigenschaften Blatt behandelt, sodass er nicht in der Vorlage enthalten ist. Der Inhalt des Headers wird in der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur der Seite und in der [**propsheeder**](pss-propsheetheader.md) -Struktur des Assistenten angegeben. Da die innere Seite zwischen dem Header und den Schaltflächen passen muss, ist die Wizard97-Dialogfeld Vorlage 317x143 Dialog Einheiten, die etwas kleiner als die Vorlage für äußere Seiten ist.

Die folgende Abbildung zeigt einen Aero-Assistenten, der aus derselben Vorlage erstellt wurde.

![Screenshot, der sich von der vorherigen Seite unterscheidet, indem oben ein Titelbereich angezeigt wird, und die Schaltflächen unten und Abbrechen](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definieren der Assistenten Seiten

Nachdem Sie die Dialogfeld Vorlagen und zugehörigen Ressourcen wie Bitmaps und Zeichen folgen Tabellen erstellt haben, können Sie die Eigenschaften Blattseiten erstellen. Die Vorgehensweise ähnelt der Vorgehensweise für Standardeigenschaften Blätter. Füllen Sie zunächst die entsprechenden Member einer [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur aus. (Einige Mitglieder sind für Assistenten spezifisch.) Rufen Sie dann [**die Funktion "**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) Funktion" in der Funktion "" auf, um das hpropsheetpage-Handle der Seite zu erstellen.

Die folgenden Assistenten bezogenen Flags können im **dwFlags** -Member der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur festgelegt werden.



| Flag                   | Beschreibung                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP- \_ hideheader        | Legen Sie dieses Flag für äußere Seiten in Wizard97 fest. Der-Header wird nicht angezeigt, und ein Wasserzeichen kann angezeigt werden.                                |
| PSP \_ useheadertitle    | Legen Sie dieses Flag für innere Seiten fest, um einen Titel im Header Bereich in Wizard97 oder am oberen Rand des Client Bereichs in einem Aero-Assistenten abzulegen. |
| PSP \_ useheaderuntertitel | Legen Sie dieses Flag für innere Seiten fest, um einen Untertitel in den Header Bereich in Wizard97 einzufügen.                                                  |



 

Wenn Sie den Wert von "PSP \_ useheadertitle" oder "PSP \_ useheadertitle" festgelegt haben, weisen Sie dem **pszheadertitle** -bzw. dem **pszheaderuntertitel** -Member den Titel und den Untertitel zu Wenn Sie den Membern der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur und der [**propsheeteader**](pss-propsheetheader.md) -Struktur Text Zeichenfolgen zuweisen, können Sie entweder einen Zeichen folgen Zeiger zuweisen oder das Makro **makeintresource** verwenden, um einen Wert aus einer Zeichen folgen Ressource zuzuweisen. Die Zeichen folgen Ressource wird aus dem Modul geladen, das im **HINSTANCE** -Member der **propsheeder** -Struktur des Assistenten angegeben ist.

Wenn Sie " [**kreatepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) " aufrufen, um eine Seite zu erstellen, weisen Sie das Ergebnis einem Element eines Arrays von hpropsheetpage-Handles zu. Dieses Array wird beim Erstellen des Eigenschaften Blatts verwendet. Der Array Index des Handles einer Seite bestimmt die Standard Reihenfolge, in der Sie angezeigt wird. Nachdem Sie das hpropsheetpage-Handle einer Seite erstellt haben, können Sie die gleiche [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur wieder verwenden, um die nächste Seite zu erstellen, indem Sie den relevanten Membern neue Werte zuweisen.

Eine alternative Möglichkeit zum Erstellen von Seiten ist die Verwendung separater [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen für jede Seite und die Erstellung eines Arrays von Strukturen. Dieses Array wird anstelle eines Arrays von hpropsheetpage-Handles verwendet, wenn das Eigenschaften Blatt erstellt wird. Durch die Verwendung separater **PROPSHEETPAGE** -Strukturen entfällt die Notwendigkeit, eine aufzurufende " [**kreatepropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) " aufzurufen. Andernfalls gibt es keinen signifikanten Unterschied zwischen den beiden Ansätzen.

Im folgenden Beispiel wird eine innere Wizard97 Seite definiert, indem einer [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur Werte zugewiesen werden. In diesem Beispiel werden der Titel, der Untertitel und die Dialogfeld Vorlage der Seite durch ihre Ressourcen-IDs identifiziert. Anschließend wird [**die Funktion "**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) -Funktion" aufgerufen, um das hpropsheetpage-Handle der Seite zu erstellen. Da es sich um die zweite Seite handelt, die angezeigt wird, wird das Handle dem Array von Handles ( *ahpsp*) mit einem Index von 1 zugewiesen.


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



### <a name="custom-page-data"></a>Benutzerdefinierte Seiten Daten

Wenn Sie eine Seite erstellen, können Sie Ihr benutzerdefinierte Daten mithilfe des **LPARAM** -Members der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur zuweisen, in der Regel durch Zuweisen eines Zeigers zu einer benutzerdefinierten Struktur.

Wenn die Seite zum ersten Mal ausgewählt wird, erhält die zugehörige Dialogfeld Prozedur eine " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung. Der *LPARAM* -Wert der Meldung verweist auf eine Kopie der [**PROPSHEETPAGE**](pss-propsheetpage.md) -Struktur der Seite, aus der Sie die benutzerdefinierten Daten abrufen können. Anschließend können Sie diese Daten für die Verwendung in nachfolgenden Nachrichten speichern, indem Sie [**setwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) mit GWL \_ UserData als Index Parameter verwenden. Mehrere Seiten können über einen Zeiger auf die gleichen Daten verfügen, und jede Änderung an den Daten, die von einer Seite vorgenommen werden, ist für die anderen Seiten in ihren Dialog Prozeduren verfügbar.

### <a name="define-the-wizard-property-sheet"></a>Definieren des Assistenten-Eigenschaften Blatts

Wie bei normalen Eigenschaften Blättern definieren Sie die Eigenschaften Seite des Assistenten, indem Sie Member einer [**propsheeder Ader**](pss-propsheetheader.md) -Struktur ausfüllen. Diese Struktur ermöglicht es Ihnen, die Seiten, die den Assistenten bilden, und die Standard Reihenfolge, in der Sie angezeigt werden, zusammen mit mehreren zugehörigen Parametern anzugeben. Anschließend starten Sie den Assistenten, indem Sie die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion aufrufen.

Im Wizard97-Stil wird der **pszcaption** -Member der [**propsheeder**](pss-propsheetheader.md) -Struktur ignoriert. Stattdessen zeigt der Assistent die Beschriftung an, die in der Dialogfeld Vorlage der aktuellen Seite angegeben ist. Wenn in der Vorlage keine Beschriftung fehlt, wird die Beschriftung der vorherigen Seite angezeigt. Wenn Sie also die gleiche Beschriftung auf allen Seiten anzeigen möchten, geben Sie die Beschriftung in der Vorlage für die Einführungsseite an.

Im Stil des Aero-Assistenten wird die Dialogfeld Beschriftung aus **pszcaption** entnommen.

Wenn Sie ein Array von hpropsheetpage-Handles für Ihre Seiten erstellt haben, weisen Sie das Array dem **phpage** -Member zu. Wenn Sie stattdessen ein Array von [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen erstellt haben, weisen Sie das Array dem **PPSP** -Member zu, und legen Sie das PSH \_ PROPSHEETPAGE-Flag im **dwFlags** -Member fest.

Im folgenden Beispiel werden *PSH* Werte zugewiesen, eine [**propsheethader**](pss-propsheetheader.md) -Struktur, und die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion wird aufgerufen, um den Assistenten zu starten. Der Wizard97-Assistent verfügt sowohl über Wasserzeichen als auch über Kopfzeilen Grafiken, die durch ihre Ressourcen-IDs angegeben werden. Das *ahpsp* -Array enthält alle hpropsheetpage-Handles und definiert die Standard Reihenfolge, in der Sie angezeigt werden.


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



### <a name="the-dialog-box-procedure"></a>Dialog Feld Prozedur

Jede Seite des Assistenten benötigt eine Dialogfeld Prozedur zum Verarbeiten von Windows-Meldungen, insbesondere Benachrichtigungen von den Steuerelementen und dem Assistenten. Die drei Nachrichten, die fast alle Assistenten verarbeiten können, sind [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog), [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy)und [**WM \_ Notify**](wm-notify.md).

Die [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung wird empfangen, bevor die Seite angezeigt wird, und wenn auf eine der Schaltflächen des Assistenten geklickt wird. Der *LPARAM* -Parameter der Nachricht ist ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Header Struktur. Die ID der Benachrichtigung ist im **Codemember** der Struktur enthalten. Die folgenden vier Benachrichtigungen müssen von den meisten Assistenten verarbeitet werden:



| Code                                | BESCHREIBUNG                                 |
|-------------------------------------|---------------------------------------------|
| [PSN- \_ SETACTIVE](psn-setactive.md) | Wird gesendet, bevor die Seite angezeigt wird.          |
| [PSN- \_ witzback](psn-wizback.md)     | Wird gesendet, wenn auf die Schaltfläche **zurück** geklickt wird.   |
| [PSN- \_ nächstes](psn-wiznext.md)     | Wird gesendet, wenn auf die Schaltfläche **weiter** geklickt wird.   |
| [PSN- \_ witzschluss](psn-wizfinish.md) | Gesendet, wenn auf die Schaltfläche **Fertig** stellen geklickt wird. |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Behandeln von WM \_ InitDialog und WM- \_ Zerstörung

Wenn eine Seite zum ersten Mal angezeigt wird, erhält die zugehörige Dialogfeld Prozedur eine " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung. Durch die Verarbeitung dieser Nachricht kann der Assistent alle erforderlichen Initialisierungs Aufgaben ausführen, z. b. das Speichern von benutzerdefinierten Daten oder das Festlegen von Schriftarten.

Wenn das Eigenschaften Blatt zerstört wird, erhalten Sie eine [**WM \_**](/windows/desktop/winmsg/wm-destroy) -Lösch Nachricht. Der Assistent wird automatisch vom System zerstört, aber die Verarbeitung dieser Meldung ermöglicht es Ihnen, alle erforderlichen Bereinigungs Schritte durchzuführen.

### <a name="handle-psn_setactive"></a>Behandeln von "PSN \_ SETACTIVE"

Der " [PSN \_ SETACTIVE](psn-setactive.md) "-Benachrichtigungs Code wird jedes Mal gesendet, wenn eine Seite sichtbar gemacht wird. Wenn Sie zum ersten Mal eine Seite besuchen, \_ folgt "PSN SETACTIVE" der " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Nachricht. Wenn die Seite anschließend erneut überprüft wird, empfängt Sie nur eine PSN- \_ SETACTIVE-Benachrichtigung. Diese Benachrichtigung wird normalerweise behandelt, um Daten für die Seite zu initialisieren und die entsprechenden Schaltflächen zu aktivieren.

Standardmäßig zeigt der Assistent die Schaltflächen **zurück**, **weiter** und **Abbrechen** mit aktivierten Schaltflächen an. Zum Deaktivieren einer Schaltfläche oder zum Anzeigen der **Fertig** Stellung anstelle von **Next** müssen Sie eine PSM-Nachricht "Setup [**\_ Buttons**](psm-setwizbuttons.md) " senden. Nachdem diese Nachricht gesendet wurde, wird der Zustand der Schaltflächen so lange beibehalten, bis Sie durch eine andere PSM-Meldung "Setup **\_ Buttons** " geändert wird, auch wenn eine neue Seite ausgewählt ist. In der Regel senden alle [PSN- \_ SETACTIVE](psn-setactive.md) -Handler diese Nachricht, um sicherzustellen, dass jede Seite über den richtigen Schaltflächen Zustand verfügt.

Sie können den Schaltflächen Zustand mit dieser Meldung jederzeit ändern. Beispielsweise möchten Sie möglicherweise, dass die Schaltfläche **weiter** zuerst deaktiviert wird. Nachdem ein Benutzer alle erforderlichen Informationen eingegeben hat, können Sie eine weitere PSM-Setup- [**\_ Schalt**](psm-setwizbuttons.md) Flächen Nachricht senden, um die Schaltfläche **weiter** zu aktivieren und den Benutzer zur nächsten Seite zu gelangen.

Das folgende Code Fragment verwendet das [**propsheet \_ setwizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) -Makro, um die Schaltflächen " **zurück** " und " **weiter** " auf einer inneren Seite zu aktivieren, bevor Sie angezeigt wird.


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



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Umgang mit "PSN \_ wiznext", "psnwizback" und "PSN \_ witzfinish"

Wenn Sie auf eine Schaltfläche " **weiter** " oder " **zurück** " klicken, erhalten Sie den Benachrichtigungs Code " [PSN \_ wiznext](psn-wiznext.md) " oder " [PSN \_](psn-wizback.md) . Standardmäßig wechselt der Assistent automatisch zur nächsten oder vorherigen Seite in der Reihenfolge, die beim Erstellen des Eigenschaften Blatts definiert ist. Ein häufiger Grund für diese Benachrichtigungen besteht darin, den Benutzer daran zu hindern, Seiten zu wechseln oder die Standardseiten Reihenfolge zu überschreiben.

Um zu verhindern, dass der Benutzer Seiten wechseln kann, müssen Sie die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem \_ auf – 1 festgelegten DWL msgresult-Wert aufrufen und **true** zurückgeben. Beispiel:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Um die Standard Reihenfolge zu überschreiben und zu einer bestimmten Seite zu wechseln, rufen Sie [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ -Wert msgresult auf die Ressourcen-ID der Seite auf, und geben Sie **true** zurück. Beispiel:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Wenn Sie auf die Schaltfläche **Fertig** stellen oder **Abbrechen** klicken, erhalten Sie jeweils den Benachrichtigungs Code " [PSN \_ wizfinish](psn-wizfinish.md) " oder " [PSN \_ Reset](psn-reset.md) ". Wenn auf eine dieser Schaltflächen geklickt wird, wird der Assistent automatisch vom System gelöscht. Sie können diese Benachrichtigungen jedoch verarbeiten, wenn Sie Bereinigungs Tasks ausführen müssen, bevor der Assistent zerstört wird. Wenn Sie verhindern möchten, dass der Assistent zerstört wird, wenn Sie eine Benachrichtigung über "PSN- \_ witzschluss" erhalten, geben Sie [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ -Wert msgresult auf **true** und **true** zurück. Beispiel:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Abwärts kompatible Assistenten

Im vorherigen Abschnitt wird davon ausgegangen, dass Sie einen Assistenten für ein System mit [Version 5](common-control-versions.md) oder höher der allgemeinen Steuerelemente implementieren.

Wenn Sie einen Assistenten für Systeme mit früheren Versionen der allgemeinen Steuerelemente schreiben, sind viele der im vorherigen Abschnitt beschriebenen Features nicht verfügbar. Eine Reihe von [**memsheethader**](pss-propsheetheader.md) -und [**PROPSHEETPAGE**](pss-propsheetpage.md) -Strukturen, die vom Wizard97-Stil verwendet werden, werden nur von den allgemeinen Steuerelementen Version 5 und höher unterstützt. Es ist jedoch weiterhin möglich, einen abwärts *kompatiblen* Assistenten mit einer Darstellung zu implementieren, die dem Wizard97-Stil ähnelt. Zu diesem Zweck müssen Sie Folgendes explizit implementieren:

-   Fügen Sie die Wasserzeichen Grafik der Dialogfeld Vorlage für die Einführungs-und Abschluss Seiten hinzu.
-   Legen Sie alle Vorlagen auf dieselbe Größe. Für innere Seiten gibt es keinen separaten, vom System definierten Header Bereich.
-   Erstellen Sie den Header Bereich der inneren Seite explizit in ihren Vorlagen.
-   Verwenden Sie keine Header Grafik, da Sie möglicherweise mit dem Titel oder Untertitel in Konflikt steht, wenn die Größe des Assistenten geändert wird.

Weitere Informationen zu abwärts kompatiblen Assistenten finden Sie unter abwärts [kompatibler Assistent 97](/previous-versions//ms737910(v=vs.85)).

## <a name="remarks"></a>Bemerkungen

Eine ausführliche Erläuterung der Entwurfs Probleme für Wizard97 finden Sie in der [Wizard97-Spezifikation](/previous-versions//ms738248(v=vs.85))an anderer Stelle im Windows SDK. Dieses Dokument enthält Richtlinien für die Dimensionen der Dialogfelder, bitmapdimensionen und Farben sowie die Platzierung von Steuerelementen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften Blättern](using-property-sheets.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 