---
title: Dialog Felder suchen und ersetzen
description: Zeigt ein nicht modalen Dialogfeld an, in dem der Benutzer eine zu suchende Zeichenfolge angeben kann, sowie Optionen, die bei der Suche nach Text in einem Dokument verwendet werden sollen.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, allgemeine Dialog Feld Bibliothek
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Suchen (Dialogfeld)
- Ersetzen (Dialogfeld)
- Dialogfeld "suchen"
- Dialogfeld "ersetzen" anpassen
- vordefinierte Dialogfelder
- Dialogfelder, suchen
- Dialogfelder, ersetzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104560913"
---
# <a name="find-and-replace-dialog-boxes"></a>Dialog Felder suchen und ersetzen

Zeigt ein nicht modalen Dialogfeld an, in dem der Benutzer eine zu suchende Zeichenfolge angeben kann, sowie Optionen, die bei der Suche nach Text in einem Dokument verwendet werden sollen. Im Dialogfeld **ersetzen** können Benutzer eine Zeichenfolge, die gesucht werden soll, und eine Ersatz Zeichenfolge sowie Optionen zum Steuern des Vorgangs angeben.

Sie erstellen und zeigen ein Dialogfeld **Suchen** an, indem Sie eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur initialisieren und die Struktur an die [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) -Funktion übergeben. Die folgende Abbildung zeigt ein typisches Dialogfeld **Suchen** .

![Suchen (Dialogfeld)](images/finddialogboxxp.png)

Sie erstellen und zeigen ein **Ersetzungs** Dialogfeld an, indem Sie eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur initialisieren und die Struktur an die [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) -Funktion übergeben. Die folgende Abbildung zeigt ein typisches Dialogfeld zum **ersetzen** .

![Ersetzen (Dialogfeld)](images/replacedialogboxxp.png)

Anders als bei anderen allgemeinen Dialogfeldern sind die Dialogfelder **Suchen** und **ersetzen** nicht modelliert. Ein nicht modalem Dialogfeld ermöglicht dem Benutzer das Wechseln zwischen dem Dialogfeld und dem Fenster, in dem es erstellt wurde. Dies ist hilfreich, wenn der Benutzer nach einer Zeichenfolge suchen, zum Anwendungsfenster wechseln soll, um an der Zeichenfolge zu arbeiten, und zurück zum Dialogfeld wechseln, um nach einer anderen Zeichenfolge zu suchen, ohne den Befehl zu wiederholen, der zum Öffnen des Dialog Felds erforderlich ist.

