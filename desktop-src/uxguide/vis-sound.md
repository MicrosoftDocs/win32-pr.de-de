---
title: Sound
description: Sound ist das Audioelement des Benutzer Erlebnisses.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 664d78d00cf75dae8f43717db07290a26574f0c6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104553232"
---
# <a name="sound"></a>Sound

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

*Sound* ist das Audioelement des Benutzer Erlebnisses. Bei entsprechender Verwendung kann Sound eine effektive Form der Kommunikation sein, die eine nicht verbale und sogar emotionale Beziehung mit ihren Benutzern herstellt. Sounds können allein oder als Ergänzung der visuellen Benutzeroberfläche verwendet werden. Das Hinzufügen eines Sound Effekts zu einer Benachrichtigung erhöht z. b. die Wahrscheinlichkeit, dass diese bemerkt wird, insbesondere, wenn der Benutzer den Bildschirm nicht auf dem Bildschirm ansieht, wenn ein Ereignis auftritt.

![Screenshot des Dialog Felds "Sound" ](images/vis-sound-image1.png)

Auf der Registerkarte Sounds des System Steuerungs Elements "Sound" können Benutzer Änderungen an Ihren System Sounds vornehmen.

In diesem Artikel wird die Verwendung von Sounds innerhalb eines Programms als Reaktion auf Ereignisse und Benutzeraktionen und das Integrieren des Sound Steuer Elements eines Programms in Windows behandelt. Die Verwendung von Musik oder Sprache wird nicht abgedeckt.

