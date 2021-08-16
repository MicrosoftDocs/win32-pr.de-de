---
title: Dialogfelder "Suchen und Ersetzen"
description: Zeigt ein modusloses Dialogfeld an, in dem der Benutzer eine zeichenfolge angeben kann, nach der gesucht werden soll, sowie Optionen, die beim Suchen nach Text in einem Dokument verwendet werden sollen.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche,Common Dialog Box Library
- Benutzereingabe, Common Dialog Box Library
- Erfassen von Benutzereingaben, Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Suchen (Dialogfeld)
- Ersetzen (Dialogfeld)
- Anpassen des Dialogfelds "Suchen"
- Anpassen des Dialogfelds "Ersetzen"
- Vordefinierte Dialogfelder
- Dialogfelder, Suchen
- Dialogfelder,Ersetzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59bc5da5a8780a4f08bbf4bf757e1703d8d9120fdefe9d1730e515ffc6feae40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503487"
---
# <a name="find-and-replace-dialog-boxes"></a>Dialogfelder "Suchen und Ersetzen"

Zeigt ein modusloses Dialogfeld an, in dem der Benutzer eine zeichenfolge angeben kann, nach der gesucht werden soll, sowie Optionen, die beim Suchen nach Text in einem Dokument verwendet werden sollen. Im Dialogfeld **Ersetzen** können Benutzer eine zeichenfolge angeben, nach der gesucht werden soll, und eine Ersatzzeichenfolge sowie Optionen zum Steuern des Vorgangs.

Sie erstellen ein Dialogfeld **Suchen** und zeigen es an, indem Sie eine [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) initialisieren und die Struktur an die [**FindText-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) übergeben. Die folgende Abbildung zeigt ein typisches Dialogfeld **Suchen.**

![Dialogfeld "Suchen"](images/finddialogboxxp.png)

Sie erstellen und zeigen ein Dialogfeld **Ersetzen an,** indem Sie eine [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) initialisieren und die Struktur an die [**ReplaceText-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) übergeben. Die folgende Abbildung zeigt ein typisches Dialogfeld **Ersetzen.**

![Dialogfeld "Ersetzen"](images/replacedialogboxxp.png)

Im Gegensatz zu anderen gängigen Dialogfeldern sind die Dialogfelder **Suchen** und **Ersetzen** moduslos. Mit einem moduslosen Dialogfeld kann der Benutzer zwischen dem Dialogfeld und dem Fenster wechseln, in dem es erstellt wurde. Dies ist nützlich, damit der Benutzer nach einer Zeichenfolge suchen, zum Anwendungsfenster wechseln kann, um an der Zeichenfolge zu arbeiten, und wieder zum Dialogfeld wechseln kann, um nach einer anderen Zeichenfolge zu suchen, ohne den Zum Öffnen des Dialogfelds erforderlichen Befehl zu wiederholen.

Wenn die [**FindText-**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) oder [**ReplaceText-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) das Dialogfeld erfolgreich erstellt, wird ein Handle für das Dialogfeld zurückgegeben. Sie können dieses Handle verwenden, um das Dialogfeld zu verschieben und mit diesem zu kommunizieren. Wenn die Funktion das Dialogfeld nicht erstellen kann, gibt sie **NULL** zurück. Sie können die Ursache eines Fehlers ermitteln, indem Sie die [**CommDlgExtendedError-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) aufrufen, um den erweiterten Fehlerwert abzurufen.

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Die registrierte FINDMSGSTRING-Nachricht](#the-findmsgstring-registered-message)
-   [Anpassen des Dialogfelds "Suchen oder Ersetzen"](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Die registrierte FINDMSGSTRING-Nachricht

Vor dem Erstellen eines Dialogfelds **Suchen** oder **Ersetzen** müssen Sie die [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) aufrufen, um einen Nachrichtenbezeichner für die registrierte [**FINDMSGSTRING-Nachricht**](findmsgstring.md) abzurufen. Anschließend können Sie den Bezeichner verwenden, um über das Dialogfeld gesendete Nachrichten zu erkennen und zu verarbeiten. Wenn der Benutzer in einem Dialogfeld auf die Schaltfläche **Weiter suchen,** **Ersetzen** oder **Alle ersetzen** klickt, sendet die Dialogfeldprozedur eine **FINDMSGSTRING-Meldung** an die Fensterprozedur des Besitzerfensters. Wenn Sie das Dialogfeld erstellen, identifiziert das **Element hwndOwner** der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) das Besitzerfenster.

Der *lParam-Parameter* einer [**FINDMSGSTRING-Nachricht**](findmsgstring.md) ist ein Zeiger auf die [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) die Sie beim Erstellen des Dialogfelds angegeben haben. Vor dem Senden der Nachricht legt das Dialogfeld die Member dieser Struktur mit der neuesten Benutzereingabe fest, einschließlich der zu suchenden Zeichenfolge, der Ersatzzeichenfolge (falls vorhanden) und der Optionen für den Such- und Ersetzungsvorgang.

In einer [**FINDMSGSTRING-Nachricht**](findmsgstring.md) enthält der **Flags-Member** der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) eines der folgenden Flags, um das Ereignis anzugeben, das die Nachricht verursacht hat.