Wenn das Dialogfeld von der [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) -oder der [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) -Funktion erfolgreich erstellt wurde, wird ein Handle für das Dialogfeld zurückgegeben. Sie können dieses Handle verwenden, um das Dialogfeld zu verschieben und mit ihm zu kommunizieren. Wenn die Funktion das Dialogfeld nicht erstellen kann, wird **null** zurückgegeben. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**kommdlgextendederror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion aufrufen, um den erweiterten Fehlerwert abzurufen.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Die registrierte Meldung "findmsgstring"](#the-findmsgstring-registered-message)
-   [Anpassen des Dialog Felds "suchen und ersetzen"](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Die registrierte Meldung "findmsgstring"

Bevor Sie ein Dialogfeld **Suchen** oder **ersetzen** erstellen, müssen Sie die [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufrufen, um eine Nachrichten-ID für die registrierte [**findmsgstring**](findmsgstring.md) -Nachricht zu erhalten. Anschließend können Sie den Bezeichner verwenden, um über das Dialogfeld gesendete Nachrichten zu erkennen und zu verarbeiten. Wenn der Benutzer auf die Schaltfläche **weiter suchen**, **ersetzen** oder **Alle ersetzen** in einem Dialogfeld klickt, sendet die Dialogfeld Prozedur eine **findmsgstring** -Meldung an die Fenster Prozedur des Besitzer Fensters. Wenn Sie das Dialogfeld erstellen, identifiziert das **hwndOwner** -Element der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur das Besitzer Fenster.

Der *LPARAM* -Parameter einer [**findmsgstring**](findmsgstring.md) -Nachricht ist ein Zeiger auf die [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, die Sie beim Erstellen des Dialog Felds angegeben haben. Vor dem Senden der Nachricht werden im Dialogfeld die Elemente dieser Struktur mit der aktuellen Benutzereingabe festgelegt, einschließlich der zu suchenden Zeichenfolge, der Ersetzungs Zeichenfolge (sofern vorhanden) und der Optionen für den Such-und Ersetzungs Vorgang.

In einer [**findmsgstring**](findmsgstring.md) -Nachricht enthält der **Flags** -Member der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur eines der folgenden Flags, um das Ereignis anzugeben, das die Meldung verursacht hat.



| Flag               | Bedeutung                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dialog-Begriff "fr" \_** | Das Dialogfeld wird geschlossen. Nachdem das Besitzer Fenster diese Nachricht verarbeitet hat, ist ein Handle für das Dialogfeld nicht mehr gültig.                                                                                    |
| **Fr \_ FindNext**   | Der Benutzer hat auf die Schaltfläche " **weiter suchen** " im Dialogfeld " **Suchen** oder **ersetzen** " geklickt. Der **lpstraufindwhat** -Member gibt die zu suchende Zeichenfolge an.                                                         |
| **Fr \_ ersetzen**    | Der Benutzer hat im Dialogfeld " **ersetzen** " auf die Schaltfläche " **ersetzen** " geklickt. Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an     |
| **Fr \_ ReplaceAll** | Der Benutzer hat auf die Schaltfläche **Alle ersetzen** im Dialogfeld **ersetzen** geklickt. Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an |



 

Für eine " **weiter** suchen"-oder " **Alle ersetzen** "-Meldung kann der **Flags** -Member eine beliebige Kombination der folgenden Flags einschließen, um die Suchoptionen anzugeben.



| Flag              | Bedeutung                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ nach unten**      | Wenn festgelegt, wird die Schaltfläche **nach unten** der Optionsfeld Richtung ausgewählt und gibt an, dass der Benutzer von der aktuellen Position bis zum Ende des Dokuments suchen möchte. Wenn die Option " **\_ nach unten** " nicht festgelegt ist, wird die Schaltfläche "nach **oben** " ausgewählt, sodass der Benutzer am Anfang des Dokuments suchen möchte.       |
| **Fr \_ MatchCase** | Wenn dieses Kontrollkästchen aktiviert ist, ist das Kontrollkästchen Groß- **/Kleinschreibung** aktivieren aktiviert. Dies bedeutet, dass der Benutzer die Groß-/Kleinschreibung beachtet Wenn **fr \_ MatchCase** nicht festgelegt ist, wird das Kontrollkästchen deaktiviert, sodass bei der Suche die Groß-/Kleinschreibung nicht beachtet werden kann.                                                                       |
| **"# \_ wholeword"** | Wenn festgelegt, wird das Kontrollkästchen **Nur ganzes Wort** suchen aktiviert, das angibt, dass der Benutzer nur nach ganzen Wörtern suchen möchte, die der Such Zeichenfolge entsprechen. Wenn **fr \_ wholeword** nicht festgelegt ist, ist das Kontrollkästchen deaktiviert, sodass Sie auch nach Wortfragmenten suchen müssen, die der Such Zeichenfolge entsprechen. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Anpassen des Dialog Felds "suchen und ersetzen"

Um das Dialogfeld **Suchen** oder **ersetzen** anzupassen, können Sie eine der folgenden Methoden verwenden:

-   Werte in der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur angeben, wenn Sie das Dialogfeld erstellen
-   Bereitstellen einer benutzerdefinierten Vorlage
-   Bereitstellen einer Hook-Prozedur

Wenn **Sie ein Dialogfeld Suchen oder** **ersetzen** erstellen, können Sie Flags im **Flags** -Member der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur festlegen, um die Steuerelemente der Suchoption auszublenden oder zu deaktivieren. Beispielsweise können Sie das Flag "fr \_ nomatchcase" festlegen, um das Kontrollkästchen Groß- **/Kleinschreibung** zu deaktivieren, oder das Flag "fr \_ hidematchcase" festlegen, um es auszublenden.

Sie **können eine Benutzer** definierte Vorlage für ein Dialogfeld Suchen oder **ersetzen** bereitstellen, z. b. Wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die Funktionen " [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) " und " [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) " verwenden Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für ein Dialogfeld "Suchen oder ersetzen" bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei FindText. DLG angegebene Standardvorlage ändern. Die in der Standard Dialogfeld für **Suchen** oder **ersetzen** verwendeten Steuerelement-IDs werden in der Datei "Dlgs. h" definiert.
2.  Verwenden Sie die [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, um die Vorlage wie folgt zu aktivieren:
    -   -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das \_ Flag "ENABLETEMPLATE" für das FR-Flag im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.

            -Oder-

        -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das \_ Flag "enabletemplatehandle" für FR fest. Verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**frhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) -Hook-Prozedur für ein Dialogfeld " **Suchen** " oder " **ersetzen** " bereitstellen. Die Hook-Prozedur kann an das Dialogfeld gesendete Nachrichten verarbeiten. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hook-Prozedur bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten.

**So aktivieren Sie eine Hook-Prozedur für ein Dialogfeld "suchen" oder "ersetzen"**

1.  Legen Sie das \_ Flag für die FR-ENABLEHOOK im **Flags** -Member der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnhook** -Member an.

Nach der Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung sendet die Dialogfeld Prozedur eine " **WM \_ InitDialog** "-Meldung an die Hook-Prozedur. Der *LPARAM* -Parameter dieser Nachricht ist ein Zeiger auf die [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, die verwendet wird, um das Dialogfeld zu initialisieren.

Wenn die Hook-Prozedur in Reaktion auf die [**WM \_ InitDialog**](wm-initdialog.md) -Nachricht **false** zurückgibt, wird das Dialogfeld nicht angezeigt, es sei denn, die Hook-Prozedur zeigt es an. Führen Sie zu diesem Zweck zunächst alle anderen Zeichnungsvorgänge aus, und nennen Sie dann die Funktionen [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) und [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) . Der folgende Code veranschaulicht dies:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 