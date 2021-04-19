---
description: DVD-Grundlagen
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: DVD-Grundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d0b2af8bc16fa0890c0103a063e750364cece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346195"
---
# <a name="dvd-basics"></a>DVD-Grundlagen

Die Features, die die DVD für Consumer attraktiv machen – nahtlose Verzweigung, mehrere Sprachen, Jugend Kontrolle, Karaoke-Unterstützung und mehrere Winkel – machen außerdem die Aufgabe des Entwicklers etwas komplexer. Ein DVD-Player darf nicht nur Audiostreams, Video-und subbildstreams wiedergeben, sondern auch die Navigationsoptionen nachverfolgen, die der Datenträger derzeit zulässt, und viele Arten von Benutzerbefehlen ordnungsgemäß verarbeiten. Der DVD-Navigator schützt Sie von einem Großteil dieser Komplexität und ermöglicht es Ihnen, eine voll funktionsfähige DVD-Anwendung zu erstellen. Sie müssen nicht auf die DVD-Spezifikation verweisen, um die DVD-Navigator-API effektiv zu verwenden, aber Sie müssen grundlegende DVD-Navigationskonzepte kennen.

**Navigations Steuerungsdaten**

Die Audiodaten und Videodaten auf einem DVD-Video-Datenträger werden in regelmäßigen Abständen mit verschiedenen Arten von Navigations Steuerungsdaten überlappt. Bei diesen Daten kann es sich um eine Anweisung handeln, die den Player anweist, etwas zu tun, z. b. eine Umstellung auf eine bestimmte Position auf dem Datenträger, oder es handelt sich um einen Informations geschützten Marker, der den Player informiert, z. b., dass der nachfolgende Inhalt eine höhere Jugend Verwaltungsebene als der vorherige Inhalt hat oder dass der Kapitel Skip-Vorgang Der Player leitet diese Informationen an eine Anwendung weiter, und es liegt in der Verantwortung der Anwendung, darauf zu reagieren. Diese Navigations Marker sind Teil der Art und weisen eine höhere Benutzer Interaktivität der DVD im Vergleich zu Video-CDs. Eine DVD-Player-Anwendung muss Ereignisse verarbeiten, die aus der Festplatte stammen, sowie Ereignisse, die aus dem Benutzer stammen.

**Audiodaten, Video-und Teil Bilddaten**

Eine DVD-Video Platte enthält drei primäre Arten von Streams: Video, Audiodatei und Teilbild.

-   Der Videostream kann bis zu neun "Winkel" enthalten, die als unter Ströme angesehen werden können. DVD-Autoren können mehrere Winkel einschließen, wo Sie dem Viewer eine Auswahl von Kamerawinkeln bieten möchten, aus denen die gleiche Szene angezeigt werden soll. Nur ein Winkel kann gleichzeitig aktiv sein. Der Videostream enthält auch Untertitel Daten der Zeile 21, sofern vorhanden.
-   Es können bis zu acht separate Audiostreams oder-Spuren vorhanden sein, die bis zu acht Multichannel-Sound Spuren bereitstellen und DVD-Karaoke-CDs die Verwendung von Multichannel-Audiodaten ermöglichen.
-   Eine DVD kann bis zu 32 *unter bildstreams* enthalten. Diese bestehen aus komprimierten 16-farbigen Bitmaps mit einem Alphakanal, der oberhalb des Videos überlastet ist. In der Regel enthalten subbildstreams Untertitel und Menü Schaltflächen, auch wenn Sie möglicherweise andere Grafiken enthalten. Ein teilbildstream kann eine angegebene Sprache aufweisen. Einige Teil Bildinhalte werden immer angezeigt, und einige Teil Bildinhalte werden nur angezeigt, wenn Sie vom Benutzer aktiviert werden.

Beachten Sie, dass die Beschriftungen in einem subbildstream nicht mit den Untertiteln für Zeilen 21 übereinstimmen. Untertitel, die für schwerhörige Viewer gedacht sind, werden in das Videosignal eingebettet. Sie bestehen vollständig aus Zeichen folgen. Untergeordnete Bild Beschriftungen hingegen sind grafische Bitmaps. Auf einem consumergerät werden Untertitel im Fernseh Satz angezeigt, während der Bild Datenstrom vom DVD-Player gerendert wird. Eine DVD kann beide Beschriftungs Typen enthalten.

**Titel und Kapitel**

