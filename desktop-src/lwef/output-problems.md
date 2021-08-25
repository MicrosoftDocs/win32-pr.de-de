---
title: Ausgabeprobleme
description: Ausgabeprobleme
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f19afb705e1d71b3b47bc44c35a51cb83029932287c582b0481ff6a5b078049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961050"
---
# <a name="output-problems"></a>Ausgabeprobleme

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>Das Zeichen hinterlässt Bilder oder Spuren, wenn es bewegt wird.

Wenn ein Agent-Zeichen animiert wird, müssen sich die Anwendungsfenster hinter dem Zeichen rechtzeitig selbst aktualisieren. Wenn das Zeichen über den Bildschirm bewegt wird, ist es normal, manchmal einige Restbilder zu sehen, die schnell verschwinden (abhängig von der Geschwindigkeit Ihres PCs und der ausgeführten Anwendungen). Wenn dies nicht der Grund ist, kann Folgendes die Ursache sein:

-   Ihr System erfüllt nicht die Mindestsystemanforderungen für den -Agent.
-   Im Anwendungsfenster hinter dem Zeichen werden Updates nicht rechtzeitig behandelt. Versuchen Sie, das Zeichen über den Desktop oder ein Ordnerfenster zu ziehen, oder fahren Sie einige Ihrer Anwendungen herunter. Wenn Sie eine spürbare Verbesserung sehen, ist das Problem möglicherweise unvermeidbar.
-   Möglicherweise ist das offizielle Release von Microsoft Internet Explorer 4.0 (oder höher) nicht installiert. Frühe Vorabversionen von Internet Explorer 4.0 haben das Aktualisieren des Bildschirms nicht ordnungsgemäß verarbeitet. Dies würde zu Restbildern des Zeichens führen, das auf dem Bildschirm verbleibt. Um das Problem zu beheben, installieren Sie das neueste offizielle Release des Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Möglicherweise liegt ein Problem mit den Bildschirmtreibern oder der Hardware Ihres Systems vor. Stellen Sie sicher, dass Sie über die neuesten Treiber für Ihre Grafikhardware verfügen. Wenn das Problem weiterhin besteht, sollten Sie sich an Ihren PC-Anbieter wenden.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>Das Zeichen erzeugt keine Audioausgabe, wenn es spricht.

Dieses Symptom kann mehrere Ursachen haben. Versuchen Sie Folgendes, um das Problem zu isolieren:

-   Vergewissern Sie sich, dass Ihre Lautsprecher angeschlossen sind und Ihre Soundkarte mit der Windows. Es ist eine gute Idee, sie mit einer anderen Soundanwendung zu testen, um zu bestätigen, dass die Audioausgabe ordnungsgemäß funktioniert.
-   Stellen Sie sicher, dass die Agent-fähige Anwendung oder Webseite Spracheingaben unterstützt. Nicht alle Beispielseiten unterstützen Spracheingaben. Halten Sie die Abhörtaste gedrückt (in der Regel ist dies die Bildlaufsperre, sofern Sie sie nicht geändert haben). Unter dem Zeichen sollte ein Popupfenster angezeigt werden. Der Text im Tipp gibt auf den Lauschenzustand des Zeichens hin. Wenn kein Tipp angezeigt wird, unterstützt entweder die Anwendung oder Webseite keine Spracheingabe, oder Sie haben keine kompatible Sprach-Engine installiert. Wenn der Tipp angezeigt wird und angibt, dass das Zeichen lausst, sprechen Sie einen der Sprachbefehle des Zeichens. Wenn Sie nicht wissen, welche Sprachbefehle verfügbar sind: Lassen Sie die Taste Lauschen, klicken Sie mit der rechten Maustaste auf das Zeichen, und wählen Sie dann im Popupmenü Fenster für Sprachbefehle öffnen aus. Wenn der Befehl nicht angezeigt wird, ist die Sprachunterstützung für die von Ihnen verwendete Anwendung oder Webseite nicht verfügbar. Wenn er angezeigt wird, drücken Sie die Abhörtaste, und halten Sie sie wieder gedrückt. Wenn der Lauschen-Tipp unter dem Zeichen angezeigt wird und angibt, dass das Zeichen lausiert, sprechen Sie einen der im Fenster aufgeführten Befehle. Wenn das Zeichen nicht antwortet, fahren Sie mit dem nächsten Schritt fort.
-   Stellen Sie sicher, dass derzeit keine andere Anwendung das Audioausgabegerät verwendet.
-   Vergewissern Sie sich, dass das von Ihnen verwendete Zeichen für die gesprochene Ausgabe konfiguriert wurde. (Möglicherweise müssen Sie sich bei der Website oder dem Anwendungsanbieter informieren.)
-   Überprüfen Sie, ob Ihre Microsoft Agent-Einstellungen für gesprochene Ausgaben aktiviert sind.
-   Wenn das Zeichen eine TTS-Engine (Text-to-Speech) verwendet, um gesprochene Ausgabe zu erzeugen, stellen Sie sicher, dass Sie eine kompatible TTS-Engine installiert haben. Bei der Installation als Internet Explorer 4.0-Add-On-Komponente werden beispielsweise nur die Kernkomponenten von Microsoft Agent installiert. Die Kernkomponenten enthalten keine Text-to-Speech-Engine. Ohne diese TTS-Engine (eine mit der Microsoft Speech-API kompatible Engine) erzeugen Microsoft Agent-Beispielzeichen keine gesprochene Ausgabe.
-   Vergewissern Sie sich, dass der Audiokanal nicht durch den Microsoft Agent blockiert wird (weitere Informationen finden Sie im nächsten Thema Anwendungen, die DIE AUDIOausgabe nicht wiedergeben, wenn Microsoft Agent ausgeführt wird).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Anwendungen, die DIE -Audioausgabe wiedergeben, haben keine Audioausgabe, wenn Microsoft Agent ausgeführt wird.

