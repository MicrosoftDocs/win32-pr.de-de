---
title: Seite einrichten (Dialogfeld)
description: Zeigt ein modales Dialogfeld an, in dem der Benutzer Einstellungen auswählen kann, die den Papiertyp, die Papierquelle, die Seitenausrichtung und die Breite der Seitenränder enthalten.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche,Common Dialog Box Library
- Benutzereingabe, Common Dialog Box Library
- Erfassen von Benutzereingaben, Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Seite einrichten (Dialogfeld)
- Anpassen des Dialogfelds "Seiteneinrichtung"
- Hooks, Dialogfeld "Seiteneinrichtung"
- Vordefinierte Dialogfelder
- Dialogfelder,Seiteneinrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af64357be8bd39217c6527dc81f7ac426f5e06e183de92b3bb479f4633c75d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741654"
---
# <a name="page-setup-dialog-box"></a>Seite einrichten (Dialogfeld)

Zeigt ein modales Dialogfeld an, in dem der Benutzer die folgenden Attribute der gedruckten Seite festlegen kann:

-   Der Papiertyp (Umschlag, Recht, Buchstabe usw.)
-   Die Papierquelle (manueller Feed, Feed für Feed, Blattfeed usw.)
-   Seitenausrichtung (Hochformat oder Querformat)
-   Die Breite der Seitenränder

Sie erstellen und zeigen ein Dialogfeld **Seiteneinrichtung** an, indem Sie eine [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) initialisieren und die Struktur an die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) übergeben. Die im Dialogfeld angezeigten Attribute variieren jedoch abhängig von den Funktionen des Druckers. Die folgende Abbildung zeigt ein typisches Dialogfeld **"Seiteneinrichtung".**