Der Videoinhalt in einer DVD ist in *Titel* und *Menüs* unterteilt. Titel sind weiter unterteilt in Einheiten, die die DVD-Spezifikation *Teile von Titeln* (PTTs) aufruft. Häufig werden diese als *Szenen* oder *Kapitel* bezeichnet. (In der DirectShow-Dokumentation wird der Begriff "Chapter" verwendet.) Der Viewer kann zu bestimmten Titeln oder Kapiteln innerhalb von Titeln navigieren.

Der Autor einer DVD entscheidet, wie der Inhalt in Titel und Kapitel aufgeteilt wird. Wenn eine DVD einen Film mit Merkmals Länge enthält, wird der gesamte Film häufig in einem Titel platziert, der in Kapitel für die einzelnen Szenen aufgeteilt ist. Zusätzliche Features auf der DVD, wie z. b. nach Spann oder gelöschte Szenen, werden in separaten Titeln platziert. Diese Abteilungen sind jedoch willkürlich, und viele DVDs sind unterschiedlich organisiert.

Es können bis zu 99 Titel auf einem Bildträger vorhanden sein, und die Autoren der Titel können den Titel in bis zu 999 logische Kapitel aufteilen. In den meisten featurefilmen auf DVD ist Movie Content als eine Reihe von Kapiteln formatiert, die automatisch nacheinander abgespielt werden. Auf solchen CDs enthält das Ende der Kapitel Markierung eine Verzweigungs Anweisung, die den Player anweist, das nächste Kapitel in der Sequenz wiedergeben zu können. Diese Titel werden als *ein sequenzieller PGC-Titel* bezeichnet. (PGC steht für Programm Kette, ein weiterer Name für eine Gruppe von Kapiteln, die miteinander verknüpft sind. Dieser Begriff wird in der Dokumentation zum DVD-Navigator nicht verwendet.) Auf Datenträgern mit anderen Inhaltstypen, wie z. b. Karaoke-Datenträgern, könnte ein Kapitel-Marker den Player anweisen, ein Menü anzuzeigen, oder den Spieler anweisen, zu beenden.

DVD-Anwendungsentwickler verwenden Titel-und Kapitelnummern, um zu bestimmten Punkten auf der Festplatte zu springen. Für einen präziserer Zugriff können eine Titel Nummer und ein Zeit Code verwendet werden. Zeit Codes können nur mit einem sequenziellen PGC-Titel verwendet werden, da andere Typen keine Zeit Code Zuordnungen enthalten.

**Menüs**

Die DVD-Spezifikation definiert sechs Menü Typen:

-   **Tel.** Das Titelmenü ist das erste Menü, das angezeigt werden soll. Normalerweise verfügen Sie über Schaltflächen zum Auswählen von Titeln. Das Menü Titel wird auch als *Video-Manager-Menü* bezeichnet. Auf einer DVD ist nur ein Titel Menü vorhanden.
-   **Fasst.** Ein Stamm Menü ist das Menü der obersten Ebene für einen Titel. Jeder Titel kann über ein Root-Menü verfügen. Die nächsten vier Menüs sind Untermenüs im Menü "root". Ein Root-Menü wird auch als *Menü für Videotitel Satz* bezeichnet. Das Stamm Menü enthält normalerweise Schaltflächen, die zu einem beliebigen Titel im Titel Satz navigieren. Außerdem kann Sie über Untermenüs verfügen, die es dem Benutzer ermöglichen, Optionen für den Audiostream, den Kamerawinkel, den subbildstream oder das Kapitel auszuwählen. Diese Untermenüs werden jedoch nicht auf den meisten DVDs verwendet.
-   **Untertitel.** Im unterbildmenü wird der teilbildstream ausgewählt.
-   **Audio.** Das Audiomenü wählt den Audiostream aus. In der Regel ermöglicht dieses Menü dem Viewer, eine sprach Verfolgung auszuwählen.
-   **Ultra.** Im Menü Winkel wird der Kamerawinkel ausgewählt.
-   **Geschlagen.** Im Kapitel Menü, das auch als PTT-Menü bezeichnet wird, werden Kapitel innerhalb eines Titels ausgewählt.

Die meisten Menüs verfügen über Schaltflächen, die *ausgewählt* und *aktiviert* werden können. Durch Auswählen einer Schaltfläche wird die Darstellung der Schaltfläche geändert. Durch das Aktivieren einer Schaltfläche wird ein DVD-Befehl ausgelöst, z. b. ein anderes Menü angezeigt oder wiedergegeben

**Eltern Verwaltungs Stufen**

