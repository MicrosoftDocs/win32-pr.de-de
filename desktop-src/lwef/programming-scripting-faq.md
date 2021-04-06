---
title: FAQ zu Programmier Skripts
description: FAQ zu Programmier Skripts
ms.assetid: 84078c5b-7b04-48fa-9d0a-d95393c323eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dec468eb5147968ca0db774f081212a78cf40d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036218"
---
# <a name="programming-scripting-faq"></a>FAQ zu Programmier Skripts

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

### <a name="when-i-use-microsoft-visual-basic-or-other-development-tools-for-scripting-microsoft-agent-i-do-not-see-all-the-properties-and-events-used-in-your-samples-how-do-i-access-them"></a>Wenn ich Microsoft Visual Basic (oder andere Entwicklungs Tools) für die Skripterstellung für den Microsoft-Agent verwende, sehe ich nicht alle Eigenschaften und Ereignisse, die in ihren Beispielen verwendet werden. Gewusst wie darauf zugreifen?

Die meisten Ereignisse, Methoden und Eigenschaften, die vom Microsoft-Agent-Steuerelement unterstützt werden, werden nur zur Laufzeit verfügbar gemacht. Weitere Informationen finden Sie [unter Programmieren des Microsoft-Agent-Steuer](programming-the-microsoft-agent-control.md) Elements.

### <a name="the-map-tag-or-some-other-tag-doesnt-seem-to-work"></a>Das Map-Tag (oder ein anderes Tag) scheint nicht zu funktionieren.

Einige Tags enthalten Zeichen folgen in Anführungszeichen. Für einige Programmiersprachen, wie z. b. Microsoft Visual Basic und Visual Basic Scripting Edition, müssen Sie möglicherweise zwei Anführungszeichen verwenden, um den Parameter des Tags anzugeben oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten. Letzteres wird in diesem Visual Basic Beispiel gezeigt:

Agent1. Characters ("Genie"). "This is \\ map =" + Chr (34) + "gesprochene Text" \_ + Chr (34) + "=" + Chr (34) + "Sprechblasen Text" + Chr (34) + " \\ ."

Stellen Sie für C-, C++-und Java-Programmierung vor umgekehrten Schrägstrichen und doppelten Anführungszeichen mit einem umgekehrten Schrägstrich voran. Beispiel:

BSTR bszsprech = SysAllocString (L "This is \\ \\ map = \\ " gesprochene Text \\ "= \\ " Sprechblasen Text \\ " \\ \\ ");

pcharacter->sprechen (bszspeak,......);

> [!Note]  
> Der Microsoft-Agent unterstützt nicht alle Tags, die in der Microsoft Speech-API angegeben sind. Außerdem kann die Unterstützung für einige Parameter von der installierten Text-zu-Sprache-Engine abhängen. Weitere Informationen finden Sie unter [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).

 

### <a name="i-dont-seem-to-get-requeststart-and-requestcomplete-events-in-my-script-or-program"></a>Es scheint keine requeststart-und requestcomplete-Ereignisse in meinem Skript (oder Programm) zu erhalten.

Dies kann durch eines der folgenden Probleme verursacht werden:

-   Die Programmiersprache unterstützt ActiveX-Steuerelemente nicht vollständig. Überprüfen Sie die Dokumentation, um sicherzustellen, dass die ActiveX-Schnittstelle und Ereignisse für ActiveX-Objekte unterstützt
-   Auf einer Skript gesteuerten Webseite konnte ein anderes Steuerelement nicht installiert oder geladen werden. Stellen Sie sicher, dass alle anderen Steuerelemente ordnungsgemäß installiert sind und ohne den Microsoft-Agent geladen werden.
-   Auf einer Skript gesteuerten Webseite mit Frames haben Sie das `<OBJECT>` Tag für das Microsoft-Agent-Steuerelement auf einer Seite und die Ereignisse, die auf einer anderen Seite erstellt werden. Ereignisse werden nur an die Seite gesendet, die das-Steuerelement hostet.

### <a name="i-am-using-the-microsoft-agent-control-with-other-activex-controls-on-my-webpage-and-i-dont-seem-to-get-any-events"></a>Ich verwende das Microsoft-Agent-Steuerelement mit anderen ActiveX-Steuerelementen auf meiner Webseite, und ich scheint keine Ereignisse zu erhalten.

