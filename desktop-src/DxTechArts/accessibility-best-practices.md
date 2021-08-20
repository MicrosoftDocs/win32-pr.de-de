---
title: Barrierefreie geschäftliche Begründungen und Entwurfsüberlegungen für Spiele
description: Dieser Artikel ist für Spieleinhaltsentwickler und -entwickler, die den Communitymarkt für Barrierefreiheit erreichen möchten, indem sie grundlegende Barrierefreiheitsfeatures hinzufügen, um Personen mit Behinderungen oder Beeinträchtigungen zu unterstützen.
ms.assetid: 95580b75-fb8e-b8a9-2137-40d6c60ae35d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686258873176c99f1942cff915c072d1c1290f6a8b2411130d7e701322d4e4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051215"
---
# <a name="making-video-games-accessible-business-justifications-and-design-considerations"></a>Zugänglich machen von Videospielen: Geschäftliche Begründungen und Entwurfsüberlegungen

Spieleherausgeber und -entwickler konzentrieren sich gerne auf Features, die ihre Titel von der Mainstream-Gaming-Community bemerken, z. B. Grafiken und Audio. Es gibt aber auch eine andere Zielgruppe, die daran teilnehmen möchte. Diese Spieler stammen aus der Community für Barrierefreiheit, einer Community von Menschen mit Behinderungen sowie aus Personen, die sich um ihre Eltern kümmern.

Dieser Artikel ist für Spieleinhaltsentwickler und -entwickler, die den Communitymarkt für Barrierefreiheit erreichen möchten, indem sie grundlegende Barrierefreiheitsfeatures hinzufügen, um Personen mit Behinderungen oder Beeinträchtigungen zu unterstützen. Die folgenden Themen werden erläutert:

