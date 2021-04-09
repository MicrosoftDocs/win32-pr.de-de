---
title: Seite einrichten (Dialogfeld)
description: Zeigt ein modales Dialogfeld an, in dem der Benutzereinstellungen auswählen kann, die den Papiertyp, die Papier Quelle, die Seitenausrichtung und die Breite der Seitenränder einschließen.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, allgemeine Dialog Feld Bibliothek
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Seite einrichten (Dialogfeld)
- Dialogfeld "Seite einrichten" anpassen
- Hooks, Dialogfeld "Seite einrichten"
- vordefinierte Dialogfelder
- Dialogfelder, Seite einrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102299"
---
# <a name="page-setup-dialog-box"></a>Seite einrichten (Dialogfeld)

Zeigt ein modales Dialogfeld an, in dem der Benutzer die folgenden Attribute der gedruckten Seite festlegen kann:

-   Der Papiertyp (Umschlag, rechts, Buchstabe usw.)
-   Die Papier Quelle (manueller Feed, Traktoren Feed, Blatt Anleger usw.)
-   Die Seitenausrichtung (Hochformat oder Querformat)
-   Die Breite der Seitenränder.

Sie erstellen und zeigen ein Dialogfeld für die **Seiten Einrichtung** an, indem Sie eine [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur initialisieren und die Struktur an die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion übergeben. Die im Dialogfeld dargestellten Attribute variieren jedoch je nach den Funktionen des Druckers. Die folgende Abbildung zeigt ein typisches Dialogfeld für die **Seiten Einrichtung** .

![Dialogfeld "Seite einrichten"](images/pagesetupdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) **true** zurück, nachdem verschiedene Member in der [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur festgelegt wurden, um die Auswahl des Benutzers anzugeben. Die **ptpapersize** -und **rtmargin** -Elemente enthalten die Werte, die vom Benutzer angegeben werden. Die Member **hDevMode** und **hDevNames** enthalten globale Speicher Handles für die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -und [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Strukturen. Diese Strukturen enthalten zusätzliche Seiten Informationen sowie Informationen über den Drucker. Mit diesen Informationen können Sie die Ausgabe vorbereiten, die an den ausgewählten Drucker gesendet werden soll.

Wenn der Benutzer das Dialogfeld **Seite einrichten** abbricht oder ein Fehler auftritt, gibt [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) den Wert **false** zurück. Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**kommdlgextendecoderror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion auf, um den erweiterten Fehlerwert abzurufen.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Das Dialog Feld "Seite einrichten" wird initialisiert.](#initializing-the-page-setup-dialog-box)
-   [Anpassen des Dialog Felds "Seite einrichten"](#customizing-the-page-setup-dialog-box)
-   [Anpassen der Beispielseite](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Das Dialog Feld "Seite einrichten" wird initialisiert.

Standardmäßig werden im Dialogfeld **Seite einrichten** Informationen zum aktuellen Standarddrucker angezeigt. Um das Dialogfeld anzuweisen, Informationen zu einem bestimmten Drucker anzuzeigen, legen Sie die Elemente einer [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -oder [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) -Struktur fest, und weisen Sie die globalen Speicher Handles dieser Strukturen dem entsprechenden Member in [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)zu. Wenn Sie den Namen eines Druckers angeben, der zurzeit nicht installiert ist, wird im Dialogfeld eine Fehlermeldung angezeigt. Verwenden Sie den Wert " **PSD \_ NoWarning** ", um zu verhindern, dass das Dialogfeld Fehlermeldungen anzeigt. Wenn Sie Informationen zum Standarddrucker abrufen möchten, ohne das Dialogfeld **Seite einrichten** anzuzeigen, verwenden Sie den Wert von " **PSD \_ returndefault** ".

Wenn das Standard Messsystem Zoll ist, verwendet das Dialogfeld Tausendstel Zoll als Standard Maßeinheit. Wenn das Standard Messungs System eine Metrik ist, werden im Dialogfeld Hundertstel Millimeter als Standard Maßeinheit verwendet. Wenn Sie die Standard Maßeinheit überschreiben möchten, legen Sie das-Flag " **PSD \_ inhundertstel thsofmillimeter** " oder " **PSD \_ intausendandthsofinches** " im **Flags** -Member der [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur fest.

Die Anfangswerte für die Ränder sind standardmäßig 1 Zoll. Wenn Sie das Flag für die **PSD- \_ Ränder** festlegen, werden im Dialogfeld die anfänglichen Rand Werte angezeigt, die im **rtmargin** -Element angegeben sind. Die Standard minimalen Werte, die der Benutzer für die Ränder angeben kann, sind die vom Drucker zulässigen minimalen Ränder. Wenn Sie das **PSD \_ minmargin** -Flag festlegen, werden im Dialogfeld die im **rtminmargin** -Member angegebenen minimalen Ränder erzwungen.

Um zu verhindern, dass Benutzer bestimmte Optionen auswählen, legen Sie eine beliebige Kombination der folgenden Flags fest, um die entsprechenden Steuerelemente zu deaktivieren.



| Flag                        | Bedeutung                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD- \_ Deaktivierungs Ränder**     | Deaktiviert die Bearbeitungs Steuerelemente, in denen der Benutzer die Rand Einstellungen eingibt. |
| **PSD- \_ disableorientation** | Deaktiviert **die Options** Felder "Hochformat" und " **quer** Format".               |
| **PSD- \_ disablepaper**       | Deaktiviert die Steuerelemente zum Auswählen des Papier Umfangs und der Papier Quelle.     |
| **PSD \_ disableprinter**     | Deaktiviert die Schaltfläche **Drucker** .                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Anpassen des Dialog Felds "Seite einrichten"

Sie können für das Dialogfeld **Seite einrichten** eine benutzerdefinierte Vorlage bereitstellen, z. b. Wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion verwendet anstelle der Standardvorlage Ihre benutzerdefinierte Vorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld "Seite einrichten" bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei prnsetup. DLG angegebene Standardvorlage ändern. Die Steuerelement-IDs, die in der standardmäßigen **Seite Setup** -Dialogfeld Vorlage verwendet werden, werden in der Datei Dlgs. h definiert.
2.  Verwenden Sie die [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur, um die Vorlage wie folgt zu aktivieren:
    -   -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das " **PSD \_ enablepagesetuptemplate** "-Flag im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lppagesetuptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.

            -Oder-

        -   Wenn die benutzerdefinierte Vorlage bereits im Arbeitsspeicher vorhanden ist, legen Sie das Flag " **\_ enablepagesetuptemplatehandle** " für PSD fest. Verwenden Sie den Member **hpagesetuptemplate** , um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

Zum Filtern von Nachrichten, die an die Dialogfeld Prozedur gesendet werden, können Sie eine [**pgesetuphook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) -Hook-Prozedur bereitstellen. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine **pgesetuphook** -Hook-Prozedur bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten. Außerdem können Sie eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Inhalte der Beispielseite anzupassen, die im Dialogfeld **Seite einrichten** angezeigt werden. Weitere Informationen zur **pagepainthook** -Hook-Prozedur finden Sie unter [Anpassen der Beispielseite](#customizing-the-sample-page).

**So aktivieren Sie eine pgesetuphook-Hook-Prozedur**

1.  Legen Sie das " **PSD \_ enablepagesetuphook** "-Flag im **Flags** -Member der [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnbingesetuphook** -Member an.

Nach der Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung sendet die Dialogfeld Prozedur eine " **WM \_ InitDialog** "-Meldung an die " [**pgesetuphook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) "-Hook-Prozedur. Der *LPARAM* -Parameter dieser Nachricht ist ein Zeiger auf die [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur, die verwendet wird, um das Dialogfeld zu initialisieren.

## <a name="customizing-the-sample-page"></a>Anpassen der Beispielseite

Das Dialogfeld **Seite einrichten** enthält ein Bild einer Beispielseite, das zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Das Bild besteht aus einem Rechteck, das das ausgewählte Papier oder den Umschlag Typ darstellt, mit einem gepunkteten Linien Rechteck, das die aktuellen Ränder darstellt, und partiellen (griechischen Text) Zeichen, um anzuzeigen, wie Text auf der gedruckten Seite aussieht.

Wenn Sie die [**pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) -Funktion aufrufen, können Sie eine [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur bereitstellen, um die Darstellung der Beispielseite anzupassen.

**So aktivieren Sie eine pagepainthook-Hook-Prozedur**

1.  Legen Sie das " **PSD \_ enablepagepainthook** "-Flag im **Flags** -Member der [**pagesetupdlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnpagepainthook** -Member an.

Wenn im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, empfängt die Hook-Prozedur die folgenden Meldungen in der Reihenfolge, in der Sie aufgelistet sind.



| Nachricht                                                  | Bedeutung                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ PSD \_ pagesetupdlg**](wm-psd-pagesetupdlg.md)     | Im Dialogfeld wird die Beispielseite gezeichnet. Die Hook-Prozedur kann diese Nachricht verwenden, um das Zeichnen des Inhalts der Beispielseite vorzubereiten.     |
| [**WM- \_ PSD \_ fullpagerup**](wm-psd-fullpagerect.md)     | Im Dialogfeld wird die Beispielseite gezeichnet. Diese Meldung gibt das umgebende Rechteck der Beispielseite an.                               |
| [**WM- \_ PSD \_ minmarginrect**](wm-psd-minmarginrect.md)   | Im Dialogfeld wird die Beispielseite gezeichnet. Diese Meldung gibt das Rand Rechteck an.                                                    |
| [**WM \_ PSD \_ marginrect**](wm-psd-marginrect.md)         | Im Dialogfeld wird das Rand Rechteck gezeichnet.                                                                                            |
| [**WM- \_ PSD \_ greektextrect**](wm-psd-greektextrect.md)   | Im Dialogfeld wird der griechische Text innerhalb des Rand Rechtecks gezeichnet.                                                                      |
| [**WM- \_ PSD- \_ präct**](wm-psd-envstamprect.md)     | Das Dialogfeld wird gerade im Umschlag Stempel Rechteck einer Umschlag Beispielseite gezeichnet. Diese Meldung wird nur für Umschläge gesendet.             |
| [**WM- \_ PSD \_ yafullpagtory**](wm-psd-yafullpagerect.md) | Im Dialogfeld wird der Rückgabe Adress Teil einer Umschlag Beispielseite gezeichnet. Diese Meldung wird für Umschläge und andere Papiergrößen gesendet. |



 

Wenn die Hook-Prozedur für eine der ersten drei Nachrichten einer Zeichnungs Sequenz " **true** " zurückgibt ("[**WM \_ PSD \_ papdlg**](wm-psd-pagesetupdlg.md)", " [**WM \_ PSD \_ fullpagance"**](wm-psd-fullpagerect.md)oder " [**WM \_ PSD \_ minmarginrect**](wm-psd-minmarginrect.md)"), werden im Dialogfeld keine weiteren Nachrichten mehr angezeigt, und es wird erst dann auf der Beispielseite gezeichnet, wenn das System die Beispielseite neu zeichnen muss. Wenn die Hook-Prozedur für alle drei Nachrichten **false** zurückgibt, sendet das Dialogfeld die übrigen Nachrichten der Zeichnungs Sequenz.

Wenn die Hook-Prozedur für eine der verbleibenden Nachrichten in einer Zeichnungs Sequenz **true** zurückgibt, wird das Dialogfeld nicht den entsprechenden Teil der Beispielseite zeichnen. Wenn die Hook-Prozedur für eine dieser Nachrichten **false** zurückgibt, wird dieser Teil der Beispielseite im Dialogfeld gezeichnet.

Um zu verhindern, dass im Dialogfeld der Inhalt der Beispielseite gezeichnet wird, können Sie das " **PSD \_ disablepagedrawing** "-Flag festlegen. Dieses Flag wirkt sich nicht auf Ihre [**pagepainthook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) -Hook-Prozedur aus, die immer noch alle **WM- \_ PSD \_ \*** -Nachrichten empfängt und den Inhalt der Beispielseite zeichnen kann.

 

 