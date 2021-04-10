---
title: Definieren eines neuen Zeichens
description: Definieren eines neuen Zeichens
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586312ac9d913a27d2df0be112cbcf92c47f4fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947836"
---
# <a name="defining-a-new-character"></a>Definieren eines neuen Zeichens

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Um ein neues Zeichen zu definieren, führen Sie den Agent-Zeichen-Editor aus. Wenn Sie eine vorhandene Zeichen Datei geladen haben, wählen Sie im Menü **Datei** den Befehl **neu** aus. Dadurch wird ein Untermenü mit Auswahlmöglichkeiten angezeigt. Wenn Sie ein Zeichen für die eigene Verwendung erstellen, wählen Sie **benutzerdefiniertes Zeichen** aus. Wenn Sie ein Zeichen erstellen möchten, das als agentstandardzeichen verwendet werden kann, wählen Sie **Standard Zeichen** aus. Dadurch wird der Editor mit allen erforderlichen Animations Namen und Animations Zustands Zuweisungen vorkonfiguriert, und die Option **unterstützt Standard-Animations Satz** wird festgelegt. Wenn Sie Office Assistant-Zeichen auswählen, wird der Editor entsprechend mit den Animations Namen und der Animations Zustands Zuweisung vorkonfiguriert, die für ein Office Assistant-Zeichen erforderlich ist. Diese Aktion wählt das **Zeichen** Symbol in der Struktur aus und zeigt die Eigenschaften Seiten auf der rechten Seite des Fensters an. In den folgenden Abschnitten wird beschrieben, wie Sie die Eigenschaften des Zeichens festlegen und Animationen für das Zeichen erstellen.

### <a name="setting-your-characters-general-information"></a>Festlegen der allgemeinen Informationen Ihres Zeichens

Um mit der Definition eines Zeichens zu beginnen, geben Sie den Namen des Zeichens in das Textfeld **Name** ein (maximal 32 Zeichen). Da der Microsoft-Agent den Namen verwendet, um Benutzern den Zugriff auf das Zeichen zu gestatten, geben Sie einen benutzerfreundlichen Namen an. Geben Sie einen Namen an, der mit herkömmlicher Schreibweise ausgesprochen werden kann, oder Sie können die Spracheingabe für das Zeichen deaktivieren. Sie können auch eine kurze optionale Beschreibung (256 Zeichen) für das Zeichen im Textfeld Beschreibung angeben. Der Server macht die im Textfeld Beschreibung für Client Anwendungen eingegebenen Elemente verfügbar.

Sie können Ihre eigenen Daten auch als Teil Ihres Zeichens mit dem ExtraData-Feld speichern. Sie können diese Funktion verwenden, um besondere Informationen über Ihr Zeichen oder andere Daten einzuschließen. Nach der Kompilierung mit dem Zeichen-Editor können Sie mithilfe der ExtraData-Eigenschaft zur Laufzeit auf diese Informationen zugreifen, wenn das Zeichen geladen wird.

Sie können den Namen, die Beschreibung und zusätzliche Daten Informationen des Zeichens basierend auf der Sprach-ID-Einstellung des Zeichens festlegen. Um diese Daten für eine andere Sprache festzulegen, wählen Sie Sprache aus, und geben Sie den Text ein. Sie müssen auch die sprach-Codepages auf dem System installiert haben, in dem Sie die Zeichen Datei erstellen. Wenn Sie nicht über die entsprechenden Spracheinstellungen verfügen, werden Sie in der kompilierten Zeichen Datei nicht berücksichtigt. Sie müssen keine Informationen in anderen Sprachen bereitstellen. Wenn diese Eigenschaften zur Laufzeit mithilfe der Agent-API abgefragt werden und keine spezifischen Einstellungen für diese Sprache vorhanden sind, werden die Einstellungen für Englisch (Standard) zurückgegeben.

### <a name="setting-your-characters-output-options"></a>Festlegen der Ausgabeoptionen für das Zeichen

Wenn Sie die Option Standard Animations Satz unterstützt festlegen, prüft der Zeichen Editor, ob Sie alle erforderlichen Animationen und Animations Zustands Zuweisungen für ein Standard Zeichen eingeschlossen haben, wenn Sie versuchen, das Zeichen zu erstellen. Wenn etwas fehlt, werden in einem Meldungs Feld die fehlenden Elemente aufgelistet. Ausführliche Informationen zum Standard Animations Satz finden Sie unter [**Entwerfen von Zeichen für den Microsoft-Agent**](designing-characters-for-microsoft-agent.md).