Überprüfen Sie, ob die anderen Steuerelemente ordnungsgemäß installiert sind. Wenn ein anderes ActiveX-Steuerelement nicht ordnungsgemäß registriert wird, empfängt das Microsoft-agentsteuerelement möglicherweise seine Ereignisse.

### <a name="what-programming-languages-can-i-use-to-program-the-microsoft-agent-control"></a>Welche Programmiersprachen kann ich verwenden, um das Microsoft-Agent-Steuerelement zu programmieren?

Der Microsoft-Agent sollte in jeder Sprache, die die ActiveX-Schnittstelle unterstützt, unterstützt werden. Es enthält Codebeispiele für Visual Basic, VBScript, JScript, C/C++ und Java.

### <a name="can-i-access-the-parameters-returned-from-microsoft-agent-using-jscript"></a>Kann ich mithilfe von JScript auf die vom Microsoft-Agent zurückgegebenen Parameter zugreifen?

Ja, aber die einzige Möglichkeit hierfür ist die Verwendung der- `<SCRIPT LANGUAGE="JScript" FOR="*object*" EVENT="event()">` Syntax. Obwohl diese Syntax für Microsoft Internet Explorer unterstützt wird, werden Sie von anderen Browsern nicht unterstützt. Daher sollten Sie die Verwendung von JScript für diesen Teil des Skripts der Seite vermeiden.

### <a name="can-microsoft-agent-be-used-with-speech-recognition-or-speech-synthesis-text-to-speech-or-tts-engines-other-than-those-supplied-by-microsoft"></a>Kann Microsoft-Agent mit sprach Erkennungs-oder Sprachsynthese Modulen (Text-zu-Sprache oder TTS) verwendet werden, die nicht von Microsoft bereitgestellt werden?

Ja, vorausgesetzt, die Engine unterstützt die vom Microsoft-Agent benötigten Microsoft Speech API (SAPI) 4,0-Schnittstellen. Wenden Sie sich an den Engine-Lieferanten. Ausführliche Informationen zu den für den Microsoft-Agent benötigten SAPI-Schnittstellen finden Sie [unter Support Anforderungen](speech-engine-support-requirements.md)für die Sprach-Engine.

### <a name="my-page-includes-html-object-tags-for-microsoft-agent-the-lernout--hauspie-truvoice-tts-engine-and-the-microsoft-command-and-control-speech-recognition-engine-but-not-all-the-components-install"></a>Meine Seite enthält HTML-Objekt Tags für den Microsoft-Agent, das lerout-& die truvoice-Engine-Engine und die sprach Erkennungs-Engine von Microsoft, aber nicht alle Komponenten.

In der Regel kann das Problem durch Aktualisieren der Seite korrigiert werden. Im Allgemeinen empfiehlt es sich, zuerst das Microsoft Agent Control `<OBJECT>` -Tag anzugeben, dann das lerout-& truvoice-Engine, dann das Befehls-und Steuerelement Spracherkennungs-Engine.

### <a name="after-calling-the-moveto-method-my-character-seems-to-freeze-even-though-i-have-return-animations-assigned-to-moving-state-animations"></a>Nach dem Aufrufen der Methode "muveto" scheint das Zeichen zu fixieren, obwohl ich dem Verschieben von Zustands Animationen Rückgabe Animationen zugewiesen habe.

Wenn Sie eine Animation wiedergeben, zeigen die Animations Dienste weiterhin den letzten Frame an, bis eine weitere Animation aufgerufen wird. Daher sollten Sie nach dem Aufrufen von " [**muveto**](moveto-method.md)" eine weitere Animation abspielen. Wenn Sie für die Animation zum **verschieben** des Zustands eine **Rückgabe** Animation definiert haben, wird Sie vom Server zuerst abgespielt.

### <a name="when-i-query-the-characters-pitch-property-it-returns-a-value-of--1"></a>Beim Abfragen der Eigenschaft "Pitch" des Zeichens wird der Wert-1 zurückgegeben.

Dies tritt auf, wenn das Zeichen mit der standardmäßigen Pitch-Eigenschaft einer Sprach-Engine kompiliert wurde. Das heißt, dass die Tonhöhe nicht geändert wurde, als das Zeichen erstellt wurde.

