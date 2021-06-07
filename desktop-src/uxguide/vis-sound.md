---
title: Sound
description: Sound ist das Audioelement der Benutzeroberfläche.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 035f718494e5a0548324f3c5449c5e3ac3f49fa1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444541"
---
# <a name="sound"></a>Sound

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

*Sound* ist das Audioelement der Benutzeroberfläche. Bei entsprechender Verwendung kann Sound eine effektive Kommunikationsform sein, die eine nicht-emotionale und sogar emotionale Beziehung mit Ihren Benutzern herstellt. Sounds können allein oder als Ergänzung zur visuellen Benutzeroberfläche verwendet werden. Beispielsweise erhöht das Hinzufügen eines Soundeffekts zu einer Benachrichtigung die Wahrscheinlichkeit, dass sie bemerkt wird, insbesondere, wenn der Benutzer den Bildschirm nicht ansieht, wenn ein Ereignis auftritt.

![Screenshot des Dialogfelds "Sound" ](images/vis-sound-image1.png)

Auf der Registerkarte Sounds des Systemsteuerungselements Sound können Benutzer Änderungen an ihren Systemsounds vornehmen.

Dieser Artikel behandelt die Verwendung von Sounds innerhalb eines Programms als Reaktion auf Ereignisse und Benutzeraktionen und die Integration des Soundsteuerelements eines Programms in Windows. Die Verwendung von Musik oder Sprache wird nicht behandelt.

