---
title: Installieren und Verwenden von Eingabemethoden-Editoren
description: Dieser Artikel enthält ein Tutorial zum Installieren und Verwenden des standardmäßigen Windows-Eingabemethoden-Editors (IME).
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6018b3a387a12409f9e46d0392bbd60015af29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369393"
---
# <a name="installing-and-using-input-method-editors"></a>Installieren und Verwenden von Eingabemethoden-Editoren

Dieser Artikel enthält ein Tutorial zum Installieren und Verwenden des standardmäßigen Windows-Eingabemethoden-Editors (IME).

-   [Installieren eines Eingabemethoden-Editors](#installing-an-input-method-editor)
-   [Chinesisch (vereinfacht)](#simplified-chinese-ime)
-   [Traditionelles Chinesisch (IME)](#traditional-chinese-ime)
-   [Japanischer IME](#japanese-ime)
-   [Koreanisch IME](#korean-ime)
-   [Anforderungen](#requirements)

## <a name="installing-an-input-method-editor"></a>Installieren eines Eingabemethoden-Editors

In den folgenden Abschnitten wird beschrieben, wie Sie Eingabemethoden-Editoren (Input Method Editors, IMEs) zum eingeben komplexer Zeichen in vier verschiedenen ostasiatischen Sprachen installieren und verwenden. Features, die für jede Sprache eindeutig sind, werden erläutert.

Informationen zum Implementieren der Funktionen des Eingabemethoden-Editors (IME) in einer Anwendung finden [Sie unter Verwenden eines Eingabemethoden-Editors in einem Spiel](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

Ein IME ist nicht standardmäßig auf Microsoft Windows XP-Systemen installiert. Führen Sie die folgenden Schritte aus, um zu installieren.

**So installieren Sie ein IME**

1.  Öffnen Sie in der Systemsteuerung Regions-und Sprachoptionen.
2.  Aktivieren Sie auf der Registerkarte Sprachen das Kontrollkästchen Dateien für ostasiatische Sprachen installieren.

    ![Registerkarte "Sprachen" der Regions-und Sprachoptionen](images/ime-1.png)

    Das Dialogfeld Unterstützung für zusätzliche Sprachen installieren wird angezeigt, in dem Sie über die Speicheranforderungen für die Sprachdateien informiert werden.

    ![Dialogfeld "Unterstützung der ergänzenden Sprache installieren"](images/ime-install-lang-dialog.png)

3.  Klicken Sie auf OK, um das Dialogfeld zu schließen.
4.  Klicken Sie auf der Registerkarte Sprachen auf OK.
5.  Ein weiteres Dialogfeld wird angezeigt, in dem ein Windows XP-Installations Datenträger oder ein Netzwerkfreigabe Speicherort angefordert wird Legen Sie einen Windows XP Compact-Datenträger ein, oder navigieren Sie zum entsprechenden Netzwerk Speicherort, und klicken Sie auf OK Microsoft Windows installiert die erforderlichen Dateien und fordert Sie auf, den Computer neu zu starten.
6.  Klicken Sie auf Ja, um den Computer neu zu starten.
7.  Öffnen Sie nach dem Neustart erneut die Systemsteuerung für Regions-und Sprachoptionen.
8.  Klicken Sie auf der Registerkarte Sprachen auf Details. Das Fenster Text Dienste und Eingabe Sprachen wird angezeigt.

    ![Fenster "ext-Dienste und Eingabe Sprachen"](images/ime-2.png)

9.  Klicken Sie auf der Registerkarte Einstellungen auf hinzufügen. Das Fenster Eingabe Sprache hinzufügen wird angezeigt.

    ![Fenster "Eingabe Sprache hinzufügen"](images/ime-3.png)

10. Wählen Sie Chinesisch (Taiwan) für Eingabe Sprache und Microsoft New Phonetic IME 2002a for Keyboard Layout/IME aus.
11. Klicken Sie auf OK. Nun können Sie weitere Sprachen und IMEs auf ähnliche Weise hinzufügen.
12. Klicken Sie erneut auf Hinzufügen, wählen Sie Chinesisch (Volksrepublik China) für Eingabe Sprache und Chinesisch (vereinfacht 3,0) aus, und klicken Sie dann auf OK.
13. Klicken Sie erneut auf Hinzufügen, wählen Sie Japanisch für Eingabe Sprache und Microsoft IME Standard 2002 ver aus. 8,1 für das Tastaturlayout/IME, klicken Sie auf OK.
14. Klicken Sie erneut auf Hinzufügen, wählen Sie Koreanisch für Eingabe Sprache und koreanisches Eingabe System (IME 2002) für Tastaturlayout/IME aus, und klicken Sie auf OK. Im Fenster Text Dienste und Eingabe Sprachen sollte das Listenfeld Installierte Dienste nun die vier neu hinzugefügten IMEs enthalten.

    ![Listenfeld "installierte Dienste"](images/ime-7.png)

15. Klicken Sie auf OK, um das Fenster Text Dienste und Eingabe Sprachen zu schließen.
16. Klicken Sie auf OK, um die Systemsteuerung für Regions-und Sprachoptionen zu schließen. Die Windows-Taskleiste sollte nun einen in rot einkreisten Eingabe Gebiets Schema Indikator enthalten. Das vorhanden sein des Indikators bedeutet, dass mehr als eine Eingabe Sprache auf dem System installiert ist.

    ![ein Indikator, der angibt, dass mehr als eine Eingabe Sprache auf dem System installiert ist.](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>Chinesisch (vereinfacht)

In diesem Abschnitt wird beschrieben, wie Sie den vereinfachten chinesischen IME (Pinyin) mit Microsoft Notepad verwenden, um einige chinesische Zeichen einzugeben.

1.  Starten Sie Notepad (verfügbar über die Schaltfläche "Start", und wählen Sie dann alle Programme und Zubehör aus). Geben Sie einige Zeichen in Notepad ein. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Ein Screenshot, der Zeichen anzeigt, mit denen das I M E-Fenster später für vereinfachtes Chinesisch besser visualisiert werden konnte.](images/ime-sc1.png)

2.  Klicken Sie mit Notepad als aktive Anwendung auf den Eingabe Gebiets Schema Indikator, und wählen Sie Chinesisch (PRC) aus. Der Indikator zeigt Änderungen an ch an, um anzuzeigen, dass die neue Eingabe Sprache Chinesisch (VR China) ist.

    ![Screenshot, der den Eingabe Gebiets Schema Indikator zum Auswählen von Chinesisch (P R C) anzeigt.](images/ime-sc2.png)

3.  Platzieren Sie den Cursor in Notepad. Drücken Sie auf der Tastatur die Startseite, sodass sich der Cursor am Anfang der Zeile befindet. Auf dem Tastatur-Typ "N", dann "I". Die folgende Abbildung zeigt die Darstellung der Anzeige. Das kleine horizontale Rechteck ist das Lese Fenster, in dem die aktuelle Lese Zeichenfolge angezeigt wird. Derzeit ist die Lese Zeichenfolge "NI", weil Sie "N" und "I" eingegeben haben.

    ![Screenshot, der eine Lese Zeichenfolge mit "n" und "i" anzeigt.](images/ime-sc3.png)

4.  Geben Sie "3" ein. Notepad weist nun die folgende Anzeige auf. Da N + I + 3 eine komplette Aussprache in vereinfachtem Chinesisch Pinyin ist, verfügt das IME über genügend Informationen, um das Zeichen zu antizipieren, das der Benutzer möglicherweise eingegeben hat. Das Lese Fenster verschwindet, weil Sie eine komplette Aussprache eingegeben haben. Am oberen Rand des Notepad-Cursors wird ein Zeichen angezeigt. Dieses Zeichen ist nicht Teil von Notepad, sondern wird in einem anderen Fenster oberhalb von Editor angezeigt und blendet die vorhandenen Zeichen im Editor aus. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in der Zeichenfolge wird als Kompositions Zeichenfolge bezeichnet. Die Kompositions Zeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot, der ein Kompositionsfenster mit einer Kompositions Zeichenfolge mit einem Zeichen anzeigt.](images/ime-sc4.png)

5.  Geben Sie nun "H", "A", "O", "3" ein, um ein anderes Zeichen einzugeben. Beachten Sie, dass das Lesefenster angezeigt wird, wenn "H" eingegeben wird und beim Eingeben von "3" nicht mehr angezeigt wird. Wie unten gezeigt, enthält die Kompositions Zeichenfolge nun zwei Zeichen.

    ![Screenshot, der ein Kompositionsfenster mit einer Kompositions Zeichenfolge mit zwei Zeichen anzeigt.](images/ime-sc5.png)

6.  Drücken Sie die nach-links-Taste auf der Tastatur. Der Kompositions Cursor verschiebt ein Zeichen nach links, bei dem zweiten Zeichen, das Sie eingegeben haben. Ein Fenster wird oben im Editor angezeigt, wie unten gezeigt. Dieses Fenster wird als Kandidaten Fenster bezeichnet. Es wird eine Liste von Zeichen oder Ausdrücken angezeigt, die der von Ihnen eingegebenen Aussprache entsprechen. Sie können das beabsichtigte Wort aus den Einträgen in der Kandidatenliste auswählen. In diesem Beispiel sind zwei Kandidaten Zeichen mit derselben Aussprache verfügbar.

    ![zwei Kandidaten Zeichen, die mit derselben Aussprache verfügbar sind](images/ime-sc6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidaten Fenster wird jetzt geschlossen, und die Kompositions Zeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot, der eine mit dem ausgewählten Zeichen aktualisierte Kompositions Zeichenfolge anzeigt.](images/ime-sc7.png)

8.  Drücken Sie die EINGABETASTE. Dadurch wird dem IME mitgeteilt, dass die Komposition fertig ist, und die Zeichenfolge sollte in diesem Beispiel an den Application-Notepad gesendet werden. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über WM char an Notepad gesendet \_ . Die Unterstreichung ist in der folgenden Abbildung zu sehen, da die beiden gezeigten Zeichen Teil des Texts in Editor sind. Der vorhandene Text "abcdefg" in Notepad wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun erfolgreich zwei vereinfachte chinesische Zeichen mit einem IME eingegeben.

    ![Es wurden zwei vereinfachte chinesische Zeichen erfolgreich mithilfe eines IME eingegeben.](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>Traditionelles Chinesisch (IME)

In diesem Abschnitt wird beschrieben, wie Sie mit dem herkömmlichen chinesischen IME (New Phonetic) mit Notepad einige chinesische Zeichen eingeben.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Notepad ein. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Screenshot, der Zeichen zeigt, mit denen das I M E-Fenster später für traditionelles Chinesisch besser visualisiert werden können.](images/ime-tc1.png)

2.  Klicken Sie in der Windows-Taskleiste auf den Eingabe Gebiets Schema Indikator, und wählen Sie Chinesisch (Taiwan) aus. Der Indikator zeigt Änderungen an ch an, um widerzuspiegeln, dass die neue Eingabe Sprache Chinesisch (Taiwan) ist.

    ![Eingabe Gebiets Schema Indikator zum Auswählen von Chinesisch (Taiwan)](images/ime-tc2.png)

3.  Platzieren Sie den Cursor in Notepad. Drücken Sie auf der Tastatur die Startseite, sodass sich der Cursor am Anfang der Zeile befindet. Auf dem Tastatur-Typ "S", dann "U". Die folgende Abbildung zeigt die Darstellung der Anzeige. Das kleine vertikale Rechteck ist das Lese Fenster, in dem die aktuelle Lese Zeichenfolge angezeigt wird. Wie in der folgenden Abbildung dargestellt, hat die Lese Zeichenfolge zwei Zeichen als Ergebnis der Eingabe von "S" und "U".

    ![Screenshot, der eine Lese Zeichenfolge mit zwei Zeichen anzeigt.](images/ime-tc3.png)

4.  Geben Sie "3" ein. Notepad weist nun die folgende Anzeige auf. Da S + U + 3 eine komplette Aussprache in traditionellem Chinesisch ist, verfügt der IME über genügend Informationen, um das Zeichen zu antizipieren, das der Benutzer möglicherweise eingegeben hat. Das Lese Fenster verschwindet, weil Sie eine komplette Aussprache eingegeben haben. Am oberen Rand des Notepad-Cursors wird ein Zeichen angezeigt. Dieses Zeichen ist nicht Teil von Notepad, sondern wird in einem anderen Fenster oberhalb von Editor angezeigt und blendet die vorhandenen Zeichen im Editor aus. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in der Zeichenfolge wird als Kompositions Zeichenfolge bezeichnet. Die Kompositions Zeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot, der ein Kompositionsfenster mit unterstrichener Kompositions Zeichenfolge anzeigt.](images/ime-tc4.png)

5.  Geben Sie nun "C", "L" und "3" ein, um ein anderes Zeichen einzugeben. Beachten Sie, dass das Lesefenster angezeigt wird, wenn "C" eingegeben und beim Eingeben von "3" nicht mehr angezeigt wird. Wie unten gezeigt, enthält die Kompositions Zeichenfolge nun zwei Zeichen.

    ![Screenshot, der ein Kompositionsfenster mit einer Kompositions Zeichenfolge und zwei Zeichen unterstrichen zeigt.](images/ime-tc5.png)

6.  Geben Sie den Pfeil nach unten auf der Tastatur ein. Ein Fenster wird oben im Editor angezeigt, wie unten gezeigt. Dieses Fenster wird als Kandidaten Fenster bezeichnet. Es wird eine Liste von Zeichen oder Ausdrücken angezeigt, die der von Ihnen eingegebenen Aussprache entsprechen. Sie können das beabsichtigte Wort aus den Einträgen in der Kandidatenliste auswählen. In diesem Beispiel sind drei Kandidaten Zeichen mit derselben Aussprache verfügbar.

    ![drei Kandidaten Zeichen, die mit derselben Aussprache verfügbar sind](images/ime-tc6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidaten Fenster wird jetzt geschlossen, und die Kompositions Zeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot, der eine mit einem ausgewählten Zeichen aktualisierte Kompositions Zeichenfolge anzeigt.](images/ime-tc7.png)

8.  Drücken Sie die EINGABETASTE. Dadurch wird dem IME mitgeteilt, dass die Komposition fertig ist, und die Zeichenfolge sollte in diesem Beispiel an den Application-Notepad gesendet werden. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über [**WM \_ char**](/windows/desktop/inputdev/wm-char)an Notepad gesendet. Die Unterstreichung ist in der folgenden Abbildung zu sehen, da die beiden gezeigten Zeichen Teil des Texts in Editor sind. Der vorhandene Text "abcdefg" in Notepad wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun erfolgreich zwei herkömmliche chinesische Zeichen mit einem IME eingegeben.

    ![zwei herkömmliche chinesische Zeichen wurden erfolgreich mithilfe eines IME eingegeben.](images/ime-tc8.png)

## <a name="japanese-ime"></a>Japanischer IME

In diesem Abschnitt erfahren Sie, wie Sie mit dem japanischen IME und Notepad einige japanische Zeichen eingeben.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Notepad ein. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Screenshot, der Zeichen anzeigt, die die Visualisierung des I M E-Fensters später für Japanisch verbessern.](images/ime-j1.png)

2.  Klicken Sie mit Notepad als aktive Anwendung auf den Eingabe Gebiets Schema Indikator, und wählen Sie Japanisch aus. Der Indikator zeigt Änderungen an JP an, um widerzuspiegeln, dass die neue Eingabe Sprache Japanisch ist.

    ![Eingabe Gebiets Schema Indikator zum Auswählen von Japanisch](images/ime-j2.png)

3.  Platzieren Sie den Cursor in Notepad. Drücken Sie auf der Tastatur die Startseite, sodass sich der Cursor am Anfang der Zeile befindet. Auf dem Tastatur-Typ "N", dann "I". Die folgende Abbildung zeigt die Darstellung der Anzeige. Da N + I eine komplette Aussprache in Japanisch ist, verfügt das IME über ausreichend Informationen, um das Zeichen vorherzusagen, das der Benutzer möglicherweise eingegeben hat. Am oberen Rand des Notepad-Cursors wird ein Zeichen angezeigt. Dieses Zeichen ist nicht Teil von Notepad, sondern wird in einem anderen Fenster oberhalb von Editor angezeigt und blendet die vorhandenen Zeichen im Editor aus. Dieses neue Fenster wird als Kompositionsfenster bezeichnet, und die Zeichenfolge in der Zeichenfolge wird als Kompositions Zeichenfolge bezeichnet. Die Kompositions Zeichenfolge wird in der Anzeige unterstrichen.

    ![Screenshot, der eine Kompositions Zeichenfolge mit einem unterstrichen mit einem japanischen Zeichen anzeigt.](images/ime-j3.png)

4.  Geben Sie nun "H", "O", "N", "G" und "o" ein, um zwei weitere Zeichen einzugeben. Die Kompositions Zeichenfolge enthält nun vier Zeichen, wie unten gezeigt.

    ![Screenshot, der eine Kompositions Zeichenfolge mit vier japanischen Zeichen zeigt.](images/ime-j4.png)

5.  Drücken Sie die Leertaste. Dies weist den IME an, den eingegebenen Text in Klauseln zu konvertieren. In der folgenden Abbildung konvertiert IME die Aussprache "Nihongo" in eine Klausel, die in Kanji geschrieben ist, d. h. "japanische Sprache".

    ![IME konvertiert japanische Aussprache](images/ime-j5.png)

6.  Drücken Sie die nach-unten-Taste auf der Tastatur. Ein Fenster wird oben im Editor angezeigt, wie unten gezeigt. Dieses Fenster wird als Kandidaten Fenster bezeichnet. Es zeigt eine Liste der Klauseln an, die der von Ihnen eingegebenen Aussprache entsprechen. Sie können das beabsichtigte Wort aus der Liste der Kandidaten auswählen. In diesem Beispiel sind drei Kandidaten Zeichen mit derselben Aussprache verfügbar. Beachten Sie, dass der zweite Eintrag hervorgehoben und die Kompositions Zeichenfolge geändert wird. Dies wird durch die Eingabe des nach-unten-Pfeils verursacht, der der IME mitteilt, dass der Eintrag nach dem zuvor angezeigten Eintrag ausgewählt werden soll.

    ![Screenshot, der das Kandidaten Fenster anzeigt.](images/ime-j6.png)

7.  Geben Sie "2" ein, um den zweiten Eintrag auszuwählen. Das Kandidaten Fenster wird jetzt geschlossen, und die Kompositions Zeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Screenshot, der die mit dem ausgewählten japanischen Zeichen aktualisierte Kompositions Zeichenfolge anzeigt.](images/ime-j7.png)

8.  Drücken Sie die EINGABETASTE. Dadurch wird dem IME mitgeteilt, dass die Komposition fertig ist, und die Zeichenfolge sollte in diesem Beispiel an den Application-Notepad gesendet werden. Das Kompositionsfenster wird geschlossen, und die beiden Zeichen werden über [**WM \_ char**](/windows/desktop/inputdev/wm-char)an Notepad gesendet. Die Unterstreichung ist in der folgenden Abbildung zu sehen, da die beiden gezeigten Zeichen Teil des Texts in Editor sind. Der vorhandene Text "abcdefg" in Notepad wird nach rechts verschoben, da zwei weitere Zeichen eingefügt wurden. Sie haben nun erfolgreich einige japanische Zeichen mit einem IME eingegeben.

    ![mit einem IME wurden einige japanische Zeichen erfolgreich eingegeben.](images/ime-j8.png)

## <a name="korean-ime"></a>Koreanisch IME

In diesem Abschnitt wird beschrieben, wie Sie mit dem koreanischen IME mit Notepad einige koreanische Zeichen eingeben.

1.  Starten Sie den Editor. Geben Sie einige Zeichen in Notepad ein. Diese Zeichen helfen Ihnen, das IME-Fenster später besser zu visualisieren.

    ![Zeichen, die die Visualisierung des IME-Fensters später besser unterstützen](images/ime-k1.png)

2.  Klicken Sie mit Notepad als aktive Anwendung auf den Eingabe Gebiets Schema Indikator, und wählen Sie Koreanisch aus. Der Indikator zeigt Änderungen an Ko an, um zu reflektieren, dass die neue Eingabe Sprache Koreanisch ist.

    ![Eingabe Gebiets Schema Indikator zum Auswählen von Koreanisch](images/ime-k2.png)

3.  Platzieren Sie den Cursor in Notepad. Drücken Sie auf der Tastatur die Startseite, sodass sich der Cursor am Anfang der Zeile befindet, und geben Sie dann "G" ein. Die folgende Abbildung zeigt die Darstellung der Anzeige. Das phonetische Element, das "G" entspricht, wird im Editor angezeigt und mit einem Block Cursor hervorgehoben. Dieses markierte Zeichen wird als Kompositions Zeichenfolge bezeichnet. Beachten Sie, dass im Gegensatz zum IME für andere Sprachen die Kompositions Zeichenfolge an Notepad gesendet und Links vom vorhandenen Text eingefügt wird, sobald der Benutzer ein einzelnes phonetisches Element eingibt.

    ![Screenshot, der eine Kompositions Zeichenfolge anzeigt, bei der ein Zeichen links neben dem vorhandenen Text eingefügt wurde.](images/ime-k3.png)

4.  Zu diesem Zeitpunkt besteht die Kompositions Zeichenfolge aus einem zwischen Zeichen, da alle zusätzlichen phonetischen Elemente, die vom Benutzer eingegeben werden, die Kompositions Zeichenfolge an Ort und Stelle ändern. Geben Sie nun "K" und dann "S" ein. Beachten Sie, dass sich das zwischen Zeichen mit jedem Tastatur Strich ändert.

    ![Kompositions Zeichenfolge](images/ime-k4.png)

5.  Drücken Sie nun die Rechte STRG-Taste. Ein Kandidaten Fenster wird angezeigt, in dem die Hanja-Zeichen aufgelistet sind, die Sie für die eingegebene Aussprache auswählen können: G + K + S.

    ![Screenshot, der ein Kandidaten Fenster mit einer Liste von Hanja-Zeichen anzeigt, die Sie unten im Fenster auswählen können.](images/ime-k5.png)

6.  Geben Sie die Zahl "1" ein, um den ersten Eintrag in der Liste auszuwählen. Das Kandidaten Fenster wird geschlossen, und die Kompositions Zeichenfolge wird mit dem ausgewählten Zeichen aktualisiert.

    ![Kompositions Zeichenfolge mit ausgewähltem Zeichen aktualisiert](images/ime-k6.png)

7.  Geben Sie "r", "N" und "r" ein. Drücken Sie dann die Rechte STRG-Taste, um ein anderes Zeichen einzugeben.

    ![Kandidaten Fenster](images/ime-k7.png)

8.  Geben Sie "1" ein, um den ersten Eintrag auszuwählen. Sie haben nun erfolgreich zwei koreanische Zeichen mit einem IME eingegeben. Die koreanischen Zeichen sind bereits Teil der Text Zeichenfolge in Notepad.

    ![zwei koreanische Zeichen wurden erfolgreich mithilfe eines IME eingegeben.](images/ime-k8.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Betriebssystem**                | Windows XP                                                                                                 |
| **Verfügbarer Festplattenspeicher**       | Mindestens 230 MB                                                                                            |
| **Speicherorte für fremde Sprachdateien** | Windows XP-Installations-oder Netzwerk Speicherort mit Windows XP-Installationsdateien                |
| **Time**                            | Etwa zehn Minuten für die Installation von fremd Sprachdateien; alle zehn Minuten, um vier verschiedene IMEs zu überprüfen. |



 

 

 