Bei der gesprochenen Ausgabe Ihres Zeichens bietet der Microsoft-Agent die Wahl einer Text-zu-Sprache-Stimme (TTS) oder einer Stimme an, die aufgezeichnete Audiodateien verwendet. Wenn Sie eine Sprachausgabe mit synthetischer Sprache verwenden möchten, aktivieren Sie die Option Verwendung synthetischer Sprache für die Sprachausgabe verwenden. Dadurch wird eine sprach Seite zum Auswählen der Merkmale der Stimme hinzugefügt. Wählen Sie die Seite Stimme aus, und wählen Sie mithilfe der Steuerelemente auf der Seite eine Stimme, eine Geschwindigkeit und eine Tonhöhe aller kompatiblen TTS-Engines aus, die Sie installiert haben. Der Bereich der sprach Parameter, die Sie auswählen können, hängt von den TTS-Engines ab. Wenn Sie noch keine TTS-Engine installiert haben, ist die Liste der Sprach-IDs leer. Sie müssen eine TTS-Engine installiert haben, bevor Sie die Spracheinstellungen Ihres Zeichens im Agent-Zeichen-Editor definieren.

Wenn Sie beabsichtigen, eine TTS-Engine für die Ausgabe Ihres Zeichens zu verwenden, müssen Sie diese Engine auch auf dem System des Benutzers installieren. Wenn Sie eine Stimme für eine bestimmte TTS-Engine auswählen, aber für den Benutzer eine andere TTS-Engine installiert ist, versucht der Server, die Stimme basierend auf den Merkmalen, die Sie im Agent-Zeichen-Editor definiert haben, abzugleichen.

Wenn Sie die Verwendung von aufgezeichneten Audiodateien () planen. WAV-Dateien) für die gesprochene Ausgabe Ihres Zeichens müssen Sie nicht die Option synthetischer Sprachausgabe verwenden aktivieren. Stattdessen müssen Sie die gesprochenen Ausgabeaudiodateien separat aufzeichnen und aus Ihrem Anwendungscode laden.

Mit der Option **Word** -Sprechblase verwenden können Sie feststellen, ob Sie eine Wort Sprechblase für Ihr Zeichen unterstützen möchten. Diese Funktion kann auch zur Laufzeit festgelegt werden.

Wenn die Option Word-Sprechblase **verwenden** aktiviert ist, können Sie auf die **Wort** Sprechblasen Seite zugreifen. Mit den Optionen auf der Seite **Wort** Sprechblase können Sie die Standardeigenschaften der Word-Sprechblase ändern. Mit der Einstellung **Zeichen pro Zeile** können Sie die Breite der Sprechblase basierend auf der durchschnittlichen Anzahl von Zeichen pro Zeile definieren. Sie können die Standardhöhe basierend auf einer festgelegten Anzahl von Zeilen, die Sie gleichzeitig anzeigen möchten, oder automatisch mit dem Text festlegen, den Sie in der [**Sprech**](speak-method.md) Methode angeben. Sie können auch festlegen, ob die Sprechblase automatisch ausgeblendet wird, **nachdem eine Sprech** Methode abgeschlossen wurde, und ob die Sprechblase automatisch die Wörter der Sprachausgabe Geschwindigkeit des Zeichens anzeigt.

Auf der **Word** -Sprechblasen Seite können Sie auch die Standard Schriftart für die Wort Sprechblase des Zeichens und die Anzeige Farben der Sprechblase festlegen. Beachten Sie jedoch, dass Benutzer die Schriftart Einstellungen der Word-Sprechblase mithilfe der Eigenschaften Seite des Microsoft-Agents überschreiben können.

### <a name="setting-your-characters-identifier"></a>Festlegen des Bezeichners für den Zeichensatz

Jedes Zeichen erfordert einen eindeutigen Bezeichner (GUID). Der Server verwendet den Bezeichner, um Zeichen zu unterscheiden. Wenn Sie ein neues Zeichen erstellen, erstellt der Editor automatisch einen neuen Bezeichner für das Zeichen. Sie müssen den Bezeichner eines Zeichens nur ändern, wenn Sie die Zeichen Definitionsdatei eines anderen Zeichens kopiert haben oder wenn Sie absichtlich ein Zeichen von einer früheren Version unterscheiden möchten. Wenn Sie den Bezeichner eines Zeichens ändern möchten, klicken Sie auf die Schaltfläche neue GUID, und der Editor generiert einen neuen Bezeichner.

 

 




