---
description: DVD-Grundlagen
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: DVD-Grundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a61299c4c0d3e83235a741c262efae685aa74ffa525aa08f9cf9a2e58b957e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102940"
---
# <a name="dvd-basics"></a>DVD-Grundlagen

Die Features, die DVD für Kunden ansprechend machen – nahtlose Verzweigung, mehrere Sprachen, Jugendkontrolle, Support für Kinder und mehrere Winkel – machen die Arbeit des Entwicklers auch etwas komplexer. Ein DVD-Player darf nicht nur Audio-, Video- und Unterbildstreams wiederverknabrufen, sondern muss auch die Navigationsoptionen nachverfolgen, die der Datenträger derzeit erlaubt, und viele Arten von Benutzerbefehlen ordnungsgemäß verarbeiten. Der DVD-Navigator schützt Sie vor einem großen Teil dieser Komplexität, während Sie eine voll funktionsfähige DVD-Anwendung erstellen können. Sie müssen nicht auf die DVD-Spezifikation verweisen, um die DVD Navigator-API effektiv zu verwenden, aber Sie müssen die grundlegenden DVD-Navigationskonzepte kennen.

**Navigationssteuerungsdaten**

Die Audio- und Videodaten auf DVD-Video Datenträger werden in regelmäßigen Abständen mit verschiedenen Arten von Navigationssteuerungsdaten übereinander gespeichert. Diese Daten können eine Anweisung sein, die den Spieler anfing, etwas zu tun, z. B. zu einer bestimmten Stelle auf dem Datenträger zu wechseln, oder es kann sich um einen informationsbasierten Marker handelt, der den Spieler informiert, z. B. dass der inhalt, der darauf folgt, eine höhere Ebene für die Verwaltung der Eltern als der vorherige Inhalt auf hat oder dass der Vorgang zum Überspringen des Kapitels deaktiviert ist. Der Player leitet diese Informationen an eine Anwendung weiter, und es liegt in der Verantwortung der Anwendung, darauf zu agieren. Diese Navigationsmarkierungen sind Teil dessen, was dvd im Vergleich zu Video-CDs einen höheren Grad an Benutzer-Interaktivität bietet. Eine DVD-Player-Anwendung muss Ereignisse verarbeiten, die vom Datenträger stammen, sowie Ereignisse, die vom Benutzer stammen.

**Audio-, Video- und Unterbilddaten**

Ein DVD-Video enthält drei Haupttypen von Streams: Video, Audio und Unterbild.

-   Der Videostream kann bis zu neun "Winkel" enthalten, die als Unterstreams betrachtet werden können. DVD-Autoren können mehrere Winkel überall dort verwenden, wo sie dem Betrachter eine Auswahl von Kamerawinkeln bieten möchten, von denen aus die gleiche Szene angezeigt werden soll. Es kann immer nur ein Winkel aktiv sein. Der Videostream enthält auch Zeilen 21-Untertiteldaten, sofern vorhanden.
-   Es kann bis zu acht separate Audiostreams oder Spuren geben, die bis zu acht Multichannel-Scheiben bereitstellen und DVD-Discs die Verwendung von Multichannel-Audio ermöglichen.
-   Eine DVD kann bis zu 32 *Unterbildstreams* enthalten. Diese bestehen aus komprimierten 16-Farbbitmaps mit einem Alphakanal, die über dem Video überlagert sind. In der Regel enthalten Unterbildstreams Untertitel und Menüschaltflächen, obwohl sie möglicherweise auch andere Grafiken enthalten. Ein Unterbildstream kann eine angegebene Sprache haben. Einige Unterbildinhalte werden immer angezeigt, und einige untergeordnete Inhalte werden nur angezeigt, wenn der Benutzer dies aktiviert.

Beachten Sie, dass Untertitel in einem Unterbildstream nicht mit Zeilen-21-Untertiteln identisch sind. Untertitel, die für Schwerhörigkeits-Viewer vorgesehen sind, sind in das Videosignal eingebettet. Sie bestehen vollständig aus Zeichenfolgen. Unterbildbeschriftungen sind hingegen grafische Bitmaps. Auf einem Consumergerät werden Untertitel vom Fernsehgerät angezeigt, während der Unterbilddatenstrom vom DVD-Player gerendert wird. Eine DVD kann beide Beschriftungstypen enthalten.

**Titel und Kapitel**

