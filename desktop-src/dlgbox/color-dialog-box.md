---
title: Farben (Dialogfeld)
description: Zeigt ein modales Dialogfeld an, das es dem Benutzer ermöglicht, einen bestimmten Farbwert auszuwählen.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- Benutzereingabe, allgemeine Dialog Feld Bibliothek
- Erfassen von Benutzereingaben, allgemeine Dialog Feld Bibliothek
- Allgemeine Dialog Feld Bibliothek
- Allgemeine Dialogfelder
- Dialogfeld "Farbe"
- partielle Farbe (Dialogfeld)
- vollständige Farbe (Dialogfeld)
- Anpassen der Farbe (Dialogfeld)
- RGB-Farbmodell
- HSL-Farbmodell
- Farbton-Helligkeit (HSL)
- HSL (Hue-Sättigungs Helligkeit)
- RGB (rotes grünes blau)
- rotes grünes blau (RGB)
- Hooks, Dialogfeld "Farbe"
- vordefinierte Dialogfelder
- Dialogfelder, Farbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb90150f49ea7bed4edac53af40ba89e0459946
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "104568115"
---
# <a name="color-dialog-box"></a>Farben (Dialogfeld)

Zeigt ein modales Dialogfeld an, das es dem Benutzer ermöglicht, einen bestimmten Farbwert auszuwählen. Der Benutzer kann eine Farbe aus einer Reihe von einfachen oder benutzerdefinierten Farbpaletten auswählen. Alternativ kann der Benutzer einen Farbwert generieren, indem er die Farbwerte RGB oder Hue, Sättigung, Brillanz (HSL) der Dialogfeld-Benutzeroberfläche ändert. Das Dialogfeld **Farbe** gibt den RGB-Wert der vom Benutzer ausgewählten Farbe zurück.

