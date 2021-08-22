---
title: Sound
description: Sound ist das Audioelement der Benutzeroberfläche.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5569fe76578fdb79b30da7cbad95939773889b0d22de92b0af4babe966ec6390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348635"
---
# <a name="sound"></a>Sound

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

*Sound* ist das Audioelement der Benutzeroberfläche. Bei entsprechender Verwendung kann Sound eine effektive Kommunikationsform sein, die eine nicht-emotionale und sogar emotionale Beziehung mit Ihren Benutzern herstellt. Sounds können allein oder als Ergänzung zur visuellen Benutzeroberfläche verwendet werden. Beispielsweise erhöht das Hinzufügen eines Soundeffekts zu einer Benachrichtigung die Wahrscheinlichkeit, dass sie bemerkt wird, insbesondere, wenn der Benutzer den Bildschirm nicht ansieht, wenn ein Ereignis auftritt.

![Screenshot des Dialogfelds "Sound" ](images/vis-sound-image1.png)

Auf der Registerkarte Sounds des Systemsteuerungselements Sound können Benutzer Änderungen an ihren Systemsounds vornehmen.

Dieser Artikel behandelt die Verwendung von Sounds innerhalb eines Programms als Reaktion auf Ereignisse und Benutzeraktionen und die Integration der Soundsteuerung eines Programms in Windows. Die Verwendung von Musik oder Sprache wird nicht behandelt.