Der gesamte oder ein Teil einer DVD-CD kann mit einer von 1 bis 8 nummerierten Jugend Verwaltungsebene (PML) codiert werden. Acht ist die restriktivste Ebene (nur Erwachsene) und eine ist die am wenigsten restriktive (alle Alters). Die Idee besteht darin, dass untergeordnete Elemente nicht in Jugend freiem Inhalt angezeigt werden, und gleichzeitig es den Erwachsenen ermöglicht wird, nicht jugendfreie Inhalte zu beobachten. In den USA und Kanada sind die Ebenen dem Bewertungssystem von MPa (G, PG, PG-13, NC-17) zugeordnet, aber dies ist in anderen Ländern oder Regionen nicht der Fall.

Da Kapitel innerhalb eines Jugend Blocks logisch vorhanden sein können, gibt es möglicherweise zwei Versionen desselben Kapitels in einem Titel, denen jeweils ein anderes PML und ein anderer Jugend Block zugewiesen wird. Beispielsweise würde ein untergeordnetes Element, das die CD anmeldet und wieder gibt, eine Version von Kapitel 3 sehen, und ein Erwachsener, der sich anmeldet, würde eine andere Version sehen, vorausgesetzt, dass die Anwendung PMLs unterstützt.

Ein Titel oder ein Kapitel kann auch temporäre PMLs enthalten, deren Inhalt höher als das PML für den Titel oder das Kapitel als Ganzes eingestuft wird. Dies bedeutet, dass ein Titel mehr als eine elternebene aufweisen kann. Temporäre PMLs werden im Allgemeinen als Spitzen Blöcke erstellt, sodass eine Szene in einem Film zwei Versionen aufweisen kann, eine Bewertung für jüngere Betrachter und eine für Erwachsene.

Es liegt in der Verantwortung der Player Anwendung, die Eltern Ebenen zu erzwingen.

**Domänen**

Der Begriff *Domäne* bezieht sich auf den internen Zustand eines DVD-Players. Es handelt sich nicht um etwas, das auf dem Laufwerk erstellt wurde. Domänen sind wichtig, da einige DVD-Befehle nur in bestimmten Domänen gültig sind. DirectShow bietet eine Möglichkeit zum Abfragen der aktuellen Domäne und zum Benachrichtigen, wenn die Domäne geändert wird. Die folgenden Domänen sind definiert:

-   **Zuerst wiedergeben.** In dieser Domäne hat der DVD-Player gerade mit der Wiedergabe der DVD begonnen. Nachdem der Spieler in die erste Wiedergabe Domäne gewechselt hat, wechselt er in eine andere Domäne – entweder eine Menü Domäne oder die Titel Domäne, abhängig von der Festplatte.
-   **Menü "Video-Manager".** Der Player zeigt das Menü Video-Manager, auch als Titelmenü bezeichnet.
-   **VTS-Menü.** Der Player zeigt ein Menü an, das einem Videotitel Satz zugeordnet ist, entweder das Stammmenü oder ein Untermenü (Audiodatei, unter Bild, Winkel oder Kapitel).
-   **Tel.** Der Player spielt Videos in einem Titel.
-   **Anzuhalten.** Der Player zeigt nichts an. (Genau genommen Ruft die DVD-Spezifikation diesen Zustand nicht als Domäne auf, Sie kann jedoch als eine Domäne behandelt werden.)

Die Domäne kann als Zustands Variable angesehen werden, die ein DVD-Player überwacht, um den Inhaltstyp nachzuverfolgen, den der Player derzeit von der Festplatte liest. DVD-Player verwenden Domänen, um zu vermeiden, dass für das DVD-Laufwerk bedeutungslose Befehle ausgegeben werden.

**Benutzer Vorgangs Steuerelemente**

Benutzer Vorgangs Steuerelemente (User Operation Controls, UOPs) sind Marker auf einer CD, die von DVD-Autoren an beliebiger Stelle eingefügt werden können, um die Navigationsoptionen Die meisten Scheiben entsprechen Standard-UOP-Einschränkungen. Beispielsweise ist es für die meisten Festplatten nicht möglich, dass der Viewer in der ersten Wiedergabe Domäne schnell vorwärts oder ein Menü anzeigt. Im Prinzip kann jede Diskette jeden beliebigen UOP-Befehl an einem beliebigen Punkt auf der Festplatte einfügen, auch wenn der Befehl andernfalls in der aktuellen Domäne gültig wäre. Beispielsweise kann ein Datenträger erstellt werden, um eine schnelle Weiterleitung in einem bestimmten Titel zu verhindern oder um zu verhindern, dass ein bestimmtes Menü angezeigt wird, nachdem der Benutzer die Titel Domäne eingegeben hat. Der DVD-Navigator hält alle Befehle von der Festplatte an und lässt nicht zu, dass eine Anwendung die UOP-Steuerelemente der CD außer Kraft setzt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



