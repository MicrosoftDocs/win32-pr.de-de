---
title: Drucken (Dialogfeld)
description: Im Dialogfeld Drucken können Benutzeroptionen für einen bestimmten Druckauftrag auswählen.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, allgemeine Dialog Feld Bibliothek
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Dialogfeld Drucken
- Dialogfeld "Druck Setup"
- Dialogfeld "Drucken" anpassen
- vordefinierte Dialogfelder
- Dialogfelder, Drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fae1dd244391ea16478a0cb4f10803cf622dc64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102298"
---
# <a name="print-dialog-box"></a>Drucken (Dialogfeld)

Im Dialogfeld **Drucken** können Benutzeroptionen für einen bestimmten Druckauftrag auswählen. Der Benutzer kann z. b. den zu verwendenden Drucker, den zu druckenden Seitenbereich und die Anzahl der Kopien angeben.

Mit der [**printdlgex**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) -Funktion können Sie ein [Druckeigenschaften Blatt](print-property-sheet.md)anzeigen, das eine **Allgemeine** Seite enthält, die Steuerelemente enthält, die dem Dialogfeld **Drucken** ähneln. Auf dem Eigenschaften Blatt können auch zusätzliche anwendungsspezifische und Treiber spezifische Eigenschaften Seiten nach der Seite **Allgemein** vorhanden sein.

Sie erstellen und zeigen ein **Druck** Dialogfeld an, indem Sie eine [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur initialisieren und die Struktur an die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion übergeben.

Die folgende Abbildung zeigt ein typisches Dialogfeld **Drucken** .

![Drucken (Dialogfeld)](images/printdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **true** zurück und verwendet die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, um Informationen zur Auswahl des Benutzers zurückzugeben. Beispielsweise geben die Member **hDevMode** und **hDevNames** in der Regel globale Speicher Handles für-und [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen zurück. Mithilfe der Informationen in diesen Strukturen können Sie einen Gerätekontext oder einen Informations Kontext für den ausgewählten Drucker erstellen.

Wenn der Benutzer das Dialogfeld **Drucken** abbricht oder ein Fehler auftritt, gibt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **false** zurück. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**kommdlgextendecoderror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion verwenden, um den erweiterten Fehlerwert abzurufen.

Das Dialogfeld **Drucken** enthält eine **Druck Bereichs** Gruppe von Options Feldern, die angeben, ob der Benutzer alle Seiten, einen Seitenbereich oder nur den markierten Text drucken möchte. Vor dem Aufrufen von [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))können Sie eine der Flags für die Angabe " **PD \_ AllPages**", "PD" oder " **PD \_ pagenums** " festlegen, um anzugeben, welche Schaltfläche anfänglich ausgewählt ist. **\_** Wenn **PRINTDLG** **true** zurückgibt, legt die Funktion eines dieser Flags fest, um die Auswahl des Benutzers anzugeben. Wenn **PD \_ pagenums** festgelegt ist, enthalten die Member **nfrompage** und **ntopage** der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur die vom Benutzer angegebenen Start-und Endseiten. Zum Deaktivieren des Options Felds **Seiten** und der zugehörigen Elemente und **zum** bearbeiten **von** Steuerelementen legen Sie das Flag " **PD \_ nopagenums** " fest. Um das Optionsfeld **Auswahl** zu deaktivieren, legen Sie das Flag **PD \_ NoSelection** fest.

Das Dialogfeld enthält ein Bearbeitungs Steuerelement, in dem der Benutzer die Anzahl der zu druckenden Kopien eingeben kann. Wenn der **hDevMode** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur nicht **null** ist, gibt der **dmkopien** -Member der-Struktur den Anfangswert für dieses Bearbeitungs Steuerelement an. Wenn **hDevMode** **null** ist, gibt der **nkopien** -Member der **PRINTDLG** -Struktur den Anfangswert an. Wenn [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) zurückgibt, gibt **nkopien** in der Regel die Anzahl der Kopien an, die vom Benutzer angegeben werden. Wenn Sie jedoch das Flag " **PD \_ usedevmudecopiesandcollate** " beim Erstellen des Dialog Felds festlegen, wird **nkopien** bei Rückgabe immer auf 1 festgelegt, und der **dmkopien** -Member von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) gibt die Anzahl der zu druckenden Kopien an.

Das Kontrollkästchen **COLLATE** gibt an, ob der Benutzer die Seiten anordnen möchte, wenn mehrere Kopien gedruckt werden. Das Flag " **PD \_ COLLATE** " wird festgelegt, wenn **das Kontrollkästchen** "sortieren" ausgewählt ist. Wenn Ihre Anwendung mehrere Kopien oder eine simulierte Sortierung nicht unterstützt, legen Sie das Flag " **PD \_ usedevmudecopiesandcollate** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur fest. Dadurch **wird das Kontroll** Kästchen sortieren und das Bearbeitungs Steuerelement **für Kopien** deaktiviert, es sei denn, der Druckertreiber unterstützt mehrere Kopien und Sortierungen.

Das Kontrollkästchen **in Datei drucken** gibt an, ob der Benutzer die Ausgabe an eine Datei anstatt an einen Drucker senden möchte. Sie können das Flag **" \_ printdefile** " festlegen, sodass das Kontrollkästchen anfänglich aktiviert ist. Um das Kontrollkästchen auszublenden, legen Sie das Flag für die Flag " **\_ hideprintdefile** " fest. Legen Sie das Flag " **\_ disableprintdefile** " fest, um es zu deaktivieren. Wenn der Benutzer die Option **in Datei drucken** auswählt, legt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) das Flag " **\_ PrintToFile** " fest und gibt "file:" an dem Offset zurück, der durch den **woutputoffset** -Member der [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Struktur angegeben wird. Wenn Sie die Funktion zum Starten des Druckvorgangs aufzurufen, geben Sie diese "file:"-Zeichenfolge im **lpszoutput** -Member der-Struktur an. Das Angeben dieser Zeichenfolge bewirkt, dass das Druck Subsystem den Benutzer nach dem Namen der Ausgabedatei abfragt.

Standardmäßig zeigt das Dialogfeld **Drucken** zunächst Informationen zum aktuellen Standarddrucker an. Um Informationen für einen anderen installierten Drucker anzuzeigen, initialisieren Sie eine-Struktur und eine [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Struktur, und weisen Sie der-Struktur die globalen Speicher Handles für die Member **hDevMode** und **hDevNames** zu. Der Gerätename, den Sie im **dmdevicename** -Element der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur und im **wdriveroffset** -Member der **DEVNAMES** -Struktur angeben, muss ein Druckergerät identifizieren, das auch im \[ Abschnitt "Geräte" \] der Win.ini Datei aufgeführt ist. Wenn das Gerät nicht aufgeführt ist, gibt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) einen Fehler zurück.

Sie können [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) anweisen, einen Gerätekontext oder Informations Kontext für den Drucker zu erstellen, indem Sie das Flag **PD \_ returndc** oder **PD \_ returnic** im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur festlegen. Die-Funktion gibt ein Handle für den Gerätekontext oder Informations Kontext im **hdc** -Member zurück. Wenn Sie das Flag " **PD \_ returndc** " verwenden, können Sie den Gerätekontext verwenden, um die Ausgabe für den Drucker zu generieren.

Wenn Sie Informationen zum Standarddrucker abrufen möchten, ohne das Dialogfeld " **Drucken** " anzuzeigen, legen Sie das Flag " **PD \_ returndefault** " fest. In diesem Fall gibt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) sofort nach dem Festlegen der Member **hDevMode** und **hDevNames** auf Handles für Strukturen zurück, die die Informationen enthalten.