**Hinweis:** Richtlinien für [Benachrichtigungen](mess-notif.md) und [Branding](exper-branding.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Um zu entscheiden, ob Sie Sound verwenden sollten, berücksichtigen Sie die folgenden Fragen:

-   **Gibt es einen deutlichen Benutzer Vorteil bei der Verwendung von Sound?** Da die Nachteile der Verwendung von Sound leicht die Vorteile überwiegen können, sollten Sie nur Sound verwenden, wenn ein eindeutiger Vorteil vorliegt.
-   **Ist die Verwendung von Sound angemessen?** Wird die Verwendung von Sound auf Dinge aufmerksam gemacht, die beachtet werden müssen? Würden Benutzer den Sound übersehen, wenn Sie nicht vorhanden waren? Konzentrieren Sie sich auf Sounds, die Benutzer auf dem laufenden halten, ihre Verhaltensweisen wahrscheinlich ändern oder nützliches Feedback bereitstellen.
-   **Ist die Verwendung von Sound ablenkend?** Gibt es häufige, laute jarringsounds? Können Benutzer das System Volume oder das Volume Ihres Programms aufgrund ihrer Verwendung von Sound wahrscheinlich reduzieren?
-   **Verwenden Sie Sound als primäre Form der Kommunikation?** In vielen Fällen, z. b. bei Benutzern, die eine bestimmte Ebene an Hörverlusten haben, sollte Sound nicht als primäres Kommunikationsmittel verwendet werden. Sound ist effektiver als Ergänzung zu anderen Kommunikationsmöglichkeiten (z. b. Text oder Visuals).
-   **Sind die primären Ziel Benutzer IT-Experten?** Sound ist in der Regel für Aufgaben, die auf IT-Experten abzielen, nicht effektiv, da viele ihrer Aufgaben unbeaufsichtigt ausgeführt Außerdem wird Sound nicht für Sie skaliert, sondern es wird nicht gleichzeitig Hunderte von Aufgaben ausgeführt, und es werden Sounds angezeigt, wenn Sie fertig sind oder nicht.

## <a name="design-concepts"></a>Entwurfskonzepte

Sound erzielt in der Regel einen oder alle der folgenden Zwecke:

-   **Benachrichtigung**. Mit einem Sound können bestimmte Ereignisse verknüpft werden. Beispielsweise weist ein "New Mail"-Sound Benutzern an, wenn eine e-Mail eingeht, ohne die aktuelle Aufgabe zu unterbrechen.
-   **Backs.** Sound kann Feedback für bestimmte Benutzeraktionen liefern. Beispielsweise bietet ein feiner Sound, der beim Freigeben des Schiebereglers für das volumesteuerelement abgespielt wird, Feedback zur Ebene der aktuellen Einstellung.
-   **BR.** Sound kann bestimmten Inhalten zugeordnet werden, um Ihr Produkt, Ihre Anwendung oder ihren Dienst zu Marken. Windows verwendet Sound auf diese Weise für den Start des Betriebssystems.
-   **Animations.** Sound wird häufig verwendet, um Unterhaltungsprodukte zu verbessern und das Produkt ansprechender zu gestalten. Beispielsweise verwenden die meisten Spiele, Schulungs Anwendungen und Consumerprodukte Sound, um Benutzer zu untersuchen und Ihre Benutzeroberflächen zu verbessern.

Bestimmte Sounds können mehrere dieser Zwecke gleichzeitig erfüllen. Der Windows-Start Sound zeigt z. b. an, dass der Startvorgang abgeschlossen wurde und der Desktop einsatzbereit ist. Außerdem bietet Sie eine leistungsstarke Form des Produkt Brandings und führt sogar eine Benutzeranwendung aus.

Sounds, die keines dieser Zwecke erfüllen, sollten wahrscheinlich eliminiert werden.

### <a name="inappropriate-use-of-sound"></a>Ungeeignete Verwendung von Sound

**Trotz der Vorteile von Sound erfordert die angemessene Verwendung von Sound eine deutliche Unterhaltung, damit ein Programm lästig und ablenkend ist.** Benutzer werden Ihren Sound vollständig deaktivieren, wenn Sie sich von häufigen, sich wiederholenden, Jarring, Unterbrechungen und schlecht entworfenen Sounds ärgern. der Grund hierfür ist, dass die audioaufmerksamkeit in der Natur von Bedeutung ist und schwer zu ignorieren ist. Tipps zum Ermitteln eines angemessenen Ausgleichs finden Sie in den [Sound Entwurfs Richtlinien](#sound-design).

Da die Nachteile der Verwendung von Sound leicht die Vorteile überwiegen können, sollten Sie nur Sound verwenden, wenn ein eindeutiger Vorteil vorliegt. **Verwenden Sie im Zweifelsfall keinen Sound.**

### <a name="make-sound-supplemental"></a>Erstellen Sie einen zusätzlichen Sound

Auch wenn der Sound entsprechend verwendet wird, gibt es viele Situationen, in denen Sound möglicherweise nicht für alle Benutzer gültig ist:

-   Einige Benutzer arbeiten möglicherweise in einer lärmenden Umgebung, in der die Sounds nicht zu hören sind.
-   Einige Benutzer arbeiten möglicherweise in einer stillen Umgebung, bei der der Sound auf einem niedrigen Volume ausgeschaltet oder festgelegt werden muss.
-   Einige Benutzer haben möglicherweise eine Beeinträchtigung oder einen Verlust des Hörens.
-   Der Computer verfügt möglicherweise nicht über Redner.

Aus diesen Gründen **sollte der für Benachrichtigungen und Feedback verwendete Sound nie die einzige Kommunikationsmethode sein,** sondern auch visuelle oder Text Hinweise ergänzen.

### <a name="desirable-characteristics-of-sound"></a>Begehrte Merkmale von Sound

Im Allgemeinen sollten Sounds wie folgt lauten:

-   Mid bis High Frequency (600 Hertz \[ Hz \] bis 2 Kilohertz \[ kHz \] ).
-   Short (weniger als eine Sekunde).
-   weich oder Mittel in Volume.
-   aussagekräftige.
-   angenehm, nicht alarmierend oder Jarring.
-   nicht verbal.
-   nicht wiederholende.

Mit Sound ist weniger weniger. **Der ideale Soundeffekt ist eine, die Benutzer kaum bemerken, aber Sie würden übersehen, wenn Sie nicht vorhanden wäre.**

**Ein gängiges Missverständnis ist, dass Sounds für kritische Ereignisse eine laute und jarringanforderung sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.** Dies trifft nicht zu, weil Sound wirklich eine ergänzende Kommunikationsmethode darstellen soll. Im Fall einer kritischen Fehlermeldung wird die Darstellung (z. u. in einem modalen Dialogfeld), das zugehörige Symbol (ein Fehler Symbol) und der zugehörige Text und Ton alle kombiniert, um die Art des Fehlers zu übermitteln. Ein effektiver Fehlerton kann etwas lauter als der typische Windows-Sound sein, muss aber nicht bedeutend lauter sein.

### <a name="characteristics-of-windows-sounds"></a>Merkmale von Windows-Sounds

Über diesen allgemeinen aufrufungstyp hinaus verwendet die Windows Sound-Ästhetik einfache, reine Töne und Glas-und luftige Klänge mit einem weichen einblenden und ausblenden (weiche "Kanten"), um abrupte, jarrte und perven Effekte zu vermeiden. Sie sind so konzipiert, dass Sie sehr fein, sanft und Konsonant sind. Windows-Sounds verwenden Echo, den Reverb und die Ausgleichs Methode, um ein natürliches Verhalten zu erzielen.

Das standardmäßige Sound Schema für Windows verwendet in der Regel keine aussagekräftigen oder erkennbaren alltäglichen Sounds, die übermäßig spezifisch oder musikalisch sind. Beispiele für Sounds, die es vermeidet, sind Musikinstrumente wie z. b. Klavier-oder Percussion-Instrumente, tierische Klänge, Umwelt Geräusche, Sprache, Stimmen, filmähnliche Soundeffekte oder andere Klänge von Menschen. Außerdem sind Windows-Sounds nicht für die Wahrnehmung als Musik gedacht (d. h., es handelt sich um mehr Notiz Melodien). Dadurch können Windows-Sounds funktionell von anderen Arten von Sounds unterschieden werden.

Da die Windows-Sounds professionell entworfen wurden, um die gewünschten Merkmale zu haben, und eine große Zielgruppe ansprechen, empfiehlt es sich, **diese integrierten Windows-Sounds zu verwenden, wenn dies angebracht ist.**

### <a name="designing-your-own-sounds"></a>Entwerfen eigener Sounds

Wenn Sie eigene Sounds erstellen müssen, entwerfen Sie diese so, dass Sie die zuvor beschriebenen Merkmale aufweisen. Möchten Sie die zugehörigen Aufgaben oder Ereignisse ergänzen.

Beachten Sie, dass das Erstellen ursprünglicher Sounds schwierig ist, insbesondere für Sounds, die für eine breite Zielgruppe gedacht sind. Sound kann ein polarisierendes Entwurfs Element sein. Für jeden Benutzer, der einen Sound liebt, gibt es viele, die ihn nicht beachten.

**Entwerfen Sie die Sounds für Ihr Programm als Gruppe, um sich zu fühlen, dass es sich um verwandte Variationen eines Designs handelt.** Das Akustik Ihres Programms sollte mit seiner visuellen Darstellung koordiniert werden. Außerdem sollte der Ton der Klänge mit dem [Text des](text-style-tone.md)Texts koordiniert werden. Stellen Sie sich vor, wie Text mit einem angenehmen, natürlichen Ton durch harte, alarmierende Sounds durchlaufen werden kann.

**Wenn Sie nur vier Dinge tun...**

1.  Verwenden Sie Sound mit Zurückhaltung, und stellen Sie sicher, dass ein eindeutiger Benutzer Vorteil vorliegt. Verwenden Sie im Zweifelsfall keinen Sound.
2.  Verwenden Sie die integrierten Windows-Sounds, wenn dies angebracht ist.
3.  Wenn Sie Ihre eigenen Sounds entwerfen, stellen Sie sicher, dass Sie über die gewünschten Sound Merkmale verfügen und sich als Ganzes wie Variationen eines Designs fühlen.
4.  Gehen Sie nicht davon aus, dass Sounds eine laute und eine jarringanforderung sein müssen, um die Aufmerksamkeit des Benutzers zu erhalten.

## <a name="usage-patterns"></a>Verwendungsmuster

Sounds haben mehrere Verwendungs Muster:



|                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aktions Abschluss**<br/> Benutzer benachrichtigt Benutzer, wenn eine Benutzer initiierte Aktion mit langer Laufzeit erfolgreich abgeschlossen wurde. <br/>                             | ![Screenshot des Dialog Felds zum Herunterladen von Dateien ](images/vis-sound-image2.png)<br/> In diesem Beispiel gibt das Dialogfeld einen Sound wieder, um die Benutzer darüber zu benachrichtigen, dass der Download abgeschlossen ist.<br/>                                                                                                                                                                                                                                      |
| **Aktions Fehler**<br/> Benutzer benachrichtigt Benutzer, wenn eine Benutzer initiierte Aktion mit langer Laufzeit fehlschlägt. <br/>                                                 | ![Screenshot der Meldung "Sicherungs Datenträger nicht erreichbar" ](images/vis-sound-image3.png)<br/> In diesem Beispiel gibt Windows einen Sound wieder, um die Benutzer darüber zu benachrichtigen, dass der Sicherungs Vorgang fehlgeschlagen ist.<br/>                                                                                                                                                                                                                                  |
| **Wichtiges System Ereignis**<br/> sonisch benachrichtigt Benutzer über wichtige Systemereignisse oder-Status, die sofortige Aufmerksamkeit erfordern. <br/>                      | ![Screenshot bei geringer Akku Nachricht ](images/vis-sound-image4.png)<br/> In diesem Beispiel werden Benutzer darüber benachrichtigt, dass ihre geringe Akkukapazität sofortige Aufmerksamkeit erfordert.<br/>                                                                                                                                                                                                                                                      |
| **Zur Kenntnisnahme**<br/> sonisch benachrichtigt Benutzer über potenziell nützliche, relevante Informationen. <br/>                                                                 | Da diese Informationen in der Regel keine sofortige Aufmerksamkeit erfordern, bietet ein voll Tonbild, das ein feines Feedback bietet, ohne den Flow des Benutzers zu unterbrechen. <br/> ![Screenshot der Live Messenger-Anmelde Nachricht ](images/vis-sound-image5.png)<br/> In diesem Beispiel wird ein Sound abgespielt, wenn sich ein Kontakt an einem Instant Messaging-Dienst anmeldet.<br/>                                                                                 |
| **Sound Effekt**<br/> sonisch stellt Feedback für Benutzerinteraktionen bereit. <br/>                                                                            | Bietet echte oder formatierte Sound Feedback, das für die Interaktion geeignet ist. Soundeffekte klingen oft so, als ob der Benutzer ein physisches physisches Objekt bearbeitet. wird manchmal auch als Foley bezeichnet. <br/> ![Screenshot des minimierten Fensters ](images/vis-sound-image6.png)<br/> In diesem Beispiel hört sich der Soundeffekt des minimieren Fensters so an, dass die Größe eines echten Objekts reduziert wird.<br/> |
| **Brandingsounds**<br/> ein Sound, der bereitgestellt wird, um die Benutzer Leistung durch emotionale Auswirkung zu verbessern und die Produktmarke als Nebeneffekt zu fördern. <br/> | Brandingsounds eignen sich am besten, wenn Sie mit visuellen Ereignissen synchronisiert werden, insbesondere von UI-Übergängen wie der Anzeige eines Programmfensters. echte Sound Marken geben die Quelle der waren an, ähnlich wie ein Wort oder Logo, das mit einem Wort versehen ist, und sind relativ ungewöhnlich. <br/> ![Screenshot des Windows-Start Symbols ](images/vis-sound-image7.png)<br/> In diesem Beispiel ist der Windows-Start ein vorübergehender Übergang.<br/>      |



 

## <a name="guidelines"></a>Richtlinien

### <a name="usage"></a>Verbrauch

-   **Verwenden Sie Sound mit Zurückhaltung, und** stellen Sie sicher, dass ein eindeutiger Benutzer Vorteil vorliegt. Konzentrieren Sie sich auf Sounds, die Benutzer auf dem laufenden halten, ihre Verhaltensweisen wahrscheinlich ändern oder nützliches Feedback bereitstellen. Verwenden Sie im Zweifelsfall keinen Sound.
-   **Wählen Sie den Sound und seine Merkmale basierend auf seiner Verwendung aus.** Eine Beschreibung der einzelnen Verwendungs Muster finden Sie in der Tabelle im vorherigen Abschnitt.
-   **Verwenden Sie für Benachrichtigungen und Feedback nicht Sound als einzige Kommunikationsmethode.** Verwenden Sie stattdessen Sound als ergänzende Methode, um visuelle oder Text Hinweise zu verstärken. Dadurch wird sichergestellt, dass Benutzer die Informationen sehen können, wenn Sie den Sound nicht hören können.
-   **Spielen Sie häufig keine laute oder rauen Sounds.** Dies ist unnötig und führt zu einem schlechten Benutzer Verhalten. Umso häufiger wird ein Sound wiedergegeben, der weniger obresive es sein sollte. Sounds müssen nicht laut oder hart sein, um Aufmerksamkeit zu erregen.
-   **Nicht mit einem Signal.** Das anken ist für moderne Programme nicht geeignet. Für die abeps können keine bestimmten Bedeutungen zugewiesen werden, und Benutzer können Sie nicht steuern.
    -   **Ausnahme:** Wichtige Systemfunktionen können darauf hinweisen, dass Benutzer über Situationen benachrichtigt werden, an denen Sie sofort teilnehmen müssen, z. b. eine äußerst geringe Akkuleistung.

### <a name="playback"></a>Wiedergabe

-   **Wiederholen Sie einen Sound nicht mehr als zwei Mal hintereinander.**
-   **Geben Sie für eine aufeinander folgende Sequenz von verknüpften Sound Ereignissen nur für das erste Ereignis einen Sound wieder.** Vermeiden Sie die Verwendung mehrerer Sounds, da Sie miteinander in Konflikt stehen oder andernfalls zu einer unangenehmen Benutzer Darstellung führen können.

### <a name="sound-selection"></a>Sound Auswahl

-   **Wählen Sie angenehme Sounds aus.** Verwenden Sie keine unangenehmen, alarmierenden Sounds, wie z. b. das treiben, abstürzen und unterbrechen.
-   **Verwenden Sie kurze** (weniger als eine Sekunde) Sounds.
-   **Verwenden Sie Sounds, die ungefähr demselben Volume wie der typische Windows-Sound entsprechen.** Benutzer müssen das Volume beim Starten eines Computers oder Programms nicht deaktivieren, insbesondere in öffentlichen Umgebungen wie Besprechungen und Präsentationen. Die Microsoft Windows-Sounddateien befinden sich im Ordner "Media" im Ordner "Windows".
-   **Wählen Sie keine Sounds aus, die eine Lokalisierung erfordern.** Dies können Sie erreichen, indem Sie Sounds verwenden, die keine Sprache verwenden, oder Kultur abhängige Bedeutungen oder Einschränkungen haben.

### <a name="windows-system-sounds"></a>Windows-Systemsounds

-   **Verwenden Sie die integrierten Windows-Systemsounds, wenn dies angebracht ist.**
-   **Entscheiden Sie sich für die Verwendung von Systemsounds basierend auf der zugehörigen Bedeutung, nicht nur auf dem eigentlichen Sound.** System Sounds müssen konsistent verwendet werden.

### <a name="sound-design"></a>Sound Design

Beim Erstellen eigener Sounds:

-   **Erstellen Sie Sounds mit den gewünschten Sound Merkmalen.**
-   **Erstellen Sie Sounds mit größtenteils mittlerer Breite bis zu hohen Frequenzen (600 Hz bis 2 kHz).** Verwenden Sie keine niedrigen Frequenzen, da Sie weiter gehen, schwieriger zu finden sind und alarmierend sein können.
-   **Legen Sie die relative Amplitude normaler Sounds auf die Ebene des typischen Windows-Sounds fest.** Die Windows-Sounds wurden für Heim-und Arbeitsumgebungen entsprechend angepasst. Wenn Sie unterschiedliche Ebenen für Ihre Sounds verwenden, werden Benutzer gezwungen, volumeanpassungen vorzunehmen.
    -   Legen Sie wichtige Sounds auf etwas lauter fest. Zu diesen Sound gehören Aktions Vervollständigungen, Aktions Fehler und wichtige Systemereignisse.
    -   Legen Sie häufig auftretende Sounds als etwas weicher fest. Hierzu gehören FYIs, brandingsounds und Soundeffekte.
-   **Wählen Sie Sounds aus, die mit der Bedeutung der Windows-Sounds übereinstimmen.** Um eine benutzerdefinierte Version eines Windows-Sounds zu erstellen, behalten Sie die gleiche Tonhöhe und das gleiche Intervall bei, ändern aber die Orchestrierung oder das Timbre. Weisen Sie Sounds mit ähnlichen Feldern und Intervallen wie Windows Sounds keine unterschiedlichen Bedeutungen zu.
-   **Entwerfen Sie den Sound für das Programm so, dass es sich um verwandte Variationen eines Designs handelt.** Das Akustik Ihres Programms sollte mit seiner visuellen Darstellung koordiniert werden.
    -   **Entwurfs Szenen Übergänge und audioübergänge.** Wenn eine Szene z. b. schrittweise ausgeblendet wird, sollte jeder Sound allmählich auch ausgeblendet werden. Vermeiden Sie nahtlose visuelle Übergänge durch abrupte Sound Übergänge.
-   **Sounds müssen im WAV-Dateiformat vorliegen.** Das 64-Bit-Format für die 16-Bit-, 44,1-Bit-Stereo Anwendung (nicht komprimierte Pulse Code Modulation) wird empfohlen Wenn die Dateigröße wichtig ist, verwenden Sie komprimierte oder Monale (Mono) Formate, aber beachten Sie, dass es einen leicht erkennbaren Qualitätsverlust gibt, der für Ihre Anwendung schlecht widerspiegeln kann.

### <a name="mixing"></a>XT

-   **Sie verfügen über keine Lautstärke-oder stumm Steuerelemente in Ihrem Programm.** Überlassen Sie die Benutzer stattdessen die relativen Volumeeinstellungen zwischen Anwendungen mit dem Windows-volumemixer. Wenn das Programm über ein Volumen Steuerelement verfügt, gibt es mehrere Stellen, an denen die Benutzer Ihre Einstellungen anpassen, was zu Verwechslungen führen kann.

    ![Screenshot des Windows-volumemischers ](images/vis-sound-image8.png)

    Mit dem Windows-volumemixer können Benutzer die hauptvolumeeinstellung sowie das Volume für jedes Programm steuern, das gerade Audiodaten wieder gibt.

<!-- -->

-   **Ausnahme:** Wenn das Programm eine Audio-oder Videowiedergabe oder-Erstellung ist, ist es möglicherweise hilfreich, eine volumesteuerung im Programm zu haben. Verwenden Sie für diesen Zweck ein Schieberegler-Steuerelement, und geben Sie sofort Feedback ein, wenn der Benutzer das Volume ändert

### <a name="windows-integration"></a>Windows-Integration

-   **Registrieren Sie die Sounds Ihres Programms in der Windows Sounds-Registrierung.** Auf diese Weise kann der Windows-volumemixer einen Schieberegler für das Programm hinzufügen.
-   **Registrieren Sie die benutzerdefinierten Sound Ereignisse Ihres Programms.** Auf diese Weise kann das Fenster "Sound" der Systemsteuerung angezeigt werden. Erstellen Sie für jedes benutzerdefinierte Sound Ereignis den folgenden Schlüssel: HKEY \_ Current \_ User \| appevents \| Ereignis Bezeichnungen \| EventName = Ereignis Name.
-   **Übertragen Sie die Klänge für die Sound Ereignisse des Programms nicht.** Geben Sie stattdessen die zu Wiedergabe enden Sounds mithilfe von Registrierungs Einträgen an. Auf diese Weise können Benutzer die Audioereignisse über das System Steuerungselement "Sound" anpassen.
    -   **Ausnahme:** Sie können die für das Branding verwendeten Sounds hart verdrahtet auswählen.
-   **Bieten Sie Benutzern keine Möglichkeit, Sounds innerhalb der Programmoptionen zu konfigurieren.** Verwenden Sie für diesen Zweck stattdessen das System Steuerungselement Windows Sounds.
-   **Ziehen Sie in Erwägung, häufig auftretende Ereignisse standardmäßig keine Sounds zuzuweisen.** Es ist nicht erforderlich, dass Benutzer ihre Art und Weise auf eine lästige anfängliche Benutzeroberflächen Weise konfigurieren.

### <a name="directsound-programming-issues"></a>Probleme mit der DirectSound-Programmierung

-   Legen Sie für DirectSound-Programme, die über eine eigene volumesteuerung verfügen, **das Programm Volume standardmäßig auf 100 Prozent fest.** Dadurch wird der dynamische Bereich ihrer Audiodaten maximiert.
-   **Sperren Sie andere Sound Ereignisse nicht, indem Sie das Programm im exklusiven Modus ausführen.** Dadurch kann verhindert werden, dass andere Programme ordnungsgemäß funktionieren. Beispielsweise wird durch die Verwendung des exklusiven Modus verhindert, dass ein Computer als Telefoniegerät verwendet wird.

## <a name="text"></a>Text

-   Verwenden Sie den Sound Adapter für Ausdrücke nicht. Verwenden Sie stattdessen Soundkarte.
-   Verwenden Sie das Gerät, um generisch auf Referenten, Kopfhörer und Mikrofon zu verweisen.
-   Verwenden Sie den Controller, um auf Audiohardware zu verweisen, die Geräte steuert, z. b. Soundkarten und Chip Sätze.
-   Verwenden Sie das Schema Sound Schema, um eine Auflistung von Sounds für allgemeine Programm Ereignisse zu beschreiben, wie z. b. die Anmeldung oder den Empfang neuer e-Mails. Verwenden Sie den Begriff Desktop Design, um eine Sammlung von visuellen Elementen und Sounds für Ihren Computer Desktop zu beschreiben.
-   Verwenden Sie den Begriff "Audio", um im Wesentlichen auf Sprache, Musik und Sounds zu verweisen. Verwenden Sie den Begriff "Sound", um genauere Informationen zu den in diesem Artikel beschriebenen Programm-und Windows-Sounds zu erhalten.

 

