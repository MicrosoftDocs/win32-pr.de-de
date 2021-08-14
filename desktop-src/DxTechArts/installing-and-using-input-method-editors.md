---
title: Installieren und Verwenden von Eingabemethoden-Editoren
description: Dieser Artikel enthält ein Tutorial zum Installieren und Verwenden des standarden Eingabemethode-Editors (Windows Input Method Editor, IME).
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45a0da52d0e917186831de8c84f39ecee3d2583ac4a267fa2501c643e2f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153514"
---
# <a name="installing-and-using-input-method-editors"></a>Installieren und Verwenden von Eingabemethoden-Editoren

Dieser Artikel enthält ein Tutorial zum Installieren und Verwenden des standarden Eingabemethode-Editors (Windows Input Method Editor, IME).

-   [Installieren eines Eingabemethode-Editors](#installing-an-input-method-editor)
-   [Vereinfachtes Chinesisch (IME)](#simplified-chinese-ime)
-   [Traditionelles Chinesisch (IME)](#traditional-chinese-ime)
-   [Japanische IME](#japanese-ime)
-   [Koreanisch IME](#korean-ime)
-   [Requirements](#requirements)

## <a name="installing-an-input-method-editor"></a>Installieren eines Eingabemethode-Editors

In den folgenden Abschnitten wird beschrieben, wie Eingabemethode-Editoren (INPUT Method Editors, IMEs) installiert und verwendet werden, um komplexe Zeichen in vier verschiedenen ostasiatischen Sprachen eineingaben. Die für jede Sprache eindeutigen Features werden erläutert.

Informationen zum Implementieren von IME-Funktionen (Input Method Editor) in einer Anwendung finden Sie unter Verwenden eines [Eingabemethode-Editors in einem Spiel.](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game)

Ein IME ist standardmäßig nicht auf Microsoft Windows XP-Systemen installiert. Führen Sie zum Installieren die folgenden Schritte aus.

**So installieren Sie einen IME**

1.  Öffnen Sie im Systemsteuerung die Optionen Regional und Sprache.
2.  Aktivieren Sie auf der Registerkarte Sprachen das Kontrollkästchen Dateien für ostasiatische Sprachen installieren.

    ![Registerkarte "Sprachen" der Optionen "Region" und "Sprache"](images/ime-1.png)

    Das Dialogfeld Zusätzliche Sprachunterstützung installieren wird angezeigt, in dem Sie über die Speicheranforderungen für die Sprachdateien informiert werden.

    ![Dialogfeld "Zusätzliche Sprachunterstützung installieren"](images/ime-install-lang-dialog.png)

3.  Klicken Sie auf OK, um das Dialogfeld zu schließen.
4.  Klicken Sie auf der Registerkarte Sprachen auf OK.
5.  Ein anderes Dialogfeld wird angezeigt, in dem sie Windows XP-Installationsdatenträger oder netzwerkfreigabespeicherort anfordern, in dem sich die Sprachunterstützungsdateien befinden. Fügen Sie einen Windows XP Compact-Datenträger ein, oder navigieren Sie zum entsprechenden Netzwerkspeicherort, und klicken Sie auf OK. Microsoft Windows installiert die erforderlichen Dateien und fordert Sie auf, den Computer neu zu starten.
6.  Klicken Sie auf Ja, um den Computer neu zu starten.
7.  Öffnen Sie nach dem Neustart erneut die Systemsteuerung "Regionale Optionen" und "Sprachoptionen".
8.  Klicken Sie auf der Registerkarte Sprachen auf Details. Das Fenster Textdienste und Eingabesprachen wird angezeigt.

    ![fenster "ext services and input languages" (Ext-Dienste und Eingabesprachen)](images/ime-2.png)

9.  Klicken Sie Einstellungen Registerkarte auf Hinzufügen. Das Fenster Eingabesprache hinzufügen wird angezeigt.

    ![Fenster "Eingabesprache hinzufügen"](images/ime-3.png)

10. Wählen Sie Chinesisch (Taiwan) als Eingabesprache und Microsoft New Phonetic IME 2002a für Tastaturlayout/IME aus.
11. Klicken Sie auf OK. Nun können Sie weitere Sprachen und IMEs auf ähnliche Weise hinzufügen.
12. Klicken Sie erneut auf Hinzufügen, wählen Sie Chinesisch (PRC) als Eingabesprache und Chinesisch (vereinfacht) – Microsoft Pinyin IME 3.0 für Tastaturlayout/IME aus, und klicken Sie dann auf OK.
13. Klicken Sie erneut auf Hinzufügen, wählen Sie Japanisch als Eingabesprache und Microsoft IME Standard 2002 ver aus. 8.1 für Tastaturlayout/IME, und klicken Sie dann auf OK.
14. Klicken Sie erneut auf Hinzufügen, wählen Sie Koreanisch als Eingabesprache und Koreanisches Eingabesystem (IME 2002) für Tastaturlayout/IME aus, und klicken Sie dann auf OK. Im Fenster Textdienste und Eingabesprachen sollte das Listenfeld Installierte Dienste nun die vier neu hinzugefügten IMEs enthalten.

    ![Listenfeld "Installierte Dienste"](images/ime-7.png)

15. Klicken Sie auf OK, um das Fenster Textdienste und Eingabesprachen zu schließen.
16. Klicken Sie auf OK, um die Systemsteuerung Für Regionen und Sprachenoptionen zu schließen. Die Windows Taskleiste sollte nun einen rot eingekreisten Eingabe-Locale-Indikator enthalten. Das Vorhandensein des Indikators gibt an, dass mehr als eine Eingabesprache auf dem System installiert wurde.

    ![Indikator, der anklangt, dass mehr als eine Eingabesprache auf dem System installiert wurde](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>Vereinfachtes Chinesisch (IME)

In diesem Abschnitt wird beschrieben, wie Sie die vereinfachte chinesische IME (PinYin) mit Microsoft Editor, um einige chinesische Zeichen ein leerzeichen.

1.  Starten Editor (verfügbar im Schaltfläche "Start", und wählen Sie dann Alle Programme und Zubehör aus). Geben Sie einige Zeichen in Editor. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Ein Bild, das Zeichen zeigt, mit denen das Fenster "I M E" später für vereinfachtes Chinesisch besser visualisiert werden kann.](images/ime-sc1.png)

2.  Klicken Editor als aktive Anwendung auf den Eingabe-Locale-Indikator, und wählen Sie Chinesisch (PRC) aus. Die Anzeige des Indikators ändert sich in CH, um anzuzeigen, dass die neue Eingabesprache Chinesisch (PRC) ist.

    ![Screenshot: Eingabe locale indicator to select Chinese (P R C) (Chinesisch (P R C))](images/ime-sc2.png)

3.  Platzieren Sie den Cursor in Editor. Drücken Sie HOME auf der Tastatur, damit sich der Cursor am Anfang der Zeile befindet. Geben Sie auf der Tastatur "N" und dann "I" ein. Die folgende Abbildung zeigt die Darstellung der Anzeige. Das kleine horizontale Rechteck ist das Lesefenster, in dem die aktuelle Lesezeichenfolge angezeigt wird. Derzeit ist die Lesezeichenfolge "ni" als Ergebnis der Eingabe von "N" und "I".

    ![Screenshot: Lesezeichenfolge mit "n" und "i"](images/ime-sc3.png)

4.  Geben Sie "3" ein. Nun Editor die folgende Anzeige angezeigt. Da N+I+3 eine vollständige Aussprache im vereinfachten Chinesisch Pinyin ist, verfügt der IME über genügend Informationen, um das Zeichen zu antizipieren, das der Benutzer möglicherweise eingeben möchte. Das Lesefenster wird nicht mehr angezeigt, da Sie eine vollständige Aussprache eingegeben haben. Ein Zeichen wird über dem Cursor Editor angezeigt. Dieses Zeichen ist nicht Teil von Editor, sondern wird in einem anderen Fenster über Editor angezeigt und blendet die vorhandenen Zeichen in Editor aus, die sich darunter befinden. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in diesem Fenster wird als Kompositionszeichenfolge bezeichnet. Die Kompositionszeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot: Kompositionsfenster mit einer Kompositionszeichenfolge mit einem Zeichen](images/ime-sc4.png)

5.  Geben Sie nun "H", "A", "O", "3" ein, um ein anderes Zeichen ein. Beachten Sie, dass das Lesefenster angezeigt wird, wenn "H" typiert ist, und verschwindet, wenn "3" typiert wird. Wie unten gezeigt, enthält die Kompositionszeichenfolge nun zwei Zeichen.

    ![Screenshot: Kompositionsfenster mit einer Kompositionszeichenfolge aus zwei Zeichen](images/ime-sc5.png)

6.  Drücken Sie einmal den Pfeil nach links auf der Tastatur. Der Kompositionscursor verschiebt ein Zeichen nach links, am zweiten Zeichen, das Sie eingeben. Ein Fenster wird über Editor angezeigt, wie unten dargestellt. Dieses Fenster wird als Kandidatenfenster bezeichnet. Es wird eine Liste von Zeichen oder Ausdrücken angezeigt, die mit der von Ihnen typierten Aussprache übereinstimmen. Sie können das beabsichtigte Wort aus den Einträgen in der Kandidatenliste auswählen. In diesem Beispiel sind zwei Kandidatenzeichen mit der gleichen Aussprache verfügbar.

    ![Zwei Kandidatenzeichen, die mit der gleichen Aussprache verfügbar sind](images/ime-sc6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidatenfenster wird jetzt geschlossen, und die Kompositionszeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot, der eine Kompositionszeichenfolge zeigt, die mit dem ausgewählten Zeichen aktualisiert wurde](images/ime-sc7.png)

8.  Drücken Sie die EINGABETASTE. Dies teilt dem IME mit, dass die Komposition abgeschlossen ist und die Zeichenfolge an die Anwendung gesendet werden soll – Editor beispiel. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über WM CHAR an Editor \_ gesendet. Die Unterstreichung ist in der folgenden Abbildung nicht mehr enthalten, da die beiden gezeigten Zeichen Teil des Texts in Editor. Der vorhandene Text "ABCDEFG" in Editor wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun erfolgreich zwei vereinfachte chinesische Zeichen mithilfe eines IME eingegeben.

    ![erfolgreich zwei vereinfachte chinesische Zeichen mit einem Ime eingegeben](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>Traditionelles Chinesisch (IME)

In diesem Abschnitt wird beschrieben, wie Sie die traditionelle chinesische IME (New Phonetic) mit Editor, um einige chinesische Zeichen ein eingeben zu können.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Editor. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Screenshot, der Zeichen zeigt, die dazu beitragen, das Fenster "I M E" später für chinesisch (traditionell) besser zu visualisieren.](images/ime-tc1.png)

2.  Klicken Sie auf der Taskleiste auf den Eingabe-Windows, und wählen Sie Chinesisch (Taiwan) aus. Die Anzeige des Indikators ändert sich in CH, um anzuzeigen, dass die neue Eingabesprache Chinesisch (Taiwan) ist.

    ![Eingabe locale indicator to select chinese (taiwan) (Eingabe locale indicator to select chinese (taiwan) (Eingabe locale indicator to select chinese (taiwan)](images/ime-tc2.png)

3.  Platzieren Sie den Cursor in Editor. Drücken Sie home auf der Tastatur, damit sich der Cursor am Anfang der Zeile befindet. Geben Sie auf der Tastatur "S" und dann "U" ein. Die folgende Abbildung zeigt die Darstellung der Anzeige. Das kleine vertikale Rechteck ist das Lesefenster, in dem die aktuelle Lesezeichenfolge angezeigt wird. Wie in der folgenden Abbildung dargestellt, enthält die Lesezeichenfolge zwei Zeichen, weil "S" und "U" angegeben wurden.

    ![Screenshot: Lesezeichenfolge mit zwei Zeichen](images/ime-tc3.png)

4.  Geben Sie "3" ein. Nun Editor die folgende Anzeige angezeigt. Da S+U+3 eine vollständige Aussprache im traditionellen Chinesisch ist, verfügt der IME über genügend Informationen, um das Zeichen zu antizipieren, das der Benutzer möglicherweise eingeben wollte. Das Lesefenster wird nicht mehr angezeigt, da Sie eine vollständige Aussprache eingegeben haben. Ein Zeichen wird über dem Cursor Editor angezeigt. Dieses Zeichen ist nicht Teil von Editor, sondern wird in einem anderen Fenster über Editor angezeigt und blendet die vorhandenen Zeichen in Editor aus, die sich darunter befinden. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in diesem Fenster wird als Kompositionszeichenfolge bezeichnet. Die Kompositionszeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot: Kompositionsfenster mit unterstrichener Kompositionszeichenfolge](images/ime-tc4.png)

5.  Geben Sie nun "C", "L" und "3" ein, um ein weiteres Zeichen ein. Beachten Sie, dass das Lesefenster angezeigt wird, wenn "C" typiert ist, und verschwindet, wenn "3" typiert ist. Wie unten gezeigt, enthält die Kompositionszeichenfolge nun zwei Zeichen.

    ![Screenshot: Kompositionsfenster mit einer Kompositionszeichenfolge und zwei unterstrichenen Zeichen](images/ime-tc5.png)

6.  Geben Sie den Pfeil nach unten einmal auf der Tastatur ein. Ein Fenster wird über Editor angezeigt, wie unten dargestellt. Dieses Fenster wird als Kandidatenfenster bezeichnet. Es wird eine Liste von Zeichen oder Ausdrücken angezeigt, die mit der von Ihnen typierten Aussprache übereinstimmen. Sie können das beabsichtigte Wort aus den Einträgen in der Kandidatenliste auswählen. In diesem Beispiel sind drei Kandidatenzeichen mit der gleichen Aussprache verfügbar.

    ![Drei Kandidatenzeichen, die mit der gleichen Aussprache verfügbar sind](images/ime-tc6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidatenfenster wird jetzt geschlossen, und die Kompositionszeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot, der eine Kompositionszeichenfolge zeigt, die mit einem ausgewählten Zeichen aktualisiert wurde](images/ime-tc7.png)

8.  Drücken Sie die EINGABETASTE. Dies teilt dem IME mit, dass die Komposition abgeschlossen ist und die Zeichenfolge an die Anwendung gesendet werden soll – Editor beispiel. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über WM CHAR an Editor [**\_ gesendet.**](/windows/desktop/inputdev/wm-char) Die Unterstreichung ist in der folgenden Abbildung nicht mehr enthalten, da die beiden gezeigten Zeichen Teil des Texts in Editor. Der vorhandene Text "ABCDEFG" in Editor wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun mithilfe eines IME erfolgreich zwei zeichen für chinesisch (traditionell) eingegeben.

    ![erfolgreich zwei traditionelle chinesische Zeichen mit einem Ime eingegeben](images/ime-tc8.png)

## <a name="japanese-ime"></a>Japanische IME

Dieser Abschnitt enthält eine exemplarische Vorgehensweise zur Verwendung des japanischen IME mit Editor eingaben einige japanische Zeichen.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Editor. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Screenshot, der Zeichen zeigt, die helfen, das IM E-Fenster später für Japanisch besser zu visualisieren.](images/ime-j1.png)

2.  Wenn Editor aktive Anwendung ist, klicken Sie auf den Eingabe-Locale-Indikator, und wählen Sie Japanisch aus. Die Anzeige des Indikators ändert sich in JP, um anzuzeigen, dass die neue Eingabesprache Japanisch ist.

    ![Eingabe locale indicator to select japanese](images/ime-j2.png)

3.  Platzieren Sie den Cursor in Editor. Drücken Sie home auf der Tastatur, damit sich der Cursor am Anfang der Zeile befindet. Geben Sie auf der Tastatur "N" und dann "I" ein. Die folgende Abbildung zeigt die Darstellung der Anzeige. Da N+I eine vollständige Aussprache auf Japanisch ist, verfügt der IME über genügend Informationen, um das Zeichen vorhersehen zu können, das der Benutzer möglicherweise eingeben möchte. Ein Zeichen wird über dem Cursor Editor angezeigt. Dieses Zeichen ist nicht Teil von Editor, sondern wird in einem anderen Fenster über Editor angezeigt und blendet die vorhandenen Zeichen in Editor aus, die sich darunter befinden. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in diesem Fenster wird als Kompositionszeichenfolge bezeichnet. Die Kompositionszeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot, der eine Kompositionszeichenfolge mit einem japanischen Zeichen unterstrichen zeigt.](images/ime-j3.png)

4.  Geben Sie nun "H", "O", "N", "G" und "O" ein, um zwei weitere Zeichen ein. Die Kompositionszeichenfolge enthält nun vier Zeichen, wie unten dargestellt.

    ![Screenshot: Kompositionszeichenfolge mit vier unterstrichenen japanischen Zeichen](images/ime-j4.png)

5.  Drücken Sie die Leerzeichenleiste. Dadurch wird der IME angewiesen, den eingegebenen Text in Klauseln zu konvertieren. In der folgenden Abbildung konvertiert der IME die Aussprache "Nihongo" in eine in Kanji geschriebene Klausel, die "Japanische Sprache" bedeutet.

    ![ime konvertiert japanische Aussprache](images/ime-j5.png)

6.  Drücken Sie einmal den Pfeil nach unten auf der Tastatur. Ein Fenster wird über Editor angezeigt, wie unten dargestellt. Dieses Fenster wird als Kandidatenfenster bezeichnet. Es wird eine Liste von Klauseln angezeigt, die mit der von Ihnen typierten Aussprache übereinstimmen. Sie können das beabsichtigte Wort aus der Liste der Kandidaten auswählen. In diesem Beispiel sind drei Kandidatenzeichen mit der gleichen Aussprache verfügbar. Beachten Sie, dass der zweite Eintrag hervorgehoben ist und sich die Kompositionszeichenfolge ändert. Dies wird durch die Eingabe des Pfeils nach unten verursacht, der den IME anfing, den Eintrag nach dem zuvor angezeigten Eintrag auszuwählen.

    ![Screenshot, der das Kandidatenfenster zeigt.](images/ime-j6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidatenfenster wird jetzt geschlossen, und die Kompositionszeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot der Kompositionszeichenfolge, die mit dem ausgewählten japanischen Zeichen aktualisiert wurde](images/ime-j7.png)

8.  Drücken Sie die EINGABETASTE. Dies teilt dem IME mit, dass die Komposition abgeschlossen ist und die Zeichenfolge an die Anwendung gesendet werden soll – Editor beispiel. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über WM CHAR an Editor [**\_ gesendet.**](/windows/desktop/inputdev/wm-char) Die Unterstreichung ist in der folgenden Abbildung nicht mehr enthalten, da die beiden gezeigten Zeichen Teil des Texts in Editor. Der vorhandene Text "ABCDEFG" in Editor wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun mithilfe eines IME erfolgreich einige japanische Zeichen eingegeben.

    ![erfolgreiche Eingabe von einigen japanischen Zeichen mit einem Ime](images/ime-j8.png)

## <a name="korean-ime"></a>Koreanisch IME

In diesem Abschnitt wird beschrieben, wie Sie den koreanischen IME mit Editor eingaben, um einige koreanische Zeichen ein.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Editor. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Zeichen, die helfen, das Ime-Fenster später besser zu visualisieren](images/ime-k1.png)

2.  Klicken Editor aktive Anwendung auf den Eingabe-Locale Indicator, und wählen Sie Koreanisch aus. Die Anzeige des Indikators ändert sich in KO, um anzuzeigen, dass die neue Eingabesprache Koreanisch ist.

    ![Eingabe locale indicator to select korean](images/ime-k2.png)

3.  Platzieren Sie den Cursor in Editor. Drücken Sie HOME auf der Tastatur, damit sich der Cursor am Anfang der Zeile befindet, und geben Sie dann "G" ein. Die folgende Abbildung zeigt die Darstellung der Anzeige. Das phonetische Element, das "G" entspricht, wird auf Editor und mit einem Blockcursor hervorgehoben. Dieses hervorgehobene Zeichen wird als Kompositionszeichenfolge bezeichnet. Beachten Sie, dass die Kompositionszeichenfolge im Gegensatz zur IME für andere Sprachen an Editor gesendet und links neben dem vorhandenen Text eingefügt wird, sobald der Benutzer ein einzelnes phonetisches Element eingibt.

    ![Screenshot: Kompositionszeichenfolge mit einem Zeichen, das links neben dem vorhandenen Text eingefügt wird](images/ime-k3.png)

4.  Zu diesem Zeitpunkt besteht die Kompositionszeichenfolge aus einem Zwischenzeichen, da alle zusätzlichen vom Benutzer eingegebenen phonetischen Elemente die Kompositionszeichenfolge direkt ändern. Geben Sie nun "K" und dann "S" ein. Beachten Sie, dass sich das Zwischenzeichen mit jeder Tastatureingabe ändert.

    ![Kompositionszeichenfolge](images/ime-k4.png)

5.  Drücken Sie nun die rechte STRG-TASTE. Es wird ein Kandidatenfenster mit den Hanja-Zeichen angezeigt, die Sie für die eingegebene Aussprache auswählen können: G+K+S.

    ![Screenshot, der ein Kandidatenfenster mit einer Liste von Hanja-Zeichen zeigt, die Sie am unteren Rand des Fensters auswählen können.](images/ime-k5.png)

6.  Geben Sie die Ziffer "1" ein, um den ersten Eintrag in der Liste auszuwählen. Das Kandidatenfenster wird geschlossen, und die Kompositionszeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Kompositionszeichenfolge mit ausgewähltem Zeichen aktualisiert](images/ime-k6.png)

7.  Geben Sie "R", "N" und "R" ein. Drücken Sie dann die rechte STRG-TASTE, um ein weiteres Zeichen einzugeben.

    ![Kandidatenfenster](images/ime-k7.png)

8.  Geben Sie "1" ein, um den ersten Eintrag auszuwählen. Sie haben nun erfolgreich zwei koreanische Zeichen mit einer IME eingegeben. Die koreanischen Zeichen sind bereits Teil der Textzeichenfolge in Editor.

    ![erfolgreiche Eingabe von zwei koreanischen Zeichen mit einem ime](images/ime-k8.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Betriebssystem**                | Windows XP                                                                                                 |
| **Verfügbarer Festplattenspeicher**       | Mindestens 230 MB                                                                                            |
| **Speicherorte von Fremdsprachdateien** | Windows Kompakter XP-Datenträger oder Netzwerkspeicherort mit Windows XP-Installationsdateien                |
| **Time**                            | Etwa zehn Minuten, um Fremdsprachdateien zu installieren. jeweils etwa zehn Minuten, um vier verschiedene IMEs zu überprüfen. |



 

 

 