### <a name="when-my-code-attempts-to-set-the-tts-mode-id-for-a-text-to-speech-engine-i-get-the-following-error-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Wenn mein Code versucht, die ID des TTS-Modus für eine Text-zu-Sprache-Engine festzulegen, wird die folgende Fehlermeldung angezeigt: ein ausgehender-Befehl kann nicht ausgeführt werden, da die Anwendung einen Eingabe synchronen-Befehl sendet.

Um die ttsmodeid-Eigenschaft festzulegen, müssen Speech.dll installiert sein. Dies ist in der Regel ein Teil des Installationscodes der Sprach-Engine. Sie können dies auch installieren, indem Sie die sprach Objekt-Systemsteuerung installieren, die auf der Microsoft-Agent-Downloadseite verfügbar ist.

### <a name="when-i-retry-loading-a-character-that-failed-to-load-the-call-fails-with-a-character-already-loaded-error"></a>Beim erneuten Laden eines Zeichens, das nicht geladen werden konnte, schlägt der-Befehl mit dem Fehler "das Zeichen wurde bereits geladen" fehl.

Das Microsoft-Agent-Steuerelement entlädt kein Zeichen Objekt (geben Sie den Verweis frei), wenn die zugehörige Zeichen Datei nicht geladen werden kann. Wenn Sie erneut versuchen möchten, das Zeichen zu laden, müssen Sie " [**entladen**](unload-method.md) " explizit [**aufzurufen, bevor Sie das zweite**](load-method.md) Mal aufgerufen werden. Wenn Sie dies in einem Webseiten Skript versuchen, müssen Sie auch dem **Entlade** Vorgang mit einer On Error Resume Next-Anweisung voranstellen, oder der **Entlade** Vorgang schlägt fehl. (Beachten Sie, dass die JScript-Anweisung keine On Error Resume Next-Anweisung aufweist.)

Allerdings müssen Sie ggf. keinen Code einschließen, um das Laden eines Zeichens sofort zu wiederholen, wenn die Datei nicht geladen werden kann. Microsoft Internet Explorer und die Microsoft-Agent-Serverkomponente versuchen automatisch mehrmals, den Vorgang zu wiederholen, sodass die Wahrscheinlichkeit, dass die Wiederholung zu einer erfolgreichen Auslastung führt, Remote ist. Eine bessere Strategie besteht darin, ein paar Sekunden vor dem erneuten Versuch zu warten (einen Zeitgeber festzulegen).

### <a name="how-can-i-install-microsoft-agent-as-part-of-my-application-or-from-my-web-server"></a>Wie kann ich den Microsoft-Agent als Teil meiner Anwendung oder meines Webservers installieren?

Sie können den-Agent über die Microsoft-Website installieren, indem Sie seine *CLSID in ein HTML-Objekttag* einschließen. Wenn Sie jedoch den-Agent aus einem eigenen Installationsprogramm der Anwendung oder von einem eigenen Server einschließen und installieren möchten, müssen Sie die selbst Installationsdatei des Microsoft-Agents herunterladen, indem Sie Sie von der Downloadseite herunterladen. Wählen Sie beim Herunterladen die Option Speichern anstelle von ausführen aus. Wenn diese Datei ausgeführt wird, wird der Microsoft-Agent automatisch auf dem Zielcomputer installiert. Daher können Sie die Datei im Installationsskript angeben.

Versuchen Sie nicht, den Microsoft-Agent zu installieren, indem Sie die verschiedenen kopieren. DLLs und versuchen, Sie selbst zu registrieren. Wenn Sie versuchen, den-Agent auf andere Weise zu installieren, wird die Ausführung der selbst installierenden CAB-Datei nicht unterstützt.

Das Zielsystem muss auch aktuelle Versionen von MSVCRT.DLL (VC + + Runtime), REGSVR32.EXE (in Microsoft VC + +) und com enthalten. Die beste Möglichkeit, um sicherzustellen, dass die richtigen Versionen installiert sind, erfordert, dass Microsoft Internet Explorer 3,02 oder höher installiert ist. Allerdings können Sie diese Lauf Zeitanforderungen auch lizenzieren. (Für die neueste Version von com greifen Sie von der Microsoft-Website auf das DCOM-Update zu.)

Microsoft Agent 2,0 wird nicht unter Microsoft Windows 2000 installiert, da diese Version des Betriebssystems bereits den-Agent enthält.