Standardmäßig zeigt [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Meldungs Felder an, wenn Fehler auftreten. Die-Funktion zeigt z. b. eine Fehlermeldung an, wenn keine Drucker installiert sind. Um zu verhindern, dass die Funktion diese Warnmeldungen anzeigt, legen Sie das Flag **PD \_ NoWarning** fest.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Anpassen des Dialog Felds "Drucken"](#customizing-the-print-dialog-box)
-   [Dialog Feld "Druck Setup"](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Anpassen des Dialog Felds "Drucken"

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld " **Drucken** " bereitstellen, z. b. Wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion verwendet anstelle der Standardvorlage Ihre benutzerdefinierte Vorlage.

So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld " **Drucken** " bereit:

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei prnsetup. DLG angegebene Standardvorlage ändern. Die in der standardmäßigen **Druck** Dialogfeld Vorlage verwendeten Steuerelement-IDs werden in der Datei "Dlgs. h" definiert.
2.  Verwenden Sie die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das Flag " **\_ enableprinttemplate** " im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lpprinttemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das Flag " **\_ enableprinttemplatehandle** " für PD fest. Verwenden Sie den **hprinttemplate** -Member, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**printhookproc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) -Hook-Prozedur für das Dialogfeld " **Drucken** " bereitstellen. Die Hook-Prozedur kann an das Dialogfeld gesendete Nachrichten verarbeiten. Es kann auch Nachrichten an das Dialogfeld senden. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hook-Prozedur bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten.

So aktivieren Sie eine Hook-Prozedur für das Dialogfeld " **Drucken** ":

1.  Legen Sie das Flag " **PD \_ enableprinthook** " im **Flags** -Member der [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnprinthook** -Member an.

Nach der Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung sendet die Dialogfeld Prozedur eine " **WM \_ InitDialog** "-Meldung an die Hook-Prozedur. Der *LPARAM* -Parameter dieser Nachricht ist ein Zeiger auf die [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) -Struktur, die verwendet wird, um das Dialogfeld zu initialisieren.

## <a name="print-setup-dialog-box"></a>Dialog Feld "Druck Setup"

Sie können ein **Druck Installations** Dialogfeld erstellen und anzeigen, indem Sie in einem Aufrufen der [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) -Funktion das Flag " **PD \_ printsetup** " festlegen. Das Dialogfeld **Druck Setup** wurde jedoch durch das Dialogfeld **Seite einrichten** abgelöst und sollte in neuen Anwendungen nicht verwendet werden.

Die folgenden Flags gelten nur für das **Druck Installations** Dialogfeld:

-   **PD \_ enablesetuphook**
-   **PD \_ enablesetuptemplate**
-   **PD \_ enablesetuptemplatehandle**

 

 