Der Videoinhalt auf einer DVD ist in *Titel und* *Menüs unterteilt.* Titel werden weiter in Einheiten unterteilt, die von der DVD-Spezifikation *als Teile von Titeln* (PARTS of Titles, PTTs) bezeichnet werden. Diese werden häufiger als Szenen *oder* Kapitel *bezeichnet.* (In der DirectShow-Dokumentation wird der Begriff Kapitel verwendet.) Der Viewer kann zu bestimmten Titeln oder Kapiteln innerhalb von Titeln navigieren.

Der Autor einer DVD entscheidet, wie der Inhalt in Titel und Kapitel unterteilt werden soll. Wenn eine DVD einen Film mit Merkmallänge enthält, wird der gesamte Film häufig in einem Titel platziert, unterteilt in Kapitel für die einzelnen Szenen. Zusätzliche Features auf der DVD, z. B. Trailer oder gelöschte Szenen, werden in separaten Titeln platziert. Diese Unterteilungen sind jedoch willkürlich, und viele DVDs sind unterschiedlich organisiert.

Es kann bis zu 99 Titel auf einem Datenträger geben, und Datenträgerautoren können den Titel in bis zu 999 logische Kapitel unterteilen. In den meisten Featurefolien auf DVD werden Filminhalte als eine Reihe von Kapiteln formatiert, die automatisch nacheinander spielen. Auf solchen Datenträgern enthält der Marker für das Ende des Kapitels eine Verzweigungsanweisung, die den Spieler anfing, das nächste Kapitel in der Sequenz weiter zu spielen. Diese Titel werden als Ein *sequenzieller PGC-Titel bezeichnet.* (PGC steht für Programmkette, ein weiterer Name für eine Gruppe von Kapiteln, die zusammengehören. Dieser Begriff wird in der Dokumentation zum DVD-Navigator nicht verwendet.) Auf Datenträgern mit anderen Inhaltstypen, z. B. Bei Einem-Band-Datenträgern, kann ein Ende-des-Kapitel-Marker den Spieler anweisen, ein Menü anzuzeigen, oder er weist den Player einfach an, anzuhalten.

DVD-Anwendungsentwickler verwenden Titel- und Kapitelnummern, um zu bestimmten Punkten auf einem Datenträger zu springen. Für einen feineren Zugriff können eine Titelnummer und ein Zeitcode verwendet werden. Zeitcodes können nur mit einem sequenziellen PGC-Titel verwendet werden, da andere Typen keine Zeitcodezuordnungen enthalten.

**Menüs**

Die DVD-Spezifikation definiert sechs Arten von Menüs:

-   **Titel.** Das Titelmenü ist das erste Menü, das angezeigt wird. In der Regel verfügt sie über Schaltflächen zum Auswählen von Titeln. Das Titelmenü wird auch als *Video-Manager-Menü bezeichnet.* Es gibt nur ein Titelmenü auf einer DVD.
-   **wurzel.** Ein Stammmenü ist das Menü der obersten Ebene für einen Titel. Jeder Titel kann über ein Stammmenü verfügen. Die nächsten vier Menüs sind Untermenüs aus dem Stammmenü. Ein Stammmenü wird auch als *Videotitelsatz-Menü bezeichnet.* Das Stammmenü verfügt in der Regel über Schaltflächen, die zu einem der Titel im Titelsatz navigieren. Darüber hinaus kann es Untermenüs geben, mit denen der Benutzer Optionen für audio stream, camera angle, subpicture stream oder chapter auswählen kann. Diese Untermenüs werden jedoch nicht auf den meisten DVDs verwendet.
-   **Subpicture.** Im Unterbildmenü wird der Unterbilddatenstrom ausgewählt.
-   **Audio.** Im Audiomenü wird der Audiostream ausgewählt. In der Regel ermöglicht dieses Menü dem Viewer die Auswahl einer Sprachspur.
-   **Winkel.** Im Menü "Winkel" wird der Kamerawinkel ausgewählt.
-   **Kapitel.** Das Kapitelmenü, auch PTT-Menü genannt, wählt Kapitel innerhalb eines Titels aus.

Die meisten Menüs verfügen über Schaltflächen, die ausgewählt *und* *aktiviert werden können.* Wenn Sie eine Schaltfläche auswählen, ändert sich die Darstellung der Schaltfläche. Das Aktivieren einer Schaltfläche löst einen DVD-Befehl aus, z. B. das Anzeigen eines anderen Menüs oder das Starten der Wiedergabe.

**Verwaltungsebenen für Eltern**