Sie erstellen und zeigen ein **Farb** Dialogfeld an, indem Sie eine [**Auswahl Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur initialisieren und die-Struktur an die [**chooabcolor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) -Funktion übergeben. Durch Festlegen verschiedener Parameterwerte für die **Auswahl Farbe** können Sie beeinflussen, wie das Dialogfeld Farbe angezeigt wird. Beispielsweise können Sie entweder eine vollständige oder eine partielle Benutzeroberflächen Version des Dialog Felds anzeigen. Die folgende Abbildung zeigt die Vollversion der Benutzeroberfläche des Dialog Felds **Farbe** .

![Farbe (Dialogfeld)](images/colordialogboxxp.png)

Wenn der Benutzer auf die Schaltfläche **OK** klickt, gibt [**Choice Color**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) **true** zurück. Der **rgbresult** -Member der [**chooseecolor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur enthält den RGB-Farbwert der vom Benutzer ausgewählten Farbe. Der RGB-Farbwert gibt die Intensitäten der einzelnen roten, grünen und blauen Farben an, die die ausgewählte Farbe ausmachen. Die einzelnen Werte reichen von 0 bis 255. Verwenden Sie die Makros [**getrvalue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**getgvalue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)und [**getbvalue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) , um einzelne Farben aus einem RGB-Farbwert zu extrahieren.

Wenn der Benutzer das Dialogfeld " **Farbe** " abbricht oder wenn ein Fehler auftritt, gibt " [**Choice Color**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) " den Wert " **false** " zurück, und der **rgbresult** -Member ist nicht definiert Um die Ursache des Fehlers zu ermitteln, rufen Sie die [**kommdlgextendecoderror**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) -Funktion auf, um den erweiterten Fehlerwert abzurufen.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Vollständige und partielle Farb Dialogfelder](#full-and-partial-color-dialog-boxes)
-   [Anpassen des Dialog Felds "Farbe"](#customizing-the-color-dialog-box)
    -   [So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld "Farbe" bereit](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [So aktivieren Sie eine Hook-Prozedur für das Dialogfeld "Farbe"](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Farbmodelle, die im Dialog Feld "Farbe" verwendet werden](#color-models-used-by-the-color-dialog-box)
    -   [RGB-Farbmodell](#rgb-color-model)
    -   [HSL-Farbmodell](#hsl-color-model)
    -   [HSL-Werte werden in RGB-Werte umgerechnet](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Vollständige und partielle Farb Dialogfelder

Das Dialogfeld Farbe verfügt über eine Vollversion und eine partielle Version der Benutzeroberfläche. Die Vollversion enthält die grundlegenden Steuerelemente und verfügt über zusätzliche Steuerelemente, mit denen Benutzer benutzerdefinierte Farben erstellen können. Die partielle Version verfügt über Steuerelemente, die die grundlegenden und benutzerdefinierten Farbpaletten anzeigen, von denen der Benutzer einen Farbwert auswählen kann.

Die partielle Version des Dialog Felds Farbe enthält die Schaltfläche **benutzerdefinierte Farben definieren** . Der Benutzer kann auf diese Schaltfläche klicken, um die Vollversion anzuzeigen. Sie können das Dialogfeld Farbe so ausrichten, dass immer die Vollversion angezeigt wird, indem Sie das **CC \_ FullOpen** -Flag im **Flags** -Member der [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur festlegen. Um zu verhindern, dass Benutzer benutzerdefinierte Farben erstellt werden, können Sie das Flag **CC \_ preventfullopen** festlegen, um die Schaltfläche **benutzerdefinierte Farben definieren** zu deaktivieren.

Die Grundfarben stellen eine Auswahl der Farben dar, die auf dem angegebenen Gerät verfügbar sind. Die tatsächliche Anzahl angezeigter Farben wird vom Anzeigetreiber bestimmt. Ein VGA-Treiber zeigt z. b. 48 Farben an, während ein monochrome Anzeigetreiber nur 16 anzeigt.

Die benutzerdefinierten Farben sind diejenigen, die Sie angeben oder die der Benutzer erstellt. Wenn Sie ein Dialogfeld für die Farbe erstellen, müssen Sie den **lpcustcolors** -Member der [**choost Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur verwenden, um die Anfangswerte für die 16 benutzerdefinierten Farben anzugeben. Wenn die Vollversion des Dialog Felds Farbe geöffnet ist, kann der Benutzer eine benutzerdefinierte Farbe mit einer der folgenden Methoden erstellen:

-   Verschieben des Cursors in das Farbspektrum-Steuerelement und das Leuchtkraft-Schiebe Steuerelement
-   Eingeben von RGB-Werten in den **roten**, **grünen** und **blauen** Bearbeitungs Steuerelementen
-   Eingeben von HSL-Werten in den Steuerelementen **Hue**, **Sat** und **Lum** Edit

Um der Anzeige benutzerdefinierter Farben eine neue benutzerdefinierte Farbe hinzuzufügen, kann der Benutzer auf die Schaltfläche **zu benutzerdefinierten Farben hinzufügen** klicken. Dies bewirkt auch, dass das Dialogfeld den RGB-Wert der neuen Farbe in das entsprechende Element im Array kopiert, auf das der **lpcustcolors** -Member verweist. Wenn Sie neue benutzerdefinierte Farben zwischen den Aufrufen von [**chootarcolor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))beibehalten möchten, sollten Sie statischen Arbeitsspeicher für das Array zuweisen. Weitere Informationen zu den RGB-und HSL-Farb Modellen finden Sie unter [Farbmodelle, die im Dialog Feld Farbe verwendet werden](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Anpassen des Dialog Felds "Farbe"

Um das Dialogfeld Farbe anzupassen, können Sie eine der folgenden Methoden verwenden:

-   Geben Sie beim Erstellen des Dialog Felds Werte in der [**Auswahl Farbe**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) an.
-   Bereitstellen einer benutzerdefinierten Vorlage
-   Bereitstellen einer Hook-Prozedur

Sie können die Darstellung und das Verhalten des Dialog Felds Farbe ändern, indem Sie die Flags im **Flags** -Member der [**chooon Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur festlegen. Beispielsweise können Sie das **CC \_ solidcolor** -Flag so festlegen, dass das Dialogfeld angewiesen wird, nur voll Tonfarben anzuzeigen. Um zu bewirken, dass im Dialogfeld anfänglich eine andere Farbe als schwarz ausgewählt wird, legen Sie das **CC \_ rgbinit** -Flag fest, und geben Sie eine Farbe im **rgbresult** -Member an.

Sie können für das Dialogfeld Farbe eine benutzerdefinierte Vorlage bereitstellen, z. b. Wenn Sie zusätzliche Steuerelemente einschließen möchten, die für Ihre Anwendung eindeutig sind. Die Funktion " [**chooscolor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) " verwendet anstelle der Standardvorlage Ihre benutzerdefinierte Vorlage.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>So stellen Sie eine benutzerdefinierte Vorlage für das Dialogfeld "Farbe" bereit

1.  Erstellen Sie die benutzerdefinierte Vorlage, indem Sie die in der Datei Color. DLG angegebene Standardvorlage ändern. Die in der standardmäßigen Farb Dialogfeld Vorlage verwendeten Steuerelement-IDs werden in der Color. DLG-Datei definiert.
2.  Verwenden Sie die-Struktur " [**chooancolor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) ", um die Vorlage wie folgt zu aktivieren:
    -   Wenn Ihre benutzerdefinierte Vorlage eine Ressource in einer Anwendung oder einer Dynamic Link Library ist, legen Sie das **CC \_ ENABLETEMPLATE** -Flag im **Flags** -Member fest. Verwenden Sie die **HINSTANCE** -und **lptemplatename** -Member der-Struktur, um das Modul und den Ressourcennamen zu identifizieren.

        -Oder-

    -   Wenn Ihre benutzerdefinierte Vorlage bereits im Arbeitsspeicher vorhanden ist, legen Sie das Flag **CC \_ enabletemplatehandle** fest. Verwenden Sie das **HINSTANCE** -Element, um das Speicher Objekt zu identifizieren, das die Vorlage enthält.

Sie können für das Dialogfeld Farbe eine [**cchookproc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) -Hook-Prozedur bereitstellen. Die Hook-Prozedur kann an das Dialogfeld gesendete Nachrichten verarbeiten. Außerdem können registrierte Nachrichten verwendet werden, um das Verhalten des Dialog Felds zu steuern. Wenn Sie eine benutzerdefinierte Vorlage verwenden, um zusätzliche Steuerelemente zu definieren, müssen Sie eine Hook-Prozedur bereitstellen, um Eingaben für die Steuerelemente zu verarbeiten.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>So aktivieren Sie eine Hook-Prozedur für das Dialogfeld "Farbe"

1.  Legen Sie das **CC \_ ENABLEHOOK** -Flag im **Flags** -Member der [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur fest.
2.  Geben Sie die Adresse der Hook-Prozedur im **lpfnhook** -Member an.

Nach der Verarbeitung der " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung sendet die Dialogfeld Prozedur eine " **WM \_ InitDialog** "-Meldung an die Hook-Prozedur. Der *LPARAM* -Parameter dieser Nachricht ist ein Zeiger auf die " [**choolcolor**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) "-Struktur, die verwendet wird, um das Dialogfeld zu initialisieren.

Wenn der Benutzer auf die Schaltfläche **OK** klickt, sendet das Dialogfeld die registrierte [**colorokstring**](colorokstring.md) -Nachricht an die Hook-Prozedur. Die Hook-Prozedur kann die ausgewählte Farbe ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt, indem beim Empfang dieser Nachricht 0 (null) zurückgegeben wird. Die Hook-Prozedur kann erzwingen, dass das Dialogfeld eine bestimmte Farbe auswählt, indem Sie die registrierte Nachricht "" von "*" [**an das Dialog**](setrgbstring.md) Feld sendet. Um diese registrierten Nachrichten zu verwenden, müssen Sie die Konstanten " **colorokstring** " und " **strgbstring** " an die [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion übergeben, um eine Nachrichten-ID zu erhalten. Anschließend können Sie den Bezeichner verwenden, um über das Dialogfeld gesendete Nachrichten zu erkennen und zu verarbeiten oder um Nachrichten an das Dialogfeld zu senden.

## <a name="color-models-used-by-the-color-dialog-box"></a>Farbmodelle, die im Dialog Feld "Farbe" verwendet werden

Mit der Erweiterung benutzerdefinierte Farben des Dialog Felds Farbe kann der Benutzer eine Farbe mithilfe von RGB-oder HSL-Werten angeben. Allerdings verwendet die [**chooset Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur nur RGB-Werte, um die vom Benutzer erstellten oder ausgewählten Farben zu melden.

-   [RGB-Farbmodell](#rgb-color-model)
-   [HSL-Farbmodell](#hsl-color-model)
-   [HSL-Werte werden in RGB-Werte umgerechnet](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>RGB-Farbmodell

Das RGB-Modell wird verwendet, um Farben für anzeigen und andere Geräte anzugeben, die ein Licht ausgeben. Gültige rote, grüne und blaue Werte reichen von 0 bis 255, wobei 0 die minimale Intensität und 255 angibt, die die maximale Intensität angibt. Die folgende Abbildung zeigt, wie die Primärfarben Rot, grün und blau kombiniert werden können, um vier zusätzliche Farben zu schaffen. (Bei Anzeigegeräten ist die Farbe schwarz, wenn die Werte rot, grün und blau auf 0 festgelegt sind. In der Anzeige Technologie ist schwarz das Fehlen aller Farben.)

![überlappende rote, grüne und blaue Kreise](images/rgbcolormodel.png)

In der folgenden Tabelle werden acht Farben des RGB-Modells und die zugehörigen RGB-Werte aufgelistet.



| Color   | RGB-Werte    |
|---------|---------------|
| Red     | 255, 0, 0     |
| Grün   | 0, 255, 0     |
| Blau    | 0, 0, 255     |
| Cyan    | 0, 255, 255   |
| Magenta | 255, 0, 255   |
| Gelb  | 255, 255, 0   |
| Weiß   | 255, 255, 255 |
| Schwarz   | 0, 0, 0       |



 

Das System speichert interne Farben als 32-Bit-RGB-Werte, die die folgende hexadezimale Form aufweisen: 0x00bbggrr.

Das nieder wertige Byte enthält einen Wert für die relative Intensität von rot. Das zweite Byte enthält einen Wert für grün; Das dritte Byte enthält einen Wert für blau. Das höchst wertige Byte muss NULL sein.

Sie können das [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) -Makro verwenden, um einen RGB-Wert basierend auf den angegebenen Intensitäten für die roten, grünen und blauen Komponenten zu erhalten. Verwenden Sie die Makros [**getrvalue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**getbvalue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)und [**getgvalue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) , um einzelne Farben aus einem RGB-Farbwert zu extrahieren.

### <a name="hsl-color-model"></a>HSL-Farbmodell

Das Dialogfeld Farbe stellt Steuerelemente zum Angeben von HSL-Werten bereit. Die folgende Abbildung zeigt das Farbspektrum-Steuerelement und das Steuerelement für die Helligkeit, das im Dialogfeld Farbe angezeigt wird. Die Abbildung zeigt auch die Wertebereiche, die der Benutzer mit diesen Steuerelementen angeben kann.

![Farbspektrum und Leuchtkraft Skala](images/colordialogranges.png)

Im Dialogfeld Farbe müssen die Werte für Sättigung und Helligkeit im Bereich von 0 bis 240 liegen, und der Hue-Wert muss zwischen 0 und 239 liegen.

### <a name="converting-hsl-values-to-rgb-values"></a>HSL-Werte werden in RGB-Werte umgerechnet

Die in Comdlg32.dll für das Dialogfeld Farbe bereitgestellte Dialogfeld Prozedur enthält Code, mit dem HSL-Werte in die entsprechenden RGB-Werte konvertiert werden. In der folgenden Tabelle werden acht Farben des RGB-Modells und die zugehörigen HSL-und RGB-Werte aufgelistet.



| Color   | HSL-Werte      | RGB-Werte      |
|---------|-----------------|-----------------|
| Red     | (0, 240, 120)   | (255, 0, 0)     |
| Gelb  | (40, 240, 120)  | (255, 255, 0)   |
| Grün   | (80, 240, 120)  | (0, 255, 0)     |
| Cyan    | (120, 240, 120) | (0, 255, 255)   |
| Blau    | (160, 240, 120) | (255 0,0)     |
| Magenta | (200, 240, 120) | (255, 0, 255)   |
| Weiß   | (240 0,0)     | (255, 255, 255) |
| Schwarz   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