| Flag               | Bedeutung                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | Das Dialogfeld wird geschlossen. Nachdem das Besitzerfenster diese Meldung verarbeitet hat, ist ein Handle für das Dialogfeld nicht mehr gültig.                                                                                    |
| **FR \_ FINDNEXT**   | Der Benutzer hat in einem Dialogfeld **Suchen** oder **Ersetzen** auf die Schaltfläche **Weiter** suchen geklickt. Der **lpstrFindWhat-Member** gibt die zeichenfolge an, nach der gesucht werden soll.                                                         |
| **FR \_ REPLACE**    | Der Benutzer hat in einem Dialogfeld **Ersetzen** auf die Schaltfläche **Ersetzen** geklickt. Der **lpstrFindWhat-Member** gibt die zu ersetzende Zeichenfolge an, und der **lpstrReplaceWith-Member** gibt die Ersetzungszeichenfolge an.     |
| **FR \_ REPLACEALL** | Der Benutzer hat in einem Dialogfeld Ersetzen auf die Schaltfläche **Alle** **ersetzen** geklickt. Der **lpstrFindWhat-Member** gibt die zu ersetzende Zeichenfolge an, und der **lpstrReplaceWith-Member** gibt die Ersetzungszeichenfolge an. |



 

Für eine Meldung **"Weiter suchen"** oder **"Alle ersetzen"** kann der **Flags-Member** eine beliebige Kombination der folgenden Flags enthalten, um die Suchoptionen anzugeben.



| Flag              | Bedeutung                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN**      | Wenn diese Option festgelegt ist, wird die Schaltfläche **Nach unten** der Optionsfelder für die Richtung ausgewählt, die angibt, dass der Benutzer vom aktuellen Speicherort bis zum Ende des Dokuments suchen möchte. Wenn **FR \_ DOWN** nicht festgelegt ist, wird die Schaltfläche **Nach oben** ausgewählt, damit der Benutzer bis zum Anfang des Dokuments suchen möchte.       |
| **FR \_ MATCHCASE** | Wenn dieses  Kontrollkästchen festgelegt ist, ist das Kontrollkästchen Groß-/Kleinschreibung abgleichen aktiviert, das angibt, dass bei der Suche die Groß-/Kleinschreibung beachtet werden soll. Wenn **FR \_ MATCHCASE** nicht festgelegt ist, wird das Kontrollkästchen deaktiviert, sodass bei der Suche die Groß-/Kleinschreibung nicht beachtet werden kann.                                                                       |
| **FR \_ WHOLEWORD** | Wenn diese Option festgelegt ist, ist das Kontrollkästchen **Nur ganzes Wort** abgleichen aktiviert, das angibt, dass der Benutzer nur nach ganzen Wörtern suchen möchte, die mit der Suchzeichenfolge übereinstimmen. Wenn **FR \_ WHOLEWORD** nicht festgelegt ist, ist das Kontrollkästchen deaktiviert, sodass Sie auch nach Wortfragmenten suchen sollten, die mit der Suchzeichenfolge übereinstimmen. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Anpassen des Dialogfelds "Suchen oder Ersetzen"

Zum Anpassen eines Dialogfelds **Suchen** oder **Ersetzen** können Sie eine der folgenden Methoden verwenden:

-   Angeben von Werten in der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) beim Erstellen des Dialogfelds
-   Bereitstellen einer benutzerdefinierten Vorlage
-   Bereitstellen einer Hookprozedur

Wenn Sie ein Dialogfeld **Suchen** oder **Ersetzen** erstellen, können Sie Flags im **Flags-Member** der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) festlegen, um eines der Steuerelemente für Suchoptionen auszublenden oder zu deaktivieren. Sie können z. B. das FR \_ NOMATCHCASE-Flag festlegen, um das **Kontrollkästchen Übereinstimmungsfall** zu deaktivieren, oder das FR \_ HIDEMATCHCASE-Flag festlegen, um es auszublenden.

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld **Suchen** oder **Ersetzen** bereitstellen, wenn Sie beispielsweise zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**Funktionen FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) und [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) verwenden Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für ein Dialogfeld Suchen oder Ersetzen bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Findtext.dlg angegebene Standardvorlage ändern. Die Steuerelementbezeichner, die in der Standarddialogvorlage **Suchen** oder **Ersetzen** verwendet werden, werden in der Datei Dlgs.h definiert.
2.  Verwenden Sie die [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) um die Vorlage wie folgt zu aktivieren:
    -   -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das FR \_ ENABLETEMPLATE-Flag im **Flags-Member** fest. Verwenden Sie die Member **hInstance** und **lpTemplateName** der Struktur, um den Modul- und Ressourcennamen zu identifizieren.

            -Oder-

        -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das FR \_ ENABLETEMPLATEHANDLE-Flag fest. Verwenden Sie den **Member hInstance,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**FRHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) für ein Dialogfeld **Suchen** oder **Ersetzen** bereitstellen. Die Hookprozedur kann Nachrichten verarbeiten, die an das Dialogfeld gesendet werden. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hookprozedur zum Verarbeiten von Eingaben für Ihre Steuerelemente bereitstellen.

**So aktivieren Sie eine Hookprozedur für das Dialogfeld Suchen oder Ersetzen**

1.  Legen Sie das FR \_ ENABLEHOOK-Flag im **Flags-Member** der [**FINDREPLACE-Struktur**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) fest.
2.  Geben Sie die Adresse der Hookprozedur im **lpfnHook-Member** an.

Nach der Verarbeitung der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sendet die Dialogfeldprozedur eine **WM \_ INITDIALOG-Nachricht** an die Hookprozedur. Der *lParam-Parameter* dieser Nachricht ist ein Zeiger auf die [**FINDREPLACE-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) die zum Initialisieren des Dialogfelds verwendet wird.

Wenn die Hookprozedur **FALSE** als Antwort auf die [**WM \_ INITDIALOG-Meldung**](wm-initdialog.md) zurückgibt, wird das Dialogfeld nur angezeigt, wenn es in der Hookprozedur angezeigt wird. Führen Sie hierzu zunächst andere Farbvorgänge aus, und rufen Sie dann die Funktionen [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) und [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) auf. Der folgende Code veranschaulicht dies:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 