### <a name="can-i-use-the-visual-basic-setup-wizard-to-install-microsoft-agent"></a>Kann ich den Visual Basic-Setup-Assistenten verwenden, um den Microsoft-Agent zu installieren?

Sie können zwar mit Visual Basic (VB)-Code Ihr eigenes Installationsprogramm erstellen, aber dazu können Sie den Visual Basic Setup-Assistenten nicht verwenden. Zum Installieren des Agents über VB können Sie den Shellbefehl verwenden, der die selbst installierte CAB-Datei für den Microsoft-Agent angibt.

### <a name="how-do-i-install-microsoft-agent-on-windows-2000"></a>Gewusst wie installieren Sie den Microsoft-Agent unter Windows 2000?

Microsoft Agent 2,0 wird nicht unter Windows 2000 installiert, da es bereits als Teil des Betriebssystems enthalten ist.

### <a name="agentsvr-crashes-when-speak-is-called-with-a-wav-file"></a>Agentsvr stürzt ab, wenn "sprechen" mit einer WAV-Datei aufgerufen wird.

Dies kann der Fall sein, wenn das Zeichen für die gesprochene Ausgabe verwendet wurde, dann ändert sich die Verwendung einer WAV-Datei. Der Text wurde nicht im ersten Parameter der Sprech Methode angegeben.

Um den Absturz zu vermeiden, schließen Sie ein Leerzeichen in den ersten Parameter der Sprech Methode ein, auch wenn keine Textausgabe vorhanden ist.

### <a name="even-though-i-have-already-installed-the-agent-language-component-dll-for-a-particular-language-i-still-got-an-error-that-the-component-is-missing-when-i-set-the-characters-language-to-that-language"></a>Obwohl ich die Agent-Sprachkomponente (dll) bereits für eine bestimmte Sprache installiert habe, habe ich weiterhin einen Fehler erhalten, dass die Komponente fehlt, wenn ich die Sprache des Zeichens auf diese Sprache festgelegt habe.

Dies geschieht normalerweise, wenn Sie Agent-Anwendungen wie Microsoft Office 2000 geöffnet haben, wenn Sie die-Agent-Sprachkomponente installieren. Schließen Sie alle Anwendungen, und versuchen Sie es noch mal. Wenn das Problem weiterhin besteht, starten Sie den Computer neu, und Sie sollten in der Lage sein, die Sprach-ID jetzt festzulegen.

### <a name="when-i-use-the-ampersand--symbol-the-text-around-the-symbol-in-the-characters-word-balloons-is-truncated"></a>Wenn ich das kaufmännische und-Zeichen "&" verwende, wird der Text um das Symbol in den Wort ballblasen des Zeichens abgeschnitten.

Dieses Problem ist bekannt. Sie können dieses Problem umgehen, indem Sie das Map-Tag verwenden. Um z. b. "a & B" in der Wort Sprechblase des Zeichens anzuzeigen, verwenden Sie \\ in der Sprech Anweisung "a map =" und "=" && " \\ B".

### <a name="my-application-allows-users-to-change-the-default-character-and-when-they-do-the-program-crashes"></a>Meine Anwendung ermöglicht es Benutzern, das Standard Zeichen zu ändern. wenn dies der Fall ist, stürzt das Programm ab.

Es gibt zwei mögliche Ursachen:

Wenn Sie die TTS-Modus-ID des Standard Zeichens ändern und dann zulassen, dass der Benutzer das Standard Zeichen durch showdefaultcharakteriproperties ändert, stürzt der agentsvr ab.

Dieses Problem wurde in den Betriebssystemen Windows 2000 und Windows XP behoben. Um den Absturz auf anderen Plattformen zu vermeiden, sollten Sie dem Benutzer nicht gestatten, das Standard Zeichen zu ändern, nachdem Sie die TTS-Modus-ID des Standard Zeichens geändert haben, oder das Standard Zeichen nicht in Ihrer Anwendung oder Webseite verwenden.

Wenn Ihre Anwendung keine von Microsoft bereitgestellten agentzeichen verwendet, stellen Sie sicher, dass das angepasste Zeichen eine Palette mit einer vollständigen Palette von 256 Farben verwendet. Weitere Informationen finden Sie im Dokument entwerfen von Zeichen für Microsoft-Agent.