**Hinweis:** Richtlinien im Zusammenhang mit [Benachrichtigungen](mess-notif.md) und [Branding](exper-branding.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Berücksichtigen Sie die folgenden Fragen, um zu entscheiden, ob Sie sound verwenden sollten:

-   **Gibt es einen eindeutigen Benutzervorteil bei der Verwendung von Sound?** Da die Nachteile der Verwendung von Sound die Vorteile leicht überwogen können, verwenden Sie Sound nur, wenn ein eindeutiger Vorteil vorliegt.
-   **Ist die Verwendung von Sound geeignet?** Lenkt die Verwendung von Sound die Aufmerksamkeit auf Dinge, die die Aufmerksamkeit erfordern? Würden Benutzer den Sound auslassen, wenn er nicht vorhanden wäre? Konzentrieren Sie sich auf Sounds, die Benutzer auf dem Laufenden halten, ihr Verhalten wahrscheinlich ändern oder nützliches Feedback geben.
-   **Ist die Verwendung von Sound ablenkend?** Gibt es häufige, laute, unausgeglichene Töne? Verringern Benutzer wahrscheinlich die Systemlautstärke oder die Lautstärke Ihres Programms als Ergebnis der Verwendung von Sound?
-   **Verwenden Sie Sound als primäre Form der Kommunikation?** In vielen Fällen, z. B. bei Benutzern mit einem gewissen Maß an Hörverlust, sollte Sound nicht als primäres Kommunikationsmittel verwendet werden. Sound ist effektiver als Ergänzung zu anderen Kommunikationsarten (z. B. Text oder Visuals).
-   **Sind die IT-Experten der primären Zielbenutzer?** Sound ist in der Regel ineffektiv für Aufgaben, die an IT-Experten gerichtet sind, da viele ihrer Aufgaben unbeaufsichtigt ausgeführt werden. Darüber hinaus kann der Sound nicht für sie skaliert werden. Angenommen, Es werden Hunderte von Aufgaben gleichzeitig ausgeführt, und es werden Sounds erhalten, wenn sie abgeschlossen werden oder fehlschlagen.

## <a name="design-concepts"></a>Entwurfskonzepte

In der Regel erreicht Sound einen oder alle der folgenden Zwecke:

-   **Benachrichtigung**. Sound kann bestimmten Ereignissen zugeordnet werden. Beispielsweise weist ein "neuer E-Mail"-Sound Benutzer an, wenn E-Mails eintreffen, ohne ihre aktuelle Aufgabe zu unterbrechen.
-   **Feedback.** Sound kann Feedback für bestimmte Benutzeraktionen bereitstellen. Beispielsweise gibt ein dezenter Sound, der wiedergegeben wird, wenn Sie den Schieberegler auf dem Lautstärkeregler freigeben, Feedback zur Ebene der aktuellen Einstellung.
-   **Branding.** Sound kann bestimmten Inhalten zugeordnet werden, um Ihr Produkt, Ihre Anwendung oder Ihren Dienst als Marke zu versehen. Windows verwendet Sound auf diese Weise für den Start des Betriebssystems.
-   **Unterhaltung.** Sound wird häufig verwendet, um Unterhaltungsprodukte zu verbessern und jedes Produkt ansprechender zu gestalten. Beispielsweise verwenden die meisten Spiele, Trainingsanwendungen und Consumerprodukte Sound, um Benutzer zu unterstützen und ihre Erfahrung zu verbessern.

Bestimmte Sounds können mehrere dieser Zwecke gleichzeitig erfüllen. Der Windows Startup-Sound gibt z. B. an, dass der Startprozess abgeschlossen wurde und der Desktop einsatzbereit ist. Darüber hinaus bietet es eine leistungsstarke Form des Produktbrandings und sorgt sogar kurzzeitig für Benutzer.

Sounds, die keinen dieser Zwecke erfüllen, sollten wahrscheinlich entfernt werden.

### <a name="inappropriate-use-of-sound"></a>Ungeeignete Verwendung von Sound

**Trotz der Vorteile von Sound erfordert die angemessene Verwendung von Sound erhebliche Zurückhaltung, da andernfalls ein Programm heiter und ablenkend sein kann.** Benutzer schalten ihren Sound vollständig aus, wenn sie von häufigen, sich wiederholenden, jarringenden, unterbrechenden, schlecht entworfenen Sounds verärgert werden. teilweise liegt dies daran, dass sound naturgemäß Aufmerksamkeit erfordert und schwer zu ignorieren ist. Tipps zum Finden eines angemessenen Gleichgewichts finden Sie in den [Soundentwurfsrichtlinien.](#sound-design)

Da die Nachteile der Verwendung von Sound die Vorteile leicht überwogen können, verwenden Sie Sound nur, wenn ein eindeutiger Vorteil vorliegt. **Verwenden Sie im Zweifelsfall keinen Sound.**

### <a name="make-sound-supplemental"></a>Ergänzen von Sound

Auch wenn der Sound angemessen verwendet wird, gibt es viele Situationen, in denen Sound möglicherweise nicht für alle Benutzer wirksam ist:

-   Einige Benutzer arbeiten möglicherweise in einer lauten Umgebung, in der die Sounds nicht gehört werden können.
-   Einige Benutzer arbeiten möglicherweise in einer stillen Umgebung, die erfordert, dass Sound deaktiviert oder bei geringer Lautstärke festgelegt wird.
-   Bei einigen Benutzern kann es zu Hörbehinderung oder -verlusten gekommen sein.
-   Der Computer verfügt möglicherweise nicht über Lautsprecher.

Aus diesen Gründen **sollte für Benachrichtigungen und Feedback verwendeter Sound nie die einzige Kommunikationsmethode sein,** sondern eher visuelle oder textbezogene Hinweise ergänzen.

### <a name="desirable-characteristics-of-sound"></a>Wünschenswerte Merkmale von Sound

Im Allgemeinen sollten Die Sounds wie hier lauten:

-   mittlere bis hohe Frequenz (600 Hertz \[ Hz \] bis 2 Kilohertz \[ kHz \] ).
-   short (weniger als eine Sekunde).
-   soft oder moderate in Volume.
-   Sinnvolle.
-   und nicht alarmierend oder jarring.
-   nicht-verbabisch.
-   nicht sich wiederholend.

Bei Sound ist weniger mehr. **Der ideale Soundeffekt ist ein Effekt, den Benutzer nicht bemerken, aber sie würden ihn übersehen, wenn er nicht vorhanden wäre.**

**Ein häufiges Missverständnis besteht darin, dass Töne für kritische Ereignisse laut und jarring sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.** Dies ist nicht richtig, da Sound eigentlich als ergänzendes Kommunikationsmittel gedacht ist. Bei einer kritischen Fehlermeldung werden die Darstellung (z. B. in einem modalen Dialogfeld), das Zugehörige Symbol (ein Fehlersymbol) und ihr Text und Ton miteinander kombiniert, um die Art des Fehlers zu kommunizieren. Ein effektiver Fehlerton kann etwas lauter sein als der typische Windows Sound, muss aber nicht wesentlich lauter sein.

### <a name="characteristics-of-windows-sounds"></a>Merkmale Windows Sounds

Über diesen allgemeinen Aufruf des Minimalismus hinaus verwendet die Windows Soundästhetik helle, reine Töne und freundliche und luftige Sounds mit einem weichen Ein- und Ausblenden (weiche "Kanten"), um plötzliche, jarringische und percussive Effekte zu verhindern. Sie sind so konzipiert, dass sie sich dezent, gefällig und konsonant anfühlen. Windows Sounds verwenden Echo, Hall und Gleichheit, um ein natürliches Umgebungslicht zu erreichen.

Das Standard-Soundschema für Windows verwendet in der Regel keine akustischen oder erkennbaren alltäglichen Sounds, die übermäßig spezifisch oder übermäßig spezifisch sind. Beispiele für Töne, die vermieden werden, sind Musikinstrumentate wie z. B. Musik- oder Musikinstrument, Tiergeräusche, Umgebungsgeräusche, Sprache, Stimmen, filmähnliche Soundeffekte oder andere Töne von Menschen. Außerdem sollen Windows Sounds nicht als Musik wahrgenommen werden (d.amp;n.b. lange Mehrfachnotizen). Dadurch unterscheiden sich Windows Sounds funktional von anderen Arten von Sounds.

Da die Windows Sounds auf professionelle Weise so konzipiert wurden, dass sie die gewünschten Merkmale aufweisen und für eine breite Zielgruppe ansprechen, **sollten Sie diese integrierten Windows Sound nach Bedarf verwenden.**

### <a name="designing-your-own-sounds"></a>Entwerfen eigener Sounds

Wenn Sie eigene Sounds erstellen müssen, entwerfen Sie sie so, dass sie die zuvor beschriebenen Merkmale aufweisen. Versuchen Sie, die zugehörigen Aufgaben oder Ereignisse zu ergänzen.

Verstehen Sie, dass es schwierig ist, originale Sounds zu erstellen, insbesondere für Sounds, die für ein breites Publikum bestimmt sind. Sound kann ein polarisierendes Entwurfselement sein. Für jeden Benutzer, der einen Sound mag, gibt es viele, die ihm nicht gefallen.

**Entwerfen Sie die Sounds für Ihr Programm als Gruppe, um das Gefühl zu haben, dass es sich um verwandte Variationen eines Designs handelt.** Die Prüfererfahrung Ihres Programms sollte mit der visuellen Erfahrung ihres Programms koordiniert werden. Außerdem sollte der "Ton" der Töne mit dem [Ton des Texts](text-style-tone.md)koordiniert werden. Überlegen Sie, wie Text mit einem ansprechenden, natürlichen Ton unterminiert werden kann, wenn er von schärferen, alarmierenden Tönen begleitet wird.

**Wenn Sie nur vier Dinge tun...**

1.  Verwenden Sie Sound mit Freundlichkeit, um sicherzustellen, dass es einen eindeutigen allgemeinen Benutzervorteil gibt. Verwenden Sie im Zweifelsfall keinen Sound.
2.  Verwenden Sie ggf. die integrierte Windows Sounds.
3.  Wenn Sie Ihre eigenen Sounds entwerfen, stellen Sie sicher, dass sie die gewünschten Soundmerkmale aufweisen und sich als Ganzes wie Variationen eines Designs anfühlen.
4.  Gehen Sie nicht davon aus, dass Töne laut und jarring sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.

## <a name="usage-patterns"></a>Verwendungsmuster

Sounds weisen mehrere Verwendungsmuster auf:



|     Soundverwendung                                                                                                                                                                 |  Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktionsabschluss**<br/> benachrichtigt Benutzer, wenn eine vom Benutzer initiierte Aktion mit langer Ausführungslaufzeit erfolgreich abgeschlossen wurde. <br/>                             | ![Screenshot des Dialogfelds "Dateidownload" ](images/vis-sound-image2.png)<br/> In diesem Beispiel gibt das Dialogfeld einen Sound wieder, um Benutzer darüber zu informieren, dass der Download abgeschlossen wurde.<br/>                                                                                                                                                                                                                                      |
| **Aktionsfehler**<br/> benachrichtigt Benutzer, wenn eine vom Benutzer initiierte Aktion mit langer Ausführungslaufzeit fehlschlägt. <br/>                                                 | ![Screenshot der Meldung "Kein Zugriff auf Sicherungsdatenträger" ](images/vis-sound-image3.png)<br/> In diesem Beispiel gibt Windows einen Sound wieder, um Benutzer darüber zu informieren, dass der Sicherungsvorgang fehlgeschlagen ist.<br/>                                                                                                                                                                                                                                  |
| **Wichtiges Systemereignis**<br/> Benachrichtigung von Benutzern über wichtige Systemereignisse oder -status, die sofortige Aufmerksamkeit erfordern. <br/>                      | ![Screenshot der Nachricht mit geringem Akkustand ](images/vis-sound-image4.png)<br/> In diesem Beispiel werden Benutzer benachrichtigt, dass ihr niedriger Akku sofort aufmerksamkeits erforderlich ist.<br/>                                                                                                                                                                                                                                                      |
| **Fyi**<br/> benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. <br/>                                                                 | Da diese Informationen in der Regel keine sofortige Aufmerksamkeit erfordern, liefert ein fyi-Sound ein dezentes Feedback, ohne den Benutzerflow zu brechen. <br/> ![Screenshot der Live-Messenger-Anmeldenachricht ](images/vis-sound-image5.png)<br/> In diesem Beispiel wird ein Sound wiedergegeben, wenn sich ein Kontakt bei einem Instant Messaging-Dienst anmeldet.<br/>                                                                                 |
| **Soundeffekt**<br/> bietet Feedback zu Benutzerinteraktionen. <br/>                                                                            | Stellt echtes oder formatiertes Soundfeedback bereit, das für die Interaktion geeignet ist. Soundeffekte klingen oft so, als würde der Benutzer ein physisches Objekt in der realen Welt bearbeiten. wird manchmal auch als foley bezeichnet. <br/> ![Screenshot des Fensters, das minimiert wird ](images/vis-sound-image6.png)<br/> In diesem Beispiel klingt der Soundeffekt "Fenster minimieren" so, als sei ein reales Objekt verkleinert.<br/> |
| **Branding von Sounds**<br/> ein Sound, der die Benutzerfreundlichkeit durch emotionalen Einfluss verbessert und als Nebeneffekt die Produktmarke fördert. <br/> | Brandingsounds eignen sich am besten, wenn sie mit visuellen Ereignissen synchronisiert werden, insbesondere benutzeroberflächenübergängen, z. B. der Anzeige eines Programmfensters. Echte Soundmarken geben die Quelle der Waren an, ähnlich wie ein Markenwort oder Logo, und sind relativ ungewöhnlich. <br/> ![Screenshot des Windows-Startsymbols ](images/vis-sound-image7.png)<br/> In diesem Beispiel ist Windows Startup eine Markenerfahrung.<br/>      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="usage"></a>Verbrauch

-   **Verwenden Sie Sound mit Freundlichkeit,** um sicherzustellen, dass es einen eindeutigen allgemeinen Benutzervorteil gibt. Konzentrieren Sie sich auf Sounds, die Benutzer auf dem Laufenden halten, ihr Verhalten wahrscheinlich ändern oder nützliches Feedback geben. Verwenden Sie im Zweifelsfall keinen Sound.
-   **Wählen Sie den Sound und seine Merkmale basierend auf seiner Verwendung aus.** Eine Beschreibung der einzelnen Verwendungsmuster finden Sie in der Tabelle im vorherigen Abschnitt.
-   **Verwenden Sie für Benachrichtigungen und Feedback nicht Sound als einzige Kommunikationsmethode.** Verwenden Sie stattdessen Sound als ergänzende Methode, um visuelle oder textbezogene Hinweise zu verstärken. Dadurch wird sichergestellt, dass Benutzer die Informationen sehen können, wenn sie den Sound nicht hören können.
-   **Geben Sie nicht häufig laute oder heitere Töne an.** Dies ist unnötig und führt zu einer schlechten Benutzererfahrung. Je häufiger ein Sound wiedergegeben wird, desto weniger obtrusiv sollte er sein. Sounds müssen nicht laut oder heiter sein, um Aufmerksamkeit zu gewinnen.
-   **Don't beep.** Beeping eignet sich nicht für moderne Programme. Signalsignalen können keine bestimmten Bedeutungen zugewiesen werden, und Benutzer können sie nicht steuern.
    -   **Ausnahme:** Kritische Systemfunktionen warnen Benutzer möglicherweise über Situationen, in denen sie sich sofort kümmern müssen, z. B. bei einem kritischen Niedrigen Akkubetrieb.

### <a name="playback"></a>Wiedergabe

-   **Wiederholen Sie einen Sound nicht mehr als zweimal hintereinander.**
-   **Für eine aufeinander folgende Sequenz verwandter Soundereignisse muss ein Sound nur beim ersten Ereignis wiedergegeben werden.** Vermeiden Sie die Verwendung mehrerer Sounds, da sie miteinander in Konflikt stehen oder auf andere Weise zu einer unaufhörlichen Benutzererfahrung führen können.

### <a name="sound-selection"></a>Soundauswahl

-   **Wählen Sie freundliche Sounds aus.** Verwenden Sie keine ängstlichen, alarmierenden Töne, wie z. B. Verrauschen, Abstürze und Breaking.
-   **Verwenden Sie kurze Sounds** (weniger als eine Sekunde).
-   **Verwenden Sie Sounds, die ungefähr derselben Lautstärke entsprechen wie der typische Windows Sound.** Benutzer möchten das Volume nicht herunterfahren, wenn sie einen Computer oder ein Programm starten, insbesondere in öffentlichen Umgebungen wie Besprechungen und Präsentationen. Die Microsoft Windows Sounddateien befinden sich im Ordner Media im Ordner Windows.
-   **Wählen Sie keine Sounds aus, die Lokalisierung erfordern.** Sie können dies erreichen, indem Sie Sounds verwenden, die keine Sprache verwenden oder kulturabhängige Bedeutungen oder Konnotationen haben.

### <a name="windows-system-sounds"></a>Windows Systemsounds

-   **Verwenden Sie nach Bedarf die integrierte Windows Systemsounds.**
-   **Wählen Sie Systemsounds basierend auf ihrer zugeordneten Bedeutung aus, nicht nur auf dem Sound selbst.** Systemsounds müssen konsistent verwendet werden.

### <a name="sound-design"></a>Sounddesign

Beim Erstellen eigener Sounds:

-   **Erstellen Sie Sounds mit den gewünschten Soundmerkmalen.**
-   **Verfassen Sie Sounds mit größtenteils mittleren bis hohen Frequenzen (600 Hz bis 2 kHz).** Verwenden Sie keine niedrigen Häufigkeiten, da sie weiter entfernt sind, schwieriger zu finden sind und alarmierend sein können.
-   **Legen Sie die relative Amplitude normaler Sounds auf die Ebene des typischen Windows Sound fest.** Die Windows Sounds wurden für Heim- und Arbeitsumgebungen entsprechend abgesenkt. Die Verwendung verschiedener Ebenen für Ihre Sounds zwingt Benutzer, Volumeanpassungen vorzunehmen.
    -   Legen Sie wichtige Sounds auf etwas lauter fest. Zu diesen Sounds gehören Aktionsabschluss, Aktionsfehler und wichtige Systemereignisse.
    -   Legen Sie häufig auftretende Sounds auf etwas weicher fest. Dazu gehören FYIs, Brandingsounds und Soundeffekte.
-   **Wählen Sie Sounds aus, die der Bedeutung der Windows entsprechen.** Um eine benutzerdefinierte Version eines Windows Sound zu erstellen, behalten Sie die gleiche Tonhöhe und das gleiche Intervall bei, ändern aber die Orchestrierung oder die Pausierung. Weisen Sie Tönen mit ähnlichen Tonhöhen und Intervallen nicht unterschiedliche Bedeutungen zu wie Windows Sounds.
-   **Entwerfen Sie die Sounds für Ihr Programm so, als handelt es sich um verwandte Variationen zu einem Design.** Die Prüfererfahrung Ihres Programms sollte mit der visuellen Erfahrung ihres Programms koordiniert werden.
    -   **Entwurfsszenenübergänge und Audioübergänge zusammen.** Wenn z. B. eine Szene allmählich ausblendet, sollte jeder Sound auch allmählich ausgeblendet werden. Nahtlose visuelle Übergänge werden nicht durch plötzliche Soundübergänge unterbrochen.
-   **Sounds müssen im WAV-Dateiformat vorliegen.** Das 16-Bit-PCM-Format (16-Bit, 44,1 kHz Stereo uncompressed pulse codecs) wird empfohlen. Wenn die Dateigröße wichtig ist, verwenden Sie komprimierte oder monische Formate (Mono), aber beachten Sie, dass es einen leicht erkennbaren Qualitätsverlust gibt, der sich negativ auf Ihre Anwendung widerspiegeln kann.

### <a name="mixing"></a>Mischen

-   **Sie verfügen nicht über Lautstärke- oder Stummschaltungssteuerelemente in Ihrem Programm.** Stattdessen können Benutzer relative Volumeeinstellungen zwischen Anwendungen mit dem Windows Volumemixer steuern. Wenn Ihr Programm über eine Volumesteuerung verfügt, gibt es mehrere Stellen, an denen Benutzer ihre Einstellungen anpassen, was zu Verwirrung führen kann.

    ![Screenshot des Windows-Volumemixers ](images/vis-sound-image8.png)

    Mit dem Windows-Volumemixer können Benutzer die Hauptvolumeeinstellung sowie die Lautstärke für jedes Programm steuern, das derzeit Audiowiedergaben verwendet.

<!-- -->

-   **Ausnahme:** Wenn der Hauptzweck ihres Programms die Audio- oder Videowiedergabe oder -erstellung ist, kann es hilfreich sein, eine Lautstärkeregler im Programm zu verwenden. Verwenden Sie zu diesem Zweck ein Schieberegler-Steuerelement, und geben Sie sofort Feedback, wenn der Benutzer das Volume ändert.

### <a name="windows-integration"></a>Windows-Integration

-   **Registrieren Sie die Sounds Ihres Programms in der Windows Sounds-Registrierung.** Auf diese Weise kann der Windows Volumemixer einen Schieberegler für Ihr Programm hinzufügen.
-   **Registrieren Sie die benutzerdefinierten Soundereignisse Ihres Programms.** Auf diese Weise kann der Windows Sound-Systemsteuerungselement diese anzeigen. Erstellen Sie den folgenden Schlüssel für jedes benutzerdefinierte Soundereignis: HKEY \_ CURRENT \_ USER \| AppEvents \| Event Labels \| EventName = Event Name.
-   **Heften Sie die Sounds für die Soundereignisse Ihres Programms nicht hart.** Geben Sie stattdessen die Sounds an, die mithilfe von Registrierungseinträgen wiedergegeben werden sollen. Auf diese Weise können Benutzer die Soundereignisse über das Systemsteuerungselement Sound anpassen.
    -   **Ausnahme:** Sie können sich für hardwire-Sounds entscheiden, die für das Branding verwendet werden.
-   **Bieten Sie benutzern keine Möglichkeit, Sounds innerhalb der Programmoptionen zu konfigurieren.** Verwenden Sie für diesen Zweck stattdessen das Windows Sounds-Systemsteuerungselement.
-   **Weisen Sie häufig auftretenden Ereignissen standardmäßig keine Sounds zu.** Es ist nicht erforderlich, dass Benutzer ihren Weg aus einer mühsamen ersten Erfahrung konfigurieren.

### <a name="directsound-programming-issues"></a>Probleme bei der DirectSound-Programmierung

-   Legen Sie für DirectSound-Programme, die über eine eigene Volumesteuerung verfügen, **das Programmvolume standardmäßig auf 100 Prozent fest.** Dadurch wird der dynamische Bereich Ihrer Audiodaten maximiert.
-   **Sperren Sie andere Soundereignisse nicht, indem Sie Ihr Programm im exklusiven Modus ausführen.** Dadurch kann verhindert werden, dass andere Programme ordnungsgemäß funktionieren. Beispielsweise verhindert die Verwendung des exklusiven Modus, dass ein Computer als Telefoniegerät verwendet wird.

## <a name="text"></a>Text

-   Verwenden Sie nicht den Ausdruckstonadapter. Verwenden Sie stattdessen eine Soundkarte.
-   Verwenden Sie das Gerät, um generisch auf Lautsprecher, Mikrofone und Mikrofone zu verweisen.
-   Verwenden Sie den Controller, um auf Audiohardware zu verweisen, die Geräte steuert, z. B. Soundkarten und Soundkarten.
-   Verwenden Sie das Ausdruckstonschema, um eine Sammlung von Sounds für allgemeine Programmereignisse zu beschreiben, z. B. anmelden oder neue E-Mails empfangen. Verwenden Sie das Desktopdesign des Ausdrucks, um eine Sammlung visueller Elemente und Sounds für Ihren Computerdesktop zu beschreiben.
-   Verwenden Sie den Begriff Audio, um sich umfassend auf Sprache, Musik und Sounds zu beziehen. Verwenden Sie den Begriff Sound, um sich enger auf das Programm und Windows in diesem Artikel beschriebenen Sounds zu beziehen.

 