Microsoft Agent verwendet DABEI, um einen Ton zu geben, wenn Sie die Abhörtaste drücken. Wenn Sie feststellen, dass dies andere Anwendungen beeinträchtigt, die DIE wiedergeben oder spracheingaben beeinträchtigen, können Sie die Option Ton wiedergeben, wenn Sie sprechen können in den Microsoft Agent-Eigenschaften deaktivieren.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Die folgende Meldung wird angezeigt: Ein ausgehender Aufruf kann nicht ausgeführt werden, da die Anwendung einen eingabesynchronen Aufruf weitersendet.

Diese Meldung kann unter den folgenden Umständen auftreten:

Wenn eine Webseite mit Microsoft Agent geschlossen wird (indem Sie mit der rechten Maustaste auf den Taskleisteneintrag der Seite klicken und im Popupmenü Schließen auswählen), kann dies auftreten. Dies liegt an einem Zeitsteuerungsproblem zwischen agent und dem Browser, wenn sie gleichzeitig heruntergefahren werden. Der Fehler ist unbedenklich. Klicken Sie auf OK, um die Meldung zu ver verworfen.

Die Agent-fähige Webseite (oder Anwendung) hat versucht, eine bestimmte TTS-Engine (Text-to-Speech) an fordern zu können. Speechapi.dll wurde nicht installiert.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Die Sprach-Engines funktionieren anscheinend nicht mit Microsoft Agent in Windows XP?

Microsoft Agent verwendet SAPI 4.0 zum Bereitstellen von Sprachdiensten. Windows XP ist jetzt jedoch mit SAPI 5.0 enthalten, das keine Abwärtskompatibilitätsunterstützung für seinen Vorgänger bietet. Glücklicherweise können SAPI 4.0 und SAPI 5.0 zusammen auf demselben xp-Computer Windows werden.

Damit die Sprach-Engines mit Microsoft Agent in Windows XP funktionieren, installieren Sie zunächst die [SAPI 4.0-Laufzeitbinärdateien](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)und installieren dann die jeweiligen Sprach-Engines.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Die Sprach-Engines, die verwendet wurden, um mit Microsoft Agent zu arbeiten, bis ich ein Upgrade auf Windows XP durchgeführt habe. Was ist passiert?

Sehen Sie sich die vorherige Frage und Antwort an. Der Upgradeprozess von Windows XP hat möglicherweise die sapi 4.0-Unterstützung entfernt, die bereits auf dem Computer vorhanden ist. Installieren Sie die SAPI 4.0-Runtime und die SAPI 4.0-Sprach-Engines nach dem Upgrade auf Windows XP erneut.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Ich habe die TTS3000-Text-to-Speech-Engines auf meinem Computer installiert, auf dem Windows XP (oder Windows 2000) ausgeführt wird, und meine Programmierung ordnungsgemäß für ihre Verwendung bearbeitet. Die Microsoft Agent-Zeichen sprechen hörbar mithilfe dieser TTS3000-Text-to-Speech-Engines, wenn ich oder andere lokale Administratoren angemeldet sind, aber nicht, wenn andere Benutzer ohne *Administratorrechte* bei diesem Computer angemeldet sind. Unter Windows 98 und Windows Funktionieren diese TTS3000-Text-to-Speech-Engines für beide Benutzergruppen ordnungsgemäß. Wie kann ich dieses Problem beheben?

Sie müssen die Sicherheitsberechtigungen für einige registrierungsschlüssel der TTS3000-Text-to-Speech-Engines konfigurieren, um die Verwendung durch Benutzerkonten ohne Administratorrechte zu ermöglichen. Dies kann mit dem Registrierungs-Editor des Betriebssystems erreicht werden.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Ich habe das Verfahren befolgt, das als Lösung für das in der vorherigen Frage beschriebene Problem beschrieben wurde. *Dies* funktionierte gut, sodass die Microsoft Agent-Zeichen mithilfe dieser TTS3000-Text-to-Speech-Engines hörbar sprechen konnten, wenn Benutzer ohne Administratorrechte beim Windows XP-Computer (oder Windows 2000)-Computer angemeldet wurden. Monate später funktionieren dieselben TTS3000-Text-to-Speech-Engines nicht mehr. Was ist passiert?

Wenn Sie das für die vorherige Frage beschriebene Verfahren befolgt haben, haben die Benutzerkonten ohne Administratorrechte Vollzugriff auf die erforderlichen Registrierungsschlüssel erhalten. Es ist möglich, dass einer dieser Benutzer die Werte wissentlich oder unerkannt bearbeitet, die Berechtigungen erneut geändert oder sogar den Registrierungsschlüssel vollständig gelöscht hat.

Überprüfen Sie, ob diese Registrierungsschlüssel und ihre Berechtigungen seitdem bearbeitet, gelöscht oder anderweitig geändert wurden. Ändern Sie diese Registrierungsschlüssel und ihre Berechtigungen bei Bedarf erneut, oder installieren Sie die TTS3000-Spracherkennung erneut.

 

 