### <a name="my-page-loads-the-agent-character-from-multiple-frames-with-ie-5-i-get-the-microsoft-agent-failed-to-load-error"></a>Meine Seite lädt das agentzeichen aus mehreren Frames. Mit IE 5 erhalte ich den Fehler beim Laden des Microsoft-Agents.

Dies ist ein bekanntes Problem mit IE 5. Es gab eine Änderung in der Art und Weise, in der der Browser ein bestimmtes Ereignis behandelt, das bewirkt, dass das HTML-Skript ausgeführt wird, bevor agentsvr gestartet wird. Damit Ihre Seite mit allen Versionen des Browsers funktioniert, müssen Sie diese Zeile zum Skript hinzufügen:

Agentcontrol. Connected = true

Dadurch wird explizit eine Verbindung mit dem agentsvr hergestellt. Beachten Sie, dass dies nur erforderlich ist, wenn die Seite den Agent aus mehreren Frames lädt.

### <a name="when-my-application-tries-to-install-microsoft-agent-on-windows-2000-or-windows-xp-i-get-the-error-that-agent-is-not-compatible-with-windows-2000-or-windows-xp"></a>Wenn die Anwendung versucht, den Microsoft-Agent unter Windows 2000 (oder Windows XP) zu installieren, erhalte ich die Fehlermeldung, dass der-Agent nicht mit Windows 2000 (oder Windows XP) kompatibel ist.

Eine frühere Version der CAB-Datei MSAGENT.exe der agentkernkomponente wird bei Ausführung unter Windows 2000 (und Windows XP) die Installation blockieren und zeigt eine ungenaue Fehlermeldung an, dass der-Agent nicht mit der Version des Betriebssystems kompatibel ist, das Sie ausführen. Tatsächlich sind Microsoft-Agent 2,0-Kernkomponenten als Teil von Windows 2000 (und Windows XP) enthalten und werden bereits standardmäßig über Windows Setup installiert.

In dieser Version wird die Überprüfung entfernt, und in der Installationsdatei wird die oben genannte Fehlermeldung unter Windows 2000 (oder Windows XP) nicht angezeigt. Beachten Sie, dass dies die einzige Änderung an der Installationsdatei ist und keine Codeänderungen an den Kernkomponenten des Agents selbst vorgenommen werden. Daher sind Sie von diesem Update nicht betroffen, wenn Sie bereits Agent 2,0 installiert haben oder wenn Ihre Website ein Objekttag verwendet, um automatische Downloads der Agent-Kernkomponenten aus dem Microsoft Object Store zu initiieren.

Wenn Sie die Installationsdatei der agentkernkomponente in Ihre Anwendung einschließen oder wenn Sie die Installationsdatei auf dem Server veröffentlichen, können Sie dieses Update herunterladen. Klicken Sie hierzu hier, und wählen Sie die Option "das Programm auf dem Datenträger speichern" aus. Sie müssen über eine gültige und aktuelle Agent-Verteilungs Lizenz für diese Umstände verfügen.

Alternativ können Sie dieses Problem auch umgehen, indem Sie die Option "automatisch" verwenden, wenn Sie die vorherige Version der MSAGENT.exe Installationsdatei installieren. Der Shellbefehl lautet wie folgt:

**MSAGENT.exe/q: a**

Das gleiche gilt für die-Agent-Sprachkomponenten, die ursprünglich im Oktober 1998 veröffentlicht wurden. Es wurde eine Prüfung durchführt, die die Installation der Sprachkomponenten Arabisch, Französisch, Deutsch, Hebräisch, Italienisch, Japanisch, Koreanisch, Chinesisch (vereinfacht), Spanisch und Chinesisch (traditionell) unter Windows 2000 (und Windows XP) verhindert. Die neueren Versionen dieser Installationsdateien enthalten neben den zusätzlichen 19 Sprachen, die im März 2000 hinzugefügt wurden, diese Prüfung nicht und werden unter Windows 2000 (und Windows XP) erfolgreich installiert.

### <a name="my-customized-character-exhibits-some-unexpected-behavior-with-its-transparency-color-on-windows-2000-and-windows-xp"></a>Das angepasste Zeichen zeigt ein unerwartetes Verhalten mit seiner Transparenz Farbe unter Windows 2000 (und Windows XP).

