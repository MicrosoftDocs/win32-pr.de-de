---
title: Ausgabe Probleme
description: Ausgabe Probleme
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314393"
---
# <a name="output-problems"></a>Ausgabe Probleme

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>Das Zeichen verlässt Bilder oder Pfade, wenn es verschoben wird.

Wenn ein agentzeichen animiert wird, müssen die Anwendungsfenster hinter dem-Zeichen rechtzeitig aktualisiert werden. Wenn das Zeichen über den Bildschirm bewegt wird, ist es normal, dass manchmal einige verbleibende Bilder angezeigt werden, die schnell verschwinden (abhängig von der Geschwindigkeit des PCs und der Anwendungen, die Sie ausführen). Wenn dies nicht der Fall ist, kann dies folgende Ursachen haben:

-   Ihr System erfüllt nicht die Mindestsystemanforderungen für den-Agent.
-   Das Anwendungsfenster hinter dem Zeichen verarbeitet Updates nicht rechtzeitig. Ziehen Sie das Zeichen über den Desktop oder das Ordner Fenster, oder schließen Sie einige Ihrer Anwendungen. Wenn eine spürbare Verbesserung angezeigt wird, ist das Problem möglicherweise unvermeidlich.
-   Möglicherweise ist die offizielle Version von Microsoft Internet Explorer 4,0 (oder höher) nicht installiert. Frühe vorab Versionen von Internet Explorer 4,0 haben das Aktualisieren des Bildschirms nicht ordnungsgemäß behandelt. Dies würde dazu führen, dass auf dem Bildschirm verbleibende Bilder angezeigt werden. Um das Problem zu beheben, installieren Sie die neueste offizielle Version von Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Möglicherweise gibt es ein Problem mit den Bildschirm Treibern oder der Hardware Ihres Systems. Stellen Sie sicher, dass Sie über die neuesten Treiber für Ihre Grafikhardware verfügen. Wenn das Problem weiterhin besteht, können Sie sich an Ihren PC-Anbieter wenden.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>Das Zeichen erzeugt keine Audioausgabe, wenn es spricht.

Dieses Symptom kann mehrere Gründe haben. Versuchen Sie Folgendes, um das Problem zu isolieren:

-   Vergewissern Sie sich, dass Ihre Referenten angeschlossen sind und Ihre Soundkarte mit Windows kompatibel ist. Es empfiehlt sich, diese mit einer anderen Sound Anwendung zu testen, um zu bestätigen, dass die Audioausgabe ordnungsgemäß funktioniert.
-   Stellen Sie sicher, dass die agentaktivierte Anwendung oder Webseite Spracheingaben unterstützt. Nicht alle Beispielseiten unterstützen Spracheingaben. Halten Sie die Abhör Taste gedrückt (in der Regel ist dies der Schiebe Sperr Schlüssel, sofern Sie ihn nicht geändert haben). Unter dem Zeichen sollte ein Popup Fenster angezeigt werden. Der Text im Tipp gibt Aufschluss über den Abhör Zustand des Zeichens. Wenn kein Tipp angezeigt wird, unterstützt die Anwendung oder Webseite keine Spracheingaben, oder Sie haben keine kompatible Sprach-Engine installiert. Wenn der Tipp angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der Sprachbefehle des Zeichens. Wenn Sie nicht wissen, welche Sprachbefehle verfügbar sind, geben Sie die Abhör Taste frei, klicken Sie mit der rechten Maustaste auf das Zeichen, und wählen Sie dann im Popupmenü die Option Sprachbefehle öffnen aus. Wenn der Befehl nicht angezeigt wird, ist die Sprachunterstützung für die verwendete Anwendung oder Webseite nicht verfügbar. Wenn er angezeigt wird, halten Sie die überwachende Taste gedrückt. Wenn der lausch Text unter dem-Zeichen angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der im Fenster aufgeführten Befehle an. Wenn das Zeichen nicht antwortet, fahren Sie mit dem nächsten Schritt fort.
-   Vergewissern Sie sich, dass zurzeit keine andere Anwendung das Audioausgabegerät verwendet.
-   Vergewissern Sie sich, dass das von Ihnen verwendete Zeichen für die gesprochene Ausgabe konfiguriert wurde. (Möglicherweise müssen Sie sich bei der Website oder dem Anwendungs Lieferanten überprüfen.)
-   Überprüfen Sie, ob die Microsoft-Agenteinstellungen für die gesprochene Ausgabe aktiviert sind
-   Wenn für das Zeichen eine Text-zu-Sprache-Engine (TTS) verwendet wird, um eine gesprochene Ausgabe zu entwickeln, vergewissern Sie sich, dass Sie eine kompatible TTS-Engine installiert haben. Wenn z. b. als Internet Explorer 4,0-Add-on-Komponente installiert wird, werden nur die Kernkomponenten des Microsoft-Agents installiert. Die Kernkomponenten enthalten keine Text-zu-Sprache-Engine. Ohne diese TTS-Engine (ein Microsoft Speech API-kompatibles Modul) ergeben Microsoft-Agent-Beispiel Zeichen keine gesprochene Ausgabe.
-   Vergewissern Sie sich, dass die Verwendung von MIDI durch den Microsoft-Agent den Audiokanal nicht blockiert (Weitere Informationen finden Sie im nächsten Thema, wenn der Microsoft-Agent ausgeführt wird, wenn der Microsoft-Agent ausgeführt wird).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Anwendungen, die mit "MIDI" wiedergeben, haben keine Audioausgabe, wenn Microsoft Agent ausgeführt wird

