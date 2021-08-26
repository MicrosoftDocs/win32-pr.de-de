---
title: Definieren eines neuen Zeichens
description: Definieren eines neuen Zeichens
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1f3d9aee78893ebc4796781947be92366baa10b9ad1e123a73121df24646ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963100"
---
# <a name="defining-a-new-character"></a>Definieren eines neuen Zeichens

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Führen Sie den Zeichen-Editor des -Agents aus, um ein neues Zeichen zu definieren. Wenn Sie eine vorhandene Zeichendatei geladen haben, wählen Sie **im** Menü Datei den Befehl **Neu** aus. Dadurch wird ein Untermenü von Auswahlmöglichkeiten angezeigt. Wenn Sie ein Zeichen für ihre eigene Verwendung erstellen, wählen Sie **Benutzerdefiniertes Zeichen aus.** Wenn Sie ein Zeichen erstellen möchten, das als Standardzeichen des -Agents verwendet werden kann, wählen Sie **Standardzeichen aus.** Dadurch wird der Editor mit allen erforderlichen Animationsnamen und Animationszustandszuweisungen vorkonfiguriert und die Option **Standardanimation** festgelegt. Wenn Sie das Office-Assistentenzeichen auswählen, ist der Editor entsprechend mit den Animationsnamen und der Animationszustandszuweisung vorkonfiguriert, die für ein Office Assistant-Zeichen erforderlich sind. Diese Aktion wählt das **Zeichensymbol** in der Struktur aus und zeigt die Eigenschaftenseiten auf der rechten Seite des Fensters an. In den folgenden Abschnitten wird beschrieben, wie Sie die Eigenschaften Ihres Zeichens festlegen und Animationen für das Zeichen erstellen.

### <a name="setting-your-characters-general-information"></a>Festlegen der allgemeinen Informationen ihres Zeichens

Um mit dem Definieren eines Zeichens zu beginnen, geben Sie den Namen des Zeichens in das Textfeld **Name** ein (maximal 32 Zeichen). Da Microsoft Agent den Namen verwendet, um Benutzern den Zugriff auf das Zeichen zu ermöglichen, geben Sie einen benutzerfreundlichen Namen an. Geben Sie einen Namen an, der mit herkömmlicher Schreibweise ausgesprochen werden kann, oder Sie können die Spracheingabe für das Zeichen deaktivieren. Sie können auch eine kurze optionale Beschreibung (256 Zeichen) für Ihr Zeichen im Textfeld Beschreibung angeben. Der Server macht das, was Sie im Textfeld Beschreibung eingeben, für Clientanwendungen verfügbar.

Sie können ihre eigenen Daten auch als Teil Ihres Zeichens speichern, indem Sie das Feld ExtraData verwenden. Mit dieser Funktion können Sie spezielle Informationen zu Ihren Zeichen oder anderen Daten enthalten. Nach der Kompilierung mit dem Zeichen-Editor kann mithilfe der ExtraData-Eigenschaft zur Laufzeit auf diese Informationen zugegriffen werden, wenn das Zeichen geladen wird.

Sie können den Namen, die Beschreibung und zusätzliche Dateninformationen des Zeichens basierend auf der Sprach-ID-Einstellung des Zeichens festlegen. Wenn Sie diese Daten für eine andere Sprache festlegen, wählen Sie Sprache aus, und geben Sie den Text ein. Außerdem müssen die Sprachcodepages auf dem System installiert sein, auf dem Sie die Zeichendatei erstellen. Wenn Sie dies nicht vornehmen, werden die entsprechenden Spracheinstellungen nicht in die kompilierte Zeichendatei aufgenommen. Sie müssen keine Informationen in anderen Sprachen bereitstellen. Wenn diese Eigenschaften zur Laufzeit mithilfe der -Agent-API abgefragt werden und es keine spezifischen Einstellungen für diese Sprache gibt, werden die Einstellungen für Englisch (Standard) zurückgegeben.

### <a name="setting-your-characters-output-options"></a>Festlegen der Ausgabeoptionen ihres Zeichens

Wenn Sie die Option Standardanimation festlegen, überprüft der Zeichen-Editor, ob Sie beim Erstellen des Zeichens alle erforderlichen Animationen und Animationszustandszuweisungen für ein Standardzeichen eingeschlossen haben. Wenn etwas fehlt, werden in einem Meldungsfeld die fehlenden Elemente aufgeführt. Weitere Informationen zum Standardanimation-Satz finden Sie unter [**Entwerfen von Zeichen für Microsoft Agent**](designing-characters-for-microsoft-agent.md).