Dies ist ein bekanntes Problem für Zeichen, die mit einer Palette von weniger als 256 Farben erstellt werden. Zu den Problemen mit diesen Zeichen zählen die Transparenz Farbe, die im Hintergrund, dem transparenten Sprechblasen Text, dem transparenten Sprechblasen Rahmen oder dem transparenten Sprechblasen Hintergrund angezeigt wird. Beachten Sie, dass solche Zeichen dazu führen können, dass Ihre Anwendungen abstürzen, wenn Sie im Dialogfeld agentzeichenauswahl oder im Microsoft Office Assistant Gallery geladen werden. Für Ihre angepassten Zeichen muss eine vollständige Palette mit 256 Farben verwendet werden. Sie können die für Office Assistant-Zeichen bereitgestellte Beispiel Palette als Ausgangspunkt mit einer vollständigen 256-Farbpalette verwenden.

### <a name="the-character-does-not-use-the-british-english-tts-engine-even-though-i-have-set-its-language-id-to-british-english-h0809"></a>Das Zeichen verwendet nicht die englischsprachige TTS-Engine, obwohl ich die Sprach-ID auf britisches Englisch &h0809 festgelegt habe.

Stellen Sie zunächst sicher, dass alle erforderlichen Komponenten installiert sind – die Agent-Kernkomponenten, die SAPI-Lauf Zeit Binärdateien und eine SAPI4 kompatible britische-TTS-Engine wie die TTS3000 British German-Engine, die auf der Seite mit den Agent-Downloads zum Download zur Verfügung steht. Wenn Ihr Zeichen weiterhin nicht die Groß-und Englisch-TTS-Engine verwendet, ist es wahrscheinlich, dass Sie auch eine American-German-TTS-Engine installiert haben. Da sowohl das britische als auch das Deutschland die gleiche primäre Sprache (Englisch) und Englisch (Englisch) verwenden, wählt der-Agent das erste verfügbare amerikanische, von SAPI zurückgegebene US-amerikanische TTS-Engine aus. Verwenden Sie stattdessen die ttsmodeid-Eigenschaft des Zeichens, um ein britisches Englisch-TTS-Modul zu verwenden. Beispielsweise lautet die ttsmodeid für die TTS3000-Sprache für britisches Englisch "{227a0e41-a92a-11d1-B17B-0020afed142e}". In Microsoft Visual Basic Sie diese Engine verwenden, indem Sie die "ttsmodeid" von Merlin wie folgt festlegen:

Agentcontrol. Characters ("Merlin"). Ttsmodeid = {227a0e41-a92a-11d1-B17B-0020afed142e}

### <a name="when-the-characters-volume-is-set-to-zero-using-the-speech-tag-vol0-it-either-has-no-effects-or-crashes-the-agentsvr"></a>Wenn das Volume des Zeichens mithilfe des Sprachtags Vol = 0 auf NULL festgelegt ist \\ \\ , hat es entweder keine Auswirkungen oder stürzt auf den agentsvr ab.

Dies ist ein bekanntes Problem. Unter den Betriebssystemen Windows 95, Windows 98 und Windows Me ändert sich das Volume des Zeichens nicht, aber es bleibt auf der zuvor festgelegten Ebene erhalten. Auf Windows NT 4,0-, Windows 2000-und Windows XP-Plattformen führt dies zu einem Absturz von agentsvr, auch wenn eine TTS-Engine nicht installiert ist. Da der Bereich des volumevolumes von 0 (Ruhe) bis 65535 (maximales Volume) groß ist und der Unterschied zwischen aufeinander folgenden Ebenen kaum erkennbar ist, besteht die einfache Problem Umgehung darin, das Volume auf den Wert 1 anstelle von 0 festzulegen, wenn die Stimme des Zeichens nicht hörbar ist.

### <a name="my-customized-characters-return-animation-does-not-play-correctly-after-the-movedown-moveleft-moveright-andor-moveup-animations"></a>Die Rückgabe Animation des angepassten Zeichens wird nicht ordnungsgemäß nach den Animations-, muveleft-, muveright-und/oder moveUp-Animationen ausgeführt.

Stellen Sie sicher, dass eine einfache sprach Animation dem Sprech Zustand zugewiesen ist. Beispielsweise können Sie einen einzelnen Frame verwenden, der aus der neutralen Position des Zeichens mit mundüberlagerungen besteht.

 

 