Der Microsoft-Agent verwendet beim Drücken der abzurufenden Taste einen Ton, um einen Ton zu spielen. Wenn Sie feststellen, dass dies zu anderen Anwendungen, die mit der Verwendung von "MIDI" oder mit der Spracheingabe beeinträchtigt werden, beeinträchtigt, können Sie den Wiedergabe Ton deaktivieren, wenn Sie die Option in den Eigenschaften des Microsoft-Agents

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Ich erhalte die folgende Meldung: ein ausgehender-Vorgang kann nicht durchgeführt werden, da die Anwendung einen Eingabe synchronen-Befehl sendet.

Diese Meldung kann unter den folgenden Umständen auftreten:

Wenn eine Webseite mit dem Microsoft-Agent geschlossen wird (indem Sie mit der rechten Maustaste auf den Eingabebereich der Seite klicken und im Popupmenü schließen auswählen), kann dies vorkommen. Dies liegt an einem Zeit überschreitungsproblem zwischen dem Agent und dem Browser, wenn Sie gleichzeitig heruntergefahren werden. Der Fehler ist harmlos. Klicken Sie auf OK, um die Meldung zu schließen.

Das ist aufgetreten, als die agentaktivierte Webseite (oder Anwendung) versuchte, eine bestimmte Text-zu-Sprache-Engine (TTS) anzufordern. Speechapi.dll wurde nicht installiert.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Die Sprach-Engines scheinen nicht mit dem Microsoft-Agent in Windows XP zu funktionieren?

Der Microsoft-Agent verwendet SAPI 4,0, um Sprachdienste bereitzustellen. Windows XP ist nun jedoch mit SAPI 5,0 ausgeliefert, das keine abwärts Kompatibilitäts Unterstützung für seine Vorgänger Umgebung bereitstellt. Glücklicherweise können SAPI 4,0 und SAPI 5,0 zusammen auf demselben Windows XP-Computer zusammen vorhanden sein.

Damit die Sprachmodule mit dem Microsoft-Agent in Windows XP funktionieren, installieren Sie zunächst die [SAPI 4,0-Lauf Zeit Binärdateien](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe), und installieren Sie dann die jeweiligen Sprach-Engines.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Die Sprach-Engines, die für die Arbeit mit dem Microsoft-Agent verwendet werden, bis ich auf Windows XP aktualisiert Was ist passiert?

Sehen Sie sich die vorherige Frage und Antwort an. Der Upgradeprozess von Windows XP hat möglicherweise die Unterstützung von SAPI 4,0 entfernt, die bereits auf dem Computer vorhanden ist. Installieren Sie einfach nach dem Upgrade auf Windows XP die Sprachmodule SAPI 4,0 Runtime und SAPI 4,0 erneut.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Auf dem Computer, auf dem Windows XP (oder Windows 2000) ausgeführt wird, habe ich die TTS3000 Text-zu-Sprache-Engines installiert und die Programmierung entsprechend ihren Verwendungszwecke ordnungsgemäß bearbeitet. Die Zeichen des Microsoft-Agents sprechen mit diesen TTS3000-Text-zu-Sprache-Engines in der Regel, wenn e oder andere lokale Administratoren angemeldet sind, aber nicht, wenn andere Benutzer *ohne Administrator Rechte* an diesem Computer angemeldet sind. Unter Windows 98 und Windows Me funktionieren diese TTS3000-Text-zu-Sprache-Engines für beide Gruppen von Benutzern ordnungsgemäß. Wie kann ich dieses Problem beheben?

Sie müssen die Sicherheits Berechtigungen für einige der Registrierungsschlüssel der TTS3000-Text-zu-Sprache-Engines konfigurieren, um die Verwendung durch Benutzerkonten ohne Administrator Rechte zu ermöglichen. Dies kann mit dem Registrierungs-Editor des Betriebssystems erreicht werden.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Ich folgte dem Verfahren, das als Lösung für das in der vorherigen Frage beschriebene Problem beschrieben wurde. Dies funktionierte gut, damit die Microsoft-agentzeichen mit den TTS3000-Text-zu-Sprache-Engines in Echtzeit kommunizieren konnten, wenn Benutzer *ohne Administrator Rechte* auf dem Computer mit Windows XP (oder Windows 2000) angemeldet waren. Nun, Monate später, werden dieselben TTS3000-Text-zu-Sprache-Engines nicht mehr funktionieren. Was ist passiert?

Wenn Sie das beschriebene Verfahren für die vorherige Frage befolgt haben, haben die Benutzerkonten ohne Administrator Berechtigung die Berechtigung Vollzugriff für die erforderlichen Registrierungsschlüssel gewährt. Es ist möglich, dass einer dieser Benutzer die Werte wissentlich oder unwissentlich bearbeitet hat, die Berechtigungen erneut geändert hat oder sogar den Registrierungsschlüssel vollständig gelöscht hat.

Überprüfen Sie, ob diese Registrierungsschlüssel und ihre Berechtigungen seit bearbeitet, gelöscht oder anderweitig geändert wurden. Ändern Sie diese Registrierungsschlüssel und deren Berechtigungen ggf. erneut, oder installieren Sie die TTS3000-Text-zu-Sprache erneut.

 

 