![Dialogfeld "Seiteneinrichtung"](images/pagesetupdialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) **TRUE** zurück, nachdem verschiedene Member in der [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) festgelegt wurden, um die Auswahl des Benutzers anzugeben. Die **Member ptPaperSize** und **rtMargin** enthalten die vom Benutzer angegebenen Werte. Die Member **hDevMode** und **hDevNames** enthalten globale Speicherhandles für die [**DEVMODE-**](/windows/win32/api/wingdi/ns-wingdi-devmodea) und [**DEVNAMES-Strukturen.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Diese Strukturen enthalten zusätzliche Seiteninformationen sowie Informationen zum Drucker. Sie können diese Informationen verwenden, um die Ausgabe vorzubereiten, die an den ausgewählten Drucker gesendet werden soll.

Wenn der Benutzer das Dialogfeld **Seiteneinrichtung** abbricht oder ein Fehler auftritt, gibt [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) **FALSE** zurück. Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**CommDlgExtendedError-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) auf, um den erweiterten Fehlerwert abzurufen.

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Initialisieren des Dialogfelds "Seiteneinrichtung"](#initializing-the-page-setup-dialog-box)
-   [Anpassen des Dialogfelds "Seiteneinrichtung"](#customizing-the-page-setup-dialog-box)
-   [Anpassen der Beispielseite](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Initialisieren des Dialogfelds "Seiteneinrichtung"

Standardmäßig werden im Dialogfeld **Seiteneinrichtung** Informationen zum aktuellen Standarddrucker angezeigt. Um das Dialogfeld anzuweisen, Informationen zu einem bestimmten Drucker anzuzeigen, legen Sie die Member einer [**DEVMODE-**](/windows/win32/api/wingdi/ns-wingdi-devmodea) oder [**DEVNAMES-Struktur**](/windows/win32/api/commdlg/ns-commdlg-devnames) fest, und weisen Sie die globalen Speicherhandles dieser Strukturen dem entsprechenden Member in [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)zu. Wenn Sie den Namen eines Druckers angeben, der derzeit nicht installiert ist, wird im Dialogfeld eine Fehlermeldung angezeigt. Verwenden Sie den **PSD \_ NOWARNING-Wert,** um zu verhindern, dass das Dialogfeld Fehlermeldungen anzeigt. Verwenden Sie den **PSD \_ RETURNDEFAULT-Wert,** um Informationen zum Standarddrucker abzurufen, ohne das Dialogfeld **Seiteneinrichtung** anzuzeigen.

Wenn das Standardmessungssystem Zoll ist, verwendet das Dialogfeld Tausendstel Zoll als Standardeinheit für messungen. Wenn das Standardmessungssystem metrik ist, verwendet das Dialogfeld Hundertstel Millimeter als Standardeinheit für Messungen. Um die Standardeinheit der Messung zu überschreiben, legen Sie das **Flag PSD \_ INLAPPENREDTHSOFMILLIMETERS** oder **PSD \_ INTHOUSANDTHSOFINCHES** im **Flags-Element** der [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) fest.

Die Anfangswerte für die Ränder sind standardmäßig ein Zoll. Wenn Sie das **\_ PSD-MARGIN-Flag** festlegen, werden im Dialogfeld die anfänglichen Randwerte angezeigt, die im **rtMargin-Member** angegeben sind. Die Standardmindestwerte, die der Benutzer für die Ränder angeben kann, sind die minimalen Ränder, die vom Drucker zugelassen werden. Wenn Sie das **PSD \_ MINMARGINS-Flag** festlegen, erzwingt das Dialogfeld die minimalen Ränder, die im **rtMinMargin-Member** angegeben sind.

Um zu verhindern, dass Benutzer bestimmte Optionen auswählen, legen Sie eine beliebige Kombination der folgenden Flags fest, um die entsprechenden Steuerelemente zu deaktivieren.



| Flag                        | Bedeutung                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD \_ DISABLEMARGINS**     | Deaktiviert die Bearbeitungssteuerelemente, in denen der Benutzer die Randeinstellungen eingibt. |
| **PSD \_ DISABLEORIENTATION** | Deaktiviert die Optionsfelder **Hochformat** und **Querformat.**               |
| **PSD \_ DISABLEPAPER**       | Deaktiviert die Steuerelemente zum Auswählen von Papiergröße und Papierquelle.     |
| **PSD \_ DISABLEPRINTER**     | Deaktiviert die Schaltfläche **Drucker.**                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Anpassen des Dialogfelds "Seiteneinrichtung"

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld **Seiteneinrichtung** bereitstellen, wenn Sie beispielsweise zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) verwendet Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

**So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld "Seiteneinrichtung" bereit**

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Prnsetup.dlg angegebene Standardvorlage ändern. Die Steuerelementbezeichner, die in der Standardvorlage des **Dialogfelds Seiteneinrichtung** verwendet werden, werden in der Datei Dlgs.h definiert.
2.  Verwenden Sie die [**PAGESETUPDLG-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) um die Vorlage wie folgt zu aktivieren:
    -   -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **PSD \_ ENABLEPAGESETUPTEMPLATE-Flag** im **Flags-Member** fest. Verwenden Sie die Member **hInstance** und **lpPageSetupTemplateName** der Struktur, um den Modul- und Ressourcennamen zu identifizieren.

            -Oder-

        -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **PSD \_ ENABLEPAGESETUPTEMPLATEHANDLE-Flag** fest. Verwenden Sie den **Member hPageSetupTemplate,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

Zum Filtern von Nachrichten, die an die Dialogfeldprozedur gesendet werden, können Sie eine [**PageSetupHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) bereitstellen. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine **PageSetupHook-Hookprozedur** bereitstellen, um Eingaben für Ihre Steuerelemente zu verarbeiten. Darüber hinaus können Sie eine [**PagePaintHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) bereitstellen, um den Inhalt der Beispielseite anzupassen, die im Dialogfeld **Seiteneinrichtung** angezeigt wird. Weitere Informationen zur Hookprozedur **PagePaintHook** finden Sie unter [Anpassen der Beispielseite](#customizing-the-sample-page).

**So aktivieren Sie eine PageSetupHook-Hookprozedur**

1.  Legen Sie das **PSD \_ ENABLEPAGESETUPHOOK-Flag** im **Flags-Member** der [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) fest.
2.  Geben Sie die Adresse der Hookprozedur im **Member lpfnPageSetupHook** an.

Nach der Verarbeitung der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sendet die Dialogfeldprozedur eine **WM \_ INITDIALOG-Nachricht** an die Hookprozedur [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) Der *lParam-Parameter* dieser Nachricht ist ein Zeiger auf die [**PAGESETUPDLG-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) die zum Initialisieren des Dialogfelds verwendet wird.

## <a name="customizing-the-sample-page"></a>Anpassen der Beispielseite

Das Dialogfeld **Seiteneinrichtung** enthält ein Bild einer Beispielseite, die zeigt, wie sich die Auswahl des Benutzers auf die Darstellung der gedruckten Ausgabe auswirkt. Das Bild besteht aus einem Rechteck, das den ausgewählten Papier- oder Umschlagtyp darstellt, mit einem gepunkteten Rechteck, das die aktuellen Ränder darstellt, und partiellen Zeichen (griechischer Text), um zu zeigen, wie Text auf der gedruckten Seite aussieht.

Wenn Sie die [**PageSetupDlg-Funktion**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) aufrufen, können Sie eine [**PagePaintHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) bereitstellen, um die Darstellung der Beispielseite anzupassen.

**So aktivieren Sie eine PagePaintHook-Hookprozedur**

1.  Legen Sie das **PSD \_ ENABLEPAGEPAINTHOOK-Flag** im **Flags-Member** der [**PAGESETUPDLG-Struktur**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) fest.
2.  Geben Sie die Adresse der Hookprozedur im **Member lpfnPagePaintHook** an.

Wenn der Inhalt der Beispielseite im Dialogfeld gezeichnet werden soll, empfängt die Hookprozedur die folgenden Nachrichten in der Reihenfolge, in der sie aufgeführt sind.



| Nachricht                                                  | Bedeutung                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)     | Im Dialogfeld wird die Beispielseite gezeichnet. Die Hookprozedur kann diese Meldung verwenden, um das Zeichnen des Inhalts der Beispielseite vorzubereiten.     |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | Im Dialogfeld wird die Beispielseite gezeichnet. Diese Meldung gibt das umgrenzende Rechteck der Beispielseite an.                               |
| [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)   | Im Dialogfeld wird die Beispielseite gezeichnet. Diese Meldung gibt das Randrechteck an.                                                    |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | Im Dialogfeld wird das Randrechteck gezeichnet.                                                                                            |
| [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)   | Im Dialogfeld wird der griechisch-Text innerhalb des Randrechtecks gezeichnet.                                                                      |
| [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)     | Das Dialogfeld wird im Umschlagsstempelrechteck einer Umschlagbeispielseite gezeichnet. Diese Nachricht wird nur für Umschläge gesendet.             |
| [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md) | Im Dialogfeld wird der Rückgabeadressteil einer Umschlagbeispielseite gezeichnet. Diese Nachricht wird für Umschläge und andere Papiergrößen gesendet. |



 

Wenn die Hookprozedur **TRUE** für eine der ersten drei Nachrichten einer Zeichnungssequenz [**(WM \_ PSD \_ PAGESETUPDLG,**](wm-psd-pagesetupdlg.md) [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)oder [**WM \_ PSD \_ MINMARGINRECT)**](wm-psd-minmarginrect.md)zurückgibt, sendet das Dialogfeld keine weiteren Nachrichten und zeichnet erst dann auf der Beispielseite, wenn das System die Beispielseite neu zeichnen muss. Wenn die Hookprozedur **FALSE** für alle drei Nachrichten zurückgibt, sendet das Dialogfeld die verbleibenden Nachrichten der Zeichnungssequenz.

Wenn die Hookprozedur **TRUE** für eine der verbleibenden Nachrichten in einer Zeichnungssequenz zurückgibt, zeichnet das Dialogfeld nicht den entsprechenden Teil der Beispielseite. Wenn die Hookprozedur **FALSE** für eine dieser Meldungen zurückgibt, zeichnet das Dialogfeld diesen Teil der Beispielseite.

Um zu verhindern, dass das Dialogfeld den Inhalt der Beispielseite zeichnet, können Sie das **PSD \_ DISABLEPAGEPAINTING-Flag** festlegen. Dieses Flag wirkt sich nicht auf ihre [**PagePaintHook-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) aus, die weiterhin alle **\_ \_ \* WM-PSD-Nachrichten** empfängt und den Inhalt der Beispielseite zeichnen kann.

 

 