Ein DVD-Datenträger kann ganz oder teilweise mit einer PML (Parental Management Level) codiert werden, die von eins bis acht nummeriert ist. Acht ist die restriktivste Ebene (nur 15 Jahre), und eine ist die am wenigsten restriktive Stufe (alle Altersklassen). Die Idee ist, zu verhindern, dass Kinder nicht jugendfrei sind, ohne Zustimmung der Eltern zu sehen, und gleichzeitig zu ermöglichen, dass kindersichere Inhalte beobachtet werden. In den USA und Kanada entsprechen die Ebenen dem Bewertungssystem der MPAA (G, PG, PG-13, NC-17), aber dies ist in anderen Ländern oder Regionen nicht der Fall.

Da Kapitel logisch innerhalb eines Elternblocks vorhanden sein können, gibt es möglicherweise zwei Versionen desselben Kapitels in einem Titel, die jeweils einer anderen PML und einem anderen Elternblock zugewiesen sind. Ein untergeordnetes Kind, das sich anmeldet und den Datenträger wiederträgt, würde z. B. eine Version von Kapitel 3 sehen, und ein erwachsener Benutzer, der sich anmeldet, würde eine andere Version sehen, vorausgesetzt, die Anwendung unterstützt PMLs.

Ein Titel oder Kapitel kann auch temporäre PMLs enthalten, deren Inhalt für den Titel oder das Kapitel als Ganzes höher bewertet wird als die PML. Dies bedeutet, dass ein Titel mehrere Elternebenen haben kann. Temporäre PMLs werden in der Regel als Winkelblöcke verfasst, sodass eine Szene in einem Film zwei Versionen haben kann, eine für betrachterische Zuschauer und eine für Diebe.

Es liegt in der Verantwortung der Playeranwendung, die Jugendebenen zu erzwingen.

**Domänen**

Der Begriff *Domäne* bezieht sich auf den internen Zustand eines DVD-Players. es handelt sich nicht um etwas, das auf dem Datenträger verfasst wurde. Domänen sind wichtig, da einige DVD-Befehle nur in bestimmten Domänen gültig sind. DirectShow bietet eine Möglichkeit, die aktuelle Domäne abfragt und benachrichtigt zu werden, wenn sich die Domäne ändert. Die folgenden Domänen sind definiert:

-   **Erste Wiedergabe.** In dieser Domäne hat der DVD-Player gerade mit der Wiedergabe der DVD begonnen. Nach dem Eintritt in die First Play-Domäne wechselt der Player je nach Datenträger zu einer anderen Domäne – entweder zu einer Menüdomäne oder zur Titeldomäne.
-   **Video-Manager-Menü.** Der Player zeigt das Video-Manager-Menü an, das auch als Titelmenü bezeichnet wird.
-   **VTS-Menü.** Der Player zeigt ein Menü an, das einem Videotitelsatz zugeordnet ist, entweder das Stammmenü oder ein Untermenü (Audio, Unterbild, Winkel oder Kapitel).
-   **Titel.** Der Player gibt Videos in einem Titel wieder.
-   **Stoppen.** Der Player zeigt nichts an. (Streng genommen wird dieser Zustand von der DVD-Spezifikation nicht als Domäne bezeichnet, sie kann jedoch als eine Domäne behandelt werden.)

Die Domäne kann als Zustandsvariable bezeichnet werden, die ein DVD-Player überwacht, um den Inhaltstyp nachzuverfolgen, den der Player gerade vom Datenträger liest. DVD-Player verwenden Domänen, um zu vermeiden, dass bedeutungslose Befehle an das DVD-Laufwerk ausgegeben werden.

**Benutzervorgangssteuerelemente**

Benutzervorgangssteuerelemente (User Operation Controls, UOPs) sind Marker auf einem Datenträger, die DVD-Autoren an einer beliebigen Stelle einfügen können, um die Navigationsoptionen eines Benutzers einzuschränken. Für die meisten Datenträger gelten UOP-Standardeinschränkungen. Die meisten Datenträger ermöglichen es dem Viewer beispielsweise nicht, ein Menü in der First Play-Domäne schnell weiterzuleiten oder ein Menü anzuzeigen. Im Prinzip kann jeder Datenträger jeden UOP-Befehl an einem beliebigen Punkt auf dem Datenträger einfügen, auch wenn der Befehl andernfalls innerhalb der aktuellen Domäne gültig wäre. Beispielsweise kann ein Datenträger erstellt werden, um eine schnelle Weiterleitung in einem bestimmten Titel zu verhindern oder um zu verhindern, dass ein bestimmtes Menü angezeigt wird, nachdem der Benutzer die Titeldomäne eingegeben hat. Der DVD-Navigator entspricht allen diesen Befehlen vom Datenträger und lässt nicht zu, dass eine Anwendung die UOP-Steuerelemente des Datenträgers überschreibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



