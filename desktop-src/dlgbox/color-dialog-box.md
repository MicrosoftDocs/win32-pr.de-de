---
title: Farben (Dialogfeld)
description: Zeigt ein modales Dialogfeld an, in dem der Benutzer einen bestimmten Farbwert auswählen kann.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- Benutzereingabe, Common Dialog Box Library
- Erfassen von Benutzereingaben, Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfeldbibliothek
- Allgemeine Dialogfelder
- Dialogfeld "Farbe"
- Partielle Farbe (Dialogfeld)
- Vollfarbe (Dialogfeld)
- Anpassen des Dialogfelds "Farbe"
- RGB-Farbmodell
- HSL-Farbmodell
- Helligkeit der Farbtonsättigung (HSL)
- HSL (Helligkeit der Farbtonsättigung)
- RGB (rotgrün blau)
- Rotgrünblau (RGB)
- Hooks, Dialogfeld "Farbe"
- Vordefinierte Dialogfelder
- Dialogfelder, Farbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bdfb1543de80ac105d4a6012a0c95ff46cd8da1fef204ed573d14d05a6dfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726397"
---
# <a name="color-dialog-box"></a>Farben (Dialogfeld)

Zeigt ein modales Dialogfeld an, in dem der Benutzer einen bestimmten Farbwert auswählen kann. Der Benutzer kann eine Farbe aus einer Reihe von einfachen oder benutzerdefinierten Farbpaletten auswählen. Alternativ kann der Benutzer einen Farbwert generieren, indem er die Farbwerte RGB oder Farbton, Sättigung, Helligkeit (HSL) der Benutzeroberfläche des Dialogfelds ändert. Das Dialogfeld **Farbe** gibt den RGB-Wert der vom Benutzer ausgewählten Farbe zurück.

Sie erstellen und zeigen ein Dialogfeld **Farbe** an, indem Sie eine [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) initialisieren und die Struktur an die [**ChooseColor-Funktion**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) übergeben. Indem Sie unterschiedliche Parameterwerte für die **CHOOSECOLOR-Struktur** festlegen, können Sie beeinflussen, wie das Dialogfeld Farbe angezeigt wird. Sie können z. B. eine vollständige oder eine teilversion der Benutzeroberfläche des Dialogfelds anzeigen. Die folgende Abbildung zeigt die vollständige Version der Benutzeroberfläche des Dialogfelds **Farbe.**

![Farbe (Dialogfeld)](images/colordialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) **TRUE** zurück. Der **rgbResult-Member** der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) enthält den RGB-Farbwert der vom Benutzer ausgewählten Farbe. Der RGB-Farbwert gibt die Intensitäten der einzelnen roten, grünen und blauen Farben an, aus denen die ausgewählte Farbe besteht. Die einzelnen Werte liegen zwischen 0 und 255. Verwenden Sie die Makros [**GetRValue,**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue) [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)und [**GetBValue,**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) um einzelne Farben aus einem RGB-Farbwert zu extrahieren.

Wenn der Benutzer das Dialogfeld **Farbe** abbricht oder ein Fehler auftritt, gibt [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) **FALSE** zurück, und der **rgbResult-Member** ist nicht definiert. Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**CommDlgExtendedError-Funktion**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) auf, um den erweiterten Fehlerwert abzurufen.

Die folgenden Themen werden in diesem Abschnitt behandelt.