**Hinweis:** Richtlinien im Zusammenhang mit [Benachrichtigungen](mess-notif.md) und [Branding](exper-branding.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Berücksichtigen Sie die folgenden Fragen, um zu entscheiden, ob Sie sound verwenden sollten:

-   **Gibt es einen eindeutigen Benutzervorteil bei der Verwendung von Sound?** Da die Nachteile der Verwendung von Sound die Vorteile leicht überwogen können, verwenden Sie Sound nur, wenn ein eindeutiger Vorteil vorliegt.
-   **Ist die Verwendung von Sound geeignet?** Lenkt die Verwendung von Sound die Aufmerksamkeit auf Dinge, die die Aufmerksamkeit erfordern? Würden Benutzer den Sound auslassen, wenn er nicht vorhanden wäre? Konzentrieren Sie sich auf Sounds, die Benutzer auf dem Laufenden halten, ihr Verhalten wahrscheinlich ändern oder nützliches Feedback geben.
-   **Ist die Verwendung von Sound ablenkend?** Gibt es häufige, laute, unausgeglichene Töne? Verringern Benutzer wahrscheinlich das Systemvolume oder die Lautstärke Ihres Programms als Ergebnis der Verwendung von Sound?
-   **Verwenden Sie Sound als primäre Form der Kommunikation?** In vielen Fällen, z. B. bei Benutzern mit einem gewissen Maß an Hörverlust, sollte Sound nicht als primäres Kommunikationsmittel verwendet werden. Sound ist effektiver als Ergänzung zu anderen Kommunikationsmedien (z. B. Text oder Visuals).
-   **Sind die IT-Experten der primären Zielbenutzer?** Sound ist in der Regel ineffektiv für Aufgaben, die an IT-Experten gerichtet sind, da viele ihrer Aufgaben unbeaufsichtigt ausgeführt werden. Darüber hinaus kann der Sound nicht für sie skaliert werden. Angenommen, es werden Hunderte von Aufgaben gleichzeitig ausgeführt, und es werden Sounds erhalten, wenn sie abgeschlossen sind oder fehlschlagen.

## <a name="design-concepts"></a>Entwurfskonzepte

In der Regel erreicht Sound einen oder alle der folgenden Zwecke:

-   **Benachrichtigung**. Sound kann bestimmten Ereignissen zugeordnet werden. Beispielsweise weist ein "neuer E-Mail"-Sound Benutzer an, wenn E-Mails eintreffen, ohne ihre aktuelle Aufgabe zu unterbrechen.
-   **Feedback.** Sound kann Feedback für bestimmte Benutzeraktionen bereitstellen. Beispielsweise gibt ein dezenter Sound, der wiedergegeben wird, wenn Sie den Schieberegler auf dem Lautstärkeregler freigeben, Feedback zur Ebene der aktuellen Einstellung.
-   **Branding.** Sound kann bestimmten Inhalten zugeordnet werden, um Ihr Produkt, Ihre Anwendung oder Ihren Dienst zu versehen. Windows verwendet Sound auf diese Weise für den Start des Betriebssystems.
-   **Unterhaltung.** Sound wird häufig verwendet, um Unterhaltungsprodukte zu verbessern und jedes Produkt ansprechender zu gestalten. Beispielsweise verwenden die meisten Spiele, Trainingsanwendungen und Verbraucherprodukte Sound, um Benutzer zu unterstützen und ihre Erfahrung zu verbessern.

Bestimmte Sounds können mehrere dieser Zwecke gleichzeitig erfüllen. Der Windows-Startsound gibt beispielsweise an, dass der Startprozess abgeschlossen wurde und der Desktop einsatzbereit ist. Darüber hinaus bietet es eine leistungsstarke Form des Produktbrandings und sorgt sogar kurzzeitig für Benutzer.

Sounds, die keinen dieser Zwecke erfüllen, sollten wahrscheinlich entfernt werden.

### <a name="inappropriate-use-of-sound"></a>Ungeeignete Verwendung von Sound

**Trotz der Vorteile von Sound erfordert die angemessene Verwendung von Sound erhebliche Zurückhaltung, da andernfalls ein Programm heiter und ablenkend sein kann.** Benutzer schalten ihren Sound vollständig aus, wenn sie von häufigen, sich wiederholenden, jarringenden, unterbrechenden, schlecht entworfenen Sounds verärgert werden. teilweise liegt dies daran, dass sound naturgemäß Aufmerksamkeit erfordert und schwer zu ignorieren ist. Tipps zum Finden eines angemessenen Gleichgewichts finden Sie in den [Soundentwurfsrichtlinien.](#sound-design)

Da die Nachteile der Verwendung von Sound die Vorteile leicht überwogen können, verwenden Sie Sound nur, wenn ein eindeutiger Vorteil vorliegt. **Verwenden Sie im Zweifelsfall keinen Sound.**

### <a name="make-sound-supplemental"></a>Ergänzen von Sound

Auch wenn der Sound angemessen verwendet wird, gibt es viele Situationen, in denen Sound möglicherweise nicht für alle Benutzer wirksam ist:

-   Einige Benutzer arbeiten möglicherweise in einer lauten Umgebung, in der die Sounds nicht gehört werden können.
-   Einige Benutzer arbeiten möglicherweise in einer stillen Umgebung, die erfordert, dass Sound deaktiviert oder bei geringer Lautstärke festgelegt wird.
-   Einige Benutzer haben möglicherweise Hörbehinderung oder Verlust.
-   Der Computer verfügt möglicherweise nicht über Lautsprecher.

Aus diesen Gründen **sollte der für Benachrichtigungen und Feedback verwendete Sound nie die einzige Kommunikationsmethode sein,** sondern eher visuelle oder textbezogene Hinweise ergänzen.

### <a name="desirable-characteristics-of-sound"></a>Wünschenswerte Merkmale von Sound

Im Allgemeinen sollten Die Sounds wie hier lauten:

-   mittlere bis hohe Frequenz (600 Hertz \[ Hz \] bis 2 Kilohertz \[ kHz \] ).
-   short (weniger als eine Sekunde).
-   soft oder moderate in Volume.
-   Sinnvolle.
-   und nicht alarmierend oder jarring.
-   nicht-nabisch.
-   nicht sich wiederholend.

Bei Sound ist weniger mehr. **Der ideale Soundeffekt ist ein Effekt, den Benutzer nicht bemerken, aber sie würden ihn übersehen, wenn er nicht vorhanden wäre.**

**Ein häufiges Missverständnis besteht darin, dass Laute für kritische Ereignisse laut und jarring sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.** Dies ist nicht richtig, da Sound eigentlich als ergänzendes Kommunikationsmittel gedacht ist. Bei einer kritischen Fehlermeldung werden die Darstellung (möglicherweise in einem modalen Dialogfeld), das Symbol (ein Fehlersymbol) und ihr Text und Ton miteinander kombiniert, um die Art des Fehlers zu kommunizieren. Ein effektiver Fehlerton kann etwas lauter als der typische Windows-Sound sein, muss aber nicht wesentlich lauter sein.

### <a name="characteristics-of-windows-sounds"></a>Merkmale von Windows-Sounds

Über diesen allgemeinen Aufruf des Minimalismus hinaus verwendet die Windows-Soundästhetik helle, reine Töne und freundliche und luftige Sounds mit einem weichen Ein- und Ausblenden (weiche "Kanten"), um plötzliche, jarringische und percussive Effekte zu verhindern. Sie sind so konzipiert, dass sie sich dezent, gefällig und konsonant anfühlen. Windows-Sounds verwenden Echo, Hall und Gleichheit, um ein natürliches Umgebungs-Gefühl zu erreichen.

Das Standard-Soundschema für Windows verwendet in der Regel keine akustischen oder erkennbaren alltäglichen Sounds, die übermäßig spezifisch oder lyrisch sind. Beispiele für Töne, die vermieden werden, sind Musikinstrumentate wie z. B. Musik- oder Musikinstrument, Tiergeräusche, Umgebungsgeräusche, Sprache, Stimmen, filmähnliche Soundeffekte oder andere Töne von Menschen. Außerdem sollen Windows-Sounds nicht als Musik wahrgenommen werden (d.amp;n.b. lang, Mehrnotizen). Dadurch unterscheiden sich Windows-Sounds funktionell von anderen Arten von Sounds.

Da die Windows-Sounds auf professionelle Weise entwickelt wurden, um die gewünschten Merkmale zu erhalten und eine breite Zielgruppe zu ansprechen, **sollten Sie diese integrierten Windows-Sounds nach Bedarf verwenden.**

### <a name="designing-your-own-sounds"></a>Entwerfen eigener Sounds

Wenn Sie eigene Sounds erstellen müssen, entwerfen Sie sie so, dass sie die zuvor beschriebenen Merkmale aufweisen. Versuchen Sie, die zugehörigen Aufgaben oder Ereignisse zu ergänzen.

Verstehen Sie, dass es schwierig ist, originale Sounds zu erstellen, insbesondere für Sounds, die für ein breites Publikum bestimmt sind. Sound kann ein polarisierendes Entwurfselement sein. Für jeden Benutzer, der einen Sound mag, gibt es viele, die ihm nicht gefallen.

**Entwerfen Sie die Sounds für Ihr Programm als Gruppe so, als handelt es sich um verwandte Variationen zu einem Design.** Die Prüfererfahrung Ihres Programms sollte mit der visuellen Erfahrung ihres Programms koordiniert werden. Außerdem sollte der "Ton" der Töne mit dem [Ton des Texts](text-style-tone.md)koordiniert werden. Überlegen Sie, wie Text mit einem ansprechenden, natürlichen Ton unterminiert werden kann, wenn er von schärferen, alarmierenden Tönen begleitet wird.

**Wenn Sie nur vier Dinge tun...**

1.  Verwenden Sie Sound mit Freundlichkeit, um sicherzustellen, dass es einen eindeutigen allgemeinen Benutzervorteil gibt. Verwenden Sie im Zweifelsfall keinen Sound.
2.  Verwenden Sie nach Bedarf die integrierten Windows-Sounds.
3.  Wenn Sie Ihre eigenen Sounds entwerfen, stellen Sie sicher, dass sie die gewünschten Soundmerkmale aufweisen und sich als Ganzes wie Variationen eines Designs anfühlen.
4.  Gehen Sie nicht davon aus, dass Töne laut und laut sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.

## <a name="usage-patterns"></a>Verwendungsmuster

Sounds haben mehrere Verwendungsmuster:



|     Verwendung von Sound                                                                                                                                                                 |  Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktionsabschluss**<br/> benachrichtigt Benutzer, wenn eine vom Benutzer initiierte Aktion mit langer Laufzeit erfolgreich abgeschlossen wurde. <br/>                             | ![Screenshot des Dialogfelds "Dateidownload" ](images/vis-sound-image2.png)<br/> In diesem Beispiel gibt das Dialogfeld einen Sound wieder, um Benutzer zu benachrichtigen, dass der Download abgeschlossen wurde.<br/>                                                                                                                                                                                                                                      |
| **Aktionsfehler**<br/> benachrichtigt Benutzer, wenn bei einer vom Benutzer initiierten Aktion mit langer Ausführungserfahrung ein Fehler auftritt. <br/>                                                 | ![Screenshot der Meldung des Sicherungsdatenträgers, auf den nicht zugegriffen werden kann ](images/vis-sound-image3.png)<br/> In diesem Beispiel gibt Windows einen Sound wieder, um Benutzer zu benachrichtigen, dass der Sicherungsvorgang fehlgeschlagen ist.<br/>                                                                                                                                                                                                                                  |
| **Wichtiges Systemereignis**<br/> warnt Benutzer über wichtige Systemereignisse oder den Status, die sofortige Aufmerksamkeit erfordern. <br/>                      | ![Screenshot der Meldung zu wenig Akku ](images/vis-sound-image4.png)<br/> In diesem Beispiel werden Benutzer benachrichtigt, dass ihre niedrige Akkukapazität sofortige Aufmerksamkeit erfordert.<br/>                                                                                                                                                                                                                                                      |
| **Fyi**<br/> benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. <br/>                                                                 | Da diese Informationen in der Regel keine unmittelbare Aufmerksamkeit erfordern, liefert ein Fyi-Sound ein subtiles Feedback, ohne den Fluss des Benutzers zu brechen. <br/> ![Screenshot der Live-Messenger-Anmeldenachricht ](images/vis-sound-image5.png)<br/> In diesem Beispiel wird ein Sound abspielt, wenn sich ein Kontakt bei einem Instant Messaging-Dienst anklangt.<br/>                                                                                 |
| **Soundeffekt**<br/> bietet Feedback zu Benutzerinteraktionen. <br/>                                                                            | Bietet für die Interaktion geeignetes Feedback aus der realen Welt oder im Stil. Soundeffekte klingen oft so, als ob der Benutzer ein reales physisches Objekt manipuliert. wird manchmal auch als foley bezeichnet. <br/> ![Screenshot des minimierten Fensters ](images/vis-sound-image6.png)<br/> In diesem Beispiel klingt der Effekt "Fensterklang minimieren" wie ein reales Objekt, das verkleinert wird.<br/> |
| **Branding von Sounds**<br/> ein Sound, der die Benutzerfreundlichkeit durch emotionalen Einfluss verbessert und als Nebeneffekt die Produktmarke fördert. <br/> | Branding-Sounds sind am besten, wenn sie mit visuellen Ereignissen synchronisiert werden, insbesondere ui-Übergänge wie die Anzeige eines Programmfensters. True Sound-Marken geben die Quelle der Waren an, ähnlich wie ein Markenwort oder Logo, und sind relativ ungewöhnlich. <br/> ![Screenshot des Windows-Startsymbols ](images/vis-sound-image7.png)<br/> In diesem Beispiel ist das Starten von Windows ein Markenneustart.<br/>      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="usage"></a>Verwendung

-   **Verwenden Sie Sound mit Freundlichkeit,** und stellen Sie sicher, dass es einen eindeutigen allgemeinen Benutzervorteil gibt. Konzentrieren Sie sich auf Sounds, die Benutzer auf dem Laufenden halten, ihr Verhalten wahrscheinlich ändern oder nützliches Feedback geben. Verwenden Sie im Zweifelsfall keinen Sound.
-   **Wählen Sie den Sound und seine Merkmale basierend auf seiner Verwendung aus.** Eine Beschreibung der einzelnen Verwendungsmuster finden Sie in der Tabelle im vorherigen Abschnitt.
-   **Verwenden Sie für Benachrichtigungen und Feedback nicht Sound als einzige Kommunikationsmethode.** Verwenden Sie stattdessen Sound als zusätzliche Methode, um visuelle oder textliche Hinweise zu verstärken. Dadurch wird sichergestellt, dass Benutzer die Informationen sehen können, wenn sie den Sound nicht hören können.
-   **Geben Sie nicht häufig laute oder ungnönliche Töne ein.** Dies ist unnötig und führt zu einer schlechten Benutzererfahrung. Wenn ein Sound häufiger abgespielt wird, desto weniger aufdringlich sollte er sein. Sounds müssen nicht laut oder ungnend sein, um Aufmerksamkeit zu erhalten.
-   **Signalen Sie nicht.** Beeping ist für moderne Programme nicht geeignet. Signaltons können keine bestimmten Bedeutungen haben, und Benutzer können sie nicht steuern.
    -   **Ausnahme:** Kritische Systemfunktionen können benutzer auf Situationen aufmerksam machen, in denen sie sofort reagieren müssen, z. B. bei kritischem Akkustand.

### <a name="playback"></a>Wiedergabe

-   **Wiederholen Sie einen Sound nicht mehr als zweimal hintereinander.**
-   **Für eine aufeinander folgende Sequenz verwandter Soundereignisse geben Sie einen Sound nur beim ersten Ereignis wieder.** Vermeiden Sie die Verwendung mehrerer Sounds, da sie möglicherweise miteinander kollidieren oder anderweitig zu einer unfreundlichen Benutzererfahrung führen.

### <a name="sound-selection"></a>Soundauswahl

-   **Wählen Sie Töne aus.** Verwenden Sie keine rauschenden, alarmierenden Töne, z. B. Überschlagen, Abstürze und Breakings.
-   **Verwenden Sie kurze Sounds** (weniger als eine Sekunde).
-   **Verwenden Sie Sounds, die ungefähr das gleiche Volumen wie der typische Windows-Sound haben.** Benutzer möchten das Volume beim Starten eines Computers oder Programms nicht deaktivieren, insbesondere in öffentlichen Umgebungen wie Besprechungen und Präsentationen. Die Microsoft Windows-Sounddateien befinden sich im Ordner Media im Windows-Ordner.
-   **Wählen Sie keine Sounds aus, die Lokalisierung erfordern.** Sie können dies erreichen, indem Sie Sounds verwenden, die keine Sprache verwenden oder kulturabhängige Bedeutungen oder Konnotationen haben.

### <a name="windows-system-sounds"></a>Windows-Systemklänge

-   **Verwenden Sie nach Bedarf die integrierten Windows-Systemklänge.**
-   **Verwenden Sie Systemsounds basierend auf ihrer zugeordneten Bedeutung, nicht nur auf dem Sound selbst.** Systemklänge müssen konsistent verwendet werden.

### <a name="sound-design"></a>Sounddesign

Beim Erstellen eigener Sounds:

-   **Erstellen Sie Sounds mit den gewünschten Soundmerkmalen.**
-   **Erstellen Sie Sounds mit größtenteils mittleren bis hohen Frequenzen (600 Hz bis 2 kHz).** Verwenden Sie keine niedrigen Frequenzen, da sie weiter entfernt sind, schwieriger zu finden sind und alarmierend sein können.
-   **Legen Sie die relative Amplitude normaler Sounds auf die Ebene des typischen Windows-Sounds fest.** Die Windows-Sounds wurden für Heim- und Arbeitsumgebungen entsprechend angepasst. Wenn Sie verschiedene Ebenen für Ihre Sounds verwenden, werden Benutzer dazu zwingen, Lautstärkeanpassungen vorzunehmen.
    -   Legen Sie wichtige Sounds auf etwas lauter fest. Zu diesen Sounds gehören Aktionen, Aktionsfehler und wichtige Systemereignisse.
    -   Legen Sie häufig auftretende Sounds so fest, dass sie etwas weicher sind. Dazu gehören FYIs, Branding-Sounds und Soundeffekte.
-   **Wählen Sie Sounds aus, die mit der Bedeutung der Windows-Sounds konsistent sind.** Um eine benutzerdefinierte Version eines Windows-Sounds zu erstellen, behalten Sie die gleiche Tonhöhe und das gleiche Intervall bei, aber ändern Sie die Orchestrierung oder Timbre. Weisen Sie Sounds mit ähnlichen Tonhöhen und Intervallen wie Windows-Sounds keine unterschiedlichen Bedeutungen zu.
-   **Entwerfen Sie die Sounds für Ihr Programm so, als ob es sich um verwandte Variationen eines Designs handelt.** Die audity-Erfahrung Ihres Programms sollte mit der visuellen Erfahrung koordiniert werden.
    -   **Entwerfen Sie Szenenübergänge und Audioübergänge zusammen.** Wenn eine Szene z. B. allmählich ausblendet, sollte jeder Sound auch schrittweise ausgeblendet werden. Lassen Sie nahtlose visuelle Übergänge nicht durch plötzliche Soundübergänge zu.
-   **Sounds müssen im WAV-Dateiformat vorliegen.** Das 16-Bit- und 44,1-kHz-Stereoformat unkomprimierten Pulse Code Codes (PCM) wird empfohlen. Wenn die Dateigröße wichtig ist, verwenden Sie komprimierte oder bare (Mono)-Formate, aber beachten Sie, dass es einen leicht erkennbaren Qualitätsverlust gibt, der sich in Ihrer Anwendung schlecht widerspiegeln kann.

### <a name="mixing"></a>Mischen

-   **Das Programm hat keine Steuerelemente für Lautstärke oder Stummschaltung.** Stattdessen können Benutzer relative Volumeeinstellungen zwischen Anwendungen mit dem Windows-Volumemixer steuern. Wenn Ihr Programm über ein Volumesteuerprogramm verfügt, gibt es mehrere Stellen, an denen Benutzer ihre Einstellungen anpassen, was zu Verwirrung führen kann.

    ![Screenshot des Windows-Volumemixers ](images/vis-sound-image8.png)

    Mit dem Windows-Volumemixer können Benutzer die Haupteinstellung des Volumes sowie das Volume für jedes Programm steuern, das derzeit Audio abspielt.

<!-- -->

-   **Ausnahme:** Wenn das Programm hauptsächlich audio- oder videowiedergabe oder -erstellung ist, kann es hilfreich sein, ein Volumesteuerprogramm im Programm zu verwenden. Verwenden Sie zu diesem Zweck ein Schieberegler-Steuerelement, und geben Sie sofort Feedback, wenn der Benutzer das Volume ändert.

### <a name="windows-integration"></a>Windows-Integration

-   **Registrieren Sie die Sounds Ihres Programms in der Windows Sounds-Registrierung.** Auf diese Weise kann der Windows-Volumemixer einen Schieberegler für Das Programm hinzufügen.
-   **Registrieren Sie die benutzerdefinierten Soundereignisse Ihres Programms.** Auf diese Weise kann das Windows Sound-Systemsteuerungselement diese anzeigen. Erstellen Sie den folgenden Schlüssel für jedes benutzerdefinierte Soundereignis: HKEY \_ CURRENT \_ USER \| AppEvents \| Event Labels \| EventName = Event Name.
-   **Heften Sie die Sounds für die Soundereignisse Ihres Programms nicht fest.** Geben Sie stattdessen die Sounds an, die mithilfe von Registrierungseinträgen wiedergegeben werden sollen. Auf diese Weise können Benutzer die Soundereignisse über das Systemsteuerungselement Sound anpassen.
    -   **Ausnahme:** Sie können sich für hardwire-Sounds entscheiden, die für das Branding verwendet werden.
-   **Bieten Sie benutzern keine Möglichkeit, Sounds innerhalb der Programmoptionen zu konfigurieren.** Verwenden Sie zu diesem Zweck stattdessen das Systemsteuerungselement Windows Sounds.
-   **Weisen Sie häufig auftretenden Ereignissen standardmäßig keine Sounds zu.** Es ist nicht erforderlich, dass Benutzer ihren Weg aus einer mühsamen ersten Erfahrung konfigurieren.

### <a name="directsound-programming-issues"></a>DirectSound-Programmierprobleme

-   Legen Sie für DirectSound-Programme, die über eine eigene Volumesteuerung verfügen, **das Programmvolume standardmäßig auf 100 Prozent fest.** Dadurch wird der dynamische Bereich Ihrer Audiodaten maximiert.
-   **Sperren Sie andere Soundereignisse nicht, indem Sie Ihr Programm im exklusiven Modus ausführen.** Dadurch kann verhindert werden, dass andere Programme ordnungsgemäß funktionieren. Beispielsweise verhindert die Verwendung des exklusiven Modus, dass ein Computer als Telefoniegerät verwendet wird.

## <a name="text"></a>Text

-   Verwenden Sie nicht den Ausdruckstonadapter. Verwenden Sie stattdessen eine Soundkarte.
-   Verwenden Sie das Gerät, um generisch auf Lautsprecher, Mikrofone und Mikrofone zu verweisen.
-   Verwenden Sie den Controller, um auf Audiohardware zu verweisen, die Geräte steuert, z. B. Soundkarten und Soundkarten.
-   Verwenden Sie das Ausdruckstonschema, um eine Sammlung von Sounds für allgemeine Programmereignisse zu beschreiben, z. B. anmelden oder neue E-Mails empfangen. Verwenden Sie das Desktopdesign des Ausdrucks, um eine Sammlung visueller Elemente und Sounds für Ihren Computerdesktop zu beschreiben.
-   Verwenden Sie den Begriff Audio, um sich umfassend auf Sprache, Musik und Sounds zu beziehen. Verwenden Sie den Begriff Sound, um sich enger auf das Programm und windows-Sounds zu beziehen, die in diesem Artikel beschrieben werden.

 