-   [Was ist Barrierefreiheit?](#what-is-accessibility)
-   [Warum ist die Barrierefreiheit wichtig?](#why-is-accessibility-important)
-   [Der Status der Barrierefreiheit in der Spielebranche](#the-state-of-accessibility-in-the-games-industry)
-   [Die Notwendigkeit barrierefreier Spiele](#the-need-for-accessible-games)
-   [Sehbehinderungen](#visual-impairments)
-   [Hörbehinderungen](#auditory-impairments)
-   [Mobilitätsbeeinträchtigungen](#mobility-impairments)
-   [Sehbehinderungen](#vocal-impairments)
-   [Zusammenfassung](#conclusion)
-   [Weitere Ressourcen](#more-resources)

## <a name="what-is-accessibility"></a>Was ist Barrierefreiheit?

Wenn Menschen an Barrierefreiheit denken, stellen sie sich häufig Dinge wie z. B. Beschreibungen und Untertitel auf dem Fernsehgerät vor. Dies liegt daran, dass sich diese Arten von Barrierefreiheitsfeatures von Personen mit offensichtlichen Behinderungen ab- und verwenden. Barrierefreiheitsfeatures sind jedoch nicht nur für Personen mit den schwerwiegendsten Behinderungen konzipiert. Unter den US-Computerbenutzern zwischen 18 und 64 Jahren profitieren 57 % (74,2 Millionen) wahrscheinlich von der Verwendung barrierefreier Technologien aufgrund von Behinderungen und Beeinträchtigungen, die sich auf die Computernutzung auswirken können. ("[The Market for Accessible Technology: The Wide Range of Abilities and Its Impact on Computer Use](https://www.microsoft.com/enable/research/phase1.aspx)," (Der Markt für barrierefreie Technologie: Die Breite der Fähigkeiten und ihre Auswirkungen auf die Computernutzung) Microsoft Corporation) Die Möglichkeit, das Volumen eines Payphones zu aktivieren, ermöglicht Es Menschen mit hörverfädlichem Hörverlust, sie zu verwenden. Eine Handschiene auf einem Flug mit Transport ermöglicht es einer Person mit Mobilitätsbehinderung, sie leichter zu verindren.

Manchmal sind reguläre Merkmale eines Produkts Merkmale, die Personen mit Beeinträchtigungen helfen können. Beispielsweise kann ein Benutzer mit Sehbehinderung die Kontrasteinstellungen auf einem Fernsehgerät verwenden, um die Anzeige des Bildschirms zu vereinfachen. Eine Person mit Einer-Berührungs-Telefonie kann einen Telefonanruf vereinfachen.

Barrierefreiheitsfeatures dienen in der Regel einer von fünf Arten von Behinderungen:

-   Sehbehinderung: Blindheit, Unfähigkeit, Farben, unscharfes Sehen und so weiter zu unterscheiden.
-   Hören: Schwerhörigkeit, Gehörschädigkeit.
-   Spracherkennung: Beeinträchtigungen der Spracherkennung, Sprachunterschiede.
-   Mobilität: Beeinträchtigungen von Hand, Arm, Bein und Hand.
-   Cognitive: Learning Beeinträchtigungen und Schwierigkeiten bei der Beeinträchtigung, einschließlich Derexie.

Im Kontext von Spielen bedeutet das Hinzufügen von Barrierefreiheit, dass ein Titel für eine Person mit einer dieser Behinderungen verwendet werden kann.

## <a name="why-is-accessibility-important"></a>Warum ist die Barrierefreiheit wichtig?

Es gibt sowohl soziale als auch finanzielle Gründe, warum Spieleentwickler darüber nachdenken sollten, ihre Produkte zugänglich zu machen.

Für Kinder und kinderbehinderte Kinder mit Behinderungen, die von Derb bis zu schwerwiegend reichen, können Spiele eine Reihe von Vorteilen bieten. Forscher an der Wheeling University haben vor Kurzem festgestellt, dass das Spielen von Sport- oder Schlägerspielen dazu beiträgt, Kinder und kindergef&160;&16;/&160;/&16;/&16;/&16;/&160;&160;/&160;/&160;/&&160;/& Darüber hinaus wurde gezeigt, dass Mithilfe von Videospielen Kinder effektiver und mit weniger Nebeneffekten behandelt werden können (The Associated Press, 19. Dezember 2004). Spiele werden sogar für die Behandlung von Patienten eingesetzt. Die Übung, die für die Wiederherstellung nach 1000 Jahren von entscheidender Bedeutung ist, wurde durch die Verwendung von Spielen wie Der revolutionierte (c) Revolution(c) empfohlen, wenn Kinder sich lehnen, an anderen Formen physischer Aktivitäten teilzunehmen.

Darüber hinaus kann das Zulassen von Personen mit Beeinträchtigungen (insbesondere Kinder) an Aktivitäten teilnehmen, die die meisten Personen als selbstverständlich nutzen, um emotionale Beeinträchtigungen und das Gefühl, ein Außenseiter zu sein, zu reduzieren.

Soziale Gründe sind nicht die einzigen Gründe, warum Spieleentwickler Barrierefreiheitsfeatures in ihre Titel einführen sollten. Barrierefreiheitsfunktionen können den Umsatz steigern, indem Sie Menschen mit Behinderungen dazu ermutigen, einen barrierefreien Titel zu erwerben. Höhere Umsätze können auch von Gamern stammen, die ein Unternehmen unterstützen möchten, das die Community für Barrierefreiheit unterstützt. Und schließlich die positive P.R. in den Medien sowie in Denkgruppen für Barrierefreiheit bietet kostenlose Werbung.

Die Nachfrage nach Barrierefreiheit wird mit dem Alter der Gaming-Bevölkerung weiter zunehmen. Wenn Die Menschen älter werden, können Beeinträchtigungen durch Beeinträchtigungen durch Denk- und Sehbehinderungen schwerwiegender werden. Außerdem entwickeln Menschen wahrscheinlich neue Schwierigkeiten und Beeinträchtigungen, wenn sie altern. Das Hinzufügen grundlegender Barrierefreiheitsfeatures zu Titeln kann Herausgebern und Entwicklern helfen, weiterhin Umsatz von diesen Kunden zu erzielen.

## <a name="the-state-of-accessibility-in-the-games-industry"></a>Der Status der Barrierefreiheit in der Spielebranche

In den meisten Spielebranchen hat die Barrierefreiheit in Videospielen eine niedrige Priorität. Ein Grund ist, dass Entwickler nicht über Probleme mit der Barrierefreiheit barrierefreiheitsbewusst sind. Entwickler, die nicht deaktiviert sind, sind sich möglicherweise nicht bewusst, wie sie einen Titel für Personen mit Behinderungen oder Beeinträchtigungen zugänglicher machen können.

Ein weiterer Grund ist, dass Entwickler über eine begrenzte Menge an Zeit und Ressourcen verfügen. Kosten-Nutzen-Analysen führen häufig zu dem Schluss, dass Barrierefreiheitsprobleme die Aufmerksamkeit und Investition der Spielebranche aufgrund von Annahmen wie den folgenden nicht wert sind:

-   Die Kosten für die Implementierung von Barrierefreiheitsfeatures lohnt sich nicht.
-   Es gibt nicht genügend Zielgruppen, um die Entwicklung der Barrierefreiheit sinnvoll zu machen.

Diese Annahmen sind fehlerhaft. Es lohnt sich, Spiele zugänglich zu machen.

## <a name="the-need-for-accessible-games"></a>Die Notwendigkeit barrierefreier Spiele

2003 hat Microsoft Corporation Forrester Research, Inc. eine umfassende Studie durchgeführt, um den aktuellen und potenziellen Markt barrierefreier Technologien im USA zu messen und zu verstehen, wie barrierefreie Technologien heute eingesetzt werden. Die Studie hat ermittelt, dass 57 % der Computerbenutzer wahrscheinlich oder sehr wahrscheinlich von der Verwendung barrierefreier Technologien profitieren werden. Und die zukünftige Nachfrage nach Barrierefreiheit wird nur noch zunehmen ("[Accessible Technology in Computing: Examining Awareness, Use, and Future Potential](https://www.microsoft.com/enable/research/phase2.aspx), Microsoft Corporation).

**Abbildung 1: Vorhergesagtes Wachstum bei der Anzahl der Benutzer zugänglicher Technologien von 2003 bis 2010**

![vorhergesagtes Wachstum der Anzahl der Benutzer zugänglicher Technologien von 2003 bis 2010](images/accessibility-growth.gif)

Die Studie hat auch festgestellt, dass die Verwendung von Barrierefreiheitsfeatures nicht auf Personen mit Behinderungen beschränkt war. Unter Computerbenutzern, die integrierte Barrierefreiheitsoptionen und Hilfsprogramme verwenden:

-   32 % haben keine Behinderungen oder Beeinträchtigungen.
-   68 % haben eine verletzungs- oder schwerwiegende Behinderungen oder Beeinträchtigung.

Die empirische Beobachtung deutet darauf hin, dass dies nicht nur ein Trend ist, der auf PCs beschränkt ist. Barrierefreiheitsfeatures werden häufig von Menschen ohne Behinderungen verwendet, um ihr Spielerlebnis zu verbessern. Beispielsweise könnte ein Gamer eine vorübergehende Behinderungen (z. B. einen gebrochenen Daumen), Umgebungsprobleme (z. B. Hintergrundgeräusche) oder andere situationelle Faktoren kompensieren.

Angesichts des potenziellen Anstiegs der Nutzung von Barrierefreiheitstechnologie ist es von entscheidender Bedeutung, die Verwaltung, Designer, Entwickler und Tester zu schulen. Viele Unternehmen suchen nach Möglichkeiten, sich außerhalb der demografischen 18-32 Jahre auf neue Märkte zu erweitern. Während Herausgeber darüber spähnen, wie sie wenig Suzy dazu bringen können, Spiele zu spielen, oder Opa und Opa, um einen Controller zu holen, gibt es einen Markt, der aus Personen besteht, die einfach Mainstream-Spiele spielen möchten, die unbemerkt sind. Der potenzielle Umsatz, der durch einen relativ geringen Aufwand erzielt werden kann, der grundlegende Barrierefreiheitsfunktionen in einem Titel bietet, ist sehr spürbar.

Die Einbeziehung grundlegender Barrierefreiheitsfeatures in einen Titel kann den Umsatz durch einen "Dominoeffekt" steigern, z. B. durch Erreichen von Gamern, die normalerweise nicht in der Lage wären, den Titel zu spielen, oder deren Erfahrung erheblich abnimmt. Indem Sie diese Spieler erreichen, erreichen Sie auch die Community für Barrierefreiheit (bekannt für einen schnellen Austausch von Informationen zu barrierefreien Produkten und deren unterstützung durch Unternehmen, die die Barrierefreiheit fördern). Unternehmen, die eine aktive Rolle in dieser Community übernehmen, profitieren von einer positiven Medienbelichtung.

Wenn Sie Barrierefreiheitsfeatures nicht verwenden, besteht das Risiko potenzieller Einbußen und Einbußen und der daraus resultierende Umsatzverluste. Viele Einzelhändler und Einzelhändler wurden wegen fehlender Barrierefreiheit belangt, und im Technologiebereich hat die blinde Community Internet Explorer 4 wegen fehlender Barrierefreiheit unterlag.

Im Folgenden finden Sie verschiedene Kategorien von Behinderungen. Jede Kategorie enthält einige relativ einfach zu implementierende Vorschläge, die einen Titel für eine größere Zielgruppe zugänglich machen können.

## <a name="visual-impairments"></a>Sehbehinderungen

*"Auf meine Präsentation folgt eine rege Frage-Antwort-Sitzung, und ein beachtenswerter Moment ist aufgetreten, als einer der Mitarbeiter eine Frage zur Barrierefreiheit in unseren \[ Spielen \] gestellt hat... diese 28-jahreige Mitarbeiterin ist ein gieriger Spieler, der unser Spiel mit einem großen Kreis von \[ \] Freunden spielt. Da er jedoch farbenblind ist, war es für ihn schwierig, die gute Heiterheit von den schlechten Schlägen zu erzählen, und das Spiel wurde schließlich zu frustrierend. Wenn die neue Version... wir hatten das Problem nicht behoben. Er und seine Freunde haben sich entschieden, stattdessen das Spiel eines Mitbewerbers \[ zu kaufen." ein anonymer Branchenleiter \]*

Der Begriff "Sehbehinderung" bringt häufig einen Menschen ins Kopf, der völlig blind ist. Es ist jedoch verblendend zu wissen, dass 8,7 % der bevölkerungsgruppe von einem Grad an Farbblindheit betroffen sind (" Wie erben Menschen[Farbenblindheit? Wie oft?](https://www.webexhibits.org/causesofcolor/2C.mdl)," WebExhibits.org). Weitere 1,2 % der Personen sind von schwerwiegenderen Formen der Sehbehinderung betroffen ("Informationen zu Behinderungen: Informationsblatt zu sehbehinderten Personen",[Nationales](https://nichcy.org/disability/specific/visualimpairment)Rechenzentrum für Kinder mit Behinderungen). Das bedeutet, dass fast jeder zehnte potenzielle Spieler Probleme hat, die sich auf das Augenlicht auswirken und sich auf das Spielerlebnis auswirken können.

Stellen Sie sich vor, dass:



| You Are A Gamer      | Und sie befinden sich in diesem Szenario                                                                                                                                                                         |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mit normalem Sehen   | Es ist hell und sonnig, sodass Sie keine dunklen Objekte auf dem Bildschirm sehen können. <br/> Sie verfügen über ein altes Fernsehset, sodass Sie aufgrund einer schlechten Bildqualität keine kleinen Objekte und Keinen Text sehen können. <br/> |
| Mit sehbehinderter Sehbehinderung | Einige Spieltexte sind so klein, dass Sie sie nicht lesen können. <br/> Sie sind farbblind, damit Sie nicht wissen, welche Schaltfläche gedrückt werden soll, wenn das Spiel Sie anfing, die rote Taste zu drücken. <br/>                   |



 

Mit einigen einfachen Schritten und Features können Sie diese Probleme beheben und das Spielerlebnis für Spieler mit normaler Sehbehinderung und Gamer mit sehbehinderten Funktionen verbessern.

1.  Testtitel auf Schwarz-Weiß-Fernsehgeräten. Beachten Sie alle Fälle, in denen Elemente, Player, Ziele und Befehle nicht unterschieden werden können, und passen Sie Ihre Farbpalette entsprechend an.
2.  Geben Sie Gamern eine Option, um die Textgröße auf ihrem Bildschirm zu erhöhen. Stellen Sie außerdem die Möglichkeit bereit, die Bildlaufrate des Texts zu ändern. Es ist wichtig zu beachten, dass die Konsolenerfahrung 10 Fuß beträgt, nicht die 2-Fuß-Gamingerfahrung, die viele PC-Entwickler gewohnt sind. Selbst bei Gamern ohne Sehprobleme kann es schwierig sein, kleine Benutzeroberflächen und Text in langen Abständen zu lesen.
3.  Stellen Sie Sprachtextfunktionen bereit, mit denen der gesamte Spieltext gesprochen werden kann, einschließlich Spielmenüs, die den Fokus auf Schaltflächen verfolgen. Ermöglichen Sie es dem Benutzer, die Geschwindigkeit, den Tonhöhen und das Geschlecht der Stimme zu steuern. Um zu verhindern, dass Text-zu-Sprache durch andere Spielgeräusche ertrunken wird, können Benutzer die Sprachmenge, Umgebungsgeräusche, aktive Spielgeräusche und Musik anpassen. Fügen Sie außerdem die Option zum Wiedergeben unterschiedlicher Sounds beim Übergang durch Menüelemente und Schaltflächen ein.
4.  Geben Sie schließlich Gamern die Möglichkeit, die Helligkeits- und Kontrasteinstellungen im Spiel zu ändern. Bieten Sie Benutzern die Möglichkeit, ihre eigenen benutzerdefinierten Farbschemas auszuwählen, sodass Text-, Hintergrund- und HUD-Farben entsprechend den Anforderungen einer Person angepasst werden können.

## <a name="auditory-impairments"></a>Auditive Beeinträchtigungen

*"Die Erinnerung an Half-Life uns wieder zu gewinnen, da uns noch ein weiteres technologisches Glanzstück \[ Halo \] für den Gehörlosen unbrauchbar ist... Wir hoffen, dass dies kein Wunder ist. das, wenn Halo 2 jemals das Licht der Welt sieht, dass es vollständig untertitelt wird." www.DeafGamers.com*

Die nächsthäufigste Form von Beeinträchtigungen, die sich auf das Spiel auswirken können, sind auditive Beeinträchtigungen. Allein in den USA sind mehr als 28 Millionen Menschen von einer Hörbehinderung betroffen. Während Hörbehinderung häufig mit dem Alter verknüpft ist, sind 17 von 1.000 Kinder unter 18 Jahren von einer Hörbehinderung betroffen[("Statistiken zu Hörstörungen, Hörinfizierungen und Gehörlosen",](https://www.nidcd.nih.gov/health/statistics/pages/hearing.aspx)National Institute on Deafness and Other Communication Anomalie). Wenn man bedenkst, dass die Spieler von heute älter werden und ihr Gehör mit einer ständig zunehmenden Rate verloren geht, ist es klar, dass die Nachfrage nach Audiozugriff nur zunimmt.

Stellen Sie sich Vor, dass Sie probleme mit der Beeinträchtigung von Prüfern besser verstehen können:



| Sie sind ein Gamer           | Und Sie befinden sich in diesem Szenario.                                                                                                                                                                                                                                                            |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mit normalem Hörvermögen       | Sie möchten niemanden stören, sodass Sie mit stummem Sound spielen, aber Sie können das Spiel nicht wiedergeben, da die Anweisungen nur in Audio angegeben werden. <br/>                                                                                                                               |
| Mit Hörbehinderung | Sie spielen auf einer lauten Party, aber Sie können nicht erkennen, dass Sie unter Bewaffnung stehen, da Sie die Schützeaufnahmen nicht hören können.<br/> Das Spiel hat viele Umgebungsgeräusche, und Sie können die ihnen erteilten anweisungen nicht hören. <br/>                                                     |
| Wer ist gehörlos               | Die Audiowiedergabe ist so weich, dass Sie sie auch in einem stillen Raum nicht hören können. <br/> Alle Ihre Ziele werden Ihnen in Audiodaten gegeben, und Sie können nicht bestimmen, was Sie tun sollen. <br/> Die gesamte Storyline wird mit einem Wort versehen, und Sie können dies nicht nachvollziehen. <br/> |



 

Mit einigen relativ geringen Arbeitsaufwand können Sie Ihr Spiel für Spieler mit normalem Hörvermögen und für Spieler mit einer auditiven Beeinträchtigung nutzbar und nutzbar machen.

1.  Schließen Sie die Beschriftung aller Dialoge. Dies schließt In-Game-Inhalte und -Tics ein. Geben Sie dem Spieler die Möglichkeit, diese Beschriftungen ein- und auszuschalten.
2.  Wenn ein Soundeffekt wichtige Informationen liefert, stellen Sie auch einen text- oder taktilen Mechanismus (Vibration) für Feedback bereit. Wenn beispielsweise normalerweise ein Rauschen in Ihrem Spiel ein schnelleres Rauschen in der Nähe seiner Explosion verursacht, stellen Sie einen visuellen Indikator (z. B. eine Zeitleiste) bereit, mit dem der Spieler auch wissen kann, wie viel Zeit vor der Explosion übrig bleibt.
3.  Wenn Ihr Spiel Onlineplay unterstützt, können Spieler Textnachrichten senden und ihre Stimme verwenden, um Informationen zwischen Teammitgliedern und anderen Onlineplayern bereitzustellen. Ein Headset ist für eine Person, die nicht hören kann, nicht nützlich, und immer mehr Spieler möchten mit anderen Personen spielen, mit denen sie online kommunizieren und geschichtet werden können.

## <a name="mobility-impairments"></a>Mobilitätsbeeinträchtigungen

*"Videogames bieten Menschen mit Behinderungen die Möglichkeit, sich wieder mit ihren Kollegen und Fähigkeiten zu verbinden, die verloren gegangen sind oder nie hatten. Meine persönliche Erfahrung stammt aus der Paralysierung im Alter von 14 Jahren und dem Besuch des Kinderzentrums im Krankenhaus, und das einzige Interesse, das ich aus meinem Kinderspielsystem hatte, bestand darin, das Videospielsystem zu spielen. Ich habe schnell das Interesse verloren, als ich gelernt habe, dass ich sie nicht spielen konnte..." RobertUngo*

Mobilitätsbeeinträchtigungen sind möglicherweise die schwerste der verschiedenen Beeinträchtigungen, zu denen feste Statistiken erstellt werden können. Dies liegt in erster Linie daran, dass diese Beeinträchtigungen durch Seuche, Schäden, Verlust von Brillen/Ziffern, Paralysierungen usw. verursacht werden können, die jeweils unterschiedliche Auswirkungen auf die Erfahrung eines Videoplayers haben können. Diese Beeinträchtigungen können Beeinträchtigungen sein oder später im Leben auftreten.

Stellen Sie sich Vor, dass Sie probleme mit der Beeinträchtigung von Prüfern besser verstehen können:



| Sie sind ein Gamer                                 | Und Sie befinden sich in diesem Szenario.                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ohne Mobilitätsbeeinträchtigung                     | Der Spielcontroller verfügt über so viele Schaltflächen, Sie (als lockerer Spieler) sind einschängig und möchten nicht lernen, wie Sie ihn verwenden. <br/>                                                                                                                                                                          |
| Mit einer vorübergehenden Mobilitätsbeeinträchtigung            | Sie haben einen gebrochenen Daumen, sodass Sie den Thumbstick nicht auf Ihrem Controller verwenden können. <br/> Sie haben ein gebrochenes Bein, sodass Sie das Pad "Pad" nicht für einen Titel verwenden können.<br/>                                                                                                                                     |
| Mit dauerhafter und schwerwiegender Mobilitätsbeeinträchtigung | Sie haben einen Arm verloren, sodass Sie keinen zweihändigen Controller verwenden können. <br/> Sie haben die Seuche, die Hände schütteln, und das führt dazu, dass Sie versehentlich Schaltflächen auf dem Controller auslösen. <br/> Sie sind vom Spiel heruntergelähmt, sodass Sie überhaupt keinen Standardspielcontroller verwenden können. <br/> |



 

Die Überlegung, all diese Spieler zu berücksichtigen, ist eine Herausforderung, aber es gibt einige einfache Dinge, die Sie bei der Entwicklung Ihrer Spiele beachten können.

1.  Minimieren Sie die Verwendung von Schaltflächen, und denken Sie mehr über Menüschnittstellen für Befehle nach. Dies ist besonders nützlich für Personen, denen möglicherweise Ziffern oder eine Hand fehlen. Sie ist auch für paralysierte Personen nützlich, die benutzerdefinierte Controller verwenden.
2.  Ermöglichen Sie Es Gamern, ihre Controllerkonfiguration und die Empfindlichkeit von Schaltflächen/Fingerabdrucks anzupassen. Dadurch können Personen mit feinen Motorkenntnissen den Controller anpassen, um die Auswirkungen ihrer Behinderungen auf das Spiel zu minimieren. Sie ermöglicht auch eine bessere Unterstützung von benutzerdefinierten Controllern für Personen mit Behinderungen.
3.  Wenn Ihr Spiel einen bestimmten Typ von Peripheriegerät verwendet (Pad, Helles Geschütz usw.), erlauben Sie anderen Controllern, die gleichen Funktionen auszuführen. Beispielsweise ermöglicht ein Spiel wie Die Revolution (c) selbst Personen mit Eingeschränkter Einschränkung, zusammen mit ihren Freunden mithilfe eines regulären handgehaltenen Controllers zu spielen.

## <a name="vocal-impairments"></a>Sehbehinderungen

Behinderungen machen einen relativ kleinen Prozentsatz der Behinderungen aus. Bestimmte Statistiken lassen sich nur schwer erstellen, aber der Beweis zeigt, dass ein Großteil der Sehbehinderung mit anderen Behinderungen (z. B. Motor- oder Hörbehinderungen) verknüpft ist. Wenn jedoch immer mehr Spielverleger damit beginnen, die Verwendung von Sprachkonferenzen und Spracherkennung in ihren Titeln zu untersuchen, werden Personen mit Beeinträchtigungen des Spielerlebnisses feststellen, dass die Qualität ihrer Spielerfahrung abnimmt. Um dies zu begegnen, gibt es grundlegende Barrierefreiheitsfunktionen, die implementiert werden können.

Stellen Sie sich Vor, dass Sie probleme mit der Beeinträchtigung von Prüfern besser verstehen können:



| Sie sind ein Gamer             | Und Sie befinden sich in diesem Szenario.                                                                                                                                                                                                                                           |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ohne Sehbehinderung    | Sie spielen ein Spiel, das gesprochene Befehle erfordert, um Ihre Zeichen zu steuern, und Sie können nicht spielen, da Sie kein Mikrofon haben. <br/> Sie spielen spät in der Nacht und möchten niemanden stören, sodass Sie Ihren Kommunikationsor nicht verwenden können. <br/> |
| Wer hat eine Sprachbehinderung | Sie spielen ein Spiel, das gesprochene Befehle erfordert, um Ihre Zeichen zu steuern, und Sie können nicht spielen, da das Spiel nicht erkennen kann, was Sie sagen.                                                                                                               |
| Wer kann nicht sprechen      | Das Spiel, das Sie spielen, erfordert Spracheingaben, sodass Sie nicht spielen können. <br/> Das Onlinespiel, das Sie spielen, erwartet, dass Sie die Strategie über den Kommunikationsor koordinieren, sodass Sie nicht effektiv spielen können. <br/>                                               |



 

Glücklicherweise gibt es einige einfache Fehlerbehebungen, mit denen Ihr Spiel für diese Gamer verwendbar und benutzerfreundlicher werden kann.

1.  Wenn ein Spiel spracherkennung verwendet, stellen Sie Gamern eine Option zur Auswahl von Befehlen aus einer Menü- oder Schaltflächenkombination zur Verfügung.
2.  Wenn Ihr Titel auch Online-Multiplayer unterstützt, geben Sie Gamern die Option eines anpassbaren Makros mit Audionachrichten oder (noch besser für Personen mit Hörbehinderung) Textnachrichten. Die Bereitstellung von Tastaturunterstützung für Chats ist ebenfalls eine Option.

## <a name="conclusion"></a>Zusammenfassung

An diesem Punkt könnten Sie denken, dass Sie nicht alle diese Spieler in all diesen Szenarien unterstützen könnten. Selbst wenn Sie jeden Vorschlag in diesem Artikel implementieren würden, konnten Sie nicht sicherstellen, dass ein Titel für alle Benutzer vollständig zugänglich ist. Wenn Sie jedoch diese Richtlinien für die Barrierefreiheit befolgen, können Sie Ihren Titel für die Barrierefreiheitscommunity wesentlich ansprechender gestalten. Und dies kann nur den Umsatz steigern.

Um einen Titel leichter zugänglich zu machen, müssen Entwickler und Herausgeber Personen mit verschiedenen Arten von Behinderungen finden, um ihre Spiele zu testen. Dieser Ansatz bietet Informationen aus erster Hand darüber, ob ein Spiel für eine bestimmte Zielgruppe zugänglich ist. Ein zusätzlicher Vorteil ist, dass unterschiedliche Entwicklungs- und Testressourcen zusätzliche Erkenntnisse bieten können, die das Spielverhalten für alle Spieler verbessern können. Am wichtigsten ist es, die Barrierefreiheitscommunity einzubinden und diese potenziellen Kunden kennenzulernen. Halten Sie eine Spiel-Bash für Ihren Titel in einem lokalen Deaf Service Center, Children es Hospital oder Ins center (Kinderhosum oder Krankenhaus) bereit. Ermuntern Sie Entwickler und Tester, sich bei lokalen Organisationen zu beteiligen, die mit Menschen mit Behinderungen arbeiten, sich für einen Kurs zur Signierensprache zu registrieren oder sich für barrierefreiheitsbezogene Kinder zu registrieren, um mit der Community Schritt zu halten. Fordern Sie Feedback zu vorherigen Titeln von deaktivierten Gamern an lokalen Schulen und Unis an.

Niemand möchte sich als Außenseiter fühlen. Indem Sie die Barrierefreiheitscommunity in Spieletests und -design einbeziehen, können Sie Ihren Titel für eine viel größere Zielgruppe auf den Markt bringen und das Richtige für die Community und Ihr Endergebnis tun.

## <a name="more-resources"></a>Weitere Ressourcen

Es gibt eine Reihe von Webressourcen, in denen die Barrierefreiheit von Spielen erörtert wird, sowie eine Reihe von Unternehmen, die sich auf deaktivierte Gamer konzentrieren. Darüber hinaus kann die Accessible Technology Group bei Microsoft unter mit PC-bezogenen Fragen zur Barrierefreiheit kontaktiert ablecat@microsoft.com werden. Fragen zur Xbox-Barrierefreiheit können an folgende Adresse gesendet werden: xaccess@microsoft.com .

Allgemeine Behinderungen:

-   [Barrierefreiheit von Spielen](https://www.game-accessibility.com/)
-   [Barrierefreiheitswebsite von Microsoft](https://www.microsoft.com/enable/)
-   [Bedienungshilfen](/previous-versions/windows/internet-explorer/ie-developer/accessibility/gg701968(v=vs.85))

Audity Impairment Sites (Standorte für auditive Beeinträchtigungen):

-   [DeafGamers.com](https://www.deafgamers.com/)
-   [Die Deaf-Ressourcenbibliothek](https://www.deaflibrary.org/)

Websites mit sehbehinderten Sehbehinderung:

-   [National Eye Institute](https://www.nei.nih.gov/)
-   [Vischeck](https://www.vischeck.com/)
-   [WebExhibits.org](https://www.webexhibits.org/causesofcolor/2.mdl)

Mobilitätsbeeinträchtigungsstandorte:

-   [RobertFlorio.com](https://www.robertflorio.com/games)
-   [WebAIM](https://webaim.org/articles/motor/)

Websites für sprachbehinderte Beeinträchtigungen:

-   [American Speech-Language-Hearing Association](https://www.asha.org/public/speech/)

 