-   [Voll- und Teilfarbendialogfelder](#full-and-partial-color-dialog-boxes)
-   [Anpassen des Dialogfelds "Farbe"](#customizing-the-color-dialog-box)
    -   [So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld Farbe bereit](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [So aktivieren Sie eine Hookprozedur für das Dialogfeld Farbe](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Vom Dialogfeld "Farbe" verwendete Farbmodelle](#color-models-used-by-the-color-dialog-box)
    -   [RGB-Farbmodell](#rgb-color-model)
    -   [HSL-Farbmodell](#hsl-color-model)
    -   [Konvertieren von HSL-Werten in RGB-Werte](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Voll- und Teilfarbendialogfelder

Das Dialogfeld Farbe verfügt über eine Vollversion und eine Teilversion der Benutzeroberfläche. Die Vollversion enthält die grundlegenden Steuerelemente und verfügt über zusätzliche Steuerelemente, mit denen der Benutzer benutzerdefinierte Farben erstellen kann. Die Teilversion verfügt über Steuerelemente, die die grundlegenden und benutzerdefinierten Farbpaletten anzeigen, aus denen der Benutzer einen Farbwert auswählen kann.

Die Teilversion des Dialogfelds Farbe enthält die Schaltfläche **Benutzerdefinierte Farben definieren.** Der Benutzer kann auf diese Schaltfläche klicken, um die Vollversion anzuzeigen. Sie können das Dialogfeld Farbe anweisen, immer die Vollversion anzuzeigen, indem Sie das **CC \_ FULLOPEN-Flag** im **Flags-Member** der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) festlegen. Um zu verhindern, dass der Benutzer benutzerdefinierte Farben erstellt, können Sie das **CC \_ PREVENTFULLOPEN-Flag** so festlegen, dass die Schaltfläche **Benutzerdefinierte Farben definieren** deaktiviert wird.

Die Basisfarben stellen eine Auswahl der Farben dar, die auf dem angegebenen Gerät verfügbar sind. Die tatsächliche Anzahl der angezeigten Farben wird vom Anzeigetreiber bestimmt. Ein VGA-Treiber zeigt z. B. 48 Farben an, und ein Monocolore-Anzeigetreiber zeigt nur 16 an.

Die benutzerdefinierten Farben sind die, die Sie angeben oder die der Benutzer erstellt. Wenn Sie ein Dialogfeld Farbe erstellen, müssen Sie den **lpCustColors-Member** der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) verwenden, um die Anfangswerte für die 16 benutzerdefinierten Farben anzugeben. Wenn die Vollversion des Dialogfelds Farbe geöffnet ist, kann der Benutzer mit einer der folgenden Methoden eine benutzerdefinierte Farbe erstellen:

-   Bewegen des Cursors im Farbspektrum-Steuerelement und im Helligkeits-Schieberegler
-   Eingeben von RGB-Werten in die Bearbeitungssteuerelemente **"Rot",** **"Grün"** und **"Blau"**
-   Eingeben von HSL-Werten in die **Farbton-,** **Sat-** und Lum-Bearbeitungssteuerelemente 

Um der Anzeige benutzerdefinierter Farben eine neue benutzerdefinierte Farbe hinzuzufügen, kann der Benutzer auf die Schaltfläche **Zu benutzerdefinierten Farben hinzufügen** klicken. Dies bewirkt auch, dass das Dialogfeld den RGB-Wert der neuen Farbe in das entsprechende Element im Array kopiert, auf das der **lpCustColors-Member** zeigt. Um neue benutzerdefinierte Farben zwischen Aufrufen von [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))beizubehalten, sollten Sie statischen Speicher für das Array zuordnen. Weitere Informationen zu den RGB- und HSL-Farbmodellen finden Sie unter [Farbmodelle, die vom Dialogfeld Farbe verwendet werden.](#color-models-used-by-the-color-dialog-box)

## <a name="customizing-the-color-dialog-box"></a>Anpassen des Dialogfelds "Farbe"

Zum Anpassen eines Dialogfelds Farbe können Sie eine der folgenden Methoden verwenden:

-   Angeben von Werten in der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) beim Erstellen des Dialogfelds
-   Bereitstellen einer benutzerdefinierten Vorlage
-   Bereitstellen einer Hookprozedur

Sie können die Darstellung und das Verhalten des Dialogfelds Farbe ändern, indem Sie Flags im **Flags-Member** der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) festlegen. Beispielsweise können Sie das **CC \_ SOLIDCOLOR-Flag** so festlegen, dass das Dialogfeld nur Volltonfarben anzeigt. Damit das Dialogfeld zunächst eine andere Farbe als Schwarz auswählt, legen Sie das **CC \_ RGBINIT-Flag** fest, und geben Sie eine Farbe im **rgbResult-Member** an.

Sie können eine benutzerdefinierte Vorlage für das Dialogfeld Farbe bereitstellen, wenn Sie beispielsweise zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die [**ChooseColor-Funktion**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) verwendet Ihre benutzerdefinierte Vorlage anstelle der Standardvorlage.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld Farbe bereit

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Color.dlg angegebene Standardvorlage ändern. Die Steuerelementbezeichner, die in der Standardvorlage Des Dialogfelds Farbe verwendet werden, werden in der Datei Color.dlg definiert.
2.  Verwenden Sie die [**CHOOSECOLOR-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **CC \_ ENABLETEMPLATE-Flag** im **Flags-Member** fest. Verwenden Sie die Member **hInstance** und **lpTemplateName** der Struktur, um den Modul- und Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn sich Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher befindet, legen Sie das **CC \_ ENABLETEMPLATEHANDLE-Flag** fest. Verwenden Sie den **Member hInstance,** um das Speicherobjekt zu identifizieren, das die Vorlage enthält.

Sie können eine [**CCHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) für das Dialogfeld Farbe angeben. Die Hookprozedur kann Nachrichten verarbeiten, die an das Dialogfeld gesendet werden. Sie kann auch registrierte Nachrichten verwenden, um das Verhalten des Dialogfelds zu steuern. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hookprozedur zum Verarbeiten von Eingaben für Ihre Steuerelemente bereitstellen.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>So aktivieren Sie eine Hookprozedur für das Dialogfeld Farbe

1.  Legen Sie das **CC \_ ENABLEHOOK-Flag** im **Flags-Member** der [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) fest.
2.  Geben Sie die Adresse der Hookprozedur im **lpfnHook-Member** an.

Nach der Verarbeitung der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sendet die Dialogfeldprozedur eine **WM \_ INITDIALOG-Nachricht** an die Hookprozedur. Der *lParam-Parameter* dieser Nachricht ist ein Zeiger auf die [**CHOOSECOLOR-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) die zum Initialisieren des Dialogfelds verwendet wird.

Das Dialogfeld sendet die registrierte [**COLOROKSTRING-Nachricht**](colorokstring.md) an die Hookprozedur, wenn der Benutzer auf die Schaltfläche **OK** klickt. Die Hookprozedur kann die ausgewählte Farbe ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt, indem null zurückgegeben wird, wenn diese Meldung empfangen wird. Die Hookprozedur kann erzwingen, dass das Dialogfeld eine bestimmte Farbe auswählt, indem die registrierte [**SETRGBSTRING-Nachricht**](setrgbstring.md) an das Dialogfeld gesendet wird. Um diese registrierten Nachrichten zu verwenden, müssen Sie die Konstanten **COLOROKSTRING** und **SETRGBSTRING** an die [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) übergeben, um einen Nachrichtenbezeichner abzurufen. Anschließend können Sie den Bezeichner verwenden, um vom Dialogfeld gesendete Nachrichten zu erkennen und zu verarbeiten oder um Nachrichten an das Dialogfeld zu senden.

## <a name="color-models-used-by-the-color-dialog-box"></a>Vom Dialogfeld "Farbe" verwendete Farbmodelle

Die Benutzerdefinierte Farberweiterung des Dialogfelds Farbe ermöglicht es dem Benutzer, eine Farbe mit RGB- oder HSL-Werten anzugeben. Die [**CHOOSECOLOR-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) verwendet jedoch nur RGB-Werte, um die vom Benutzer erstellten oder ausgewählten Farben zu melden.

-   [RGB-Farbmodell](#rgb-color-model)
-   [HSL-Farbmodell](#hsl-color-model)
-   [Konvertieren von HSL-Werten in RGB-Werte](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>RGB-Farbmodell

Das RGB-Modell wird verwendet, um Farben für Displays und andere Geräte festzulegen, die Licht ausgeben. Gültige rote, grüne und blaue Werte liegen zwischen 0 und 255, wobei 0 die minimale Intensität und 255 die maximale Intensität angeben. Die folgende Abbildung zeigt, wie die Primärfarben Rot, Grün und Blau kombiniert werden können, um vier zusätzliche Farben zu erzeugen. (Bei Anzeigegeräten wird die Farbe Schwarz angezeigt, wenn die Werte rot, grün und blau auf 0 festgelegt sind. In der Anzeigetechnologie ist Schwarz das Fehlen aller Farben.)

![Überlappende rote, grüne und blaue Kreise](images/rgbcolormodel.png)

In der folgenden Tabelle sind acht Farben des RGB-Modells und die zugehörigen RGB-Werte aufgeführt.



| Color   | RGB-Werte    |
|---------|---------------|
| Red     | 255, 0, 0     |
| Grün   | 0, 255, 0     |
| Blau    | 0, 0, 255     |
| Cyan    | 0, 255, 255   |
| Magenta | 255, 0, 255   |
| Gelb  | 255, 255, 0   |
| White   | 255, 255, 255 |
| Schwarz   | 0, 0, 0       |



 

Das System speichert interne Farben als 32-Bit-RGB-Werte mit der folgenden hexadezimalen Form: 0x00bbggrr.

Das Low-Order-Byte enthält einen Wert für die relative Intensität von Rot. Das zweite Byte enthält einen Wert für Grün. und das dritte Byte enthält einen Wert für blau. Das höher geordnete Byte muss 0 (null) sein.

Sie können das [**RGB-Makro**](/windows/desktop/api/wingdi/nf-wingdi-rgb) verwenden, um einen RGB-Wert basierend auf den angegebenen Intensitäten für die roten, grünen und blauen Komponenten abzurufen. Verwenden Sie die Makros [**GetRValue,**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue) [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)und [**GetGValue,**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) um einzelne Farben aus einem RGB-Farbwert zu extrahieren.

### <a name="hsl-color-model"></a>HSL-Farbmodell

Das Dialogfeld Farbe stellt Steuerelemente zum Angeben von HSL-Werten bereit. Die folgende Abbildung zeigt das Farbspektrum-Steuerelement und das Helligkeits-Schiebesteuerelement, das im Dialogfeld Farbe angezeigt wird. Die Abbildung zeigt auch die Wertebereiche, die der Benutzer mit diesen Steuerelementen angeben kann.

![Farbspektrum und Helligkeitsskala](images/colordialogranges.png)

Im Dialogfeld Farbe müssen sich die Werte für Sättigung und Helligkeit im Bereich von 0 bis 240 und der Farbtonwert im Bereich von 0 bis 239 liegen.

### <a name="converting-hsl-values-to-rgb-values"></a>Konvertieren von HSL-Werten in RGB-Werte

Die in Comdlg32.dll für das Dialogfeld Farbe bereitgestellte Dialogfeldprozedur enthält Code, der HSL-Werte in die entsprechenden RGB-Werte konvertiert. In der folgenden Tabelle sind acht Farben des RGB-Modells und die zugehörigen HSL- und RGB-Werte aufgeführt.



| Color   | HSL-Werte      | RGB-Werte      |
|---------|-----------------|-----------------|
| Red     | (0, 240, 120)   | (255, 0, 0)     |
| Gelb  | (40, 240, 120)  | (255, 255, 0)   |
| Grün   | (80, 240, 120)  | (0, 255, 0)     |
| Cyan    | (120, 240, 120) | (0, 255, 255)   |
| Blau    | (160, 240, 120) | (0, 0, 255)     |
| Magenta | (200, 240, 120) | (255, 0, 255)   |
| White   | (0, 0, 240)     | (255, 255, 255) |
| Schwarz   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