Für die gesprochene Ausgabe Ihres Zeichens bietet Microsoft Agent die Wahl zwischen einer synthetisierten TTS-Stimme (Text-to-Speech) oder einer Stimme, die aufgezeichnete Audiodateien verwendet. Wenn Sie eine synthetisierte Stimme verwenden möchten, aktivieren Sie die Option Synthetisierte Sprache für Sprachausgabe verwenden. Dadurch wird eine Voice-Seite zum Auswählen der Merkmale der Stimme hinzugefügt. Wählen Sie die Seite Stimme aus, und verwenden Sie die Steuerelemente auf der Seite, um eine Stimme, Geschwindigkeit und Tonhöhe aller kompatiblen TTS-Engines auszuwählen, die Sie installiert haben. Der Bereich der Sprachparameter, die Sie auswählen können, hängt von TTS-Engines ab. Wenn Sie noch keine TTS-Engine installiert haben, ist die Liste Sprach-ID leer. Sie müssen eine TTS-Engine installiert haben, bevor Sie die Spracheinstellungen Ihres Zeichens im Agent-Zeichen-Editor definieren.

Wenn Sie eine TTS-Engine für die Ausgabe Ihres Zeichens verwenden möchten, müssen Sie diese Engine auch auf dem System des Benutzers installieren. Wenn Sie eine Stimme basierend auf einer bestimmten TTS-Engine auswählen, aber der Benutzer eine andere TTS-Engine installiert hat, versucht der Server, die Stimme basierend auf den Merkmalen, die Sie im Agent-Zeichen-Editor definiert haben, zu finden.

Wenn Sie die Verwendung aufgezeichneter Sounddateien planen (. WAV-Dateien) für die gesprochene Ausgabe Ihres Zeichens müssen Sie die Option Synthetisierte Sprache für Sprachausgabe verwenden nicht aktivieren. Stattdessen müssen Sie die gesprochenen Ausgabeaudiodateien separat aufzeichnen und aus Ihrem Anwendungscode laden.

Mit der **Option Wortsprechblase** verwenden können Sie bestimmen, ob Sie einen Wortsprechblasen für Ihr Zeichen unterstützen möchten. Dieses Feature kann auch zur Laufzeit festgelegt werden.

Wenn die **Option Wortsprechblase** verwenden ausgewählt ist, können Sie auf die Seite **Word Balloon (Wortsprechblasen)** zugreifen. Mit den Optionen auf der **Seite Word Balloon** (Wortsprechblasen) können Sie die Standardmerkmale des Wortsprechblasens ändern. Mit **der Einstellung Zeichen** pro Zeile können Sie die Breite des Balloons basierend auf der durchschnittlichen Anzahl von Zeichen pro Zeile definieren. Sie können die Standardhöhe entweder basierend auf einer festen Anzahl von Zeilen festlegen, die Sie gleichzeitig anzeigen möchten, oder basierend auf der automatischen Größe des Texts, den Sie in der [**Speak-Methode festlegen.**](speak-method.md) Sie können auch festlegen, ob der Sprechblasen nach Abschluss einer **Speak-Methode** automatisch ausblendet und ob der Sprechblasen automatisch Wörter an die Sprachausgabe-Geschwindigkeitseinstellung des Zeichens "beschleunigt" oder anzeigt.

Auf der Seite Wortsprechblasen können Sie auch die Standardschriftart für die Wortsprechblase des Zeichens und die Anzeigefarben des Sprechblasens festlegen.  Beachten Sie jedoch, dass Benutzer die Schriftarteinstellungen für Wortsprechblasen mithilfe des Microsoft Agent-Eigenschaftenblatts überschreiben können.

### <a name="setting-your-characters-identifier"></a>Festlegen des Zeichenbezeichners

Jedes Zeichen erfordert einen eindeutigen Bezeichner (GUID). Der Server verwendet den Bezeichner, um Zeichen zu unterscheiden. Wenn Sie ein neues Zeichen erstellen, erstellt der Editor automatisch einen neuen Bezeichner für Das Zeichen. Sie müssen den Bezeichner eines Zeichens nur ändern, wenn Sie die Zeichendefinitionsdatei eines anderen Zeichens kopiert haben oder wenn Sie absichtlich ein Zeichen von einer früheren Version unterscheiden möchten. Um den Bezeichner eines Zeichens zu ändern, klicken Sie auf die Schaltfläche Neue GUID, und der Editor generiert einen neuen Bezeichner.

 

 




